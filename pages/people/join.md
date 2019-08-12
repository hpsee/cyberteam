---
layout: wide
title: Join the Team
---

Calling all students, mentors, and researchers! We'd love for you to join the Cyberteam.
The cyberteam site is maintained at [{{ site.github_user }}/{{ site.github_repo }}]({{ site.repo }}),
and you can join as a student, researcher, mentor, or some combination of those three (e.g., a researcher
could also be a mentor). 

<div style="float:right">
<img src="{{ site.baseurl }}/assets/img/join-the-team.png">
</div>


### 1. Clone the Repository 

To add your profile, first fork the repository to your [GitHub](https://github.com)
account, and then clone the fork:

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

### 2. Add your Profile

The profiles are markdown files located in `_people`. You can copy a template
for either a researcher, mentor, or student, and you want to name the file in
all lowercase with your full name. It will be used as your identifier across the website.

```bash
$ cp _people/_mentor_template.md _people/mickey-mouse.md
$ cp _people/_student_template.md _people/mickey-mouse.md
$ cp _people/_researcher_template.md _people/mickey-mouse.md
``` 

If you fall into more than one category, you can copy one of the two, and glance
at the other to see if you want to add additional fields. The fields
are explained in each of the files, and you can remove extraneous that you
don't want to add. Minimally we require a name, and institution.

### 3. Add your Headshot

If you want a headshot to go along with your profile, along with adding the basefile
name as the "image" parameter in the markdown file, you should add the image to 
`assets/img/people`, named equivalently to your markdown file, but with an appropriate
image extension (png or jpg).

### 4. Open a Pull Request

When you are ready, make sure you are checked out on a new branch, add the files,
and push to your remote.

```bash
$ git checkout -b add/profile-mickey-mouse
$ git add _people/mickey-mouse.md
$ git add assets/img/people/mickey-mouse.png
$ git commit -a -s -m 'adding mickey mouse profile'
$ git push origin add/profile-mickey-mouse
```

And then when you are ready, open a pull request to the upstream at `{{ site.github_user }}/{{ site.github_repo }}`.
It will be reviewed, and when merged, your profile will be live on the site.
