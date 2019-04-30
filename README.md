**Lower-board for ZJUDancer robot in 2016, designed by Huang Haojun, who was a member of ZJUDancer.**

**It contains 3 boards, and the MainBoard carries 3 small modules.**

---

#**MainBoard**

The mainboard carries Core module, Motor module and BatMeasure module, and connects FrontBboard.

+ **Core module**: receives motor position data from upper-computer, sends them to motor, gets IMU data and communicates with BatMeasure module.

+ **Motor module**: receives motor position data from core module, packs them and sends to Dynamixel motors. It also controls the speed of motors and reads data from motors.

+ **BatMeasure module**: Measures the voltage of battery and sends voltage data to core. The buzzer is in this board, when voltage is low, it will alarm.

#**FrontBoard**

Two USB-port, one for camera, and the other one for Upper-computer. Connects RS-485 signal for Motor module and Dynamixel motor wires. Gets power from BottomBoard. Shows voltage message through a LCD screen(Not in this version, because it is easily broken).

#**BottomBoard**

2 big fuzes to ensure 2 line power safety. 2 port for Upper-computer and lower-board switches. 2 battery ports.

#**Library**

Commonly used schematic lib and PCB lib.

#**Others**

Compass module------The rule allowed compass in 2016, and there is no compass in ADIS IMU, so this board gives data of magnetic field(tends to break down, not stable enough). FSR module------power problem not fixed, not in use in 2016.