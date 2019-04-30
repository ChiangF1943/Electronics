**The lower-board of ZJUDancer in 2019, designed by Jiang Chaofeng.**

**Lower-board is nearly removed last year and TX1 controls motors directly through USB-UART-RS485. 
However, the test results show that the delay time in IMU data and motor data reading directly by upper-computer is massive, and it`s unacceptable. As a consequence, the concept of lower-board is used again. 
Core module is replaced by Motor module to reduce workload, so the change is mainly in BottomBoard compared to boards in 2018.**

---

# **USBBoard**

It connects to the USB port of TX1 carrier board, and branches off into 4-way USB. One USB for camera, one for keyboard or mouse, one switches into RS-485 and connects Dynamixel motors, and the last one switches into RS-TTL and connects Core module in BottomBoard to get IMU data. There is also a power port for TX1 carrier board.

# **BottomBoard**

+ Gets power through dual-port from two battery;

+ Voltage stabilization;

+ Two power switch;

+ Low voltage alarm;

+ A serial line connects upper board and Motor board;

+ Motor board and IMU board connector;

+ 3-way Dynamixel motors ports;


# **SmallBoard**

+ Motor module: Reads IMU data through SPI1 from IMU, sends data to upper-board through UART1, sends to and reads from Dynamixel motors through USART2/3/4 concurrently. 

+ IMU module: A carrier board for IMU.

+ Input module: A carrier board for battery sockets. Just changes the battery sockets direction, so that it`s easy to plug in the batteries.

# **FootBoard**

Foot pressure sensor board, reads 4-way analog signals of pressure gauge through ADC1/2/3/4. Pressure data is sent through UART1, and transferred into RS-485 signals to upper-computer.
