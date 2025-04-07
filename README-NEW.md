# 🛠️ Installation Guide

## Requirements

- macOS with [Homebrew](https://brew.sh/)
- [pyenv](https://github.com/pyenv/pyenv)
- Python 3.11.x
- [Fontlab 7, Version 7.2.0.7644 (or possibly later)](https://fontlab.s3.amazonaws.com/fontlab-7/7644/FontLab-7-Mac-Install-7644.dmg)
- You have to install their Python 2.7 package

## 1. Install system dependencies

```bash
brew install pyenv cairo

pyenv install 3.11.8
pyenv local 3.11.8

# Install pipx (if not already installed)
brew install pipx
pipx ensurepath

# Install pipenv using pyenv's Python
pipx install pipenv --python "$(pyenv which python3.11)"
```

## 2. Install project dependencies

```bash
pipenv install
```

## 3. Build the project

```bash
pipenv shell
bash tools/build-macos.command
```

This will open FontLab 7 and run the build script. You can skip version upgrades and just use the free trial. It asked me if I want to keep fractions or round them.
I chose to round them because the button was blue.

It will take a while to finish, so be patient. It will more than once inform you then some export/build has worked.

When FontLab 7 is done, I had to close it myself.

After that, the script will continue and build the fonts.