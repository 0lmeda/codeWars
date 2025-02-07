# Sum of two lowest positive integers
## Description
Create a function that returns the sum of the two lowest positive numbers given an array of minimum 4 positive integers. No floats or non-positive integers will be passed.

For example, when an array is passed like [19, 5, 42, 2, 77], the output should be 7.

[10, 343445353, 3453445, 3453545353453] should return 3453455.



## Solution
<description of the challenge>
  
        #include <vector>
        #include <iostream> 
        
        long sumTwoSmallestNumbers(std::vector<int> numbers)
        {
        
          int size = numbers.capacity();
          long lowestsNumbers [2];
          
          if(numbers[0] < numbers[1]){
            lowestsNumbers[0] = numbers[0];
            lowestsNumbers[1] = numbers[1];
          }
          else{
            lowestsNumbers[0] = numbers[1];
            lowestsNumbers[1] = numbers[0];
          }
            
          for(int x = 0; x<2; x++){
        
            for(int y=0; y<size; y++){
            
              switch(x){
                  
                  case 0:
                  if(lowestsNumbers[x] > numbers[y] ){
        
                    lowestsNumbers[x] = numbers[y];
                  }
                  break;
                  
                  case 1:
                    if(lowestsNumbers[x] > numbers[y] && lowestsNumbers[0] != numbers[y] ){
                    lowestsNumbers[x] = numbers[y];
                  }
                  
                  break;
              }
            }
          } 
            return lowestsNumbers[0]+lowestsNumbers[1];
        }
        
        
          int main() {
          
          long actual = sumTwoSmallestNumbers({ 5, 8, 12, 19, 22 });
          std::cout << sumTwoSmalesstNumbers;
           return 0;
         }
         
