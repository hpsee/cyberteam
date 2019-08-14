---
title: Submit a Project
---

Submitting a project is easy! You should first join the Cyberteam, which
comes down to adding your profile to the site. See [complete instructions here]({{ site.baseurl }}/pages/people/join/).

<br>
<hr>

### 1. Clone the Repository 

Once you have joined, you can equivalently fork and clone the respository:

```bash
$ git clone https://github.com/<myusername>/cyberteam
```
or with ssl:

```bash
$ git clone git@github.com:<myusername>/cyberteam
```

Change directory into the root of the repository:

```bash
$ cd cyberteam
```

### 2. Add the Project

Projects are markdown files located in `_projects`. You can copy a template to get started:

```bash
$ cp _projects/_template.md _projects/2019/my-new-project.md
``` 

Notice that the files are organized by year, so we've written the file into
the 2019 folder.


### 3. Add content

Within the project file, you'll need to fill in the header section with details for your
project. You'll notice complete instructions for each entry:

```yaml
---
title:

# basename, located in assets/img/projects 
image:

# see https://hpsee.github.io/cyberteam/tags/
tags: [one, two]

# One of "New and recruiting" "In progress" "Finishing up" "Complete"
status:
project_institution: 
anchor_institution: 

# Describe the type of student you are recruiting
recruiting:

# Should correspond with filename (without extension) under _people
owner: mickey-mouse
mentors: [mickey-mouse, minnie-mouse]
email:
---
```

After the header section, you can write any markdown (text) to describe your project.
This will be rendered into HTML on the page.

 - **image**: is displayed on the front page, and should be added to `assets/img/projects`
 - **status**: should be one of "New and recruiting" "In progress" "Finishing up" "Complete"
 - **project_institution**: is the institution hosting the project
 - **anchor_institution**: is the institution supporting the project
 - **recuriting**: is a few sentences to describe the ideal students (or other) you are looking for
 - **owner** must correspond with a markdown file name under people, e.g., "mickey-mouse" implies there is a file `_people/mickey-mouse.md`
 - **mentors**: has the same requirement, but can be a list of people.
 - **email**: a contact email for the project.


### 4. Open a Pull Request

When you are ready, make sure you are checked out on a new branch, add the files,
and push to your remote.

```bash
$ git checkout -b add/project-my-project
$ git add _project/2019/my-new-project.md
$ git add assets/img/projects/my-project.png
$ git commit -a -s -m 'adding my project'
$ git push origin add/project-my-project
```

And then when you are ready, open a pull request to the upstream at `{{ site.github_user }}/{{ site.github_repo }}`.
It will be reviewed, and when merged, your project will be live on the site.
