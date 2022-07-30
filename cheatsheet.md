# A cheatsheet for GIT

By Ryan Edmondson (hello@ryanedmondson.com)

Helpful blogs for beginners:

- Coming soon

## Table of contents

- Coming soon

1. Setup
   1. [Installing GIT](#Installing-GIT)
   2. [Initiating a repository](#Initiating-a-repository)
   3. [Editing files](#Editing-files)

## Setup

### <a name="Installing-GIT">Installing GIT</a>

1. Download from https://git-scm.com/downloads & install.
2. Test installation using `git --version`.
3. Find your .gitconfig file using `git config --list --show-origin`.
   - Mac: Usually ~/.gitconfig
   - Windows: Usually C:\ProgramData\Git\config
   - Linux: Usually ~/.gitconfig
4. Edit the global config file to include your username, email, editor settings & more.

[My boilerplate config settings]()

### <a name="Initiating-a-repository">Initiating a repository</a>

1. Navigate to desired directory.
2. Initate GIT using `git init`.
3. Create a file named ".gitignore" to exclude files & directories.

[My boilerplate .gitignore settings]()

### <a name="Editing-files">Editing files</a>

Once you have initiated your repository in a directory, git will automatically track any changes you make inside that directory. These changes will appear as "unstaged" unless they are captured by your .gitignore settings.
