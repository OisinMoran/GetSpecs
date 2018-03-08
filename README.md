# GetSpecs
GetSpecs is a simple tool to promote reproducible computing by making it easier to share system specifications & versioning information. Pull requests welcome & encouraged.

## Motivation
Reproducibility is central to the scientific method: if no one can reproduce your results they are under no obligation to belive them. The same goes for computing&mdash;and as machine learning tries to shake off it's alchemical tendencies, we must take reproducibililty and reproducible computing seriously.

A common source of issues in running Other People's Code™ is trying to run it on a system it was not designed for, or with different versions of the packages it depends on.
This tool aims to make explicit the system and package versions used in research projects, to decrease the time and frustration in attempting to set up an experimental system or reproduce someone else's results.

## Installation
Download this respository:
```
$ git clone https://github.com/OisinMoran/GetSpecs.git
```

Give the script permission to execute (so we can call it without the `bash` prefix):
```
$ chmod +x GetSpecs/get_specs.sh
```

Create a symlink (so we can call it from anywhere, and do so without the `.sh` suffix):
```
$ sudo ln -s ~/GetSpecs/get_specs.sh /usr/bin/get_specs
```

**Optional:**
Download the wonderful [Grip](https://github.com/joeyespo/grip "Grip GitHub Respository"), which enables you to render local readme files before sending them off to GitHub:
```
$ pip install grip
```


## Usage
Activate the environment you wish to share the details of (skip if not applicable):
```
$ source activate ENV_NAME
```

Change directory to the repository containing your valuable machine learning research:
```
$ cd PROJECT_FOLDER
```

Append the markdown formatted table of system specifications and version numbers to `README.md` file:
```
$ get_specs >> README.md
```

Optional: Preview the `README.md` using Grip:
```
$ grip -b
```

Alternatively, if you wish to place the information in a separate file, you can run:
```
$ get_specs > system.md
```

And view it using:
```
$ grip -b system.md
```

## To Do:
- [ ] Add commandline arguments (GPU flag, package list, etc.)
- [ ] Mac compatibility
- [ ] Windows compatibility
