# Task2-elec.eng

# code
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
# code explanation
1- started by defining the library for Servo  motor.

2- initializing all the six servos as servo1, servo2, servo3, etc.

3- set setting all the servo’s input pin with Arduino.

-In the void loop() function, we are just rotating all the servo from 0 to 180 degree and then 180 to 0 degree. The delay used in the below code is used to increase or decrease the speed of the servo using the variable ‘i’.
  


# circuit image
<img width="899" alt="Screenshot 2024-07-02 at 11 18 06 AM" src="https://github.com/Remasj/Task2-elec.eng/assets/144160139/a762725b-4cb6-4a45-8072-f5df73aacde6">

__image 1 description:__
I connected the arduino to 6 servo motors along with a small breadboard and 4 1.5V batteries(1.5V x 4 =6V) as the servo cannot run on 5V in arduino only.
I connected each servo to positive and negative along with a digtial PMW pin because we want the output signal to be a square wave.


