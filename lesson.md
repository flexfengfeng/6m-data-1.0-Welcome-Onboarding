# Lesson - this lesson will be delivered in coaching session 1

## Brief

## Preparation

### Prerequisite knowledge for this program

Good news: **no prior coding experience is needed** for this session. Today is all about setting up your tools, one command at a time — and every command comes with a plain-English explanation of what it does and why you're typing it. If you can follow a recipe, you can follow along here.

### Lesson Overview

This lesson contains a lot of software installations, and installs can be a little bumpy — that's completely normal and not a sign you've done anything wrong. If you're in a live session, there may be short pauses while the instructor helps other learners; if you're studying on your own, some downloads simply take a few minutes. Either way, treat the waiting time as a bonus: use it to read ahead in the pre-class guide, and you'll arrive at the next section a step ahead.

---

## Part 1 - Introduction to data science and databases

Conceptual knowledge, refer to slides.

---

## Part 2 - Introduction to data science toolbox

To get started, we'll need to set up your environment with essential software applications that will allow you to run models and execute Python and SQL code.

One key aspect of this course is learning to use the Command Line Interface (CLI). The CLI is a powerful tool that data scientists and engineers use to interact with their computers and execute commands efficiently. Instead of clicking through a graphical user interface (GUI), you'll be typing commands into a text terminal application. Think of the terminal as **texting your computer instructions instead of clicking** — you type a short message, press Enter, and the computer texts back its reply.

![CLI image](./assets/linux_terminal.png)

If you're new to the CLI, don't worry! While it might seem intimidating at first, using command-line tools will become second nature as you progress through the course. The CLI offers several advantages for data scientists:

- **Efficiency**: Executing commands quickly without navigating through menus
- **Automation**: Easily scripting repetitive tasks
- **Flexibility**: Accessing powerful tools and utilities

To help you get started with the CLI, here are some excellent online resources and tutorials:

