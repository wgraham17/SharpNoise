# SharpNoise

A library for generating coherent noise. It can be used to procedurally create natural-looking textures (such as wood, stone, or clouds), terrain heightmaps, and other things.

SharpNoise is a loose port of Jason Bevins' [libNoise](http://libnoise.sourceforge.net/) to C#. It adds some .Net features such as serialization and support for [C# Object Initializer syntax](http://msdn.microsoft.com/en-us/library/bb384062.aspx). SharpNoise is published unter the terms of the Gnu LGPL 3.

Available on NuGet: https://www.nuget.org/packages/SharpNoise

## Usage

SharpNoise has [modules](https://bitbucket.org/rthome/sharpnoise/src/tip/SharpNoise/Modules/?at=default) as building blocks for noise generators. There are two kinds of modules:

* Generators, which produce the actual noise
* Modifiers and Combiners, which take one or more inputs and do something with them, producing a new value

These modules can be joined together in a tree structure to generate very complex noise patterns.

### Example Applications

To see how to use SharpNoise, check out the example applications:

* [ComplexPlanetExample](https://bitbucket.org/rthome/sharpnoise/src/tip/ComplexPlanetExample/?at=default) generates a complex planetary surface, using [over 100 connected noise modules](https://bitbucket.org/rthome/sharpnoise/src/tip/ComplexPlanetExample/PlanetGenerator.cs?at=default).
* [OpenGLExample](https://bitbucket.org/rthome/sharpnoise/src/tip/OpenGLExample/?at=default) renders ever-changing data from a simpler noise generator in real time, using OpenGL 3.3.