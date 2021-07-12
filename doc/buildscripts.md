# Buildscripts

This document aims to describe a buildscript, line by line

## Example

### Name

The name is the official name of the software. This way, something like Node would be named NodeJS here.

```
# name: Example
```

### Package name

The package name is what the package is called. For example, Discord is called discord-bin, since it's a binary file.

```
# pack: example-bin
```

### Description

The description is a short summary of the software.

```
# desc: Never gonna give you up
```

### Dependencies

The dependencies are the packages that the software depends on to build and run, seperated by commas.

```
# deps: Never, Gonna, Let, You, Down
```

### Version

The version is the version of the software. Binaries will have a set version, but software built from source will have a version of 'git'.

```
# ver: 6.9.42.0
```

### Type

The type helps shade know whether it should use wget or git to download the package. Direct is for direct downloads, and git for git repositories.

```
# type: direct
```

### Source

The source is the url to be downloaded or cloned.

```
# source: https://example.com/rickastley/linux.tar.gz
```

## Real example

This is an example of a real buildscript, in this case an Emacs buildscript.

```
# name: Emacs
# pack: emacs
# desc: The extensible, customizable, self-documenting real-time display editor
# deps: gnutls, jansson, gtk3
# ver: git
# type: git
# source: git://git.sv.gnu.org/emacs.git

cd emacs
./configure --prefix=/opt/shade
make
make install
```
