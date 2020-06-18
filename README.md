# Makefile

This is a generic Makefile template that I can use for most of my C projects.

## Usage

In the project's root directory, place all source files in a `src` directory and header files in an `include` directory. Then simply update the following variables in the template as per the project.

```
LDLIBS
CFLAGS
EXEC
```

## Example

For a project that uses [GTK](https://www.gtk.org/), I could use

```
LDLIBS  = `pkg-config --libs gtk+-3.0`
CFLAGS  = -Wall -MMD -MP `pkg-config --cflags gtk+-3.0`
EXEC    = main
```

Make will then create the following folder structure.

```
dep/
    ...
include/
    ...
obj/
    ...
src/
    ...
main
Makefile
README.md
...
```
