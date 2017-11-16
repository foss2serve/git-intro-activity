# Git Intro Activity

Participants, in teams of 2-3, work through an activity to learn how to install, configure, and use git to manage local repositories.

## Required Resources

- Participants: 2+
- Each team needs:
  - 1 computer with
    - A command-line interface
    - A plaintext editor
    - A browser
    - A working Internet connection with ports open for HTTP and HTTPS

## Prerequisite Knowledge and Skills

Participants must be able to:

- Command-line operations:
  - Change working directory (cd)
- Filesystem operations:
  - Create, rename, move, and delete directories and files
- Plaintext editor operations:
  - Edit and save a file

## Learning Outcomes

Participants will be able to:

- Install git
- Configure git
- Make and commit changes to a repository
- Add new files to a repository
- Remove a file from a repository
- Modify a file and commit the change
- Stage changes for commit
- Unstage changes for commit
- Explain the purpose of the stage/cache/index
- Inspect the state of a repository
- Undo a commit

## Targeted Process Skills

- Critical thinking

## Contents

- activity.md - Primary activity that students work together to complete
- cheatsheet.md - Contains common command-line commands, vim commands, and other resources
- presentation.pptx - Provides a little context

## Facilitation

- 10 min:
  - Provide overview using presentation.pptx
  - Form teams
  - Handout cheatsheet.md and activity.md, one copy per team
- 30-50 min: Supervise teams as they work through activity.md
- 5-10 min: Discuss responses to key questions; this can be done along the way

## FAQ

Here are some common questions that students may ask.

1. __Why stage?__
    Staging commits gives developers fine-grain control over what to commit. Here are are some references on the subject:
    - https://softwareengineering.stackexchange.com/questions/69178/what-is-the-benefit-of-gits-two-stage-commit-process-staging
    - http://stackoverflow.com/questions/4878358/why-would-i-want-stage-before-committing-in-git
    - http://gitolite.com/uses-of-index.html

2. __What's the difference between  `git add .` and `git add -A .`?__ As of Git 2.0, nothing; they both stage all modifications recursively starting in the current directory.

3. __What is the meaning of HEAD?__ HEAD refers to the branch or commit currently checked out.

4. __What is the meaning of `^` in `HEAD^`?__  "Parent". `HEAD^` is the parent of HEAD.

5. __What's the difference between `git commit -a` and `git add . ; git commit`?__ `git commit -a` will only stage changes in ___tracked___ files. `git add .` adds changes in ___all___ files (that are not ignored). So it will add changes in untracked files too.


## License

(c) 2016 Darci Burdge and Stoney Jackson SOME RIGHTS RESERVED

This work is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-sa/4.0/ .
