# Turbo Bash
A bash library for complex bash scripting.

## Usage

You may download `turbobash.lib` and modify it as needed. It is encouraged, if you make an addition that could have widespread usage outside of your scripts and applications, that you contribute to upstream. Summon its functionalities, as usual in bash, by the command `source /path/to/turbobash.lib`.

## Features

### Basic Newt preset look and quick message boxes

It exports variables for a solid look for newt's whiptail graphics. It also provides a quick setup to message boxes:

    local title="title"
    local msg="message"
    _msgbox_

### Quick install command

A dependable solution for Debian/Ubuntu, Fedora/openSUSE, Arch and all derivated operating systems that are compliant with their packaging and use their package managers.

`insta packagename`

### Batch package installation and dependency parser

A dependable solution for Debian/Ubuntu, Fedora/openSUSE, Arch and all derivated operating systems that are compliant with their packaging.

    local _packages=(package1 package2 package3)
    _install_

You may set exceptions for parsing if your application requires by changing `list|exceptions|here` for each section.

### Batch flatpak installation

Easily list desired flatpaks for instalation with automated presets. The library default setting installs them for the user.

    _flatpaks=(this.flatpak.1 this.flatpak.2)
    _flatpak_

### Logger

Quick logger setup wherever your script needs.

    logfile="/path/to/logfile"
    _log_

### OS Language Detector

Quick and easy detection that outputs a `langfile` variable. It can be extended to add support to as many languages as you may require.

    _lang_
    source /path/to/lang/$langfile

### Script Invoker

Can summon scripts from your repository, allowing more flexibility and quick deployment of bugfixes. Requires setting up your repository URL in the `turbobash.lib` file.

    invoke="filename"
    _invoke_

### Root Wrapper

Wraps a function in `sudo`.

    func () {
        echo "I am SUDO!"
    }
    ...
    _root_ func



