# Installation of cpvx using GitHub

1. Clone the Repository
Clone the cpvx repository from GitHub using git:

```term
$ git clone https://github.com/pineplugins/cpvexcel
Cloning into 'cpvexcel'...
remote: Counting objects: 25, done.
remote: Compressing objects: 100% (20/20), done.
remote: Total 25 (delta 4), reused 24 (delta 4), pack-reused 0
Receiving objects: 100% (25/25), done.
Resolving deltas: 100% (4/4), done.
```

1. Enter the Cloned Folder
Navigate to the cloned directory:

```term
$ cd cpvexcel
```

1. Install Using pip
Once inside the folder, use pip to install the package:

```term
$ pip install .
Obtaining file:///home/user/cpvx-1.0.0
Installing build dependencies ... done
Checking if build backend supports build_editable ... done
Getting requirements to build editable ... done
Preparing editable metadata (pyproject.toml) ... done
Requirement already satisfied: requests in /home/user/venv/lib/python3.12/site-packages (from cpvx==1.0.0) (2.32.3)
Requirement already satisfied: rich in /home/user/venv/lib/python3.12/site-packages (from cpvx==1.0.0) (14.0.0)
Requirement already satisfied: charset-normalizer<4,>=2 in /home/user/venv/lib/python3.12/site-packages (from requests->cpvx==1.0.0) (3.4.1)
Requirement already satisfied: idna<4,>=2.5 in /home/user/venv/lib/python3.12/site-packages (from requests->cpvx==1.00) (3.10)
Requirement already satisfied: urllib3<3,>=1.21.1 in /home/user/venv/lib/python3.12/site-packages (from requests->cpvx==1.0.0) (2.4.0)
Requirement already satisfied: certifi>=2017.4.17 in /home/user/venv/lib/python3.12/site-packages (from requests->cpvx==1.0.0) (2025.1.31)
Requirement already satisfied: markdown-it-py>=2.2.0 in /home/user/venv/lib/python3.12/site-packages (from rich->cpvx==1.0.0) (3.0.0)
Requirement already satisfied: pygments<3.0.0,>=2.13.0 in /home/user/venv/lib/python3.12/site-packages (from rich->cpvx==1.0.0) (2.19.1)
Requirement already satisfied: mdurl~=0.1 in /home/user/venv/lib/python3.12/site-packages (from markdown-it-py>=2.2.0->rich->cpvx==1.0.0) (0.1.2)
Building wheels for collected packages: cpvx
Building editable for cpvx (pyproject.toml) ... done
Created wheel for cpvx: filename=cpvx-1.0.0-0.editable-py3-none-any.whl size=3353 sha256=b06a744cce4c591e1067695994546a5566a69434fd85de1fa826ec8878c0635e
Stored in directory: /tmp/pip-ephem-wheel-cache-123456/wheels/ed/4b/c8/4c6cf31d6e56e0eee646595e04a52b4313b962bdf781725cce
Successfully built cpvx
Installing collected packages: cpvx
Attempting uninstall: cpvx
Found existing installation: cpvx 1.0.0
Not uninstalling cpvx at /home/user/cpvx/src, outside environment /home/user/venvCan't uninstall 'cpvx'. No files were found to uninstall.
Successfully installed cpvx-1.0.0
```

4. Check Installation
After successful installation, check whether cpvx is installed:

```term
cpvx -v
cpvx 1.0.0
```

Troubleshooting

- git not recognized? Make sure git is installed.
  To install git on Linux:

```term
$ sudo apt install git
>> 100%
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following additional packages will be installed:
  git-man less
Suggested packages:
  git-daemon-run | git-daemon-sysvinit git-doc git-el git-email git-gui gitk
  gitweb
The following NEW packages will be installed:
  git git-man less
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
Need to get 58.0 MB of archives.
After this operation, 237 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu focal/universe amd64 git amd64 1:2.25.1-1ubuntu3.2 [58.0 MB]
Fetched 58.0 MB in 5s (11.4 MB/s)
Selecting previously unselected package git.
(Reading database ... 245245 files and directories currently installed.)
Preparing to unpack .../git_1%3a2.25.1-1ubuntu3.2_amd64.deb ...
Unpacking git (1:2.25.1-1ubuntu3.2) ...
Setting up git (1:2.25.1-1ubuntu3.2) ...
Processing triggers for libc-bin (2.31-0ubuntu9.9) ...

```
  On Windows or macOS, download it from https://git-scm.com/
- pip not recognized? Run with:

```term
$ python3 -m pip install .
# or
$ py -m pip install .
```

- Permission Error on Linux/macOS? Add sudo in front:

```term
$ sudo pip install .
```

- Cloning failed? Make sure the repository URL is correct and you have an internet connection.
    Retry the cloning process:

```term
$ git clone https://github.com/pineplugins/cpvexcel
```

Conclusion

Installing via GitHub allows you to access the latest version of cpvx directly from the repository. If you prefer to install from the source, cloning the repository is an effective way.
To update to a new version, simply pull the latest changes and reinstall using:

```term
$ pip install .
```