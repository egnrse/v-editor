# v-editor
[![License](https://img.shields.io/github/license/egnrse/v-editor)](https://github.com/egnrse/v-editor/blob/main/LICENSE)
[![GitHub last commit (branch)](https://img.shields.io/github/last-commit/egnrse/v-editor/main)](https://github.com/egnrse/v-editor/commits/main)
[![GitHub tag (latest SemVer pre-release)](https://img.shields.io/github/v/tag/egnrse/v-editor?label=version)](https://github.com/egnrse/v-editor/releases)

A simple wrapper for your editor written in bash. I just found writing `nvim` took to long if i wanted to just edit a file. Of course u could also just use a bash/zsh macro.

# Installation
To make `v` availabe as a system wide command:
 - put `v-editor.sh` into `/usr/bin/v`	(this file should be named `v`) or anywhere else on your path.
 - and make it executable: `sudo chmod +x v`

to keep your `EDITOR` environment variable with sudo:
 - execute `sudo visudo` and add `Defaults env_keep += EDITOR`

If there is a package for your OS you should probably use that:

[![Packaging status](https://repology.org/badge/vertical-allrepos/v-editor.svg)](https://repology.org/project/v-editor/versions)

Or just use a macro? (put this in your shell config: `alias v=$EDITOR`)

# Usage
This script starts the program stored in the `EDITOR` environment variable with all given arguments (by calling `$EDITOR $@`). If `EDITOR` is empty, will try to start `vi` instead.

To open `test.txt` execute:  
`v test.txt`

There is a man page: `v.1`
