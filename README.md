4x5-Font
========

A 4x5 font for small displays.

    http://clubweb.interbaun.com/~rc/Papers/microfont.pdf
    
Use this tool to help get the hex:

    http://www.quinapalus.com/hd44780udg.html

Try to make sure that the array is in the same order as:

    http://ecee.colorado.edu/~ecen4633/index_files/ASCII-Map.pdf
    
So as to help with embedded projects.

`4x5-font.js` contains a javascript object describing the font.
Key/Value pairs are character/mapping pairs. Mapping is list of rows (4 bits).

Works in Python (remove `var`):

    python3
    >>> char_map = ...
    >>> char = 'A'
    >>> for row in char_map(char_map[char]):
    ...     print(bin(row))
    ...
    0b0100
    0b1010
    0b1110
    0b1010
    0b1010

That's an uppercase 'A':

     *
    * *
    ***
    * *
    * *
