# cs50-pset1-cash
Cs50 Pset1 Cash




#include <stdio.h>
#include <cs50.h>
#include <math.h> 
int main(void)
{
  //Creating a variable for change
  float f;
  int coins;
      
  //Prompting the user for change owed
  
   do
   {
       f = get_float("How much change are you owed:\n");
   }
    while (f <= 0);
 
//Converting float to int(dollars to cent)
   int change = 0;
       change = ((int)round(f*100));
    
   //Using the largest coins possible- quarters
    coins = 0; 
    
    while (change >= 25)
    {
        coins++;
        change = change - 25;
    }
   
    // Using dimes
     while (change >= 10)
    {
        coins++;
        change = change - 10;
    }
   
    // For nickels
    while (change >= 5)
    {
        coins++;
        change = change - 5;
    }
   
    // For pennies
     while (change >= 1)
    {
        coins++;
        change = change - 1;
    }
   printf("%i\n", coins);
}
