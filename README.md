# CPP-Program-for-Octal-to-Decimal-Conversion

Octal to Decimal Conversion in C++
Here, on this page, we will discuss octal to decimal conversion in C++. Let’s have a look at an example before moving ahead with code of Octal to Decimal in C++.

(462)8 = 4 * 82 + 6 * 81 + 2 * 80
256 + 48 + 2 = (306)10
Octal to Decimal in C++
While loop in C
Different Methods discussed
We will discuss the following methods in the post –

Algorithmic way (Octal to Decimal)
Inbuilt Method (Octal to Decimal)
Method 1
Octal to Decimal Conversion in C++
Algorithm:-
Initialize i = 0, decimal = 0, base = 8
Extract the last digit (digit = num% 10)
Calculate decimal equivalent of this digit
Add it to decimal variable
decimal += digit * pow(8 ,i);
Reduce the number (num /= 10
increment i value
C++ Code:-
Run
#include<iostream>

#include<math.h>
using namespace std;

// function to convert octal to decimal
int getOctal(long long num)
{
    int i = 0, decimal = 0;
    
    // will only work for bases 2 - 10
    int base = 8;
    
    //converting octal to decimal
    while (num!=0)
    {
        int digit = num % 10;
        decimal += digit * pow(base, i);

        num /= 10;
        i++;
    }
    return decimal;
}

// main program
int main()
{
    // long used rather than int to store large values
    // Ex : int wont store 111111111111 (12 digits) as
    // limit for int is 2147483647 (10 digits)
    long long octal = 462;
    
    cout << getOctal(octal);   
    
    return 0;
}
Output
306
Related Pages
Program to find GCD

Program for octal to decimal conversion

Program for hexadecimal to decimal conversion

Program for decimal to binary conversion

Program for decimal to octal conversion

 

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
Method 2
Methods used
The following method uses inbuilt function stoi(), which has given template -

stoi(binary_in_string_format, 0, base_value)
C++ Code:-
Run
 

#include<iostream>
using namespace std;
 
int main()
{
    // important input has to be in string format only here
    string binaryNumber;
    cin >> binaryNumber;
    
    int base = 8;
    // format stoi(binary_in_string_format, 0, base_value)
    cout << stoi(binaryNumber, 0, base);
 
    return 0;
}
Output
462
306
