GoGolf: Number of golf players predicton program (C++ Project)
======
.cpp file
------

'''

    ConsoleApplication12.cpp : Defines the entry point for the console application.
    #include <iostream> // IDE library direcive does not need quotes
    #include "playgolfh.h"
    using namespace std;
   
    int main()
    {
    estimate membertotal; // compare is the name of the class , value is the name of the function
    membertotal.get_temp(); 
    membertotal.compare_weather(); 

    system("pause");
    return 0;
    }
  
'''
    
header.h - Header File 
------

'''

	#include <iostream> // # sign indicates a direcive/macro
	#include <string>

	using namespace std; 

	class estimate
	
	{
	public:
  	void get_temp();
  	void compare_weather();
	void TotalMembersPlaying();

	private:
  	int val1;
  	int val2;
	int sunnyvalue;
	int overcastvalue;
	int rainvalue;
	};

	void estimate::get_temp()
	{
  	std::cout << "Welcome to the golf player predicton program!\n";
	std::cout << "\nWhat is the weather outlook for today? \nFor sunny weather, enter '1'" ;//information goes out to user
	std::cout << "\nFor overcast weather, enter '2' ";
	std::cout << "\nFor rainy weather, enter '3'\n"; 
  	std::cin  >> val1; //information used for comparison with 'if' statements
	std::cout << "What is the LOWEST temperature outlook for today?\n";
	std::cin  >> val2;
	}
	void estimate::compare_weather()
	{
	if (val2 < 32 )
	{
	cout << "The temperature is below 32 degrees; no members will play today\n";
	}



	else if (val1 == 1 && val2 > 32)
	{
	std::cout << "\nPlease enter the average number of members expected today : ";
	std::cin >> sunnyvalue;
	cout << "\nSince the outlook is 'sunny'; therefore 25% of members will play today \n";
	cout << (sunnyvalue * .25) << " is the estimates number of members that will play today!\n";
	}

	else if (val1 == 2 && val2 > 32)
	
	{
	std::cout << "\nPlease enter the average number of members expected today : ";
	std::cin >> overcastvalue;
	std::cout << "\nSince the weather is overcast; therefore 12% of members will play today \n";
	std::cout << (overcastvalue * .12) << " is the estimated number of members that will play today!\n";
	}

	else if (val1 == 3 && val2 > 32)
	{
	std::cout << "\nPlease enter the average number of members expected today : ";
	std::cin >> rainvalue;
	std::cout << "\nSince the outlook is 'rainy'; therefore 3% of members will play today \n";
	std::cout << (rainvalue * .03) << " is the estimated number of members that will play today!\n";
	}
  	}
  
'''
