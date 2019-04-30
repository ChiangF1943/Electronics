**The lower-board of ZJUDancer in 2018, designed by Jiang Chaofeng.**

**Due to the use of NVIDIA JETSON TX1/TX2, new lower-board is designed as below.**

---

# **USBBoard**

It connects to the USB port of TX1 carrier board, and branches off into 4-way USB. One USB for camera, one for keyboard or mouse, one switches into RS-485 and connects Dynamixel motors, and the last one switches into RS-TTL and connects Core module in BottomBoard to get IMU data. There is also a power port for TX1 carrier board.

# **BottomBoard**

+ Gets power through dual-port from two battery;

+ Voltage stabilization;

+ Two power switch;

+ Low voltage alarm;

+ core board and IMU board connector;

+ Dynamixel motors ports;

+ Port to connect USBBoard.

# **SmallBoard**

+ Core module: Reads IMU data through SPI1 from IMU, and sends data to upper-computer through RS-TTL UART1.

+ IMU module: A carrier board for IMU.

+ Input module: A carrier board for battery sockets. Just changes the battery sockets direction, so that it`s easy to plug in the batteries.

# **FootBoard**

Foot pressure sensor board, reads 4-way analog signals of pressure gauge through ADC1/2/3/4. Pressure data is sent through UART1, and transferred into RS-485 signals to upper-computer.