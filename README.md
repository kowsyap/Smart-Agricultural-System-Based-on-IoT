# Smart Agriculture system based on IoT

This is a system which enables farmers to monitor and control their farms with a web-based application built with Node-RED. It uses IBM IoT Watson cloud platform as its backend.

## Description

  * Smart Agriculture System based on IoT can monitor soil moisture and climatic conditions to grow and yield a good crop.
  
  * The farmer can also get the realtime weather forecasting data by using external platforms like Open Weather API.
  
  * Farmer is provided a mobile app using which he can monitor the temperature, humidity and soil moisture parameters along with weather forecasting details.
  
  * Based on all the parameters he can water his crop by controlling the motors using the mobile application.
  
  * Even if the farmer is not present near his crop he can water his crop by controlling the motors using the mobile application from anywhere.
  
  * Here we are using the Online IoT simulator for getting the Temperature, Humidity and Soil Moisture values.

## Simulator

The data of the farm like soil moisture, humidity and temperature are collected from sensors and then need to be sent to cloud
but here I am using a simulator in which we are going to connect it to the IBM cloud account and send data to cloud.

The simulator I used is [here](https://watson-iot-sensor-simulator.mybluemix.net/)

![Simulator](/tasks/IoT_simulator.png)

## Web App User Interface

Web App is created using NodeRed.

There are two tabs in this Web App :

###  1.Home tab

   This tab contains measured and online weather forecast data displayed in guages.
  
   I used [OpenWeather](https://openweathermap.org/guide) to collect weather forecast data.
   
   ![Home tab](/tasks/Home_UI.png)
   
###  2.Controls tab

   This tab contains the controls of motor to switch it on, off and also a button to specify motor to run for 30 minutes continuosly.
   
   ![Controls tab](/tasks/Controls_UI.png)

## NodeRed Program Flow

This is the program flow of the web app created using NodeRed. 

>[flows.json](/flows.json) is the nodeRed file.

  ![flow](/tasks/program_flow.png)
  
## Virtual Farm Command Receiver on Python

Commands from the NodeRed are sent to the cloud and the following commands are received using Raspberry Pi or any other device with the following python code. (i.e, [iot_motor.py](/iot_motor.py))

Below image contains the python console showing the received commands.

![Receiver](/tasks/motor_output_in_console.PNG)
  
#### For a detailed view of the project, read [project report](/project_report.pdf).
