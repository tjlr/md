
### command line arguments
If you don't want to use the args array passed to your main function then you could use ```System.Environment.GetCommandLineArgs()``` instead. Note this will include the name of the program being run as the first item, unlike the args array given to your main function.

```F#
open System

[<EntryPoint>]
let main(args) =    
    printfn "args: %A" args
    printfn "env.cmdline: %A" <| Environment.GetCommandLineArgs()    
    0
```
