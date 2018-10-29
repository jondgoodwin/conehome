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

Clone this repository to the location of the build environment, e.g.:

    git clone https://github.com/jondgoodwin/conehome.git \cone

Set the Windows CONEHOME environment variable to point to the new folder.
Also, include the $CONEHOME/bin folder in the PATH environment variable.

Be sure you have Visual Studio C++, the Windows SDK, and LLVM installed.
Obtain and build the Cone compiler as per its instructions.
You should be able to run 'conec --help' (set PATH as needed).

The "congo" build tool **must** be invoked within the "Developer Command Prompt" app.
This sets up the PATH, INCLUDE, LIBPATH and other environment variables correctly,
without which congo will fail to work.

Build the Cone runtime library
    cd $CONEHOME\packages\conert
	congo


## Building (Linux)

Clone this repository to where you want to place the build environment, e.g.:

    git clone https://github.com/jondgoodwin/conehome.git /cone

Modify the `~/.bash_profile` or equivalent file to define CONEHOME, e.g.:

    export CONEHOME="/cone"

Make congo usable by creating a symbolic link:

    ln -s /cone/bin/congo /usr/bin/congo

Obtain and build the Cone compiler as per its instructions.
You should be able to run 'conec --help' (set symbol link as needed).

Build the Cone runtime library
    cd $CONEHOME\packages\conert
	congo


## License

Cone home is distributed under the terms of the MIT license. 
See LICENSE for details.