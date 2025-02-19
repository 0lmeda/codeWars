# Highest Scoring Word

## Description
Given a string of words, you need to find the highest scoring word.

Each letter of a word scores points according to its position in the alphabet: a = 1, b = 2, c = 3 etc.

For example, the score of abad is 8 (1 + 2 + 1 + 4).

You need to return the highest scoring word as a string.

If two words score the same, return the word that appears earliest in the original string.

All letters will be lowercase and all inputs will be valid.

## Solution
    #include <string>
    
    std::string highestScoringWord(const std::string &str)
    {
      //Divide words
      std::vector <std::string> words;
      std::string ss = "";
      for(char c : str){
        if(c == ' '){
          words.push_back(ss);
          ss = "";
        }
        else{
          ss += c;
        }
      }
      
      if(!ss.empty()){
        words.push_back(ss);
      }
      
      //Find the value of each letter
      int highScore = 0, score = 0, time;
      int position = 0;
      for(int i = 0; i<words.size(); i++){
        
        for(char c : words[i]){
          position  = c-96;
          score += position;
        }
        
        if(score > highScore){
          highScore = score;
          time = i;
        }
        
        score = 0;
      }  
      std::cout<< words[time];
      return words[time];
    }
