#Arducom
Arducom is Arduino Serial Communication Libraries written in different languages. Currently in python and C++.

##Arducom C++ Library
Written in C++

##How To Use?
At First Download the files and copy the C++ library to your working directory then

  #include"src/Arducom.h"
  Arducom Ser("COM4");

Here Arducom is the name of class and Ser is name of Object. COM4 is the name of Serial Port. Incase of linux We Use dev/ttyACM0 or something similar. First see in which serial port arduino is communicating with your computer


##getPort()
This function simply returns you some string. The string will be the port your are Currently using.

Usuage:

std::string CurrentPort = Ser.getPort();
cout << CurrentPort << endl;

This will print Current Port you are working with.

##printPort()
This fuction will print the port you are working with on the screen.
Usage:

Ser.printPort();

##resetPort(portname,0 or 1)
This funciton resetPort is used to reset the port to another name. It takes two arguments. Where first argument is name of port and the second one in integer. 0 or 1. 1 denotes the verbose on and 0 for verbose off. Simply 0 will not print anything and 1 will print Some informations.

Usuage:

Ser.resetPort("/dev/ttyACM0",0);
or
Ser.resetPort("/dev/ttyACM0",1);

##sendBuffer();
This function is used to send information over seial port. It takes one parameter. You can send both integer and string variable to this function. It returns 0 or 1 with success or failure of sending the information.

Usage:

Ser.sendBuffer("Hello World");
Ser.sendBuffer(1);

##getBuffer();
This function returns information that is being sent over serial port!

Note: Contributions are highly appreciated!
