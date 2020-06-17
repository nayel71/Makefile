# Makefile
This is a general Makefile template that I can use for most of my C projects.

Place all source files in the `src` directory and header files in the `include` directory, in the project's root directory. Then simply update the following variables in the template based on the project.

```
LDLIBS
CFLAGS
EXEC
```

E.g. for a project that uses [GTK](https://www.gtk.org/), I could use

```
LDLIBS  = `pkg-config --libs gtk+-3.0`
CFLAGS  = -Wall -MMD -MP `pkg-config --cflags gtk+-3.0`
EXEC    = main
```

Running `make` will then create the following folder structure.

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
