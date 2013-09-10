crack
=====

A ruby script to brute force crack a password protected archive file.

why
----

I forgot the password to a 14 year-old Stuffit self-extracting (`.sea`) archive file of some importance.

requirements
----

* pre-generated word list files (1 word per line, multiple files allowed)
	* I used [crunch](http://sourceforge.net/projects/crunch-wordlist/)
* [randland/progressbar](https://github.com/randland/progressbar) for pretty progress
	* You don't need this library, turn on -v flag to see output
* Tested with `ruby 1.9.3p125 (2012-02-16 revision 34643) [x86_64-darwin11.4.0]`
* [unar](http://unarchiver.c3.cx/commandline) (if you don't already have it installed)

help
----
	> crack -h
	usage: crack FILE
	    -d, --dir [DIR]                  word list directory
	    -w, --wordlist [WORDLIST]        word list file
	    -v, --verbose                    display verbose output
	    -h, --help                       help

examples
----

use a single word list file

	./crack -w words.txt sample.zip

use a directory of word list files

	./crack -d path/to/dir sample.zip

warranty, disclaimer, legal, etc
----

There is no warranty. Use at your own risk.