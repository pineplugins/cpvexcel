# Installation with pip

Installing via `pip` is the **simplest and fastest method** to get started.  
However, this method **does not allow you to modify the source code directly**.

---

## Check if Python is Installed

Before installing anything, make sure Python is installed.

### Windows

```term
> python -V
Python 3.12.3
```

### Linux

```term
$ python3 -V
Python 3.12.3
```

### macOS

```term
$ python3 -V
Python 3.12.3
```

---

## Install pip (Python Package Installer)

`pip` is the official Python package manager used to install libraries such as `flask`, `requests`, `cpvexcel`, etc.

---

### Windows

#### Method 1: Via Python Installer (Recommended)

1. Download Python from [python.org](https://www.python.org/downloads/)
2. During installation, **check this option**:

   ```
    Add Python to PATH
   ```

3. Click **Install Now**
4. After installation, verify pip:

```term
> pip --version
pip 23.2.1 from C:\Python312\Lib\site-packages\pip (python 3.12)
```

#### If pip is not detected

Run the following:

```term
> python -m ensurepip --upgrade
Looking in links: C:\Program Files\Python312\Lib\ensurepip
Requirement already satisfied: pip in C:\Python312\Lib\site-packages (23.2.1)
Requirement already satisfied: setuptools in C:\Python312\Lib\site-packages (67.8.0)
```

---

### macOS

#### Method 1: Ensure pip is installed

```term
$ python3 -m ensurepip --upgrade
Looking in links: /Library/Frameworks/Python.framework/Versions/3.12/lib/python3.12/ensurepip
Requirement already satisfied: pip in /usr/local/lib/python3.12/site-packages (23.2.1)
Requirement already satisfied: setuptools in /usr/local/lib/python3.12/site-packages (67.8.0)
```

#### Method 2: Install Python via Homebrew

```term
$ brew install python
==> Downloading https://formulae.brew.sh/api/formula/python.json
==> Installing python
==> Pouring python-3.11.5.big_sur.bottle.tar.gz
🍺  /opt/homebrew/Cellar/python@3.11/3.11.5: 4,332 files, 60MB

pip3 has been installed as:
  /opt/homebrew/bin/pip3
```

Verify:

```term
$ pip3 --version
pip 23.2.1 from /opt/homebrew/lib/python3.11/site-packages/pip (python 3.11)
```

---

### Linux (Ubuntu/Debian-based)

Install pip:

```term
$ sudo apt update
Hit:1 http://archive.ubuntu.com/ubuntu jammy InRelease
Reading package lists... Done

$ sudo apt install python3-pip
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  python3-pip python3-setuptools python3-wheel
0 upgraded, 3 newly installed
Need to get 2,500 kB of archives.
After this operation, 10.2 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/... python3-pip ...
...
Setting up python3-pip ...
```

Verify:

```term
$ pip3 --version
pip 23.2.1 from /usr/lib/python3/dist-packages/pip (python 3.12)
```

> For other distros (Fedora, Arch, etc.), use `dnf`, `yum`, or `pacman` accordingly.

---

## Final Check

Run one of these commands to ensure pip is working properly:

```term
$ pip --version
pip 23.2.1 from /home/username/venv/lib/python3.12/site-packages/pip (python 3.12)
```

or

```term
$ pip3 --version
pip 23.2.1 from /home/username/venv/lib/python3.12/site-packages/pip (python 3.12)
```

---

## Install cpvexcel

1. open temrinal
2. instal with pip
```term
$ pip install cpvx
Looking in indexes: https://pypi.org/simple
Collecting cpvx
  Downloading cpvx-1.0.0-py3-none-any.whl (12 kB)
     |████████████████████████████████| 12 kB 56.2 MB/s eta 0:00:01
Requirement already satisfied: pyperclip in /home/user/.local/lib/python3.12/site-packages (from cpvx) (1.8.2)
Requirement already satisfied: requests in /home/user/.local/lib/python3.12/site-packages (from cpvx) (2.28.1)
Requirement already satisfied: charset-normalizer<3,>=2 in /home/user/.local/lib/python3.12/site-packages (from requests->cpvx) (2.1.1)
Requirement already satisfied: idna<4,>=2.5 in /home/user/.local/lib/python3.12/site-packages (from requests->cpvx) (3.4)
Requirement already satisfied: urllib3<2,>=1.21.1 in /home/user/.local/lib/python3.12/site-packages (from requests->cpvx) (1.26.12)
Requirement already satisfied: certifi>=2017.4.17 in /home/user/.local/lib/python3.12/site-packages (from requests->cpvx) (2022.9.24)
Installing collected packages: cpvx
Successfully installed cpvx-1.0.0
```

verivication instalation

```term
$ pip show cpvx
Name: cpvx
Version: 1.0.0
Summary: Simple package to interact with cpvexcel
Home-page: https://github.com/pineplugins/cpvexcel
Author: pineplugins
Author-email: openpineaple@gmail.com
License: MIT
Location: /home/user/.local/lib/python3.12/site-packages
Requires: pyperclip, requests
Required-by:
```

selamat cpvx berhaisl di ninstall
