# Autonomous System of a FCHEV Bus
![image](https://user-images.githubusercontent.com/85165363/120798406-fcd27b80-c545-11eb-9694-399bbd61de94.png)

## Intro
This project represents an analysis and design of a level 4 autonomous system for an electric bus with a hydrogen fuel cell range extender. The bus was envisioned to replace the current fleet in the Loughborough University campus.

## Aims and Objectives
The aim was to design the autonomous passenger systems - which include vision devices, door and ramp systems - in order to satisfy the SAE level 4 of autonomy. The objectives were as followed:
1. No critical blind spots around the bus
1. Sensor field of view to reach 200 m in range, which would help with gaining time and preventing unexpected manoeuvres
1. Select a sufficiently powerfull control unit
1. Average 1 minute saved every campus bus cycle compared to non-autonomous driving
1. Design and package the door systems and the wheelchair ramps in accordance to legislation and autonomous needs
1. Efficient autonomous passenger loading system
1. Contactless payment
1. Door system opening/closing and ramp deployment/retracting times of about 5 seconds 
 
## Field of View
The autonomous devices used to produce the FOV are a Lidar, 3 mono cameras, a long range radar, a medium range radar, 4 short range radars, 8 ultrasonics, a GPS, an inertial measurement unit (IMU) and a control unit. The required vision range of 200 m was obtained via the Lidar and long range radars. The horizontal and vertical FOVs are shown in the images below.

![Screenshot 2021-06-04 164311](https://user-images.githubusercontent.com/85165363/120810768-ffd46880-c553-11eb-9935-7f4185b57bb9.jpg)
![Screenshot 2021-06-04 164156](https://user-images.githubusercontent.com/85165363/120810790-0531b300-c554-11eb-98bd-aba9532b8f70.jpg)

The positioning of these devices around the bus is also shown below.

![image](https://user-images.githubusercontent.com/85165363/120811168-5cd01e80-c554-11eb-9334-eccab92407b6.png)
![image](https://user-images.githubusercontent.com/85165363/120811214-69547700-c554-11eb-8713-c57ceb5779cc.png)
![image](https://user-images.githubusercontent.com/85165363/120811190-648fc300-c554-11eb-8887-8e11a40822fd.png)

Below the positioning of the control unit and the system flow chart are shown.
![image](https://user-images.githubusercontent.com/85165363/120822917-8a6e9500-c55f-11eb-97c6-5efd8400b274.png)
![flow](https://user-images.githubusercontent.com/85165363/120823088-b9850680-c55f-11eb-99e8-cc5313b9327e.jpg)

Standard Kalman filtering was used in order to predict the time of doing one bus cycle, which ended up being on par with the time averaged by a human driver. Where the autonomous system could have a time advantage over the human driving is when taking into consideration the breaks and shift changes when dealing with human workers and with preventing obstacles quicker by having larger FOV.

![Screenshot 2021-06-04 182112](https://user-images.githubusercontent.com/85165363/120825077-b1c66180-c561-11eb-8bb5-f499ce4c03a9.jpg)

## Passengers Loading
The process of dealing with the passengers would be made easier by having a phone application where wheelchair ramps can be requested, live timetables can be shown and it would offer surveilance in order to prevent buses meeting up at stops. The actual loading system would benefit from cameras installed on the side of the bus to provide FOV (first 2 images) and from a programmed door closing procedure (3rd image).

![image](https://user-images.githubusercontent.com/85165363/120825848-78dabc80-c562-11eb-8049-50eb0d1c2a36.png)
![image](https://user-images.githubusercontent.com/85165363/120825872-7e380700-c562-11eb-886e-fe0b78dbe031.png)
![Screenshot 2021-06-04 182738](https://user-images.githubusercontent.com/85165363/120825934-9019aa00-c562-11eb-8437-d4236791c57a.jpg)

## Door and Ramp Systems
The door system selected was a pneumatic one. In order to satisfy the 5 sec as the opening and closing time, a force of 420 N would be required to pull the doors.

![image](https://user-images.githubusercontent.com/85165363/120832590-821b5780-c569-11eb-8027-fb479ba71c1f.png)
![image](https://user-images.githubusercontent.com/85165363/120832608-86477500-c569-11eb-889b-b5d9117e3ae6.png)
![Screenshot 2021-06-04 191826](https://user-images.githubusercontent.com/85165363/120832745-a9722480-c569-11eb-929d-ecde10bd4c1f.jpg)

0.12 kW would be the power required to pull the wheelchair ramp within the time limit and, consequently, an appropriate motor was chosen. The design of the ramp shows that it would be packaged in an underfloor cassette and deployed/retracted longitudinally. This would be more advantageous than a folding ramp in case of a fully packed bus.

![image](https://user-images.githubusercontent.com/85165363/120833216-3321f200-c56a-11eb-9bed-fa18a323374f.png)

