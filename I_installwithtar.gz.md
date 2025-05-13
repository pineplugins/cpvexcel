# Installation of cpvx using tar.gz

## 1. Download the tar.gz File
First, download the cpvx-{version}.tar.gz file from the release page.

```term
$ wget https://example.com/cpvx-1.0.0.tar.gz
````

Download cpvx-1.0.0.tar.gz

## 2. Extract the tar.gz File

Once the file is downloaded, extract it using the appropriate command for your operating system.

On Windows:
If you use an application like 7-Zip, you can right-click the `.tar.gz` file and select "Extract Here" or "Extract to folder."

On Linux/macOS:
Use the following command in the terminal to extract the tar.gz file:

```term
$ tar -xzvf cpvx-1.0.0.tar.gz
```

## 3. Enter the Extracted Folder

Once the file is extracted, navigate to the folder containing the extracted files:

```term
$ cd cpvx-1.0.0
```

## 4. Install Using pip

Now, install the package using pip from the extracted directory:

```term
$ pip install .
```

If you're using Python 3, use:

```term
$ pip3 install .
Obtaining file:///home/user/cpvx-1.0.0
Installing build dependencies ... done
Checking if build backend supports build_editable ... done
Getting requirements to build editable ... done
Preparing editable metadata (pyproject.toml) ... done
Requirement already satisfied: requests in /home/user/venv/lib/python3.12/site-packages (from cpvx==1.0.0) (2.32.3)
Requirement already satisfied: rich in /home/user/venv/lib/python3.12/site-packages (from cpvx==1.0.0) (14.0.0)
Requirement already satisfied: markdown-it-py>=2.2.0 in /home/user/venv/lib/python3.12/site-packages (from rich->cpvx==1.0.0) (3.0.0)
Requirement already satisfied: pygments<3.0.0,>=2.13.0 in /home/user/venv/lib/python3.12/site-packages (from rich->cpvx==1.0.0) (2.19.1)
Building wheels for collected packages: cpvx
Building editable for cpvx (pyproject.toml) ... done
Created wheel for cpvx: filename=cpvx-1.0.0-0.editable-py3-none-any.whl size=3353 sha256=b06a744cce4c591e1067695994546a5566a69434fd85de1fa826ec8878c0635e
Stored in directory: /tmp/pip-ephem-wheel-cache-123456/wheels/ed/4b/c8/4c6cf31d6e56e0eee646595e04a52b4313b962bdf781725cce
Successfully built cpvx
Installing collected packages: cpvx
Attempting uninstall: cpvx
Found existing installation: cpvx 1.0.0
Not uninstalling cpvx at /home/user/cpvx/src, outside environment /home/user/venv
Can't uninstall 'cpvx'. No files were found to uninstall.
Successfully installed cpvx-1.0.0
```

## 5. Check Installation

After successful installation, check whether cpvx is installed by running:

```term
$ cpvx --v
cpvx 1.0.0
```

## Troubleshooting

* **tar not recognized?** Make sure it is installed by running:

```term
$ sudo apt install tar
```

On macOS:

```term
$ brew install gnu-tar
```

* **pip not recognized?** Run with:

```term
$ python3 -m pip install .
# or
$ py -m pip install .
```

* **Permission Error on Linux/macOS?** Add `sudo` in front:

```term
$ sudo pip install .
```

* **Extraction failed?** Make sure the `.tar.gz` file is not damaged during download. Try downloading it again.

## Conclusion

Installing via tar.gz is a straightforward method for users who prefer not to use pip directly. If you need to update to a new version, simply download the latest tar.gz file, extract it, and reinstall using pip:

```term
$ pip install .
```
