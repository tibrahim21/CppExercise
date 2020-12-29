
#include <iostream>
using namespace std;



int main()
{
    /* Write a program that computes the cost of a long-distance call. The cost of
    the call is determined according to the following rate schedule:
     
     a. Any call started between 8:00 am and 6:00 pm, Monday through Friday,
     is billed at a rate of $0.40 per minute.
     b. Any call starting before 8:00 am or after 6:00 pm, Monday through
     Friday, is charged at a rate of $0.25 per minute.
     c. Any call started on a Saturday or Sunday is charged at a rate of $0.15 per
     minute.
     
     The input will consist of the day of the week, the time the call started, and
     the length of the call in minutes. The output will be the cost of the call. The
     time is to be input in 24-hour notation, so the time 1:30 pm is input as
     13:30
     
     The day of the week will be read as one of the following pairs of character
     values, which are stored in two variables of type char:
     Mo Tu We Th Fr Sa Su
     
     Be sure to allow the user to use either uppercase or lowercase letters or a
     combination of the two. The number of minutes will be input as a value
     of type int. (You can assume that the user rounds the input to a whole
     number of minutes.) Your program should include a loop that lets the user
     repeat this calculation until the user says she or he is done.*/
    
    
    
    const double option1 = 0.4; //betweeen 8:00am and 6pm
    const double option2 = 0.25; //starting before 8:00am or after  6:00pm
    const double option3 = 0.15; //started on saturda or sunday
    string days;
    string Continue;
    char colon;
    
    int hour, length, min;
    double cost=0;
    
    do{
    
    cout <<"Enter the day of the week: ";
    cin>>days;
    
    cout <<"Enter the time  the call started (HH:MM):  ";
    cin>>hour>>colon>>min;
    
    cout <<"Enter the length of the call minutes: ";
    cin>>length;
        
        // The statement below determines the cost of the calls based on the requirements provided above.
    
    if(days == "Mo"||days == "mo"||days == "MO" ||days == "Tu"||days == "tu"||days == "TU" ||days == "Wu"||days == "wu"||days == "WU" || days == "Th"||days == "th"||days == "TH" ||days == "Fr"||days == "fr"||days == "FR" ){
        
        if(hour >=8 && hour <=18)
        {
            cost = length * option1;
            
        }
        else if(hour <=8 || hour >= 18)
        {
            cost = length * option2;
        }
        
        
    }
    else if (days == "Sa"||days == "SA"||days == "sa" || days == "Su"||days == "su"||days == "SU" )
    {
        if (hour >=8 && hour <=18)
        {
            cost = length * option3;
        }
        else
            cout <<"You made a wrong input"<<endl;
    }
    cout <<"The total cost of this call is: $"<<cost<<endl;
        
    
        cout<<"Do you want to calculate another bill? (yes/No)"<<endl;  //checks if the user would like to calculate another bill
        cin>>Continue;

    }
    while(Continue == "yes" || Continue =="Yes");
    cout <<"End of the program!"<<endl;
  
    
    
   
    
    
}