- [Ubuntu CLI Tutorial](https://ubuntu.com/tutorials/command-line-for-beginners) - Linux command line for beginners from Ubuntu
- [Learning the Linux Shell](https://linuxcommand.org/lc3_learning_the_shell.php) - Part 1 of a comprehensive guide to the world of Linux.
- [Basic Linux Commands (video)](https://www.youtube.com/watch?v=7fs1i7TAMck) - One of the many, many Linux CLI tutorials you can find on YouTube

**Your first three "text messages" to the computer** — you'll use these constantly, so here's a 3-line mini-primer:

- `pwd` = "where am I?" (shows which folder you're currently in)
- `cd` = "go to this folder" (moves you into another folder)
- `ls` = "what's in here?" (lists the files in your current folder)

### Please refer to the [installation](./installation.md) file to install the required applications for this module.

---

## Part 3 - Python environments and git + github workflow

### Python environments

**Why do we need this?** Imagine baking two different cakes in the same mixing bowl without washing it — the flavours would contaminate each other. A **conda environment is a clean, separate mixing bowl for each project**: each one gets its own Python and its own packages, so the "recipe" for one project never contaminates another.

We can use conda to install different versions of Python. Conda also allows us to create and manage virtual environments for different projects. A `conda environment` is a self-contained virtual environment that contains its own Python installation and packages. This allows us to have different versions of Python and packages for different projects, without them conflicting with each other.

The commands below are the everyday moves for working with these "mixing bowls" — listing them, creating a new one, stepping into one, and cleaning one out. You don't need to memorise them; this page works as a cheat sheet you'll return to all module.

#### Get a list of conda environment in the system

```bash
conda env list
```

#### Create a conda environment

```bash
conda create -n <env_name> python=<python_version>
```

for example:

```bash
conda create -n myenv python=3.11
```

#### Activate a conda environment

```bash
conda activate <env_name>
```

#### Deactivate a conda environment

```bash
conda deactivate
```

#### Remove a conda environment

```bash
conda remove -n <env_name> --all
```

#### Install packages in a conda environment

```bash
conda install -n <env_name> <package_name>
```

or activate the environment first, then:

```bash
conda install <package_name>
```

to install multiple packages at once:

```bash
conda install <package_name_1> <package_name_2> <package_name_3>
```

#### Uninstall packages in a conda environment

```bash
conda uninstall -n <env_name> <package_name>
```

or activate the environment first, then:

```bash
conda uninstall <package_name>
```

#### Freeze dependencies

Freezing dependencies is the process of writing the dependencies of an environment to a file. This allows us to recreate the exact same environment for the application, with the exact same versions of packages.

Activate the environment first, then:

```bash
conda env export --no-builds > environment.yml
```

> Walk through the creation of an environment for this module

#### Recreate conda environment from environment.yml

```bash
conda env create -f environment.yml
```

#### Running python scripts in a conda environment

After activating the environment, run:

```bash
python <script_name.py>
```

### Git

**Why do we need this?** Think of **git as a camera that takes snapshots of your project over time**. Every time you reach a good stopping point, you take a photo (a "commit"). If something breaks later, you can always look back at — or return to — an earlier snapshot. Formally, git is a version control system which allows us to track changes to our code.

The commands below follow the photo-taking routine: choose what goes in the shot (`git add`), click the shutter (`git commit`), and check your camera roll (`git log`).

#### Create a git repository

```bash
git init
```

#### Add files to staging area

```bash
git add <file_name>
```

or add all files to staging area:

```bash
git add .
```

#### Commit changes

```bash
git commit -m "<commit_message>"
```

for example:

```bash
git commit -m "Initial commit"
```

#### Check status

```bash
git status
```

#### Check commit history

```bash
git log
```

#### Push changes to remote repository

```bash
git push
```

### Github

**Why do we need this?** If git is the camera taking snapshots, **GitHub is the photo album in the cloud** — a safe place to store your snapshots online, share them, and collaborate with other people. Formally, GitHub is a cloud-based hosting service for git repositories.

Two words you'll see a lot, defined before we use them:

- **Fork** = your own copy of someone else's GitHub project — like photocopying a shared recipe so you can scribble all over your copy without touching the original.
- **Clone** = downloading a copy of a GitHub project (usually your fork) onto your own computer, so you can actually work on the files.

The commands below move snapshots between your computer and the cloud album: `git clone` to download, `git pull` to fetch the latest, and `git push` to upload your new snapshots.

#### Clone a git repository

```bash
git clone <your_repo_url>
```


#### Pull changes from remote repository

```bash
git pull
```

#### Push changes to remote repository

```bash
git push
```

#### Checking the source of your remote repository

```bash
git remote -v
```

> Walk through the forking of this repository and cloning of the forked repository to the local machine. Then attempt the 1st question of the assignment, and push the changes to the forked repository.

### Cloning a Lesson 
- For every new lesson, you need to fork + clone the lesson repository (repo).
- For a new lesson, fork the repo (one time only) at the Github website. Go to the NTU repository, e.g. https://github.com/su-ntu-ctp/6m-data-1.0-Welcome-Onboarding.
- Click on the `Fork` button at the top of the repo page.
- Create a new fork by confirming the name (for example Dave) of your new repo, e.g. dave/5m-data-1.1-intro-data-science.
- Next we need to clone the repo to your local PC
- Go to your local Terminal window (WSL users: check for $ prompt).
- Type `pwd` to check your working directory. Otherwise, use cd to change to the correct directory.
- Type `git clone https://github.com/su-ntu-ctp/6m-data-1.0-Welcome-Onboarding`.
- Change to your cloned directory with the cd, e.g.  `cd 6m-data-1.0-Welcome-Onboarding`.

Please refer to the following video:

https://drive.google.com/file/d/1V5cAbaTgYoOqZreht038gN0Q0CEVYW9e/view?usp=drive_link

### Update changes from NTU repo
- Go to the your forked repo, e.g. https://github.com/dave/6m-data-1.0-Welcome-Onboarding.
- Click on `Sync fork` button on the repo home page to update your repo with the new content from the NTU repo. If there are no changes, you will see a message "The branch is not behind the upstream"---nothing to update.
- Go to your local Terminal window and change to your cloned directory e.g.  `cd 6m-data-1.0-Welcome-Onboarding`.
- Type `git pull` to download the new changes from your personal forked repository.
