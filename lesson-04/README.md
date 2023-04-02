# This directory contains solution to the lesson-04

#include <iostream>
#include <string>

class Temperature {
private: 
	double Celsius; 
	   double Kelvin; 
public: 
	double CelsiusValue() { return this->Celsius; }; 
	double KelvinValue() { return this->Kelvin; };
	Temperature() { this->Celsius = 0.0; this->Kelvin = 273.0; };
	Temperature(double temp) { this->Celsius = temp; this->Kelvin = temp +273; };
	Temperature(float temp) : Temperature(static_cast<double>(temp)) {};
	Temperature(int temp) : Temperature(static_cast<double>(temp)) {}; 
	Temperature(std::string temp) : Temperature(std::stod(temp)) {};

};

int main() {
	Temperature defaultCelsius;
	Temperature doubleCelsius(23.45); 
	Temperature floatCelsius(56.78);
	Temperature stringCelsius("78.89"); 
	Temperature intCelsius(10); 
	std::cout << defaultCelsius.CelsiusValue() << std::endl;
	std::cout << doubleCelsius.CelsiusValue() << std::endl;
	std::cout << floatCelsius.CelsiusValue() << std::endl; 
	std::cout << stringCelsius.CelsiusValue() << std::endl; 
	std::cout << intCelsius.CelsiusValue() << std::endl; 
	std::cout << doubleCelsius.KelvinValue() << std::endl;

	return 0;
}
