# Leetspeak Generator

A Python-based leetspeak generator that takes an input string of up to three words and generates all possible leetspeak variations.

## Overview

Leetspeak, also known as 1337 or leet, is an alternative alphabet used primarily on the internet. It uses various combinations of ASCII characters to replace certain letters. This tool allows you to generate all possible leetspeak variations of an input string containing up to three words. The resultant list can then be used as a base dictionary for password cracking. This comes in handy when targeting a particular organisation say 'mega corp'. 

Generating a list using the input phrase 'mega corp' to start with generates a ~1.1MB file with 93312 lines. 
Generating a list using the input phrase 'mega company' to start with generates a ~53MB file with 3359232 lines. 

As you can see, using a long/large starting input is not ideal as it will quickly generate large lists. 


## Features

- Accepts input of up to three words, separated by spaces
- Supports command line arguments for direct input and help message
- Generates all possible leetspeak variations for the given input string, including spaces
- Ignores numbers, special characters and upper case letters.  

## How to Use

### Interactive Mode (default)

- Run the script using the following command: `python leetspeak-generator.py`

### Direct Input Mode

- Run the script with the input string directly using the following command: `python leetspeak-generator.py -i "words here"`
- The script will generate and display all possible leetspeak variations of the input string. 
- Save to file with something like `python leetspeak-generator.py -i "words here" > words_here_leet.txt`

### In practice

The dictionary generated by itself is likely of little use/success in password cracking directly (although you might get lucky!), but ideally this is combined with rules from hashcat or similar. Using this as a base dictionary and then running rules against it is ideal.

### Display Help Message

- Run the script with the `-h` flag to display the help message: `python leetspeak-generator.py -h`

## Customization

The leetspeak character substitutions are defined in a dictionary within the script. You can easily update or modify the dictionary to include additional characters or alternative substitutions as needed. You can also up the word limit, but I wouldn't reccomend it as it'll create massive files. 

## ToDo 

Add more variation from: https://www.gamehouse.com/blog/leet-speak-cheat-sheet/
