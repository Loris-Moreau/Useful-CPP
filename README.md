# Useful CPP

Collection of useful functions in C++

[C++ Best Practices](https://github.com/cpp-best-practices/cppbestpractices/tree/master)

[C++ Built in Functions](https://github.com/Bhupesh-V/30-seconds-of-cpp)

## Random
```
#include <iostream>
#include <random>

int main()
{
    std::random_device rd; // obtain a random number from hardware
    std::mt19937 gen(rd()); // seed the generator

    // For no range put : std::uniform_int_distribution<> distr(0, RAND_MAX);
    std::uniform_int_distribution<> distrInt(-10, 10); // define the range Int
    int randInt = distrInt(gen); // Generate random Int in range
    std::cout << "Random Int in Range : " << randInt << '\n'

    std::uniform_real_distribution<> distrDouble(-10.5, 10.5); // define the range Double
    double randDouble = distrDouble(gen); // Generate random Double in range
    std::cout << "Random Double in Range : " << randDouble << '\n'
}
```
---

## Rounded Value
```
// 10 for 1 after the comma, 100 for 2 after the comma & so on.
float val = 3.14159265359
float rounded_down = floorf(val * 10) / 10;   // returns 3.1
float rounded_down = floorf(val * 100) / 100; // returns 3.14
```

## Quick "if" formating
````
int test = 0;

m_value? test = 1 : test = 2 // do any bool operations before the "?" (ex: <, >, ==, etc...)

// is equivalent to :
if (m_value)
{
    test = 1;
} else
{
    test = 2;
}
````


