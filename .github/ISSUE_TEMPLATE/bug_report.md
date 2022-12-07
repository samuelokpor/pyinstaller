---
name: Bug report
about: Report a bug encountered while freezing you program or running your frozen program
title: ''
labels: triage
assignees: ''
---

<!--
Welcome to the PyInstaller issue tracker! Before creating an issue, please heed the following:

1. This tracker should only be used to report bugs and request features / enhancements to PyInstaller
    - For questions and general support, use the discussions forum.
2. Use the search function before creating a new issue. Duplicates will be closed and directed to
   the original discussion.
3. When making a bug report, make sure you provide all required information. The easier it is for
   maintainers to reproduce, the faster it'll be fixed.
-->

<!-- +++ ONLY TEXT +++ DO NOT POST IMAGES +++ -->

## Description of the issue

### Context information (for bug reports)

* Output of `pyinstaller --version`: pyinstaller 5.6.2 pyinstaller-hooks-contrib 2022.13
* Version of Python: python 3.8.5
* Platform: windows 10
* How you installed Python: anaconda 2020.11, using base conda
* Did you also try this on another platform? Does it work there?


* try the latest development version, using the following command:

```shell
pip install https://github.com/pyinstaller/pyinstaller/archive/develop.zip
```

* follow *all* the instructions in our "If Things Go Wrong" Guide
  (https://github.com/pyinstaller/pyinstaller/wiki/If-Things-Go-Wrong) and

### Make sure [everything is packaged correctly](https://github.com/pyinstaller/pyinstaller/wiki/How-to-Report-Bugs#make-sure-everything-is-packaged-correctly)

  * [ ] start with clean installation
  * [ ] use the latest development version
  * [ ] Run your frozen program **from a command window (shell)** — instead of double-clicking on it
  * [ ] Package your program in **--onedir mode**
  * [ ] Package **without UPX**, say: use the option `--noupx` or set `upx=False` in your .spec-file
  * [ ] Repackage you application in **verbose/debug mode**. For this, pass the option `--debug` to `pyi-makespec` or `pyinstaller` or use `EXE(..., debug=1, ...)` in your .spec file.


### A minimal example program which shows the error
i suspect its a pyqt issue, the program converts my previous version and runs smoothly and then stops working, error code 

### Stacktrace / full error message

Traceback (most recent call last):
    File "myfilename.py", line 1, in <module>
        from PyQt5 import QtCore, QtGui, QtWidgets
ImportError:DLL load failedwhile importing QtCore: the specific procedure could not be found.
[14292] Failed to execute script 'myfilename' due to unhandled exception!


Please also see <https://github.com/pyinstaller/pyinstaller/wiki/How-to-Report-Bugs>
for more about what would use to solve the issue.
