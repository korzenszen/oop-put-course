# This directory contains solution to the lesson-05
#include <iostream>

using namespace std;

class ChemicalProperty {
public:
    virtual float Data() const = 0;
};

class Moles : public ChemicalProperty { 
public:
    Moles(float m, float M) : Rmass(m), Mmass(M) {}

    float Data() const {
        return (Rmass / Mmass);
    }

protected:
    float Rmass;
    float Mmass;
};

class MolarConcentration : public ChemicalProperty {
public:
    MolarConcentration(float m, float M, float v) : Rmass(m), Mmass(M), volume(v) {}

    float Data() const {
        return (Rmass / Mmass) / volume;
    }

protected:
    float Rmass;
    float Mmass;
    float volume;
};

class PercentageConcentration : public ChemicalProperty {
public:
    PercentageConcentration(float m, float s) : Rmass(m), Smass(s) {}

    float Data() const {
        return (Rmass / Smass) * 100;
    }

protected:
    float Rmass;
    float Smass;
};

int main() {
    Moles Mol(2.71, 36.45);
    MolarConcentration Cm(2.71, 36.45, 1.3);
    PercentageConcentration Cp(2.71, 4.36);

    cout << "Liczba moli HCL wynosi: " << Mol.Data() << endl;

    cout << "Stezenie molowe HCL wynosi: " << Cm.Data() << endl;

    cout << "Stezenie procentowe roztworu HCL wynosi: " << Cp.Data() << endl;

    return 0;
}
