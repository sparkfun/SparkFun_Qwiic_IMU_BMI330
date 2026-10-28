# Hardware Overview

## BMI330 6DoF IMU

The BMI330 6 Degree of Freedom (DoF) intertial measurement unit (IMU) from Bosch Sensortech combines a high-precision 3-axis accelerometer with a 3-axis gyrocope with an integrated motion interrupt engine to measure six directions of motion in a wide variety of applications. The sensor also operates well in extreme environments and can function at temperatures up to 150&deg;C. The sensor communicates over I<sup>2</sup>C, I<sup>3</sup>C and SPI and has two interrupt pins that are configurable to trigger on any of the sensor's motion interrupt engine events. The interrupt engine can trigger on sensing any motion, step detection and counting, orientation and flat detection as well as single, double and triple tap detection. 

The 3-axis accelerometer has four selectable measurement ranges: &plusmn;2g, &plusmn;4g, &plusmn;8g and &plusmn;16g with 180&micro;g/&radic;Hz noise density and a sensitivity error of 0.5%.  the 3-axis gyroscope has four configurable measurement ranges of &plusmn;125&deg;/s, &plusmn;250&deg;/s, &plusmn;500&deg;/s, &plusmn;1000&deg;/s and &plusmn;2000&deg;/s. 

The BMI330 accepts a supply voltage of 1.71 to 3.63V and runs at 3.3V on this breakout. It has four operating modes: High Performance, Normal, Low Power and Suspend. It draws a max of 790&micro;A with both sensors enabled in performance mode, 390&micro;A in low power mode and only 15&micro;A in suspend mode. The sensor has an operating temperature range of -40 to +105&deg;C.

## Connections

### Qwiic Connectors

This breakout configures the BMI330 to communicate over I<sup>2</sup>C by default and includes a pair of Qwiic connectors tied to the BMI330's power (3.3V and GND) and I<sup>2</sup>C pins (SDA/SCL) for solderless integration into a Qwiic circuit. This breakout sets the BMI330's I<sup>2</sup>C to 0x68 by default. Read on to the Solder Jumpers section for information on changing the address or enabling SPI.

### Plated Through-Holes

The board also includes two 0.1"-spaced headers on either side of the board. The bottom header routes out power and ground as well as all communication pins for both I<sup>2</sup>C, SPI and I3C. The top header routes to the BMI330's INT1 and INT2 pins.

## LED

The sole LED on the board is a red power status LED to indicate when the board has power.

## Solder Jumpers

This Qwiic breakout has four solder jumpers labeled <b>LED</b>, <b>CS</b>, <b>SDO/POCI</b> and <b>I</sup>2</sup>C</b>. The list below outlines their functionality, default states and any notes on their uses.

* **LED** - The LED jumper completes the power LED circuit and is CLOSED by default. Open this jumper to disable the power LED.
* **CS** - The CS jumper controls the default state of the Chip Select pin on the board, either pulled HIGH or Floating. This solder jumper is CLOSED by default to pull CS HIGH and enable I<sup>2</sup>C. Open this jumper to use the CS pin for SPI communication on the BMI330.
* **SDO/POCI** - The SDO/POCI jumper sets the BMI330's I<sup>2</sup>C address or enables SPI communication for the BMI330 by setting the SDO/POCI pin HIGH, LOW or Float. This three-way jumper pulls the SDO/POCI pin to Ground by default to set the I<sup>2</sup>C address to **0x68**. Adjust the solder jumper to the 3V3 side to set the address to **0x69**. Completely open the solder jumper to leave the SDO/POCI pin floating to use it for SPI communication.

## Board Dimensions

This board is a standard Qwiic breakout and measures 1" x 1" (25.4mm x 25.4mm) with four mounting holes that fit a 4-40 screw.