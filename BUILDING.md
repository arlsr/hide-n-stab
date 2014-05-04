#Building Hide-n-Stab

##Install Dependencies

###[Haxe](http://haxe.org/download)
###[Lime](http://www.openfl.org/documentation/setup/install-lime/)

As easy as:

	haxelib install lime
	haxelib run lime setup


###[OpenFL](http://www.openfl.org/documentation/setup/install-openfl/)
Rename OpenFL version from 1.4.0 to 1.2.3 somehow.

###[spinehaxe](http://github.com/bendmorris/spinehaxe)
Clone the repository, enter that directory, and run the command `haxelib dev <library name> src`.

###[SpinePunk](http://github.com/bendmorris/SpinePunk)
clone the repository, enter that directory, and run the command `haxelib dev <library name> src`.

###[HaxePunk (fork)](http://github.com/bendmorris/HaxePunk)
*(use the "all" branch) *

Clone the fork, check out the "all" branch, and run `haxelib dev HaxePunk path/to/haxepunk`.

##Configure
Before building, modify `src/hidenstab/Defs.hx` to change the host and port.

Copy the `lime.ndll` file from the correct `HaxeToolkit/haxe/lib/lime/0,9,7/ndll` directory to the hide-n-stab directory.

##Make
The targets you want are "flash-final" for the client and "server" for the server.

	make flash-final
	make server

##Troubleshooting
Try adding "-Dnetwork-sandbox" to the command in the Makefile that builds the flash client.

In HaxePunk, edit the file `include.xml`. Find OpenFL, remove the version completely (just "<haxelib name=openfl />"), save and try again.
