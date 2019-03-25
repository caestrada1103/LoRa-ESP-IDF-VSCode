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
After the previous step, we return to VSCode and include the lora.h in our proyect just like that:

![Example2](https://github.com/Estraus96/Prueba-ESP32/blob/master/EJ2.jpg)

## STEP 4:
After all previus step, we see 8 mistakes the file "lora.c", this is because we didn't define the ports will be normaly use with this library, now we need to define the ports will be use.

## STEP 5:
Then we need to open and edit the file "sdkconfig.h" (file that generate automaticaly when finished the compiler task)

after of all the configuration, we need to add this follow lines code, corresponding to the ports that LoRa will be use

```C
#define CONFIG_CS_GPIO 15
#define CONFIG_RST_GPIO 32
#define CONFIG_MISO_GPIO 13
#define CONFIG_MOSI_GPIO 12
#define CONFIG_SCK_GPIO 14
```

## STEP 6:
Then it's time to compile, and test your proyects and conexions with this library.

![Example4](https://github.com/Estraus96/Prueba-ESP32/blob/master/ej4.jpg)
