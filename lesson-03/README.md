# This directory contains solution to the lesson-03
#include <iostream>
using namespace std;

class Potion {
private:
  string type;
public:
};

class Shrek {
private: 
  string race;
public:
  Shrek LovePotion(string newRace) {
    this->race = move(newRace);
    return *this;
  }
  string NormalPotion() {
    return this->race;
  }
};

int main() {
  Shrek greenOgre;
  greenOgre.
}
