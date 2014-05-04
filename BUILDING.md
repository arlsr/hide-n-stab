Install:

* haxe
* lime
* openfl, rename openfl version from 1.4.0 to 1.2.3
* spinehaxe: github.com/bendmorris/spinehaxe
* SpinePunk: github.com/bendmorris/SpinePunk
* my fork of HaxePunk: github.com/bendmorris/HaxePunk (use the "all" branch) 

To install spinehaxe and SpinePunk, clone the repository, enter that directory, and run the command "haxelib dev <library name> src". For HaxePunk, clone my fork, check out the "all" branch, and run "haxelib dev HaxePunk path/to/haxepunk"

Before building, modify src/hidenstab/Defs.hx to change the host and port.

In HaxePunk, edit the file "include.xml." Find openfl, remove the version completely (just "<haxelib name=openfl />"), save and try again.

The targets you want are "flash-final" for the client and "server" for the server.

	make flash-final
	make server

You'll need to run "lime setup linux" to build the lime.ndll file and then copy it into the hide-n-stab directory.

Try adding "-Dnetwork-sandbox" to the command in the Makefile which builds the flash client.
