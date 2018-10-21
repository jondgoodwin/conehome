# Cone Home: The Build Environment

Cone home provides a build environment that makes it easier to organize and transform
[Cone](https://github.com/jondgoodwin/cone)-based projects
into ready-to-use native executables and web pages.
It does this by providing:

- A consistent folder organization (see below)
- Access to helpful tools, such as:
  - **conec**. The cone compiler
  - **congo**. The cone package and build manager
  - **cone**. The environment configuration tool

## $CONEHOME Folder Organization
  
The $CONEHOME systems environment variable specifies the root folder of this repository.
Its folders hold build tools, configuration files, useful packages, and sample programs
organized across the following folders:

- **bin**. Tools and program executables appear here ($PATH should specify)
- **lib**. Link-able libraries
- **packages**. Cone libraries (source)
- **javascript**. Javascript libraries
- **conec**. Cone compiler source
- **samples**. Cone sample projects
- **projects**. Cone program and library projects go here. Each project may have these subfolders:
  - **src**. Cone source files
  - **public**. Constructed web-site
  - **obj**. Cone object files
  - **images**. Image source files

## Building (Windows)

## Building (Linux)

## License

Cone home is distributed under the terms of the MIT license. 
See LICENSE for details.