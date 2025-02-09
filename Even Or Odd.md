#Even or Odd

## Description
Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.


## Solution
      #include <string>
      
      std::string even_or_odd(int number) 
      {
        if(number % 2 == 1 || number % 2 ==-1){
          return "Odd";
        }
        else{
          return "Even";
        }
      
        
      }
