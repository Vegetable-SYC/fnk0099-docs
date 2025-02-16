##############################################################################
Chapter Serial Communication
##############################################################################

Serial Communication is a means of communication between different devices/devices. This section describes ESP32-S3’s Serial Communication.

Project 3.1 Serial Print
************************************

This project uses ESP32-S3's serial communicator to send data to the computer and print it on the serial monitor.

Component List
===============================

.. list-table:: 
   :width: 100%
   :header-rows: 1 
   :align: center
   
   * -  ESP32-S3 WROOM x1
     -  USB cable x1

   * -  |Chapter01_00|
     -  |Chapter01_01|

.. |Chapter01_00| image:: ../_static/imgs/1_LED/Chapter01_00.png
.. |Chapter01_01| image:: ../_static/imgs/1_LED/Chapter01_01.png

Related knowledge
===============================

Serial communication
-------------------------------

Serial communication generally refers to the Universal Asynchronous Receiver/Transmitter (UART), which is commonly used in electronic circuit communication. It has two communication lines, one is responsible for sending data (TX line) and the other for receiving data (RX line). The serial communication connections of two devices is as follows:

.. image:: ../_static/imgs/3_Serial_Communication/Chapter03_00.png
    :align: center

Before serial communication starts, the baud rate of both sides must be the same. Communication between devices can work only if the same baud rate is used. The baud rates commonly used is 9600 and 115200.

Serial port on ESP32-S3
-------------------------------

Freenove ESP32-S3 has integrated USB to serial transfer, so it could communicate with computer connecting to Type C cable.

.. image:: ../_static/imgs/3_Serial_Communication/Chapter03_01.png
    :align: center

Arduino Software also uploads code to Freenove ESP32-S3 through the serial connection.

Your computer identifies serial devices connecting to it as COMx. We can use the Serial Monitor window of Arduino Software to communicate with Freenove ESP32-S3, connect Freenove ESP32-S3 to computer through the Type C cable, choose the correct device, and then click the Serial Monitor icon to open the Serial Monitor window.

.. image:: ../_static/imgs/3_Serial_Communication/Chapter03_02.png
    :align: center

Interface of serial monitor window is as follows. If you can't open it, make sure Freenove ESP32-S3 has been connected to the computer, and choose the right serial port in the menu bar "Tools".

.. image:: ../_static/imgs/3_Serial_Communication/Chapter03_03.png
    :align: center

Circuit
==========================

Connect Freenove ESP32-S3 to the computer with Type C cable.

.. image:: ../_static/imgs/2_WS2812/Chapter02_00.png
    :align: center

Sketch
======================

Sketch_03.1_SerialPrinter
-------------------------------

.. image:: ../_static/imgs/3_Serial_Communication/Chapter03_04.png
    :align: center

Download the code to ESP32-S3 WROOM, open the serial port monitor, set the baud rate to 115200, and press the reset button. As shown in the following figure:

.. image:: ../_static/imgs/3_Serial_Communication/Chapter03_05.png
    :align: center

As shown in the image above, "ESP32-S3 initialization completed! " The previous is the printing message when the system is started. The user program is then printed at a baud rate of 115200.

The following is the program code:

.. literalinclude:: ../../../freenove_Kit/C/Sketches/Sketch_03.1_SerialPrinter/Sketch_03.1_SerialPrinter.ino
    :linenos: 
    :language: c
    :dedent:

Reference
---------------------------

.. py:function:: void begin(unsigned long baud, uint32_t config=SERIAL_8N1, int8_t rxPin=-1, int8_t txPin=-1, bool invert=false, unsigned long timeout_ms = 20000UL);	
    
    Initializes the serial port. Parameter baud is baud rate, other parameters generally use the default value.

.. py:function:: size_t println( arg );	

    Print to the serial port and wrap. The parameter arg can be a number, a character, a string, an array of characters, etc.

.. py:function:: size_t printf(const char * format, ...)  __attribute__ ((format (printf, 2, 3)));	

    Print formatted content to the serial port in the same way as print in standard C.

.. py:function:: unsigned long millis();	

    Returns the number of milliseconds since the current system was booted.

Project 3.2 Serial Read and Write
********************************************

From last section, we use serial port on Freenove ESP32-S3 to send data to a computer, now we will use that to receive data from computer.

Component and circuit are the same as in the previous project.

Sketch
=============================

Sketch_03.2_SerialRW
-------------------------------

.. image:: ../_static/imgs/3_Serial_Communication/Chapter03_06.png
    :align: center

Download the code to ESP32-S3 WROOM, open the serial monitor, and set the top right corner to **Newline** , **115200** . As shown in the following figure:

Then type characters like 'ABCDEFG' into the data sent at the top, and press Ctrl+Enter to send the message. 

.. image:: ../_static/imgs/3_Serial_Communication/Chapter03_07.png
    :align: center

The following is the program code:

.. literalinclude:: ../../../freenove_Kit/C/Sketches/Sketch_03.2_SerialRW/Sketch_03.2_SerialRW.ino
    :linenos: 
    :language: c
    :dedent:

In loop(), determine whether the serial port has data, if so, read and save the data, and if the newline character is read, print out all the data that has been read.

Reference
-------------------

.. py:function:: String();	
    
    Constructs an instance of the String class.
    
    For more information, please visit
    
    https://www.arduino.cc/reference/en/language/variables/data-types/stringobject/

.. py:function:: int available(void);	
    
    Get the number of bytes (characters) available for reading from the serial port. This is data that’s already arrived and stored in the serial receive buffer.

.. py:function:: Serial.read();	
    
    Reads incoming serial data.