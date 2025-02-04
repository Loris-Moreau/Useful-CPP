# Useful CPP
Collection of useful functions in C++

## Random
```
#include <iostream>
#include <random>

int main()
{
    std::random_device rd; // obtain a random number from hardware
    std::mt19937 gen(rd()); // seed the generator
    std::uniform_int_distribution<> distr(25, 63); // define the range

    int randNum = distr(gen); // Generate random number in range
    std::cout << "Random Int in Range : " << randNum << '\n'
}
```
