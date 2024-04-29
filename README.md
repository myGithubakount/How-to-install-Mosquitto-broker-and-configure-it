# How to install Mosquitto broker and configure it on Windows
In this project you can find an information about how to install your own local broker and configure it 
------------------------------------------
## Description

- Installing mosquitto
- Configure Firewall
- Run mosquitto broker
- Configure mosquitto.conf
- Install MQTT explorer
- connect to your MQTT broker

## Installing mosquitto

First of all, we need to download the [mosquitto installer](https://mosquitto.org/download/)

![alt text](image.png)

After downloading it run the installer and follow the instructions

![alt text](image-1.png)

## Configuring Firewall

Open the Windows Defender Firewall -> Advanced settings

![alt text](image-2.png)

Go to the "Inbound Rules" and press "New Rule..."

![alt text](image-4.png)

Select "Predifined -> File and Printer Sharing"

![alt text](image-5.png)

Next, select "File and Printer Sharing (Echo Request - ICMPv4-ln)". Then press Finish

![alt text](image-6.png)

Now we need to add one more New Rule. This time we select "Port"

![alt text](image-7.png)

Next we need to enter the number of port (1883)

![alt text](image-8.png)

At the and, we need to give a name to our new rule

![alt text](image-9.png)

