# Cerbose Documentation
## Introduction
**Skip reading this introduction if you want to. You won't miss any info.**  
Cerbose is a very simple Python library, so this documentation on it shouldn't be hard to understand. This document serves the purpose of going more in-depth than any other creator-made Cerbose information source (website, README), obviously excluding the source code itself. The goal of this is to allow you, the programmer, to effectively use Cerbose in your projects and understand how to use its various functions.  

## Table of Contents
Yes, I put the table of contents before the introduction. So what? I think it looks cool.
- [Installation](#installation) -- Can be skipped, assuming you know how to install a Python package.
    + [Manual Install](#manual-install)

## Installation
**You can skip reading this if you already know how to install a Python library.**
Similarly to any other Python library, there are two ways to install cerbose.
### PyPI Install
Cerbose is a hosted package ![here on PyPI](https://pypi.org/project/cerbose). To install it, simply run this command in your terminal:  
```bash
pip install cerbose
```
This should automatically install Cerbose and its dependency, `colorama`. If for some reason `colorama` isn't installed, you can install it manually:
```bash
pip install colorama
```
**Virtual Environments:**
Some systems exhibit odd behaviour with misconfigured PATH variables. If this arises, use a virtual environment. Follow the method that is for your operating system. If you use macOS, follow the Linux instructions.

**Linux:**  
```bash
python -m venv venv
source venv/bin/activate

deactivate  # run this when done with the venv
```

**Windows:**
```powershell
python -m venv venv
venv/Scripts/activate.bat                                          # use this for CMD
venv\Scripts\Activate.ps1                                          # use this for PowerShell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process   # do this if a security error occurs

deactivate                                                         # run this when done with the venv
```

> Note that Windows may require extra configuration for Python libraries.

If PIP is not properly configured:
- On Linux, ensure packages along the lines of `python-pip` and `python` are installed. (These are NOT the same per distro. Remember to check your distribution's repositories.)
- On Windows, ensure your Enviornment Variables and PATH are properly configured. Find elsewhere online for help on this.

The following code snippet shows the most important other operations for Cerbose (and any other Python library):
```bash
pip install --upgrade cerbose  # Update Cerbose
pip uninstall cerbose          # Remove Cerbose (what did i do wrong ): )
```


### Manual Install
weiners
