# Installation of cpvx using .zip file

1. Download .zip File
Download the cpvx-{version}.zip file from the release page.
Example: [Download cpvx-1.0.0.zip]

2. Extract .zip File
On Windows:
Right-click the .zip file → select Extract All.
Or use an application like 7-Zip.

On Linux:
Use this command in the terminal:

```term
$ unzip cpvx-1.0.0.zip
```

If you don't have unzip, install it first:

```term
$ sudo apt install unzip
```

On macOS:
The macOS built-in terminal supports unzip:

```term
4 unzip cpvx-1.0.0.zip
```

3. Enter the Extracted Folder
Once successfully extracted, navigate to the folder:

```term
$ cd cpvx-1.0.0
```

4. Install Using pip
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

5. Check Installation
After successful installation, check whether cpvx is installed:

```term
$ cpvx --version
cpvx 1.0.0
```

Troubleshooting
- pip not recognized? Run with:

```term
$ python3 -m pip install .
$ # or
$ py -m pip install .
```

- Permission Error on Linux/macOS? Add sudo in front:

```term
$ sudo pip install .
```

- Extraction failed? Make sure the .zip file is not damaged during download. Try downloading it again.

Conclusion
Installation via .zip is very simple and suitable for Windows, Linux, and macOS users. To update to a new version, download the latest .zip file, extract it, and reinstall with:
    pip install .
