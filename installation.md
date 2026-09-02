# Module 1 First-Time Software Installation

## Hardware Requirements
- Desktop/laptop computer running the latest version of macOS/Linux/Windows operating system (OS)
- Recommended 16GB onboard memory (RAM) 
- Recommended 50GB available hard disk storage space (HDD/SSD)
- Webcam and microphone for online Zoom sessions

> <span style="color:red">**[!WARNING]**
> 
> <span style="color:red">**Intel Mac is no longer supported, please consult with your instructors for alternative.**

## Software Requirements

Install the software **in the order shown below**. The order follows when you will actually
need each tool in the course, so you are never blocked in class.

| Step | Software | Description | Platform | Needed by | Details |
|------|----------|-------------|----------|-----------|---------|
| 1 | DBGate (or DBeaver) | Database viewer for the SQL lessons | All platforms | Lesson 1.3–1.5 | [Installation Guide](#step-1--database-viewer-dbgate) |
| 2 | WSL | Windows Subsystem for Linux | Windows only | Lesson 1.0 | [Installation Guide](#step-2--wsl-for-windows-windows-users-only) |
| 3 | Visual Studio Code (VSCode) | Source code editor | All platforms | Lesson 1.0 | [Installation Guide](#step-3--visual-studio-code-vscode) |
| 4 | Git CLI + GitHub | Version control — used to download every lesson | All platforms | Lesson 1.0–1.1 | [Installation Guide](#step-4--git-cli-and-github) |
| 5 | Conda/Miniconda | Python package and environment manager | All platforms | Lesson 1.3 assignment, then Lesson 1.6 onwards | [Installation Guide](#step-5--condaminiconda) |
| 6 | Test Installation | Confirm everything is working | All platforms | Before Lesson 1.3 | [Verification Guide](#step-6--verification-of-installation-mac-and-windows-users) |

### If you are short on time

- **Step 1 (DBGate) takes about five minutes and works on any laptop.** Do it now — it is the tool you will spend the most class time in.
- **Before your first class (Lesson 1.0/1.1):** finish Steps 2–4. That is enough to join class and clone lessons.
- **Before the Lesson 1.3 assignment and the Python lessons (1.6 onwards):** finish Step 5, then run the verification in Step 6.

## Step 1 — Database Viewer: DBGate

> **Needed for:** Lessons 1.3, 1.4 and 1.5 — the SQL lessons.
>
> **Why this is first:** DBGate is a plain desktop application on **every operating system — Windows, macOS and Linux**. It does not depend on WSL, VSCode, Git or Conda, and Windows users install the normal **Windows** version (not a WSL version). It is the quickest win in this guide, so get it done before anything else.

We will be using DBGate SQL client throughout this course to connect to databases and write SQL code. The free version is called DBGate Community. 

Download and install DbGate Community version [here](https://www.dbgate.io/download-community/).

![alt text](assets/dbGate.png)

### Alternative 
Alternatively, you can use another Duckdb browser called Dbeaver, you can download and install DBeaver Community [here](https://dbeaver.io/download/)

## Step 2 — WSL for Windows *(Windows users only)*

> **Needed for:** everything from Lesson 1.0 onwards (Windows users). Apart from DBGate in Step 1, install WSL before any of the remaining tools — VSCode, Git and Miniconda are all configured to run inside WSL.

### *For Windows users only* - Windows Subsystem for Linux (WSL)

Windows users should install WSL which allows you to run Windows and Linux at the same time on a Windows machine. WSL allows you to install a Linux distribution (e.g. Ubuntu, OpenSUSE, Kali, Debian, etc.) and use Linux applications and utilities such as command-line (CLI) tools. 

Most software engineering and development tools are initially developed for Linux and then adapted for Windows. As a result, they often perform better on Linux. Although Windows versions of popular tools are widely available, we strongly recommend using the Linux version whenever possible for optimal performance.
You must be running Windows 11 or 10 version 2004 and higher. 

For a step by step installation instruction guide, please refer to [here](guides/install_wsl.md).

For a very basic usage guide, please refer to [here](guides/wsl_linux_basics.md)

If you encounter issues with the guide above, you can refer to the official installation instructions [here](https://learn.microsoft.com/en-us/windows/wsl/install) to install Ubuntu on WSL.

### Additional Learning Resource
You can access your WSL files using regular Windows applications, such as File Explorer. While you in your Linux directory, type: 

`explorer.exe .`

Read this [tutorial](https://learn.microsoft.com/en-us/windows/wsl/filesystems) to find out how it works.

Please refer to [Reference - WSL on Windows](reference.md#wsl-on-windows) for more learning resource on WSL.

## Step 3 — Visual Studio Code (VSCode)

> **Needed for:** Lesson 1.0 onwards — you will open every lesson, notebook and SQL file in VSCode.

You will need a code editor to write Python or SQL code in the course. VSCode is a popular source code editor used by developers for writing, debugging and editing code across various programming languages. 

Download and install VSCode [here](https://code.visualstudio.com/download).


[Video: Install VSCode for Windows User](https://drive.google.com/file/d/15s22OloEAY3SMtiFE_uSjCiM73cZD9nW/view?usp=drive_link)

> Windows WSL users, install the Windows version as VSCode will work across both Windows and WSL environments.

[Video: Install VSCode for Mac User](https://drive.google.com/file/d/1wQY5fhUb7pCo7nHJwbrIP6UCYFNSOkRd/view?usp=drive_link)

For Windows user, please connect to WSL before proceeding with the rest. Please refer to [the guide](guides/wsl_vscode_config.md)

### Install the following vscode extensions 

Go to the `Extensions` tab, search for the following extensions in the marketplace and install them:

- Python
- Jupyter
- Colab
- WSL - (*For Windows/WSL user only:* Auto-install when connect to WSL)

### Setting Auto-Save

This is optional but we find that a lot of code running issue happen because learner forget to save their setting. 

In `VSCode`, please checked `Autosave`. It will help in future troubleshooting. 

![alt text](assets/autosave_vscode.png)

### Additional Learning Resource
Please refer to [Reference - VSCode](reference.md#vscode) for more learning resource on VSCode.

## Step 4 — Git CLI and GitHub

> **Needed for:** Lesson 1.0–1.1 — this is how you download (clone) each lesson repository and submit assignments.

### Git vs GitHub

Git and GitHub are two essential tools in software engineering. Git is a version control system that helps developers track changes in their code locally. GitHub is a web-based platform where developers can store and share their Git projects, facilitating collaboration and code management. Together, they enable a workflow where developers work on code locally with Git and then share it on GitHub for others to see, review, and contribute. This combination supports efficient collaboration, version control, and project management, making it indispensable for modern software engineering teams.

### Git CLI

We will be using Git extensively in this course and you will need to install the command line interface (CLI) application on your computer.

### Download and install Git CLI [here](https://git-scm.com/downloads).

For WSL users, git is already installed in Ubuntu. However, you need to configure git. Please follow the config guide below.

[Video: Install Git for Mac User](https://drive.google.com/file/d/1_NdWjc4pqYkuaFqRgYCGI62FoDufK4Bs/view?usp=drive_link)

### Configure Git (Apply to Mac and Windows User)
For Mac users, you need to launch a `terminal` to perform the following configuration. For Windows (WSL) user, please note that you need to launch `WSL` or `Ubuntu` to run the following configuration.

- Launch `WSL` (Windows user) or `terminal` (Mac Users)

Run the following command:
```bash
git config --global user.name "Your Name"
```

```bash
git config --global user.email "your_github_email@domain.com"
```

To confirm the configuration above 
```bash
git config --global --list
```

#### Additional config (Mac Users Only - Optional)
Mac users may run the following command to avoid possible error in the future:
```bash
git config --global http.postBuffer 524288000
```

If you encounter error in syncing your git repository please use the command above.

### Connecting VScode with Github (Apply to Mac and Windows User)
To connect Github with VSCode, you just need to click `Clone Git Repository` at the `Welcome` page. To access the welcome page, on the menu bar click `Help` > `Welcome`

Please checkout the video belong which applies for both Mac and Windows user.

[Video: Configuring Git and Using Git in VSCode](https://drive.google.com/file/d/1kyBHa4G4K5bgTBVrA-doMxuZdfXr8jZp/view?usp=drive_link)

> The video above also applies to Windows and Mac user. Only exception is that Windows users are required to connect to WSL first.

### Additional Learning Resource
Windows WSL users may read this official tutorial [Get Started using Git on WSL](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-git) to understand more about Git in WSL. *You may ignore the Azure setup.*

Please refer to [Reference - Git and Github](reference.md#git-and-github) for more learning resource on Git and Github.

## Step 5 — Conda/Miniconda

> **Needed for:** the **Lesson 1.3 assignment** (creating the `ddb` environment to build the DuckDB database file), and from **Lesson 1.6 onwards** to run Python and Jupyter notebooks. The in-class SQL activities in 1.3–1.5 use ready-made `.db` files and only need DBGate.

Conda is a package and environment manager that we will be using throughout this program, to manage our Python packages and environments. Miniconda is a lightweight version of the Anaconda distribution, designed for users who prefer a minimal installation. It includes only the essentials: Python, conda (the package and environment manager), and their dependencies. Unlike Anaconda, which comes preloaded with hundreds of scientific packages, Miniconda allows you to install only the packages you need, making it more flexible and less resource-intensive.

### Special Notes for Intel Mac

Please note that Anaconda has stopped building packages for Intel Mac. Their official message is as follows:

> As of August 15, 2025, Anaconda has stopped building packages for Intel Mac computers (osx-64). Existing Intel (MacOSX-x86_64) installers are still available at https://repo.anaconda.com/miniconda/ and the last Miniconda installer release for Intel Mac computers will be 25.7.x. For more information, see [our blog](https://www.anaconda.com/blog/intel-mac-package-support-deprecation) on the end of Intel mac support.

Therefore, laptop with Intel Mac will not be supported. Please consult instructors regarding alternatives. 

### Download and install miniconda [here](https://www.anaconda.com/docs/getting-started/miniconda/main)

> Windows WSL users, please follow instructions for **Linux/Unix**. You must install miniconda in your WSL **Ubuntu** environment, not Windows.

Windows WSL users can also follow the step by step instruction [here](guides/wsl_install_miniconda.md).

Mac users please follow the following guide [here](guides/mac_install_miniconda.md)

To verify this, your conda command prompt should show `(base) $`

[Video: Install Miniconda on WSL for Windows User](https://drive.google.com/file/d/1M6ioKVQ47084fMlXO03U2Aj2z910IFBR/view?usp=drive_link)

### Additional Learning Resource
Please refer to [Reference - Conda or Miniconda](reference.md#conda-or-miniconda) for more learning resource on Conda/Miniconda.

## Step 6 — Verification of Installation (Mac and Windows Users)
- To confirm if your github installation is successful, please refer to [Lesson - Cloning a Lesson](lesson.md#cloning-a-lesson) and try to clone this lesson to your PC. If you manage to clone your repository into your PC, we can confirm the git configuration is good.

- Please refer to the following exercise [here](guides/run_conda_python.md) to see if you can create a conda environment and run a python file to create a test database. Please proceed to next step if you manage to run the command without errors.

- To confirm if you can see the data, open `DbGate` or `DBeaver` and connect to the test database `test_duck.db`. 
    - For DbGate user please follow the guide [here](guides/dbgate_connect.md)
    - For DBeaver user please following the guide [here](guides/dbeaver_connect(optional).md)

Please make sure you can see 3 records.


## FAQ
1. **What Operating System (Windows/Mac/Linux) is recommended for this course?**
- **Ans:** We support a variety of operating systems, provided they are actively maintained and compatible with your computer. If you are using Windows, you will need to install the Windows Subsystem for Linux (WSL) to proceed.


2. **What Python version is required?**
- **Ans:** You don't need to worry about the version of Python during installation. We use `conda` to managed different versions of python, ensuring compatibility as needed.  


3. **I have Anaconda installed do I need to install Miniconda?**
- **Ans:** No need for Mac User. Once Anaconda is installed, you can access the same conda environment from VSCode. For Windows user, since we will be developing in WSL, you need to install Miniconda in WSL.


4. **Can I use Anaconda instead of VSCode?**
- **Ans:** VSCode is the preferred option because it integrates seamlessly with Github, WSL, Colab and Docker. Integration of duckdb and other platform also available by using extensions. In addition, it is more light weight compare to Anaconda. Other AI-IDE such as Cursor and Anti-Gravity also uses VScode interface.


5. **I have installed Github Desktop for Mac/Windows, do I still need to install Git?**
- **Ans:** There’s no extra step required. Once the GitHub software is installed, Git is already included and ready to use. However, we need to connect VSCode with Github to integration.


6. **Can I use Github Desktop for Mac/Windows instead?**
- **Ans:** We encourage you stick with VSCode as VSCode can be linked to Github. Please note that when you clone a repository into VSCode, it will not be registered or noticeable by Github Desktop Mac/Windows.


7. **Why can't I use my Intel based MacBook?**
- **Ans:** From Aug 2025, Anaconda has stop developing conda packages which this course relies on. In addition, PyTorch has stop Intel mac development since 2022. You will not be able to run neural network based software on Intel Mac. If you are reluctant to change laptop, please consult instructors as there are alternatives available.

