---
title: Getting the source
layout: code
tab: code
unique_id: codepage
author: Emmanuel Bernard
---
# #{page.title}

We publish everything on GitHub under the [Ceylon organization](https://github.com/ceylon).

You need to install the Java Development Kit 6 or above (from Oracle or OpenJDK). 
You also need to install `git`.

## Ceylon projects

The Ceylon project is actually made up of four smaller projects:

- [Parser, typechecker and specification](#parser_typechecker_and_specification)
- [Compiler and documentation compiler](#compiler_and_documentation_compiler)
- [Ceylon language module](#ceylonlanguage_module)
- [Ceylon Eclipse IDE plugin](#ceylon_eclipse_ide_plugin)
- [Module system](#module_system)
- [Launcher](#launcher)

### Parser, typechecker and specification

<table>
 <tr><th>Git repository</th><td><a href="https://github.com/ceylon/ceylon-spec">https://github.com/ceylon/ceylon-spec</a></td></tr>
 <tr><th>Issue reporting</th><td><a href="https://github.com/ceylon/ceylon-spec/issues">https://github.com/ceylon/ceylon-spec/issues</a></td></tr>
</table>

This is a library that parses Ceylon source files, and runs type analysis on them, 
producing a list of warnings and errors, and a the model of the analyzed source
code. This is the compiler frontend.

The Ceylon language specification is also kept in this project.

#### Building

You can build and publish the typechecker to the local Ceylon repository (`~/.ceylon`) 
like this:

<!-- lang: bash -->
    ant publish

You can also build the language specification:

<!-- lang: bash -->
    ant doc

The generated documentation will be available in `build/en/html/index.html`

There's more info in the [README](https://github.com/ceylon/ceylon-spec/blob/master/README.md).

### Compiler and documentation compiler

<table>
 <tr><th>Git repository</th><td><a href="https://github.com/ceylon/ceylon-compiler">https://github.com/ceylon/ceylon-compiler</a></td></tr>
 <tr><th>Issue reporting</th><td><a href="https://github.com/ceylon/ceylon-compiler/issues">https://github.com/ceylon/ceylon-compiler/issues</a></td></tr>
</table>

This is where you'll find the `ceylonc` compiler and the `ceylond` API documentation compiler,
as well as the Ceylon ant tasks.

You can find out how to run these commands from the [documentation](#{site.urls.spec}#tools).

Feeling adventurous and want to help us with the compiler backend? Read [how to work on that project](/code/contribute).

#### Building

This project depends on the [Parser and typechecker](#parser_typechecker_and_specification) 
and [Ceylon language module](#ceylonlanguage_module) projects. Youshould check them out and 
build them first.

You can build the compiler project like this:

<!-- lang: bash -->
    ant build

There's more info in the [README](https://github.com/ceylon/ceylon-compiler/blob/master/README.md).

### `ceylon.language` module

<table>
 <tr><th>Git repository</th><td><a href="https://github.com/ceylon/ceylon.language">https://github.com/ceylon/ceylon.language</a></td></tr>
 <tr><th>Issue reporting</th><td><a href="https://github.com/ceylon/ceylon.language/issues">https://github.com/ceylon/ceylon.language/issues</a></td></tr>
</table>

This projects contains the module `ceylon.language`, the core classes 
mentioned in the language specification.

See the [API documentation](#{site.urls.apidoc}/) for more information.

#### Building

You can build and publish the language module to the local Ceylon repository 
(`~/.ceylon`) like this:

<!-- lang: bash -->
    ant publish

There's more info in the [README](https://github.com/ceylon/ceylon.language/blob/master/README.md).

### Module system

<table>
 <tr><th>Git repository</th><td><a href="https://github.com/ceylon/ceylon-module-resolver">https://github.com/ceylon/ceylon-module-resolver</a></td></tr>
 <tr><th>Issue reporting</th><td><a href="https://github.com/ceylon/ceylon-module-resolver/issues">https://github.com/ceylon/ceylon-module-resolver/issues</a></td></tr>
</table>

This is where you'll find the Ceylon module system, based on JBoss Modules.

#### Building

You can build the module system project like this:

<!-- lang: bash -->
    mvn install

There's more info in the [README](https://github.com/ceylon/ceylon-module-resolver/blob/master/README.md).

### Launcher

<table>
 <tr><th>Git repository</th><td><a href="https://github.com/ceylon/ceylon-runtime">https://github.com/ceylon/ceylon-runtime</a></td></tr>
 <tr><th>Issue reporting</th><td><a href="https://github.com/ceylon/ceylon-runtime/issues">https://github.com/ceylon/ceylon-runtime/issues</a></td></tr>
</table>

This is where you'll find the Ceylon `ceylon` launcher command, which runs Ceylon modules.

#### Building

This project depends on the [Ceylon language module](#ceylonlanguage_module) project, make sure
you read the [README](https://github.com/ceylon/ceylon-runtime/blob/master/README.md) information
to set it up correctly.

You can build the launcher project like this:

<!-- lang: bash -->
    mvn install

There's more info in the [README](https://github.com/ceylon/ceylon-runtime/blob/master/README.md).

### Ceylon Eclipse IDE plugin

<table>
 <tr><th>Git repository</th><td><a href="https://github.com/ceylon/ceylon-ide-eclipse">https://github.com/ceylon/ceylon-ide-eclipse</a></td></tr>
 <tr><th>Issue reporting</th><td><a href="https://github.com/ceylon/ceylon-ide-eclipse/issues">https://github.com/ceylon/ceylon-ide-eclipse/issues</a></td></tr>
</table>

This project contain the Ceylon IDE Eclipse plugin.

#### Building

Instructions may be found in the
[README](https://github.com/ceylon/ceylon-ide-eclipse/blob/master/README.md).
