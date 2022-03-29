# RFID_attendance_SERVER
in this prj we have two NODEMCU ( ESP8266) and  two RFID_RC522 and some rfid tags we used ARDUINO IDE on NODEMCU and running server with XAMPP

# EXPLAIN prj
in this prj we have two type devices 

MASTER ENROLL device :
> you can add or remove card in the server or you can limit some card to access some doors ( NODEMCU + RFID + MODEM)

DOOR devices:
> in this devices we have a relay that we can use to OPEN or CLOSE the door . this action can be up the tag which RFID read (NIDEMCU + RFID + RELAY + LOCK + MODEM)

we use diffrent language in order to do this prj ( C++ , CSS , HTML , PHP , JAVASCRIPT )

# APPLICATION

you have to install XAMPP 

you have to install ARDUINO IDE 
>#include <ESP8266WiFi.h>
>
>#include <ESP8266HTTPClient.h>
>
>#include <SPI.h>
>
#include <MFRC522.h>

# README 

when you run the code you have to change this line and put your user and pass for your modem to let micro access to the server

>const char *ssid = "Galaxy";
>const char *password = "noproblem";

and also you need to get your system ip to put in the each code in this line  before [ /rfidattendance/getdata.php ]: 
 
>String URL = "http://192.168.57.73/rfidattendance/getdata.php";

and then after running XAMPP you have get two device_token for each (enroll and attendance door) and put the id token here for each micro 

>const char* device_token  = "adc46c6518ccd334"


# Explain Code

you can see that in the attendance system when the card put on the reader this system check information with the server and if the card was saved in the server the details would be saved and then the door will be open 

else the door still be closed 

and in the master system the admin can add or remove the card also they can watch who came and who left and also when they did  

![](https://github.com/mohammadst99/RFID_attendance_SERVER/blob/main/pictures/Picture%201.jpg)

the door will be opened with the relay because most of LOCK works with higher than 5V so we need relay 

![](https://github.com/mohammadst99/RFID_attendance_SERVER/blob/main/pictures/Picture%202.jpg)

this is the systeam (NODEMCU and RFID RC522)

![](https://github.com/mohammadst99/RFID_attendance_SERVER/blob/main/pictures/Picture%203.jpg)



# Test Image 
 you have to fill the user and pass for MASTER who have the acccess to the server (defult it is :"admin" for both)
 
 ![](https://github.com/mohammadst99/RFID_attendance_SERVER/blob/main/pictures/Picture%206.png)
 
 
 in this picture the MASTER can see the ALL the users defined in the server 
 
 ![](https://github.com/mohammadst99/RFID_attendance_SERVER/blob/main/pictures/Picture%208.png)
 
 
 in this picture the MASTER can see the ALL the users log (entarance data) 
  
   ![](https://github.com/mohammadst99/RFID_attendance_SERVER/blob/main/pictures/Picture%2010.png)
   
 
 in this page the MASTER can give access or get from some one or add/remove cards from server 
 
 ![](https://github.com/mohammadst99/RFID_attendance_SERVER/blob/main/pictures/Picture%209.png)
 
 
 
 


