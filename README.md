# Guess_num
This is my first DSA project in C++. This project guess the number which is randomly generated.



#include <iostream>
#include <cstdlib>
#include <ctime>
using namespace std;

int main() 
{
   srand(time(0));   
   int secretNum = rand()%100 + 1;  
   int userGuess; int count=0;   
   
   cout<<"Number Guessing Game"<<endl;
   cout<<"I picked a number between 1 and 100\n";

   do{
       cout<<"Enter guess: ";
       cin>>userGuess;
       count++;

       if(userGuess > secretNum)
       {
           cout<<"Too high... try smaller"<<endl;
       }
       else if(userGuess < secretNum)
       {
           cout<<"Too low... try bigger"<<endl;
       }
       else{
           cout<<"Yesss!! you got it!"<<endl;
           cout<<"Tries taken: "<<count<<"\n";
       }

   }while(userGuess != secretNum);

   return 0; 
}