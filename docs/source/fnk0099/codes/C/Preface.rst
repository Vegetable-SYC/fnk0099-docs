##############################################################################
Preface
##############################################################################

ESP32-S3 is a micro control unit with integrated Wi-Fi launched by Espressif, which features strong properties and integrates rich peripherals. It can be designed and studied as an ordinary Single Chip Micyoco(SCM) chip, or connected to the Internet and used as an Internet of Things device.

ESP32-S3 can be developed using the Arduino platform, which will definitely make it easier for people who have learned arduino to master. Moreover, the code of ESP32-S3 is completely open-source, so beginners can quickly learn how to develop and design IOT smart household products including smart curtains, fans, lamps and clocks.

Generally, ESP32-S3 projects consist of code and circuits. Don't worry even if you've never learned code and circuits, because we will gradually introduce the basic knowledge of C programming language and electronic circuits, from easy to difficult. Our products contain all the electronic components and modules needed to complete these projects. It's especially suitable for beginners.

We divide each project into four parts, namely Component List, Component Knowledge, Circuit and Code. Component List helps you to prepare material for the experiment more quickly. Component Knowledge allows you to quickly understand new electronic modules or components, while Circuit helps you understand the operating principle of the circuit. And Code allows you to easily master the use of SEP32 and accessory kit. After finishing all the projects in this tutorial, you can also use these components and modules to make products such as smart household, smart cars and robots to transform your creative ideas into prototypes and new and innovative products.

In addition, if you have any difficulties or questions with this tutorial or toolkit, feel free to ask for our quick and free technical support through support@freenove.com 

ESP32-S3 WROOM
*********************************

ESP32-S3-WROOM-1 has launched a total of two antenna packages, PCB on-board antenna and IPEX antenna respectively. The PCB on-board antenna is an integrated antenna in the chip module itself, so it is convenient to carry and design. The IPEX antenna is a metal antenna derived from the integrated antenna of the chip module itself, which is used to enhance the signal of the module.

.. list-table:: 
   :width: 100%
   :header-rows: 1 
   :align: center
   
   * -  PCB on-board antenna
     -  IPEX antenna

   * -  |Preface00|
     -  |Preface01|

.. |Preface00| image:: ../_static/imgs/Preface/Preface00.png
.. |Preface01| image:: ../_static/imgs/Preface/Preface01.png

In this tutorial, the ESP32-S3 WROOM is designed based on the PCB on-board antenna-packaged ESP32-S3-WROOM-1 module. 

ESP32-S3 WROOM Lite

.. image:: ../_static/imgs/Preface/Preface02.png
    :align: center

The hardware interfaces of ESP32-S3 WROOM are distributed as follows:

.. image:: ../_static/imgs/Preface/Preface03.png
    :align: center

Compare the left and right images. We've boxed off the resources on the ESP32-S3 WROOM in different colors to facilitate your understanding of the ESP32-S3 WROOM.

.. list-table:: 
   :width: 100%
   :header-rows: 1 
   :align: center
   
   * -  Box color 
     -  Corresponding resources introduction

   * -  |Preface04|
     -  **GPIO pin**

   * -  |Preface05|
     -  **LED indicator**

   * -  |Preface06|
     -  **Reset button, Boot mode selection button**

   * -  |Preface07|
     -  **USB port**

.. |Preface04| image:: ../_static/imgs/Preface/Preface04.png
.. |Preface05| image:: ../_static/imgs/Preface/Preface05.png
.. |Preface06| image:: ../_static/imgs/Preface/Preface06.png
.. |Preface07| image:: ../_static/imgs/Preface/Preface07.png

For more information, please visit: https://www.espressif.com.cn/sites/default/files/documentation/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf. 

CH343 (Importance)
**********************************

ESP32-S3 WROOM uses CH343 to download codes. So before using it, we need to install CH343 driver in our computers.

Windows
====================================

Check whether CH343 has been installed
-----------------------------------------------

1.	Connect your computer and ESP32-S3 WROOM with a Type C cable.

.. image:: ../_static/imgs/Preface/Preface08.png
    :align: center

2.	Turn to the main interface of your computer, select "This PC" and right-click to select "Manage".

.. image:: ../_static/imgs/Preface/Preface09.png
    :align: center

3.	Click "Device Manager". If your computer has installed CH343, you can see "USB-Enhances-SERIAL CH343 (COMx)". And you can click :ref:`here <MAC>` to move to the next step.

