
#include <iostream>
#include <string>
#include <fstream>
using namespace std;		//


char
DNAbasemRNAbase (char dna)         //
{

  if (toupper (dna) == 'A')	// The toupper() function converts ch to its uppercase version if it exists
    return 'U';
  else if (toupper (dna) == 'T')
    return 'A';
  else if (toupper (dna) == 'C')    //
    return 'G';
  else if (toupper (dna) == 'G')
    return 'C';                    //
  else
    return ' ';
}

string
DNAmRNA (string input)    //
{
  string output = "";


  for (int i = 0; i < input.size (); ++i)
    {
      output = output + DNAbasemRNAbase (input[i]);      //
    }

  return output;
}


int
main ()                  //
{

  ifstream fin ("dna.txt");   //
  string cool;

  if (fin.fail ())
    {
      cerr << "File cannot be read.\n";
      exit (1);                  //
    

  while (getline (fin, cool))
    {
      cout << DNAmRNA (cool) << endl;
    }
  fin.close ();
  return 0;
}
