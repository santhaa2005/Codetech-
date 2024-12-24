"#include <iostream>
using namespace std;

class Complex
{
    private:
      float real;
      float imag;
    public:
       Complex(): real(0), imag(0){ }
       void input()
       {
           cout << "Enter real and imaginary parts respectively: ";
           cin >> real;
           cin >> imag;
       }

       // Operator overloading
       Complex operator - (Complex c2)
       {
           Complex temp;
           temp.real = real - c2.real;
           temp.imag = imag - c2.imag;

           return temp;
       }

       void output()
       {
           if(imag < 0)
               cout << "Output Complex number: "<< real << imag << "i";
           else
               cout << "Output Complex number: " << real << "+" << imag << "i";
       }
};

int main()
{
    Complex c1, c2, result;

    cout<<"Enter first complex number:\n";
    c1.input();

    cout<<"Enter second complex number:\n";
    c2.input();

    // In case of operator overloading of binary operators in C++ programming, 
    // the object on right hand side of operator is always assumed as argument by compiler.
    result = c1 - c2;
    result.output();

    return 0;
}
In this program, three objects of type Complex are created and user is asked to enter the real and imaginary parts for two complex numbers which are stored in objects c1 and c2.

Then statement result = c1 -c 2 is executed. This statement invokes the operator function Complex operator - (Complex c2).

When result = c1 - c2 is executed, c2 is passed as argument to the operator function.

In case of operator overloading of bin"
 https://www.programiz.com/cpp-programming/operator-overloading/binary-operator-overloading#:~:text=Overloading%20to%20Subtract%20Complex%20Number-,%23include%20%3Ciostream%3E%0Ausing%20namespace%20std%3B%0A%0Aclass%20Complex%0A%7B,In%20case%20of%20operator%20overloading%20of%20binary,-operators%20in%20C%2B%2B%20programming%2C%20the
