# CMake JUCE Prototype
A prototype for using CMake and JUCE 6.

The goal is to keep environment management to a minimum,
and create consistency across devs and machines.

Project resource variables (JUCE files, custom modules, etc) 
are in the top CMakeLists.txt. This streamlines new projects by reducing setup time.

Another benefit is realized through the sharing of related projects and modules under the same configuration.
This encourages both code and build system settings sharing.

##Build

To build, open this project in an IDE
and click 'build' for one of the targets.

A project can also be generated for Xcode using:
```
cmake -G Xcode -B build
```
Or Visual Studio for Windows using:
```
cmake -G "Visual Studio 16 2019" -B build
```
For package management [CPM.cmake](https://github.com/TheLartians/CPM.cmake) is used.

CPM automatically fetches JUCE from GitHub, but you can also use the variable:
CPM_JUCE_SOURCE to point to a local JUCE folder using:
``-DCPM_JUCE_SOURCE="Path_To_JUCE"``
when invoking CMake.

More information on JUCE can be found [here](https://github.com/juce-framework/JUCE).


License:
Everything in this repo is free to use for any purpose. Please consult the CPM and JUCE repos
for their respective licensing information.
