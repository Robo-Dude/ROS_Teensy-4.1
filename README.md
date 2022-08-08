# ROS_Teensy-4.1
Complete Tutorial on how to setup Teensy 4.1 with ROS on Nvidia Jetson.

This Tutorial is consist of two parts -
1. Setting Up Teensy 4.1 With Arduino IDE on Jetson Nano.
2. Testing of Teensy 4.1 With ROS Program On Jetson Nano.

### Setting Up Teensy 4.1 With Arduino IDE on Jetson Nano.

HARDWARE REQUIRED 
Nvidia Jetson Nano
Teensy 4.1
Datesheet-Teensy 4.1 
Micro USB cable 

SOFTWARE REQUIRED
Linux (Ubuntu) , Arduino IDE , TeensyDuino , TeensyLoader

![image](https://user-images.githubusercontent.com/65345575/183485704-a4d30459-008d-4b6c-897a-d5d8c64b5bf3.png)  

![image](https://user-images.githubusercontent.com/65345575/183485737-e45fa74a-e108-4b40-b681-839fc32c8d1e.png)

#### DESCRIPTION AND SPECIFICATION OF TEENSY 4.1 

Teensy 4.1 Is the First Arduino-Compatible Board with 100 Mbit Ethernet . The new Teensy 4.1 from PJRC simplifies that decision because It combines the real-time nature of an Arduino-compatible microcontroller with the processing and I/O performance of an operating system-based SBC in a slim package. 
Teensy 4.1 from PJRC is an update of their already mighty Arduino-compatible board. As the minor revision number suggests, the new board is an extension that builds on the previously introduced 4.0.

To Know Go to this Youtube link - https://www.youtube.com/watch?v=I4MDh-lencY&feature=youtu.be


##### Specification of Teensy 4.1

![image](https://user-images.githubusercontent.com/65345575/183486569-b5ba9c7a-6c0b-416a-bbad-8e356b90bcf7.png)

#### Pin Diagram of Teensy 4.1

![image](https://user-images.githubusercontent.com/65345575/183486798-7b5d149d-063c-400e-bbe8-8a526051a249.png)

#### INSTRUCTIONS- 

##### Step 1

Establishing the connection between the PC and the Teensy 4.1 using the Micro USB

Simply Connect the micro USb side to the Teensy 4.1 microcontroller and plug in USB to your system , you can also use your mobile charger to establish the connection. 

![image](https://user-images.githubusercontent.com/65345575/183487198-241ba838-c5ce-4683-9d8f-f2ae33a9b03a.png)


#### Step 2

Download the Teensyduino in Linux and Setup in Arduino IDE and Linux Environment

Teensyduino is a software add-on for the Arduino software. So to download it you can go to this website - [Teensyduino Download](https://www.pjrc.com/teensy/td_download.html)


Once You open this site , it’s look like this -

![image](https://user-images.githubusercontent.com/65345575/183487872-ec738191-bfaf-4c9e-88c0-3b4dc8e7d303.png)

Now, You have to choose the corresponding Teensyduino file according to your system requirements , Here were setting up the teensy 4.1 on jetson nano so, we have opted the
[Linux Installer (X86 64 bit)](https://www.pjrc.com/teensy/td_157/TeensyduinoInstall.linux64) option.

Once you download the Teensyduino Installer file on Linux system, keep it aside and follow this steps..

1. Download the Linux udev rules from this link Linux udev rules and copy the file to /etc/udev/rules.d.
    
2. To do this create the text file and paste the all the linux udev rules into this text file
    
     #### And rename the file name with “00-teensy.rules”
            
3. After that, open the folder where you keep this text file “00-teensy.rules” and open the terminal and execute this command line which move/paste          this text to “/etc/udev/rules.d/00-teensy.rules” location
    
            sudo cp 00-teensy.rules /etc/udev/rules.d/
                
4. Now Install the arduino IDE in your system if not installed yet.
    
5. If the arduino IDE already installed in your system than you have to install the teensyduino in your system , for installing the teensyduino go           back to the Teensydunino file folder and open terminal and run this lines on it to start installation process 
          
          chmod 755 TeensyduinoInstall.linux64
          
          sudo ./TeensyduinoInstall.linux64
          

Just running this command lines on terminal a small window will be get open on the screen like this -

![image](https://user-images.githubusercontent.com/65345575/183489953-56d509c6-1ad8-436f-bf9c-41026eee9f34.png)


#### Teensyduino Graphical Installer

The Teensyduino installer adds the necessary support files to Arduino. Your copy of Arduino must be one of the supported versions listed on this first screen.          

![image](https://user-images.githubusercontent.com/65345575/183490062-57b483b2-7327-4e2d-9751-74b631efc075.png)


Select the location where you extracted the Arduino Software
The Next button will only activate when a supported version of the Arduino Software is found.

![image](https://user-images.githubusercontent.com/65345575/183490125-7149d7c1-9bbf-40aa-a5c6-c337cceba28c.png)


Teensyduino can automatically install many libraries that are tested and verified to work with Teensy. Usually it's best to allow the installer to add them all. 

![image](https://user-images.githubusercontent.com/65345575/183490247-321bd23e-e755-406a-b422-ea68a09d54eb.png)

The installer will copy all the necessary files into your Arduino Software, when you click the "Install" button.

![image](https://user-images.githubusercontent.com/65345575/183490297-596c4f13-00b7-49d3-bab2-6e8e8dba88c5.png)

When installation is finished, you will see this final screen. Just click Done to quit the installer. 

![image](https://user-images.githubusercontent.com/65345575/183490359-05f08862-810a-430c-b053-ca9b83431199.png)


#### Step 3

### Programming of Teensy 4.1 using Arduino IDE and Teensyduino

Programming of Teensy 4.1 using Arduino IDE and Teensyduino

1. Start Arduino & Choose The Board , Now you are ready to run Arduino. The first step is to select the board you will be using, from the Tools->Boards menu. This menu will have entries for Teensy because you ran the Teensyduino installer. 

![image](https://user-images.githubusercontent.com/65345575/183491196-f5c130ad-6fe8-4e5e-9b27-ff372b3f0642.png)

2. The Arduino Software comes with many examples. Use the File->Examples->Digital->Blink menu to open the LED blink example. 

![image](https://user-images.githubusercontent.com/65345575/183491305-e78dda88-9e00-4864-82b5-08f7d01181c3.png)

3. Compile and Download To compile this code, click the "Verify" button. 

![image](https://user-images.githubusercontent.com/65345575/183491398-2e74d448-1233-41ba-8eea-8d3a2b569dff.png)

A message will appear showing the compiled size. The Teensy Loader will update with the new file  Just press the button on Teensy to program the code.

![image](https://user-images.githubusercontent.com/65345575/183491477-7ef58abb-eb85-4b70-b703-17aa7441af14.png)

## Completed

Teensy 4.1 Setup in Linux System Jetson Nano using TeensyDuino and Arduino IDE.

https://user-images.githubusercontent.com/65345575/183492639-801f63d4-252a-491b-afd7-90fa21022afa.mp4






