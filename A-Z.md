# From A to Z

## Description
Given a string indicating a range of letters, return a string which includes all the letters in that range, including the last letter.
Note that if the range is given in capital letters, return the string in capitals also!

Examples
"a-z" ➞ "abcdefghijklmnopqrstuvwxyz"
"h-o" ➞ "hijklmno"
"Q-Z" ➞ "QRSTUVWXYZ"
"J-J" ➞ "J"
Notes
A hyphen will separate the two letters in the string.
You don't need to worry about error handling in this kata (i.e. both letters will be the same case and the second letter will not be before the first alphabetically).

## Solution
    #include <string>
    
    std::string gimme_the_letters(const std::string& sp)
    {
        std::string letter;
        std::string letters;
        for(char c : sp){
          if(c == '-'){
            continue;
          }
          else{
              letter.push_back(c);
          }
    
          
        }
      
            for (char c = letter[0]; c <= letter[1]; ++c) {
                letters.push_back(c);
            }
      
        return letters;
    }
