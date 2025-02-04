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
char text = "test";

m_value? text = "true" : text = "false" // do any bool operations before the "?" (ex: <, >, ==, etc...)

// is equivalent to :
if (m_value)
{
    text = "true";
} else
{
    text = "false";
}
````


