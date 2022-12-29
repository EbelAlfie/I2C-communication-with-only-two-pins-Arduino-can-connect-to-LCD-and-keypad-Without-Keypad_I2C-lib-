# Arduino Lcd and keypad with only two pin Without Keypad_I2C library
In this project, arduino is connected to LCD and Keypad with only two pin using I2C communication

This project requires you to have proteus simulation software to simmulate the circuit and arduino IDE as coding IDE

I2C or inter-integrated circuit is a communication protocol which is very efficient. With it, one master can communicate to multiple slaves using just two pin, namely the SDA and SCL. It is a serial communication, which means that data/information is sent bit by bit into the SDA. The SCL pin is responsible to send clock signal in order to synchronize data transfer between the arduino and the slaves. So, basically I2C is just SPI communication with a total of UART cable (only two instead of four).

It is shown in this project that arduino (The master) is communicating with two slaves, that is LCD and 3x4 Keypad. Normally, LCD needs to be connected to approximately 8 pins and the 3x4 keypad to 7 pins on the Arduino, this sure will limits the other devices from connecting to Arduino. With the use of I2C, both devices just need to be connected to two PCF8574, which is an I2C IC that can be found on I2C expanding board or I2C interface that is usually used on LCD. And then, the I2C IC SDA and SCL pin to Arduino's SDA and SCL pin. The library used here is LiquidCrystal_I2C.h which will assist in controlling the LCD and Wire.h. Actually, you can just replace Wire.h into Keypad_I2C.h to receive input from the keypad. Wire.h is used in order to make everyone understands how to understand I2C communication and manually transmit and receive data from the keypad. You can understand how keypad works too, even though it is not too necessary 
