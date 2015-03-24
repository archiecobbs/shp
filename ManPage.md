
```
SHP(1)                               BSD General Commands Manual                              SHP(1)

NAME
     shp - Like PHP except you write your script in shell script

SYNOPSIS
     shp [script [args ...]]

DESCRIPTION
     shp parses and executes SHP scripts in the manner of PHP, except nested scripts are written in
     shell scripting language instead of the PHP language.  shp outputs its script file, with nested
     <?shp ... ?> blocks executed as shell scripts.

     If no script is provided, standard input is read.  Otherwise, any subsequent arguments are
     passed to the script.

     To pass arguments to a standard input script, use `-' for script.

     If the first line of the input script starts with a shebang (`#!'), it is ignored.  This allows
     scripts to be made executable by putting #!/usr/bin/shp as the first line.

OPTIONS
     --check
          Just check the syntax of the script instead of executing it.

     --dump
          Just output the generated shell script instead of executing it.

     --shell
          Specify an alternate shell (the default is `/bin/bash -s').

     --help
          Display command line help.

     --version
          Display version and exit.

VERSION
     This man page documents shp version 1.0.2.

AUTHOR
     Archie L. Cobbs <archie@dellroad.org>

BSD                                       November 1, 2011                                       BSD
```