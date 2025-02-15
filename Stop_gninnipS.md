# Stop gninnipS My sdroW!

## Description
Write a function that takes in a string of one or more words, and returns the same string, but with all words that have five or more letters reversed (Just like the name of this Kata). Strings passed in will consist of only letters and spaces. Spaces will be included only when more than one word is present.

Examples:

"Hey fellow warriors"  --> "Hey wollef sroirraw" 
"This is a test        --> "This is a test" 
"This is another test" --> "This is rehtona test"

## Solution
    std::string spinWords(const std::string &str)
    {
      //Variables to spit the words
      std::vector <std::string> words;
      std::string word = "";
      
      //Save each word of the sentence
      for(char c : str){
        if(c == ' '){
    
          words.push_back(word);
          word ="";
        }
        else{
              word +=c;
        }
      }
      
        if (!word.empty()) {
            words.push_back(word);
        }
    
      
         
        int sizes = words.size();
        std:: string tempS, s;
     
        //Join the words and if there's one words that it is equal or more than 5 letter, it will be reversed.
        for(int i = 0; i<sizes; i++){
          
          if(words[i].length() >=5){
            tempS = std::string(words[i].rbegin(), words[i].rend());
            s += tempS;
            tempS = "";
          }
          else{
            s +=words[i];
          }
          
          if(i<words.size()-1){
            s+=" ";
          }
        
        }
      
    
    
      
      return s;
    }
