# S18T
Simple terminal game engine, written in Ruby.

## Getting Started
First, download the engine source code (S18T directory) to the empty location. Then, in the new file with the extension .rb, include the file S18T.rb located in the S18T directory. For example:
```
require "/path/to/S18T/S18T.rb"
```
It's enough to use the game engine classes.

### Using engine class
All classes and engine components are in the module named "S18T". Therefore, any reference to engine classes should be preceded by "S18T ::":
```
S18T::ClassName
```
For easier writing, it is recommended to write the code in the S18T module.

### Simple using S18T Engine
The simplest application using S18T looks like this:
```
module S18T
  require "/path/to/S18T/S18T.rb"

  Engine.Start();
  #do something
  Engine.Stop();
end
```
