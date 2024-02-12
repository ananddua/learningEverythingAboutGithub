// POINTER APPROACH IN C++ BY LOVE BABBAR BHAIYA
#include <iostream>
// using namespace std;
bool
armstrongNumber (int X)
{
  //introducing variable
  int result = 0;
  int Y = X;
  if (X < 0)
	{
	  return false;
	}
  while (X != 0)
	{
	  int a = X % 10;			//extracting the last number is done by taking the number from the
	  // code using highest factor of division
	  result = result + (a * a * a * a);
	  X = X / 10;				//re-structure an integer using highest adding value
	}
  if (result == Y)
	{
	  return true;
	}
  else
	return false;
}

int
main ()
{
  std::
	cout << "The number is an armstrong number? (T/F) => " <<
	armstrongNumber (1634) << std::endl;
  return 0;
}
