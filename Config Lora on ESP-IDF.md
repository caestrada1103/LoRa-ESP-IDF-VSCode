# How to correctly install the LoRa library in VSCode with framework ESP-IDF on ESP32?
hi every one, this tutorial is for show/explain how configure correctly the LoRa Libray in VSCode with in ESP-IDF.

It is clear that this explanation works for any library, especially if you want to use a library for a single project (locally, not globally)

## STEP 1:
Create a normal proyect on VSCode with Framework ESP-IDF, in my case, i will be use Board DOIT ESP32 DEVKIT V1

![Example1](https://github.com/Estraus96/Prueba-ESP32/blob/master/EJ1.jpg)

## STEP 2: 
Download the LoRa Library right here https://github.com/Inteform/esp32-lora-library

### STEP 2.1:
Extract them

### STEP 2.2:
Go to the Extract Folder and find into folder called "components"

### STEP 2.3:
Into Components you can see the folder called "lora", in there can see the lora.c and other folder called "include"
copy the "lora.c" and paste on your folder proyect that was created on VSCode into "Your_Folder\Test_LoRa\src"

### STEP 2.4:
Into the folder previously named "include", copy the file "lora.h" and do the same process explained above

after the above, the src folder of the project must contain these files:

![Example3](https://github.com/Estraus96/Prueba-ESP32/blob/master/EJ3.jpg)

## STEP 3:
After the previous step, we return to VSCode and include the lora.h in our proyect just like that

![Example2](https://github.com/Estraus96/Prueba-ESP32/blob/master/EJ2.jpg)
