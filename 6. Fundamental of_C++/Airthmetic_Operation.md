# Airthmetic Operation

## Introduction:
Arithmetic operations in C++ are similar to other languages. We’ll have a quick discussion about them here and then you can practice programming (+, -, *, /, %)

```
/*Goal: practice arithmetic operations in C++
**Write a program that calculates the volumes of:
**a cube, sphere, cone.
**Cube Volume = side^3
**Sphere Volume = (4/3) * pi * radius^3
**Cone Volume = pi * radius^2 * (height/3)
**Write the values to the console.
*/

#include<iostream>

int main()
{
    //Dimension of the cube
    float cubeSide = 5.4;
    //Dimension of sphere
    float sphereRadius = 2.33;
    //Dimensions of cone
    float coneRadius = 7.65;
    float coneHeight = 14;
    
    float volCube, volSphere, volCone = 0;
    
    //find volume of cube
     volCube = std::pow(cubeSide, 3);
    //find volume of sphere
    volSphere = (4.0/3.0)*M_PI*std::pow(sphereRadius,3);
    //find volume of cone
    //M_PI is in the cmath library, it does not need to reference the
    //std namespace. On the other hand, pow() needs to reference it.
    volCone = M_PI * std::pow(coneRadius, 2) * (coneHeight/3);
    std::cout <<"\nVolume of Cube: "<<volCube<<"\n";
    std::cout <<"\nVolume of Sphere: "<<volSphere<<"\n";
    std::cout <<"\nVolume of Cone: "<<volCone<<"\n";

    return 0;
}
```