#include <iostream>
#include <string>
#include <fstream>
#include <cstdlib>
using namespace std;


char
DNAbasemRNAbase (char dna)
{

  if (toupper (dna) == 'A')   // The toupper() function converts ch to its upper case

    return 'U';

  else if (toupper (dna) == 'T')    //djfklsdjfkdsjlf

    return 'A';

  else if (toupper (dna) == 'C')   //jfkdsjkdsjflks

    return 'G';

  else if (toupper (dna) == 'G')     //dsjfkdlsjfsk

    return 'C';    //dfsksjlkfjsl

  else

    return ' ';       //djsfklsdjfklds

}



string
DNAmRNA (string input)
{


  string output = "";  //sdjfksljfksdl


  for (int q = 0; q < input.size (); ++q)    //dksjfldks

    {


      output = output + DNAbasemRNAbase (input[q]);

    }

  return output;  //dsjfkldsjfds

}



string
dictionary_read (string codon, ifstream & dict)   //fdjskfjsldjl
{

  string key, value;


  dict.clear ();   //dsjfksljfd


  dict.seekg (0);

  while (dict >> key >> value)

    {

      if (codon == key)

	return value;

    }

  return " ";

}


int
main ()
{


  ifstream dnaFin ("dna2b.txt");

  ifstream dicFin ("codons.tsv");   //sdjfksjlfkds

  string strand;


  if (dnaFin.fail ())

    {

      cerr << "File cannot be opened.\n";

      exit (1);

    }


  while (getline (dnaFin, strand))     //dsjfksldjfkdlsj

    {


      bool startOccur = false;


      for (int i = 0; i < strand.size (); i = i + 3)

	{


	  string codon = DNAmRNA (strand.substr (i, 3));

	  if (codon == "AUG")

	    {

	      startOccur = true;

	    }


	  if (codon == "UAA" || codon == "UGA" || codon == "UAG")

	    {

	      break;

	    }

	  if (startOccur == true)

	    {

	      cout << dictionary_read (codon, dicFin);

	    }

	  if (i < i + 3)

	    {

	      string nxtCodon = DNAmRNA (strand.substr (i + 3, 3));

	      if (startOccur != false && nxtCodon != "UAA"
		  && nxtCodon != "UGA" && nxtCodon != "UAG")

		{

		  cout << "-";

		}

	    }

	}

      cout << endl;

    }

  dnaFin.close ();

  dicFin.close ();

  return 0;

}
