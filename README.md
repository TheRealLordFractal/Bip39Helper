# Bip39 Super Fast Generator for BTC Crypto

This creates automated 12 random word phrases to use with brainflayer, The speed on this is super fast

The was originally written in pyton and converted to C for speed and to run multipul instances.

# Usage

Just running the script from the commandline will randomly generate 3, 6, 12 BIP39 code phrases::

	The C Dependencies are listed below 
      
      - Python 2.7 installed for library purposes on some machines

COMPILING: 

gcc -v -Os -I /usr/include/python2.7/ -L /usr/local/lib/python2.7/  -o bip39helper bip39helper.c  -lpython2.7  -lpthread -lm -lutil 
-ldl
	


Running the script is simple

USAGE EXAMPLES:


Make it super simple I have encluded the BIP39.txt files for the different languages,  all you need to do is choose your target.  I will update and work on this more.. However right now all you need to do is for EXAMPLE
english, copy the english.txt to wordlist.txt      In unix its cp english.txt wordlist.txt, you can do this for any language.

./bip39helper -n 5000000 >> 12words.txt 

In this example the script generates 12 random words per line of a text file, the -n specifys the # of lines you wish to make your txt file, and then save them to 12words.txt as output file
*NOTE* This can create VERY LARGE .txt files depending how many <-n> you pass to the script

-

This example Does not create any massive txt file and directs output directly to brainflayer, this is the most effect and fastest way to start checking BIP39 phrases

./bip39helper -n 9000000000000000000 | ../brainflayer/brainflayer -v -m tablefile.tab -o foundkeys.txt -b testfile.blm


SAMPLE OUTPUT:

rate:  270111.98 p/s found:     0/786432     elapsed:   11.218 s

*NOTE* I have been able to use this with over 10 process's running smooth on a I7-8400K


## Operators
* -n <number of lines you wish to create>

	* Generates <x> code phrases. Without selecting this option the default is 5.


* -w <file> or --wordlist <file>

	* Imports file to use for generating random phrases instead of the default wordlist.txt. 

Multiple operators can be used together. 

# License

Free and OpenSource to the public 

If you find this useful and wish to donate:

BTC Address:  1PJbzgqXDcbeqv2NXccQhY7HFWFxeURE22

