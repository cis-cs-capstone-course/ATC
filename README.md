# ATC
Autonomous-Tracking-Car

## Features 
1) ATC can be driven by the webapp generated by running the app.py file. The web app has the ability to make the car move left, right, forwards, and backwards. 
2) ATC has the ability to take photos and store photos using the "take picture" button. 
3) ATC can show a live stream of what the car sees
4) ATC can do a simple follow me going fowards to follow the user as the user gets further away from the car.

## Bugs 
1) The follow me feature is not completely matured. It can only follow the users if they are in frame and are only moving away or closer to the vehichle, the vehicle cannot turn with the follow me feature.
2) The frames per second and live stream is off by an average of a  second from real time (may vary due to internet connection) 

## How to run ATC 
This you will need:
  Arduino 
  Raspberry pi (model 3+ preferred since you will need a good amount of computing power and wifi chips come standard in   pi3 and up)  
  Picamera 
  ATC car

1) use the program you must be on the raspberry pi and have access to a screen or you can ssh into a pi, if you prefer the latter you can follow this guide https://itsfoss.com/ssh-into-raspberry/

2) Then you will need to activate the picamera on the raspiberry pi, here a tutorial on how enable it          https://www.raspberrypi.org/documentation/configuration/camera.md

2) Once you sucesssfully have the pi setup with the picamera enabled you can now git clone the master branch to get started with the program. 

3) From the ATC folder run the command: pip3 install -r requirements.txt 
   this will get the required dependencies for you to run the project 
   
4) Next you will need to go into the flask directory using: cd flask

5) Once you are inside the pi you will need to make an adjustment to the code to make it run on your ip adress, to do this follow this guide to identify your ip address https://www.pcworld.com/article/240803/how_to_find_your_ip_address_and_mac_address.html

6) Once you have your ip address, change the code in app.py's main to have it connect to your ip address (the port does not need to changed)

7) Now you will be able to run the program! to do this you type in the command: python3 app.py 

8) Once it is running the terminal will give you and address which you can copy and paste into your browser to access the webapp to control the car! 
