# Split Strings

## Description
Complete the solution so that it splits the string into pairs of two characters. If the string contains an odd number of characters then it should replace the missing second character of the final pair with an underscore ('_').

Examples:

* 'abc' =>  ['ab', 'c_']
* 'abcdef' => ['ab', 'cd', 'ef']


## Solution
    #include <string>
    #include <vector>
    
    std::vector<std::string> solution(const std::string &s)
    {
        std::vector <std::string> ss;
        std::string characters = "";
        int counter = 0;
        for(char c: s){
          characters += c;
          counter++;
          if(counter == 2){
            ss.push_back(characters);
            counter = 0;
            characters  = "";
          }
        }
      
        if(!characters.empty()){
          if(counter==1){
            characters += "_";
          }
          ss.push_back(characters);
        }
        return ss; // Your code here
    }
