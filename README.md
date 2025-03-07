
# Introduction

In this task, I used the app Tinkercad to give me a simulation of how the Arduino Uno R3 can help me power servo motors and eventually use them in robotics.

__Components:__ Arduino Uno R3, a small breadboard, 6 Micro servos, and an external power supply of 4 1.5V batteries, along with multiple wires to connect the components to each other.

__Structure:__ The servo motor has 3 pins. I connected the first one to a negative pin, the second to a positive, and the third to a control signal which in this case is the digital PWM signal. I specifically used the digtial PMW pin because they send digital signals and are also 0 or 1 and we want the output signal to be a square wave.

__Purpose of project:__ to be able to give robot joints, specifically the legs, a range of motion, using the servo motors. I used servo motors because they are high-performing with precision and effeciency, as well as being lighter than stepper motors which will help in balance and flexibility.
 


# Circuit image
<img width="899" alt="Screenshot 2024-07-02 at 11 18 06 AM" src="https://github.com/Remasj/Task2-elec.eng/assets/144160139/a762725b-4cb6-4a45-8072-f5df73aacde6">

__Image description:__
I connected the arduino to 6 servo motors along with a small breadboard and 4 1.5V batteries(1.5V x 4 =6V) as the servo cannot run on 5V in arduino only.

# Tinkercad Simulation
Click on the link below to try out my simulation!

[Tinkercad simulation](https://www.tinkercad.com/things/kzcujmXtH5q-magnificent-amberis/editel?tenant=circuits)

# Code
``` C++
#include <Servo.h>

Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;
Servo servo6;
 
int pos = 0;
 
void setup() {
servo1.attach(3);
servo2.attach(5);
servo3.attach(6);
servo4.attach(9);
servo5.attach(10);
servo6.attach(11);
}
 

void loop() 
{
  for (pos = 0; pos <= 180; pos += 1) 
  { 
    servo1.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  
  for (pos = 180; pos >= 0; pos -= 1) 
  { 
    servo1.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 0; pos <= 180; pos += 1) 
  { 
    servo2.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  
  for (pos = 180; pos >= 0; pos -= 1) 
  { 
    servo2.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 0; pos <= 180; pos += 1) 
  { 
    servo3.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  
  for (pos = 180; pos >= 0; pos -= 1) 
  { 
    servo3.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 0; pos <= 180; pos += 1) 
  { 
    servo4.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  
  for (pos = 180; pos >= 0; pos -= 1) 
  { 
    servo4.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 0; pos <= 180; pos += 1) 
  { 
    servo5.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  
  for (pos = 180; pos >= 0; pos -= 1) 
  { 
    servo5.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 0; pos <= 180; pos += 1) 
  { 
    servo6.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  
  for (pos = 180; pos >= 0; pos -= 1) 
  { 
    servo6.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  
}
```
# Code explanation

*Language used is C++

1- Started by defining the library for Servo motor.

2- Initialized all the six servos as servo1, servo2, servo3, etc.

3- Set variable to store servo position (pos) to value 0.

4- Set all the servo’s input pin with Arduino.

5- In the void loop() function, we are just rotating all the servo from 0 to 180 degree and then 180 to 0 degree. The delay used in the below code is used to increase or decrease the speed of the servo using the variable ‘i’.
  



