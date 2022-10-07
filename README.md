# joystick-controlled-microcontroller
This project uses the STM32F401 (μC), the mbed application shield, which contains the MMA7660FC accelerometer, and the 24LC32 EEPROM.
With these, and using C++, it implements a Finite State Machine that maps each of the mbed's joystick movement to one of the following actions:  
  1. Sample the accelerometer, and use the sampled value to create a 60-byte data packet.
  2. Read/Write the data packet to the external EEPROM module using the I²C protocol.
  3. Display the previous/next packet-field in the mbed's LCD display.

In addition this code implements an Acknowledge Polling strategy.
