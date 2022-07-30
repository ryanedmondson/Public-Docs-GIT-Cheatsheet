# A cheatsheet for GIT

By Ryan Edmondson (hello@ryanedmondson.com)

Helpful blogs for beginners:

- Coming soon

## Table of contents

1. Setup
   1. [Installing GIT](#Installing-GIT)
   2. [Initiating a repository](#Initiating-a-repository)
   3. [Editing files](#Editing-files)
2. GIT status
   1. [What is the GIT status](#What-is-the-git-status)
   2. [How to get the GIT status](#How-to-get-the-GIT-status)
      - [Detailed GIT status](#Detailed-GIT-status)
      - [Short GIT status](#Short-GIT-status)
3. Staging area
   1. [Add a file to the staging area](#Add-a-file-to-the-staging-area)
   2. [Remove a file from the staging area](#Remove-a-file-from-the-staging-area)
   3. [Remove a file from the staging area & the project](#Remove-a-file-from-the-staging-area-&-the-project)

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

## Git Status

### <a name="What-is-the-git-status">What is the GIT status</a>

The GIT status gives us an overview of our updates. There are 3 key status points:

1. Nothing edited:

   > nothing to commit, working tree clean

2. Files edited but not staged:

   > Changes not staged for commit

3. Files staged for commit:

   > Changes to be committed

### <a name="How-to-get-the-GIT-status">How to get the GIT status</a>

#### <a name="Detailed-GIT-status">Detailed GIT status</a>

To get a detailed summary of your GIT status run `git status` inside your repository's directory.

#### <a name="Short-GIT-status">Short GIT status</a>

To get a short summary of your GIT status run `git status -s` inside your repository's directory.

The first 2 characters of the status will indicate one of the following:

| Character | Description           |
| --------- | --------------------- |
| M         | Modified.             |
| T         | File type changed.    |
| A         | Added.                |
| D         | Deleted.              |
| R         | Renamed.              |
| C         | Copied.               |
| U         | Updated but unmerged. |
| ?         | Untracked changes.    |

The very first character represents the status in the staging area & the second character represents the status of the working directory.

## Staging

### <a name="Staging-area-context">Staging area context</a>

After you edit a file, it will be laballed as "unstaged" in the GIT status. You wouldn't want all your updates to be reflected in the repository as you may have accidently edited one. This is why GIT flags them as modified rather than putting them straight into the queue for commitment.

_Tip: Think of the staging area as the commitment queue_

### <a name="Add-a-file-to-the-staging-area">Add a file to the staging area</a>

To add a file to the staging area use `git add` followed by your file name.

### <a name="Remove-a-file-from-the-staging-area">Remove a file from the staging area</a>

To remove a file from the staging area use `git reset head` followed by your file name.

### <a name="Remove-a-file-from-the-staging-area-&-the-project">Remove a file from the staging area & the project</a>

To remove a file from the staging area use `git rm -f` followed by your file name.
