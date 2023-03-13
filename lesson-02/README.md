# This directory contains solution to the lesson-02

#include <iostream>
using namespace std;
class Shirt
{
public:
    string color;
    string size;
};

class Cat
{
public:
    string name;
    string breed;
    int age;
};

class Film
{
public:
    string genre;
    string name;
    int yearofrelease;
};

int main(int argc, const char * argv[])
{
    Shirt myShirt;
    myShirt.color = "black";
    myShirt.size = "small";

    cout << myShirt.color << endl;
    cout << myShirt.size << endl;

    Cat myCat;
    myCat.name = "Guapa";
    myCat.breed = "british";
    myCat.age = 11;

    cout << myCat.name << endl;
    cout << myCat.breed << endl;
    cout << myCat.age << endl;

    Film favFilm;
    favFilm.genre = "psychological";
    favFilm.name = "primal fear";
    favFilm.yearofrelease = 1996;

    cout << favFilm.genre << endl;
    cout << favFilm.name << endl;
    cout << favFilm.yearofrelease << endl;

    return 0;
}
