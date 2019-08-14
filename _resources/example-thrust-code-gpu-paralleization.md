---
title: Examples of Thrust code for GPU Parallelization
tags: [cuda, parallelization, gpus]
levels: [Beginner, Intermediate, Advanced, Expert]
---
Some examples for writing Thrust code. To compile, download the CUDA compiler from NVIDIA. This code was tested with CUDA 9.2 but is likely compatible with other versions. Before compiling change extension from thrust_ex.txt to thrust_ex.cu. Any code on the device (GPU) that is run through a Thrust transform is automatically parallelized on the GPU. Host (CPU) code will not be. Thrust code can also be compiled to run on a CPU for practice.

```cpp
#include <thrust/host_vector.h>
#include <thrust/device_vector.h>

#include <iostream>

// create a struct called myfunc 
// input is two ints, output is an int
struct myfunc : thrust::binary_function<int, int, int>
{
 	__host__ __device__ // compiles for both host and device
    int operator()(int a, int b) // overloads () operator
    {return a * b;} // contents of the function body
};

int main(void)
{
    // Host vector H has storage for 4 integers
    thrust::host_vector<int> H(4);

    // initialize to 0, 1, 2..
    thrust::sequence(H.begin(), H.end());
    
    // H.size() returns the size of vector H
    std::cout << "H has size " << H.size() << std::endl;

    // print contents of H
    for(size_t i = 0; i < H.size(); i++)
        std::cout << "H[" << i << "] = " << H[i] << std::endl;

    // Copy host_vector H to device_vector D
    thrust::device_vector<int> D = H;
    
    // to set D1 = -D
    thrust::device_vector<int> D1(D.size());
    // runs from D.begin() to D.end(), stores in D1
    thrust::transform(D.begin(), D.end(), D1.begin(), thrust::negate<int>()); 
  
    // print contents of D1
    for(size_t i = 0; i < D1.size(); i++)
        std::cout << "D1[" << i << "] = " << D1[i] << std::endl;

    //creates instance of myfunc
    // mf is a Thrust function that can be used in a transform
    myfunc mf ; 

    // unitialized device vector of size 100
    thrust::device_vector<int> D2(100);

    // counts up by 7 starting from 21: 21, 28, 35, ...
    thrust::sequence(D2.begin(), D2.end(), 21, 7);
    std::cout << "Expecting 21, 714" << D2[0] << " , " 
        << D2[99] << std::endl;

    thrust::host_vector<int> H1(100);
    thrust::sequence(H1.begin(), H1.end());
    
    thrust::host_vector<int> twos(100);
    // set twos[i] = 2 for all i
    thrust::fill(twos.begin(), twos.end(), 2);
    
    // runs from H1.begin() to H1.end(). 
    // performs mf on H1[i] and twos[i] and saves output in twos[i]
    thrust::transform(H1.begin(), H1.end(), twos.begin(), 
        twos.begin(), mf);
    for (int i = 0; i < 100; ++i)
    {
        std::cout << twos[i] << " " << std::endl;
    }

    // H and D are automatically deleted when the function returns
    return 0;
}

// to compile:
// need CUDA compiler free download from nvidia (I used CUDA 9.2) 
// cuda thrust_ex.cu -o thrust_ex
```
