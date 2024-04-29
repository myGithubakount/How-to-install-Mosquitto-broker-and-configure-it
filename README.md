# How to install Mosquitto broker and configure it on Windows
In this project you can find an information about how to install your own local broker and configure it 
------------------------------------------
## Description

- Installing mosquitto
- Configure Firewall
- Configure mosquitto.conf
- Run mosquitto broker
- Install MQTT explorer
- Connect to your MQTT broker

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


## Configure mosquitto.conf

Now we need to configure our mosquitto. To do this, we go to the directory of our mosquitto. Usually, it is located in C:\Program Files\mosquitto

![alt text](image-10.png)

Open the mosquitto.conf file in editor. You can use any editor you want. Now we search for #listener. We have to uncomment it and setup the number of port

![alt text](image-11.png)

Now we need to find #allow_anonimous false, uncomment it and set the value to true

![alt text](image-12.png)

## Run mosquitto broker

After all this simulations, don't forget to save the .config file. After saving it, we can run our mosquitto MQTT broker. Run PowerShell as an administration and type "net start mosquitto"

![alt text](image-14.png)

## Install MQTT explorer

Now you can use any MQTT client to test your mosquitto MQTT broker. In this case we use Mqtt explorer

![alt text](image-15.png)