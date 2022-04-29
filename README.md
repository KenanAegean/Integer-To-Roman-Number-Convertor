# Integer-To-Romen-Number-Convertor
C++ Code For Roman Numerals To Integer 

This is the Algorithm that I wrote to convert Integer Numbers to Roman Numbers as a Challenge

```C++
#include <iostream>
using namespace std;

//make protoype of function
void roman(int nNumber);

int main()
{
  int nNumber;
  for(int i;i=!0;++i)
  {
    cout<<"Enter a number: ";
    cin >>nNumber;
    cout << "Roman numaric equality is: " ;
    roman(nNumber);
    
    cout << endl << endl;
  }
  
  system("CLS");     
  return 0;
}

void roman(int nNumber)
{
    int d1, d2, d3;

    //Divide number for digits
    d1 = nNumber / 100;
    nNumber = nNumber - (d1 * 100);
    d2 = nNumber / 10;
    nNumber = nNumber - (d2 * 10);
    d3 = nNumber;

    //cout << d1 << endl << d2 << endl << d3 << endl;

    if (d1 <= 3)
    {
        for (int i; i < d1; ++i)
        {
            cout << "C";
        }
    }
    else if (d1 > 3 && d1 <= 8)
    {
        if (d1 == 4)
        {
            cout << "C";
        }
        cout << "D";
        for (int i; i < d1 - 5; ++i)
        {
            if (d1 == 4)
            {
                continue;
            }

            cout << "C";
        }

    }
    if (d1 == 9)
    {
        cout << "CM";
    }



    if (d2 <= 3)
    {
        for (int i; i < d2; ++i)
        {
            cout << "X";
        }
    }
    else if (d2 > 3 && d2 <= 8)
    {
        if (d2 == 4)
        {
            cout << "X";
        }
        cout << "L";
        for (int i; i < d2 - 5; ++i)
        {
            if (d2 == 4)
            {
                continue;
            }

            cout << "X";
        }

    }
    if (d2 == 9)
    {
        cout << "XC";
    }

    if (d3 <= 3)
    {
        for (int i; i < d3; ++i)
        {
            cout << "I";
        }
    }
    else if (d3 > 3 && d3 <= 8)
    {
        if (d3 == 4)
        {
            cout << "I";
        }
        cout << "V";
        for (int i; i < d3 - 5; ++i)
        {
            if (d3 == 4)
            {
                continue;
            }

            cout << "I";
        }

    }
    if (d3 == 9)
    {
        cout << "IX";
    }


}

```
