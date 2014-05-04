#Building Hide-n-Stab
Tested on Linux and Windows.

##Install Dependencies

###[Haxe](http://haxe.org/download)
###[Lime](http://www.openfl.org/documentation/setup/install-lime/)

As easy as:

	haxelib install lime
	haxelib run lime setup


###[OpenFL](http://www.openfl.org/documentation/setup/install-openfl/)

As easy as:

	lime install openfl
	haxelib set openfl 1.3.0

###[spinehaxe](http://github.com/bendmorris/spinehaxe)
Clone the repository, enter that directory, and run the command `haxelib dev spinehaxe src`.

###[SpinePunk](http://github.com/bendmorris/SpinePunk)
Clone the repository, enter that directory, and run the command `haxelib dev SpinePunk src`.

###[HaxePunk (fork)](http://github.com/bendmorris/HaxePunk)
(use the "all" branch) 

Clone the fork, check out the "all" branch, and run `haxelib dev HaxePunk .`.

##Configure
Before building, modify `src/hidenstab/Defs.hx` to change the host and port.

Copy the `lime.ndll` file from the correct `HaxeToolkit/haxe/lib/lime/0,9,7/ndll` directory to the hide-n-stab directory.

##Make
The targets you want are "flash-final" for the client and "server" for the server.

	make flash-final
	make server

##Troubleshooting

###[Flash network security](http://haxe.org/doc/flash/security)
Try adding `-D network-sandbox` to the command in the Makefile that builds the flash client.

###OpenFL issue
In HaxePunk, edit the file `include.xml`. Find OpenFL, remove the version completely (just "<haxelib name=openfl />"), save and try again.

###Could not read HXCPP config
Run `haxelib run hxcpp` first.

###Lime not found
Run `haxelib run lime <args>` instead of `lime <args>`.

###Could not find haxelib "openfl" version 1.3.0
Run `haxelib set openfl 1.3.0` and agree to install.

##Links
* [Getting Started with HaxePunk](http://haxepunk.com/documentation/tutorials/getting-started/)

##Credits
Compiled by [arlsr](https://github.com/arlsr/) from comments by 	
[bendmorris](https://github.com/bendmorris/hide-n-stab) and lucb1e @HN.
