---
title: Examples of code using JSON nlohmann header only Library for C++
tags: [C++]
levels: [Beginner]
---

This code showcases how to work with the header-only nlohmann JSON library for C++. In order to compile, change the extensions from json_test.txt to json_test.cpp and test.txt to test.json. You must also download the header files from https://github.com/nlohmann/json. Complilation instructions are at the bottom of json_test. This code is very helpful for creating config files, for example.

```cpp
#include <iostream>
#include <nlohmann/json.hpp>
#include <fstream>

using json = nlohmann::json;

int main(int argc, char const *argv[])
{
    // read in the json file
	std::ifstream f("test.json", std::ifstream::in);

    json j; //create unitiialized json object

    f >> j; // initialize json object with what was read from file

    std::cout << j << std::endl; // prints json object to screen

    // uses at to access fields from json object
    std::cout << j.at("cal") << std::endl;
    std::cout << j.at("months") << std::endl;

    int days = j.at("days");

    std::cout << days <<std::endl;

	return 0;
}

// to compile with gcc:
// need header files from https://github.com/nlohmann/json
// g++ -std=c++11 -I/json-nlohmann-folder/include jsontest.cpp -o json
```

```json
{
	"days": 365,
	"months": 12,
	"cal": "Gregorian"
}
```
