# MCCI-CATENA-4618 DOCUMENTATION

[Installing IDE on windows](#Installing-IDE-on-windows)

[Install SM32 board support library](#install-SM32-board-support-library)

[uploading 4618 sketch](#uploading-4618-sketch)

[provision your catena 4618](#provision-your-catena-4618)

[programming methods](#programming-methods)

[Installing zadig tool](#Installing-zadig-tool)

[Teraterm](#teaterm)

[lorawan TTN console](#lorawan-TTN-console)

[register application and devices](#register-application-and-devices)

[provisioning](#provisioning)

[Decoding the data](#Decoding the data)




## Installing-IDE-on-windows

1. Install arduino IDE for windows by using this link ----- https://en.softonic.com/download/arduino-ide/windows/post-

2. Mcci Catena 4618 code available in github login page.

## Install SM32 board support library

1. For that we have to choose board type STM32 on Tools --> board. 

2. If it is not available download in Boards manager.

3. And get those libraries for the board 4618 by cloning in your arduino library path.

## uploading 4618 sketch

1. Check the code if I have any issues or missing libraries fix them and verify by using
       Sketch -->verify
       
2. If it successful upload the sketch by using
        Sketch --> upload

## programming methods

Catena 4618 has two methods 
1. DFU
2. ST- LINK

 In the serial interface select --> Usbserial

 In the tools upload method --> select DFU AND PROGRAMMER --> STM boot loader


## installing zadig tool

1. ZADIG is the tool required for using DFU method.

2. Connect the board 4618 using usb cable interfaced to port in working laptop.

3. BOOT 0 and VDD should be shorted using wire.

4. In the zadig tool, select options -->list all devices shown.

5. Select STM-boot loader in the dropdown list.

6. Also change the driver to Win Usb and install the driver.


## teraterm
1. upload the sketch.

2. Download TERA TERM for view the output. Use this link to download https://tera-term.en.lo4d.com/windows


## lorawan TTN console

1. Create an account in LORAWAN TTN CONSOLE by using this link https://learn.adafruit.com/using-lorawan-and-the-things-network-with-circuitpython/tinylora-ttn-setup


## register application and devices

1. Click application and add application. Enter unique ID and in the handle registration choose TTn handler eu and add the application.

2. Now register the devices .In that page enter the device ID and click register.

3. Unplug the wire and in windows select --> device manager and check the port.

4. comeback to arduino sketch choose port -->and select the port mentioned in device manager.

5. In the tera term use the command to configure sketch with lorawan. For that it checks the id, if it is true ok will be printed in terminal.


## provisioning

1. Using tera term choose Setup-->terminal-->newline-->receiveauto

2. use command 

3. Fram reset hard, lorawan configure deveui, lorawan configure appeui, lorawan configure appkey and lorawan configure join 1.

4. System configure syseui,system configure platforguid and system configure operatingflags 1 and reset.


## decoding the data
1. In lorawan console page click data and that data is in the encode format. 

2. To decode the information, choose payload option and paste the decode format code.

3. Finally, the information of sensor values given.
