# Lab-21.30
// This program demonstrates default function arguments.
#include <iostream>
using namespace std;
// the first call is one row of 10. The second call is just one row of 5 and the last call is 3 rows of 7 displayStars. They need different calls because they each have a different output and need their own unique paramters.
// Function prototype with default arguments
void displayStars(int cols = 10, int rows = 1);

int main()
{
   displayStars();      // Use default values for cols and rows.
   cout << endl;
   displayStars(5);     // Use default value for rows.
   cout << endl;
   displayStars(5, 7);  // Use 7 for cols and 3 for rows.
   return 0;
}

//********************************************************
// Definition of function displayStars.                  *
// The default argument for cols is 10 and for rows is 1.*
// This function displays a square made of asterisks.    *
//********************************************************
void displayStars(int cols, int rows)
{
   // Nested loop. The outer loop controls the rows
   // and the inner loop controls the columns.
   for (int down = 0; down < rows; down++)
   {
      for (int across = 0; across < cols; across++)
         cout << "*";
      cout << endl;
   }
}
