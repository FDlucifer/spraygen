# spraygen
Password list generator for password spraying - prebaked with goodies

<p align="center">
  <img width=400px src="resources/spraygenlogo.png" />
</p>

Generates permutations of Months, Seasons, Years, Sports Teams (NFL, NBA, MLB, NHL), Sports Scores, "Password".

All permutations are generated with common attributes appended/prepended (such as "!" or "#"), or custom separators (such as "." or "_").

Users can extend the attributes and separators using comma delimited lists of characters.

Spraygen also accepts single words or external wordlists that allow you to generate tuned custom wordlists as well.

You could use tools like crunch, a fancy bashloop over SecLists, or whatever have you but that takes time...this one is made for spraying, so get to it!


```
python3 spraygen.py -h                                                                                                                                                                          

     _
    (  \_
    (    \_
    (       \_  
    (         \_            ___
    ( Password   \         |   |
    (   Spray     |คคคคคคคค|___|
    (           _ /          |
    (       _ /         /~~~~~~~~~\
    (   _ /            (  Spray    )
    (_/                 |  This   |
                        |         |
                        | Get     |
                        |  Creds  |
                        |_________|

    Original Art by Alex Chudnovsky (Unaffiliated)
    Tool by 3ndG4me
    
usage: spraygen.py [-h] [--year_start YEAR_START] [--year_end YEAR_END] [-s separators] [-a attributes] [-w wordlist] [-n single word] [--mode {all,nosep,noattr,plain}] [--type {all,sports,months,seasons,password,custom}]
                   [-o output file] [-p]

Parse Spray List Arguments.

optional arguments:
  -h, --help            show this help message and exit
  --year_start YEAR_START
                        starting year for a range of years
  --year_end YEAR_END   ending year for a range of years
  -s separators         a comma delimited list of one or more separators
  -a attributes         a comma delimited list of one or more attributes
  -w wordlist           path to a custom wordlist
  -n single word        single custom word to generate a custom wordlist with
  --mode {all,nosep,noattr,plain}
                        Mode for list generation. Can be all, no separators, no attributes, or plain.
  --type {all,sports,months,seasons,password,custom}
                        Type of list to generate. Can be all, sports, months, seasons, password, or custom
  -o output file        name of a file to create and write the final output to
  -p                    prints the output line by line as plaintext
  ```

  ## Basic Usage
  1. Install dependencies `pip3 install -r requirements.txt`
  2. Run `python3 spraygen.py -p` - this will generate all default built in wordlists with all permutations and print them to the screen