# Contributing

Thank you for showing interest in contributing to the Shade buildscripts.
To communicate, you can join the [Matrix room](https://matrix.to/#/!seeNYJscvKSNvmTcQE:matrix.org?via=matrix.org)

You must have a basic knowledge of bash to contribute,
since buildscripts are essentially bash scripts.

## Conduct

### Respect others

Don't be a jerk to others.
Some people may be contributing for the first time to an open source project,
and you need to show them that open source isn't scary.

### Reasonable expectations

The Shade buildscripts are currently maintained by two people,
people who sleep and have day-to-day routines.
We can't always review your pull request immediately.
Additionally, don't expect Shade to become something huge.
It's a small hobby project for the moment, nothing big.

## Coding style

- Indentation must be 4 spaces. Not 1 tab, not 2 spaces, not 8 spaces.
- To run different code on different platforms, use $OSTYPE and an `if` statement

```sh
if [[ $OSTYPE == "darwin"* ]]; then
    # Do something for macOS
elif [[ $OSTYPE == "linux-gnu"* ]]; then
    # Do something for Linux
else
    exit 1
fi
```

- Use the templates in `doc/Build-template.md`
- You must write a metadata file. Templates are in `doc/Meta-template.md`
