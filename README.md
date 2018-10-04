/*# Doodle-Cpp
Motivation for a project in C++. 
 I'm in love with C++, hence a start here!*/
//doodle code for simply math...for any scientific calculator.
#include<cmath>
#include<iostream>
#include<sstream>
#include<string>
using namespace std;
float calcSA(float, float);
float calcV(float, float);
void displaySA(float);
void displayV(float);
const float PI=22.0/7.0;
int main(){
    string Tylen;
    float r=0, h=0;
    cout<<"Enter r and h:\n";
    getline(cin,Tylen);
    stringstream(Tylen)>>r;
    getline(cin,Tylen);
    stringstream(Tylen)>>h;
    displaySA(calcSA(r,h));
    displayV(calcV(r,h));
    return 0;
}
float calcSA(float r, float h){
    return PI*r*(r+sqrt(pow(h,2.0)+pow(r,2.0)));
}
float calcV(float r, float h){
    return PI*pow(r,3.0)*h/3.0;
}
void displaySA(float SA){
    cout<<"\n The surface area is:\t"<<SA<<endl;
}
void displayV(float V){
    cout<<"\n The volume is:"<<"\t"<<V<<endl;
}
    
