# S18T
Simple terminal game engine, written in Ruby.

## Getting Started
S18T Engine requires installed Ruby on OS.
### First steps
First, download the engine source code (S18T directory) to the empty location. Then, in the new file with the extension .rb, include the file S18T.rb located in the S18T directory. For example:
```Ruby
require "/path/to/S18T/S18T.rb"
```
It's enough to use the game engine classes.

### Using engine class
All classes and engine components are in the module named "S18T". Therefore, any reference to engine classes should be preceded by "S18T ::":
```Ruby
S18T::ClassName
```
For easier writing, it is recommended to write the code in the S18T module.

### Simple using S18T Engine
The simplest application using S18T looks like this:
```Ruby
module S18T
  require "/path/to/S18T/S18T.rb" #include S18T engine

  Engine.Start(); # start engine
  #do something
  Engine.Stop(); # stop engine
end
```
Application template using the S18T engine can be found in path "examples/template". It contains a code:
```Ruby
module S18T
    #Include S18T
    dir = "./"+File.dirname(__FILE__)+"/"
    require dir+"../../S18T/S18T.rb"

    #start S18T Engine
    Engine.Start();
    #clear terminal
    Screen.Clear();
    #set scene
    Engine.SetScene( Scene.new() );
    
    #mainloop
    #if engine working this loop will be still doing
    while Engine.Working?() do
        
        #call MainLoop() meth, S18T update Input class and scene.
        Engine.MainLoop();

        #if user press CTRL + C (^C), stop engine.
        if( Input.Key( KEY[:CTRL_C]))
            Screen.Clear();
            Engine.Stop();
        end
    end
end
```
## 
