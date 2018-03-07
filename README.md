> **Note:** This README is currently unfinished and the script has yet to be uploaded.

# GetSpecs
GetSpecs is a simple tool to promote reproducible computing by making it easier to share system specifications & versioning information.

## Motivation
barrier
open-source software

scientific reproducibility
programs should be simpler

## Installation
Download this respository
```
$ git clone https://github.com/OisinMoran/GetSpecs.git
```
Give the script permission to execute (so we can call it without the `bash` prefix)
```
$ chmod +x get_specs.sh
```
Create a symlink (so we can call it from anywhere, and do so without the `.sh` suffix)
```
$ sudo ln -s ~/get_specs.sh /usr/bin/get_specs
```

Optional:
[Grip](https://github.com/joeyespo/grip "Grip GitHub Respository")
```
$ pip install grip
```


## Usage
Activate environments
```
$ source activate ENV_NAME
```
Append the markdown formatted table of system specifications and version numbers to `README.md` file.
```
$ get_specs >> README.md
```
Optional: Preview the `README.md` using Grip.
```
$ grip -b
```

Alternatively, if you wish to place the information in a separate file, you can run:
```
$ get_specs > system.md
$ grip -b system.md
```
