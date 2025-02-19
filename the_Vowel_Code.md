# The Vowel Code

## Description
Step 1: Create a function called encode() to replace all the lowercase vowels in a given string with numbers according to the following pattern:

a -> 1
e -> 2
i -> 3
o -> 4
u -> 5
For example, encode("hello") would return "h2ll4". There is no need to worry about uppercase vowels in this kata.

Step 2: Now create a function called decode() to turn the numbers back into vowels according to the same pattern shown above.

For example, decode("h3 th2r2") would return "hi there".

For the sake of simplicity, you can assume that any numbers passed into the function will correspond to vowels.

## Solution
    #include <string>
    
    std::string encode(const std::string &str) {
      
      std::string ss = "";
    
      for(char c : str){
        switch(c){
            case 'a':
            ss += '1';
            break;
            case 'e':
            ss += '2';
            break;
            case 'i':
            ss += '3';
            break;
            case 'o':
            ss += '4';
            break;
            case 'u':
            ss += '5';
            break;
            
            default:
            ss+=c;
            break;
        } 
      }
      
      
      
      return ss;
    }
    
    std::string decode(const std::string &str) {
      
       std::string ss = "";
    
      for(char c : str){
        switch(c){
            case '1':
            ss += 'a';
            break;
            case '2':
            ss += 'e';
            break;
            case '3':
            ss += 'i';
            break;
            case '4':
            ss += 'o';
            break;
            case '5':
            ss += 'u';
            break;
            
            default:
            ss+=c;
            break;
        } 
      }
      
      return ss;
    }