.. image:: ../_static/imgs/Preface/Preface10.png
    :align: center

Installing CH343
----------------------------------

1.	First, download CH343 driver, click http://www.wch-ic.com/search?t=all&q=ch343 to download the appropriate one based on your operating system.

.. image:: ../_static/imgs/Preface/Preface11.png
    :align: center

If you would not like to download the installation package, you can open " **Freenove_ESP32_S3_WROOM_Board_Lite/CH343** ", we have prepared the installation package.

.. image:: ../_static/imgs/Preface/Preface12.png
    :align: center

2.	Open the folder "Freenove_ESP32_S3_WROOM_Board_Lite/CH343/Windows/"

.. image:: ../_static/imgs/Preface/Preface13.png
    :align: center

3.	Double click "CH343SER.EXE".

.. image:: ../_static/imgs/Preface/Preface14.png
    :align: center

4.	Click "INSTALL" and wait for the installation to complete.

.. image:: ../_static/imgs/Preface/Preface15.png
    :align: center

5.	Install successfully. Close all interfaces.

.. image:: ../_static/imgs/Preface/Preface16.png
    :align: center

6.	When ESP32-S3 WROOM is connected to computer, select "This PC", right-click to select "Manage" and click "Device Manager" in the newly pop-up dialog box, and you can see the following interface.

.. image:: ../_static/imgs/Preface/Preface17.png
    :align: center

7.	So far, CH343 has been installed successfully. Close all dialog boxes. 

.. _MAC:

MAC
================================

First, download CH343 driver, click http://www.wch-ic.com/search?t=all&q=ch343 to download the appropriate one based on your operating system.

.. image:: ../_static/imgs/Preface/Preface18.png
    :align: center

If you would not like to download the installation package, you can open "Freenove_ESP32_S3_WROOM_Board_Lite/CH343", we have prepared the installation package.

Second, open the folder "Freenove_ESP32_S3_WROOM_Board_Lite/CH343/MAC/"

.. image:: ../_static/imgs/Preface/Preface19.png
    :align: center

Third, click Continue.

.. image:: ../_static/imgs/Preface/Preface20.png
    :align: center

Fourth, click Install.

.. image:: ../_static/imgs/Preface/Preface21.png
    :align: center

Then, waiting Finsh.

.. image:: ../_static/imgs/Preface/Preface22.png
    :align: center

Finally, restart your PC.

.. image:: ../_static/imgs/Preface/Preface23.png
    :align: center

If you still haven't installed the CH340 by following the steps above, you can view readme.pdf to install it. 

.. image:: ../_static/imgs/Preface/Preface24.png
    :align: center

Programming Software
**********************************

Arduino Software (IDE) is used to write and upload the code for Arduino Board.

First, install Arduino Software (IDE): visit https://www.arduino.cc, click "Download" to enter the download page.

.. image:: ../_static/imgs/Preface/Preface25.png
    :align: center

Select and download corresponding installer according to your operating system. If you are a windows user, please select the "Windows Installer" to download to install the driver correctly.

.. image:: ../_static/imgs/Preface/Preface26.png
    :align: center

After the download completes, run the installer. For Windows users, there may pop up an installation dialog box of driver during the installation process. When it popes up, please allow the installation.

After installation is complete, an Arduino Software shortcut will be generated in the desktop. Run the Arduino Software.

.. image:: ../_static/imgs/Preface/Preface27.png
    :align: center

The interface of Arduino Software is as follows:

.. image:: ../_static/imgs/Preface/Preface28.png
    :align: center

Programs written with Arduino Software (IDE) are called sketches. These sketches are written in the text editor and saved with the file extension.ino. The editor has features for cutting/pasting and searching/replacing text. The message area gives feedback while saving and exporting and also displays errors. The console displays text output by the Arduino Software (IDE), including complete error messages and other information. The bottom right-hand corner of the window displays the configured board and serial port. The toolbar buttons allow you to verify and upload programs, create, open, and save sketches, and open the serial monitor.

