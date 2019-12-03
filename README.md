[![JetBrains incubator project](https://jb.gg/badges/incubator-plastic.svg)](https://confluence.jetbrains.com/display/ALL/JetBrains+on+GitHub)

Kotlin.TeamCity
===============

An Ant script and TeamCity meta-runner to automatically setup all 
required settings for IntelliJ IDEA build runner to build kotlin 
projects

It declares all parameters as specified in 
https://confluence.jetbrains.com/display/JET/Setting+up+a+TeamCity+build+that+uses+Kotlin

Installation
============
- Download and apply meta-runner ```kotlinc.xml``` to your TeamCity installation.
- Add ```Setup Kotlinc``` build runner to the build(s) before the ```IntelliJ IDEA``` build runner
- Enjoy


Internals
==========
The script uses TeamCity service message to set all necessary build parameters. 

It also sets/overrides the ```system.path.macro.KOTLIN.BUNDLED``` parameter with 
full path to Kotlin on build agent. The parameter is the alias to 
the ```KOTLIN_BUNDLED``` IntelliJ IDEA path variable in the build runner.
You may have any value of the ```system.path.macro.KOTLIN.BUNDLED``` parameter 
in TeamCity build parameters tab.


License
=======
MIT

You may do what ever you like with the script


