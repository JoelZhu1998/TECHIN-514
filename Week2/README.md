<h1> Dashboard for Bicycle Riding
<h4> A bicycle dashboard project that can record total distance, current speed, average speed, and travel time.<br><br>

![](/Week2/IMAGE/Sketch.jpg)

<h2> Sensors Device
<h4> 1.DS3231 RTC Module : For accurate time tracking, especially for the travel time calculation.<br><br>
2.A3144 Hall Effect Sensor : It will detect the revolutions of the bike wheel to calculate the speed.<br><br><br>
<h2> Display Device
<h4> 3.ST7920 LCD : 128*64<br><br><br>
4.Stepper Motor Gauge
<h2> How the devices communicate with each other?
<h4> 1. Speed Sensor to Microcontroller <br><br>
Function: The speed sensor (often a Hall effect sensor) is used to measure the speed of the bicycle. It detects the revolutions of the bicycle wheel.
Communication:
Each time the wheel completes a revolution, the sensor sends a signal to the microcontroller.
This signal is usually a simple digital pulse.
The microcontroller counts these pulses over time to calculate the speed and distance.<br><br>
2. Real-Time Clock (RTC) Module to Microcontroller<br><br>
Function: The RTC module keeps track of the current time and duration of the bicycle trip.
Communication:
The RTC module continuously maintains the current time, even when the microcontroller is powered off, thanks to its own battery.
The microcontroller queries (reads) the RTC module at regular intervals to get the current time.
This information is used to calculate the travel time and, in conjunction with the speed data, can also be used to calculate average speed.<br><br>
3. Microcontroller to LCD/OLED Display<br><br>
Function: The display shows the rider real-time information about speed, distance, and travel time.
Communication:
The microcontroller sends data to the display, instructing it what to show.
This can include the current speed, calculated distance, average speed, and elapsed time.
Communication is typically done through a digital interface like I²C, SPI, or parallel connections, depending on the type of display used.<br><br>
4. Power Source<br><br>
Function: Provides the necessary electrical power to all components.
Communication:
While not involving data communication, the power source is crucial for the operation of all components.
It needs to supply the correct voltage and current as required by the microcontroller, sensors, and display.<br><br>
5. Data Flow Overview<br><br>
The speed sensor continuously feeds rotation data to the microcontroller.
The microcontroller processes this data to calculate speed and distance. It also periodically reads the time from the RTC module.
Using these inputs, the microcontroller updates the display with the current speed, total distance, average speed, and travel time.
All components are powered by the power source, ensuring consistent operation.<br><br><br>

<h2> Detailed Diagram
![](/Week2/IMAGE/Diagram.jpg)
