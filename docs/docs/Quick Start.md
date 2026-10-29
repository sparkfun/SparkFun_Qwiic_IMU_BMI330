# Quick Start Guide

In this Quick Start guide we'll wire the SparkFun 6DoF IMU - BMI330 (Qwiic) into a Qwiic circuit with a RedBoard IoT - RP2350 and use the Basic Readings example from the SparkFun BMI330 Arduino library to view acceleration and orientation data measured by the BMI330.

This guide assumes you have an understanding of using the Arduino IDE including Arduino libraries and board packages, using digital interrupts as well as the Qwiic ecosystem. If you're not familiar with one or more of these concepts or would like more information on the BMI330 or these concepts, we recommend reading through the more detailed sections of this Hookup Guide.

## Basic Assembly

Since this is a Qwiic breakout, assembly is just two simple steps.

* Connect the BMI330 breakout to the RedBoard IoT with a Qwiic cable.
* Connect the RedBoard IoT - RP2350 to a computer over USB-C

![Photo of completed Qwiic circuit with a RedBoard IoT](/img/QwiicBMI330-Assembly.jpg)

## Arduino Example - Basic Readings

* Open the [Arduino IDE](https://www.arduino.cc/en/software/)
* Install the SparkFun BMI330 Arduino library by searching for "SparkFun BMI330" in the [Libraray Manager tool](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-installing-a-library/). Note, this library requires the SparkFun Toolkit to be installed as well. Install that library by searching for "SparkFun Toolkit" in the Library Manager.
* Open "Example01_BasicReadingsI2C" from the BMI330 library. Select your Board and click the "Upload" button.
* After the code finishes uploading, open the [serial monitor](https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-serial-monitor/) with the baud set to **15200**.

The code initializes the sensor and sets the accelerometer and gryoscope ranges to &plusmn;4g and &plusmn;500&deg;/s, respectively, to work with general handheld motion. After the sensor initializes, the code prints out values for the x, y and z axes for both sensors every 100ms. Now all that data streaming by can be a bit hard to interpret. Try opening the [serial plotter]() for a better visualization of the data from the BMI330. Having all six values printed out simultaneously can be a bit busy but thankfully the plotter lets us select which values to plot so you can separate it into acceleration data (values 1-3) and gyroscope data (values 4-6) to get a clearer picture of the motion sensed by each like the screenshots below:

![Screenshot of serial plotter data from the accelerometer](/img/BMI330_Ex1A.png)

![Screenshot of serial plotter data from gycrosope](/img/BMI330_Ex1G.png)
