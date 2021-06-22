# Buildscripts

This document aims to describe a buildscript, line by line

## Example

### Name

The name is the official name of the software. This way, something like Node would be named NodeJS here.

```
NAME: Example
```

### Package name

The package name is what the package is called. For example, Discord is called discord-bin, since it's a binary file.

```
PKGNAME: example-bin
```

### Description

The description is a short summary of the software.

```
DESC: Never gonna give you up
```

### Dependencies

The dependencies are the packages that the software depends on to build and run.

```
DEPS: Never, Gonna, Let, You, Down
```

### OS

This entry specifies which OS the package works on.

```
OS: Linux, Darwin
```

### Version

The version is the version of the software. Binaries will have a set version, but software built from source will have a version of 'git'.

```
VERSION: 6.9.42.0
```

### Type

The type helps shade know whether it should use wget or git to download the package. Direct is for direct downloads, and git for git repositories.

```
TYPE: direct
```

### Source

The source is the url to be downloaded or cloned. If a different url is required for different operating systems, specify it with SOURCE-${OS}.

```
SOURCE:
    SOURCE-DARWIN: https://example.com/rickastley/darwin.tar.gz
    SOURCE-LINUX: https://example.com/rickastley/linux.tar.gz
```

### Commands

This entry describes which commands have to be run to build and install the package. If different steps are required for different operating systems, specify them with COMMANDS-${OS}.

```
COMMANDS:
    COMMANDS-DARWIN: tar xzvf darwin.tar.gz; cd darwin; make; make install
    COMMANDS-DARWIN: tar xzvf linux.tar.gz; cd linux; make; make install
```

## Real example

This is an example of a real buildscript, in this case an Emacs buildscript.

```
NAME:     Emacs
PKGNAME:  emacs
DESC:     The extensible, customizable, self-documenting real-time display editor
DEPS:     gnutls, jansson, gtk3
OS:       Linux, Darwin
VERSION:  git

TYPE:     git
SOURCE:   git://git.sv.gnu.org/emacs.git
COMMANDS: cd emacs; ./configure --prefix=/usr/loca/shade; make; make install
```
