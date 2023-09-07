Git Intro Activity
==================

A. Form teams
-------------

Form a 2-person team. Try to find someone who uses the same platform as you (e.g., Windows, Linux, etc.). If you can't, that's fine. If you are the odd-person-out, join a team of 2.

Assign the following roles to the members of your team. If you are in a
team of 2, assign the recorder and navigator roles to the same person.

Roles:

-   Driver: Creates and maintains a local git repository.

-   Navigator: Reads instructions and records answers.

3rd person role (if you have a 3-person team):

-   Quality Assurance Person: Ensures instructions are being carried out correctly, answers are clear, and looks for ways for the team to work together more effectively.

You will be rotating roles. Your instructor will let you know when to switch roles. Switching roles requires switching computers. So, plan accordingly.


B. Setup
-------------

1. Create and share a shared document (Google Doc, Etherpad, etc.) for your team.
2. Copy and paste this document into your shared document.

C. Download and install Git
---------------------------

Download and install Git for your operating system:

-   <https://git-scm.com/downloads>

Starting a terminal:

-   **Windows**:

    -   git-bash.exe (Linux style commands)

    -   git-cmd.exe (Windows style commands)

-   **Mac OSX:** Finder -&gt; Applications -&gt; Utilities -&gt;
    Terminal.app

-   **Linux:** will vary depending on your window manager

D. Getting help
---------------

Run the following commands.

    git help
    git help -ag
    git help init

1.  What does `git help` do?

    ```
git help gives you commands and tell you what they do

    ```

2.  What does `-ag` cause `git help` to do?

    ```
git help -ag list available subcommands and some concept guides.


    ```

E. Identify yourself
--------------------

Run the following commands, replacing BOGUS NAME and BOGUS@EMAIL with
your name and email.

    git config --global user.name 'BOGUS NAME'
    git config --global user.email 'BOGUS@EMAIL'

WARNING: The name and email you give will be listed on each commit you make.
If this repository is ever published, your name and email on every commit
will be too. Also, if you are working on a shared computer, you should
consider changing this configuration before you walk away.


1.  What are these commands doing?

    ```

These commands identifies you so that whatever changes you make on the repo will be  published with your name and email on every commit.

    ```

2.  What is the purpose of `--global`?

    ```
the purpose of --global is to connect your github and terminal

    ```

F. Create a repository
----------------------

From the command line, run the following commands.

```
mkdir first_project
cd first_project
```

1.  By default any file that starts with `.` is hidden. How do you
    display a hidden file?

    ```
dir /a

    ```

2. Run this command to show the hidden files in the current directory. Are there any?

    ```

no there isn't

    ```

3. Now run the following command.

    ```
    git init
    ```


4. Check for hidden files again.  What was created by `git init`?

    ```

nothing

    ```


3.  What do you think would happen if you delete `.git`?

    ```

I believe the directory won't be able to be found so it would cause errors

    ```

4.  Using your observations to the previous questions, answer the following.
    You find an old project on your hard drive. You do not remember if
    it is a under version control. What could you look for to determine
    if the project is being managed using Git?

    ```
I would use git status to see if the project was made with git


    ```

G. Basic commands
-----------------

Use a plain text editor to create `names.txt` inside the `first_project`
folder. Put the names of your team in the file. Save and exit.

Run `git status` before and after each of these commands.

    git add names.txt
    git commit –m “Add our names.”
    git log

1.  What kind of information does `git status` report?

    ```
This command will show the current status of the project, including information about untracked and modified files.

    ```

2.  What does `git add names.txt` do?

    ```


    ```

3.  What does `git commit -m "Add our names."` do?

    ```

This command commits all changes

    ```

Use a plain text editor to create the following files:

-   `birthdays.txt` - Put your birthdays in this file.

-   `movies.txt` - Put the last movie each of you watched in alphabetical order.

Run `git status` before and after each of these commands.

    git add .
    git commit		Note:  Commit will open the vim editor; write a multi-line commit
						   message, save and quit (press esc and then type :wq).
    git log

