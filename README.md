# Husky-Lens-micro-bit-MicroPython-Library
### A MicroPython library made specifically for the micro:bit V2 microcontroller to interact with a Husky Lens machine learning module. 


In the summer of 2022, I worked on a project which paired the micro:bit with a Husky Lens machine learning module. I learned DFRobot has only accommodated using the Husky Lens with the micro:bit via the Microsoft MakeCode editor. There does exist a [Python library](https://github.com/HuskyLens/HUSKYLENSPython) for using the Husky lens with a Raspberry Pi, but the I2C libraries on which this library was built (smbus in particular) simply do not work on the micro:bit. Moreover, the I2C functions for the micro:bit's version of MicroPython are incredibly simple, making it difficult to change only a few lines of code in the pre-built library. Thankfully, DF Robot does include the I2C registers and addresses needed to send commands and activate various modes on the Husky Lens in its [protocol Github Page](https://github.com/HuskyLens/HUSKYLENSArduino/blob/master/HUSKYLENS%20Protocol.md). 

This library builds upon DF Robot's original Python library for the Husky Lens and utilizes the micro:bit's I2C functions to successfully facilitate control of the module. At the moment, there are only two modes actively capable of being called by the micro:bit: OBJECT_TRACKING and OBJECT_CLASSIFICATION. These were the only two modes I needed for my afforementioned project, but if one were to incorporate more, they would need only to go to the above Husky Lens protocols link and find the 4 bits associated with their desired mode. The format of the Obj_Class() and Obj_Track() functions could then be followed to activate said node.

While MakeCode is a wonderful tool for beginners, MicroPython offers far more potential for designing complex and advanced projects. Still, the occasional advanced project has timing and hardware limitations, thus giving birth to libraries such as this one. I hope that this library will be of aid to others. If it is, please do let me know. If you have any questions, feel free to contact me. 

Alex P. Sharper 

alexpsharper@gmail.com
