# Cerbose Documentation
This file comes with every installation of Cerbose. If you already knew that...I can tell.

## Introduction
**Skip reading this introduction if you want to. You won't miss any info.**  
Cerbose is a very simple Python library, so this documentation on it shouldn't be hard to understand. This document serves the purpose of going more in-depth than any other creator-made Cerbose information source (website, README), obviously excluding the source code itself. The goal of this is to allow you, the programmer, to effectively use Cerbose in your projects and understand how to use its various functions.  

## Table of Contents
Yes, I put the table of contents before the introduction. So what? I think it looks cool.
- [Installation](#installation) -- Can be skipped, assuming you know how to install a Python package.
    - [PyPI Install](#pypi-install)
    - [Manual Install](#manual-install)
- [Post-Installation](#post-installation)
- [Functions](#functions) -- Skip to here if you already have Cerbose installed
    - [INTERNAL_SUBSITUTE](#internal_subsitute)
    - [cprint](#cprint)

## Installation
**You can skip reading this if you already know how to install a Python library.**
Similarly to any other Python library, there are two ways to install cerbose.

NOTE FOR LINUX: Some distributions will have `python3` in the command line instead of `python` as listed in docs. Use this to check:
```bash
which python
which python3
```

### PyPI Install
Cerbose is a hosted package [here on PyPI](https://pypi.org/project/cerbose). To install it, simply run this command in your terminal:  
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
- On Windows, ensure your Environment Variables and PATH are properly configured. Find elsewhere online for help on this.

The following code snippet shows the most important other operations for Cerbose (and any other Python library):
```bash
pip install --upgrade cerbose  # Update Cerbose
pip uninstall cerbose          # Remove Cerbose (what did i do wrong ): )
```

### Manual Install
> NOTE: This is NOT recommended. The PyPI install is much easier and this currently only has Linux instructions (not like that's a bad thing).

To install Cerbose manually, you first need the library files. Clone it with git using this command:
```bash
git clone https://github.com/jasperredis/cerbose-lib
cd cerbose-lib
```
Now use any of these commands to install the library (make sure to read the comments to know what you're doing!):
```bash
python -m pip install .     # Regular install, recommended
python -m pip install -e .  # Editable install, so it creates a symlink from the cloned repository to your site packages.
sudo cp src/cerbose.py /usr/lib/python3.x/site-packages/cerbose.py    # Not recommended; manually copying the script to site packages. Skips dependency, version, and update checking. Ensure python3.x is your actual Python version number.
```

## Post Installation
No, don't skip this, this is unique to Cerbose.
Upon installing Cerbose, your directory should look like this:
```plaintext
cerbose-lib
├── .readme/
│   ├── jrisbanner.png
│   ├── logo.png
│   └── test.png
├── docs/
│   └── DOCS.md
├── examples/
│   ├── config.json
│   └── test.py
├── src/
│   └── cerbose.py
├── LICENSE
├── LICENSE-GPL
├── LICENSE-LGPL
├── LICENSE-MIT
├── pyproject.toml
├── README.md
```
If it doesn't...well, that's not *good*.  
If you don't have the directory (you probably installed via PyPI), that's okay, either run this in your terminal:
```bash
git clone https://github.com/jasperredis/cerbose-lib
```
and `cd` into the directory, or simply go to [the repository on GitHub](https://github.com/jasperredis/cerbose-lib) and download really the only thing you need: `examples/test.py`.

Assuming it does, you can probably delete `.readme/` now, you don't need it unless you're actively checking the README (which is on the GitHub repository anyways).  
Now, to make sure Cerbose is working, try running the test script via the terminal command here (ENSURE YOU ARE INSIDE OF THE `cerbose-lib/` DIRECTORY!:
```bash
python examples/test.py
```
And if on Windows that doesn't work, try this in PowerShell:
```powershell
py examples/test.py
```
If that works, you can continue!

## Functions
Finally, we move on to the most important part of this documentation; how to actually use Cerbose.  
First, like any other Python library, ensure that Cerbose is actually imported, with:
```python
import cerbose
```
at the top of your file.  
I also reccomend adding:
```python
from cerbose import cprint, mprint
```
and even adding `cerbar` or `cin` to it if you really need those functions a lot. Though, `cprint`/`mprint` are the functions you absolutely do not want to have to type `cerbose.` for.

### INTERNAL_SUBSITUTE
Before we get into functions, there is a universal variable across them; internally, this shouldn't need to be used. This is a list containing the names you input for functions requesting a colour to replace the `colorama` colours. Here is a table showing what all of these colours are:

| Subsitute Text | `colorama` Colour | Description |
| --- | --- | --- |
| `"black"` | `Fore.BLACK` | Difficult to see. |
| `"red"` | `Fore.RED` | -- |
| `"green"` | `Fore.GREEN` | -- |
| `"yellow"` | `Fore.YELLOW` | -- |
| `"blue"` | `Fore.BLUE` | -- |
| `"magenta"` | `Fore.MAGENTA` | -- |
| `"cyan"` | `Fore.CYAN` | -- |
| `"white"` | `Fore.WHITE` | -- |
| `"lightblack"` | `Fore.LIGHTBLACK_EX` | -- |
| `"lightred"` | `Fore.LIGHTRED_EX` | -- |
| `"lightgreen"` | `Fore.LIGHTGREEN_EX` | -- |
| `"lightyellow"` | `Fore.LIGHTYELLOW_EX` | -- |
| `"lightblue"` | `Fore.LIGHTBLUE_EX` | -- |
| `"lightmagenta"` | `Fore.LIGHTMAGENTA_EX` | -- |
| `"lightcyan"` | `Fore.LIGHTCYAN_EX` | -- |
| `"lightwhite"` | `Fore.LIGHTWHITE_EX` | -- |
| `"normal"` | `Fore.RESET` | Normal terminal text colour; default for normal text. |

### cprint
`cprint`, the highlight function of Cerbose, allows you to output highly configurable tagged text to the console. Here is a deep overview of how to use it!

`cprint` is defined in Cerbose as:
```python
cprint(type, text, *, logfile=None, logfeedback=False, textcol="normal", stagtype=None, timestamp=False, valonly=False):
```
This means that type and text are the first two required arguments, and the rest are optional keyword arugments.

`type` defines the "tag" the output uses.  
Here is an output of text from Cerbose (examples/test.py)
```plaintext
[OK]  : I like frogs.
[NOTE]: I like frogs.
[WARN]: I like frogs.
[ERROR]: I like frogs.
[DEBUG]: I like frogs.
```
Despite not being able to see the colours, you can see the parts in brackets. Those are tags.  
Assuming you are using the default configuration, there are 14 of them. That number varies by your configuration, but you will always have at least 1 (if you don't want errors, that is).

Here is a table showing the default configurations of the tags in cprint:
| Input | Text | Colour |
| --- | --- | --- |
| `'none'` | `NONE` | `'white'` |
| `'ok'` | `OK` | `'green'` |
| `'note'` | `NOTE` | `'cyan'` |
| `'warn'` | `WARN` | `'yellow'` |
| `'error'` | `ERROR` | `'red'` |
| `'debug'` | `DEBUG` | `'magenta'` |
| `'info'` | `INFO` | `'cyan'` |
| `'input'` | `INPUT` | `'lightblue'` |
| `'load'` | `LOAD` | `'red'` |
| `'pause'` | `PAUSE` | `'yellow'` |
| `'stat'` | `STAT` | `'magenta'` |
| `'fatal'` | `FATAL` | `'red'` |
| `'trace'` | `TRACE` | `'magenta'` |
| `'proc'` | `PROC` | `'magenta'` |

#### Logging
Logging in `cprint` is simple.  
Set the `logfile` argument to whatever file you want (e.g., `logfile="log.txt"`), and upon running the `cprint` function, that log file will be created if it doesn't already exist, and written to (assuming no errors occur).  
You can also 