4.  What does `git add .` do? What do you think `.` means?

    ```



    ```

5.  What does `git commit` (without -m) do?

    ```



    ```

6.  If you want to write a more detailed commit message (which is
    good practice) what command would you use?

    ```



    ```

7.  What does `git log` do?

    ```



    ```


H. Stage/Cache/Index
--------------------

Do the following:

-   Modify `names.txt` so that names are listed in *Last, First* format,
    one per line.

-   Modify `movies.txt` so they are in reverse alphabetical order
    by title.

-   Create a new file `foods.txt` that contains your favorite foods (one
    for each team member).

Run the following commands:

    git add names.txt
    git status

1.  Categorize the state of each file by writing each file name under the appropriate state below. Compose a definition for each state.

    **Staged**

    ```
name.txt


    ```

    **Unstaged**

    ```



    ```

    **Untracked**

    ```
birthdays.txt
foods.txt
movies.txt

    ```

1.  If you run `git commit` what changes will be committed (***don't do
    it***)?

    ```
it will save the changes 


    ```

2.  What command do you run to stage changes?

    ```

git add

    ```

3.  What command do you run to unstage changes?

    ```

git reset

    ```

Run the following commands:

    git diff
    git diff --cached

1.  What does `git diff` display?

    ```
this command displays the differences, or changes, between two sets of code


    ```

2.  What does `git diff --cached` display?

    ```
this command displays the differences between the files that have been staged

    ```

3.  Formulate a sequence of commands to unstage changes to `names.txt`,
    and stage the changes to `movies.txt`. Execute your commands and
    confirm they worked.

    ```
it worked


    ```

4.  Edit `movies.txt`, change any one of the movies, and save it. Then
    run `git status`. What do you observe? Explain what you think is
    going on.

    ```

I think that the git status updates all changes that are made to the files

    ```

5.  Delete `names.txt`. Then run `git status`. What do you observe?
    Explain what you think is going on.

    ```

It shows what file is deleted

    ```

6.  Rename `movies.txt` to `last-movies`. Run `git status`. Observe
    and explain.

    ```
It updated the name change


    ```

7.  Formulate a sequence of commands to stage all changes including the
    untracked file and commit (with any reasonable message you like).
    Execute them.

    ```



    ```

8.  In Git vernacular, `index`, `cache`, and `stage` all refer to the
    same thing. What does it hold?

    ```

It holds the set of changes that are marked for the next commit

    ```

9.  Why have a `stage`? Why not just commit all changes since the last
    commit?

    ```

The staging area provides an opportunity to review and validate your changes before they become part of the permanent history. 

    ```

I. Undo
-------

Run the following commands:

    git log
    git status
    git reset --soft "HEAD^"
    git log
    git status

1.  What does `git reset --soft ``"HEAD^" `do?

    ```

it undoes the last commit while keeping the changes from that commit in the staging area. 

    ```

Run the following commands:

    git commit –m "Redo."
    git log
    git status
    git reset --hard "HEAD^"
    git log
    git status

1.  What does `git reset --hard "HEAD^"`` `do?

    ```
it used to erase the last commit and all changes associated with it, both staged and unstaged. 


    ```

2.  What is the difference between `--hard` and `--soft`?

    ```
hard discards changes while soft perserves changes


    ```

3.  What do you think `HEAD` means?

    ```
I think it shows latest commit

    ```

4.  What do you think `HEAD^` means?

    ```
I think it shows the last commit that was made.

    ```

J. Helpful resources
--------------------

-   <https://git-scm.com/doc>

-   <https://www.atlassian.com/git/tutorials/>

-   <https://services.github.com/on-demand/downloads/github-git-cheat-sheet.pdf>

K. Copyright and Licensing
--------------------------

Copyright 2016, Darci Burdge and Stoney Jackson SOME RIGHTS RESERVED

This work is licensed under the Creative Commons Attribution-ShareAlike
4.0 International License. To view a copy of this license, visit
<http://creativecommons.org/licenses/by-sa/4.0/> .