.. list-table:: 
   :width: 100%
   :header-rows: 1 
   :align: center
   
   * -  Box color 
     -  Corresponding resources introduction

   * -  |Preface29|
     -  **Verify** 
      
        Check your code for compile errors. 


   * -  |Preface30|
     -  **Upload** 
      
        Compile your code and upload them to the configured board. 

   * -  |Preface31|
     -  **Debug** 
      
        Debug code running on the board. 
        
        (Some development boards do not support this function)

   * -  |Preface32|
     -  **Development board selection**
      
        Configure the support package and upload port of 
        
        the development board.

   * -  |Preface33|
     -  **Serial Plotter**
      
        Receive serial port data and plot it in a discounted graph. 

   * -  |Preface34|
     -  **Serial Monitor**  
      
        Open the serial monitor.  

.. |Preface29| image:: ../_static/imgs/Preface/Preface29.png
.. |Preface30| image:: ../_static/imgs/Preface/Preface30.png
.. |Preface31| image:: ../_static/imgs/Preface/Preface31.png
.. |Preface32| image:: ../_static/imgs/Preface/Preface32.png
.. |Preface33| image:: ../_static/imgs/Preface/Preface33.png
.. |Preface34| image:: ../_static/imgs/Preface/Preface34.png

Additional commands are found within the five menus: File, Edit, Sketch, Tools, Help. The menus are context sensitive, which means only those items relevant to the work currently being carried out are available.

Install Arduino ESP32 Package
**************************************

First, open the software platform arduino, and then click File in Menus and select Preferences.

.. image:: ../_static/imgs/Preface/Preface35.png
    :align: center

Second, click on the symbol behind "Additional Boards Manager URLs" 

.. image:: ../_static/imgs/Preface/Preface36.png
    :align: center

Third, fill in https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json in the new window, click OK, and click OK on the Preferences window again.

.. image:: ../_static/imgs/Preface/Preface37.png
    :align: center

Fourth, click "Boards Manager". Enter "esp32" in Boards manager and select 3.0.4, Then click "INSTALL".

.. image:: ../_static/imgs/Preface/Preface38.png
    :align: center

Arduino will download these files automaticly. Wait for the installation to complete.

.. image:: ../_static/imgs/Preface/Preface39.png
    :align: center

When finishing installation, click Tools in the Menus again and select Board: "Arduino Uno", and then you can see information of ESP32. click "ESP32-S3 Dev Module" so that the ESP32-S3 programming development environment is configured.

.. image:: ../_static/imgs/Preface/Preface40.png
    :align: center

Config ESP32S3 WROOM Lite
*****************************************

Please configure the ESP32S3 WROOM as follows when opening each Sketch.

.. image:: ../_static/imgs/Preface/Preface41.png
    :align: center

Notes for GPIO
***************************************

Strapping Pin

There are four Strapping pins for ESP32-S3:GPIO0, GPIO45, GPIO46, GPIO3。

With the release of the chip's system reset (power-on reset, RTC watchdog reset, undervoltage reset), the strapping pins sample the level and store it in the latch as "0" or "1" ", and keep it until the chip is powered off or turned off.

Each Strapping pin is connecting to internal pull-up/pull-down.  Connecting to high-impedance external circuit or without an external connection, a strapping pin's default value of input level will be determined by internal weak pull-up/pull-down. To change the value of the Strapping, users can apply an external pull-down/pull-up resistor, or use the GPIO of the host MCU to control the level of the strapping pin when the ESP32-S3’s power on reset is released.

**When releasing the reset, the strapping pin has the same function as a normal pin.**

The followings are default configurations of these four strapping pins at power-on and their functions under the corresponding configuration.

.. image:: ../_static/imgs/Preface/Preface42.png
    :align: center

If you have any difficulties or questions with this tutorial or toolkit, feel free to ask for our quick and free technical support through support@freenove.com at any time.

or check: https://www.espressif.com/sites/default/files/documentation/esp32-s3-wroom-1_wroom-1u_datasheet_en.pdf

PSRAM Pin
================================

The module on the ESP32-S3-WROOM board uses the ESP32-S3R8 chip with 8MB of external Flash. When we use the OPI PSRAM, please note that the GPIO35-GPIO37 on the ESP32-S3-WROOM board will not be available for other purposes. When OPI PSRAM is not used, GPIO35-GPIO37 on the board can be used as normal GPIO.

.. image:: ../_static/imgs/Preface/Preface43.png
    :align: center

USB Pin
==============================

In Micropython, GPIO19 and GPIO20 are used for the USB function of ESP32S3, so they cannot be used as other functions!