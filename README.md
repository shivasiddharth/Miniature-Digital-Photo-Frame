# Miniature-Digital-Photo-Frame
Pocket sized digital photo frame

## Build instructions   
************************
Materials Required   
************************
  I. Hardware requirements:   
    Adafruit 1.44” TFT display   
    Wemos D1 Mini (you could use other ardunio based boards)   
    Jumper wires (if you do not want to print a PCB)   
    General purpose PCB (once again if you do not want to print a PCB)   

  II. Software requirements:   
      The code has been tested and found to be working with the following versions of software.         
      Arduino IDE – 1.8.13   
      Fastone image resizer   
      Fritzing – Any version   
      Arduino Libraries     
        ArduinoJson – 5.13.5  
        Adafruit ST7735 and ST7739 Library – 1.6.0   
        Adafruit GFX Library – 1.10.4   
        TFT – 1.2.1   


************************
Connection Diagram    
************************  
The connections have been made in the Breadboard section of the Fritzing software as shown above. Mind the “Lite” pin connection, without which the backlight will not work.


************************
PCB Design    
************************
In the PCB tab of the Fritzing software, the PCB size and connections can be finalized. This design is difficult to be fabricated as a single layer board, hence two layers are being used. The pins have been labelled as the silkscreen print. The final PCB design has been shown below. You could use the “autoroute” function if you find it difficult to route the tracks.


************************
Printing the PCB   
************************  

To fabricate the PCB, the PCB design is first exported in the Gerber format as shown in the image. I used the services of https://jlcpcb.com to fabricate the PCB, as they offered excellent value for money.   


************************
Software for the Photo Frame   
************************   

I scripted the Arduino program that displays bitmap (BMP) images on the TFT display. I added a variable to change the duration of the slideshow or in other words, the time interval between concurrent images. You can find the full code here Arduino Sketch.

The program can be compiled and uploaded to the Wemos D1 Mini (or any other board that you may use). If you run into compilation errors, please double check the version of the libraries that you have used/installed against the version that I have listed above in the requirements.


************************    
Adding the Images     
************************   

The display has a fixed dimension of 128x128 pixels. So, it will not display larger images accurately. All the images to be used have to be resized to the dimensions of the TFT display. I downloaded emoji images of random sizes as shown in the first image.


Using the Fastone image resizer software, the emoji images were resized to the TFT limits and in the BMP format as shown in the second image.


The resized images have been shown below. They can now be copied to a SD Card and inserted into the SD Card slot of the Adafruit display.


************************
Final Outcome    
************************   

The TFT display and the Wemos D1 mini has been put together via the headers. For a size comparison, the mini digital photo frame has been placed beside a Mr.Bean Funko-Pop figure.
