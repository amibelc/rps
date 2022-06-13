# rps
rock scissors paper
#include <iostream>
#include <cstdlib> // for randnumber 
#include <ctime>

using namespace std;

int main ()
{  
    int user=0;
    int Computer=0;

// display the user choice 

    cout << "You will play the game of Rock, Paper and Scissors against the computer.\n";
    cout << "Enter the number of your choice :\n";
    cout << " 1- Rock\n";
    cout <<" 2- Paper\n";
    cout <<" 3- Scissors\n";
    cin >> user;

    if (user==1)
    {
        cout <<" You choose Rock\n";
    }
    else if  (user==2)
    {
        cout << " You choose Paper\n";
    }
    else
     {  
           cout << "You choose Scissors\n";
     }

// Display the computer choice
 srand (time (NULL));

 Computer = rand ()% 3+1;

    if (Computer==1)
    {
        cout <<" Computer choose Rock\n";
    }
    else if  (Computer==2)
    {
        cout << " Computer choose Paper\n";
    }
    else
     {  
           cout << "Computer choose Scissors\n";
     }
   
// Display the Winner 
// user choice : Rock 

    if (user==1)
    {
        if (Computer==1)
        {
        cout<< "It's a tie!!\n";
        }
        else if (Computer==2)
        {
        cout <<" The computer choose Paper.\n";
        cout << " Rock is covered by Paper the computer wins!!!! \n";
        }
        else 
        {
        cout << " The computer choose Scissors\n ";
        cout << " Rock crushes Scissors you win!";
        }
    }
    else if (user<1 || user>3 )
    {

    cout <<"Please enter you choice from 1 to 3\n";
    }
// user choice : Paper paper

if ( user== 2)
{   
    if(Computer == 2)
{
        cout << " The computer chooses Paper\n";
        cout << " It's a tie\n";
}
    else if (Computer==1)
{
        cout << " The computer chooses Rock\n";
        cout << "Paper covers Rock you win!\n";
}
    else
{
        cout <<"The computer choose Scissors\n";
        cout << "Paper is cut by Scissors the computer wins!";
}
}

// User choice : Scissors
if ( user==3 )
{   if (Computer==3)
    {
    
    cout << " It's a tie !!\n";
    }
    else if (Computer== 2)
    {
    
    cout << " Scissors cuts Paper you win!\n";
    }
    else 
    {
    
    cout << "Scissors are crushed by Rock computer wins!\n";
    }
}


  return 0;
}
 
    
