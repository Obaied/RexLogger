# RexLogger

Add `RexLogger.smali` to a decompiled app to inject logs in the app. For more info on instructions, see `RexLogger.java`

# Usage
- Make a directory called `rex` in the `smali` directory on the decompiled app. I'm assuming you've used `apktool` to do the decompilation.
- Put `RexLogger.smali` in the newly created `rex` directory.
- Rename `com/aaa/rex` in `RexLogger.smali` to the package directory you've put it in.
- Look up the smali reference for each function you wanna call in `RexLogger.java`. 

An example invocation would be something like:
```smali
    invoke-static {}, Lcom/spotify/rex/RexLogger;->d()I
```

Printing a stacktrace would look like this:

```smali
    invoke-static {}, Lcom/spotify/rex/RexLogger;->stacktrace()I
```