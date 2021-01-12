**DOCUMENTATION OF MCCI-CATENA 4618:**

STEP 1: Install arduino IDE for windows by using this link ----- **https://en.softonic.com/download/arduino-ide/windows/post**-download

STEP 2:Mcci Catena 4618 code available in github login page.

STEP 3:And get those libraries for the **board 4618** by cloning in your **arduino library path.**

STEP 4: For that we have to choose board type **STM32** on **Tools à board**. If it is not available download in **Boards manager.**

STEP 5:Check the code if I have any issues or missing libraries fix them and verify by using

`        `**Sketch à verify**

STEP 6:If it successful upload the sketch by using

`        `**Sketch à upload**

STEP 7:Catena 4618 has two methods 

1. DFU
1. ST- LINK

STEP 8:In the **serial interface select àUsbserial**

STEP 9:In the tools upload method à **select DFU AND PROGRAMMER àSTM boot loader**

STEP 10:**ZADIG** is the tool required for using DFU method

STEP 11:Connect the board 4618 using usb cable interfaced to port in working laptop.

STEP 12**:BOOT 0** and **VDD** should be shorted using wire.

STEP 13:In the zadig tool, select **options àlist all devices shown.**

Step 14:Select **STM-boot loader** in the dropdown list.

STEP 15:Also change the **driver** to **Win Usb** and install the driver.

STEP 16:now **upload the sketch**

STEP 17:Download **TERA TERM** for view the output. Use this link to download <https://tera-term.en.lo4d.com/windows>

STEP 18:Create an account **in LORAWAN TTN CONSOLE** by using this link <https://learn.adafruit.com/using-lorawan-and-the-things-network-with-circuitpython/tinylora-ttn-setup>

STEP 19:Click **application** and **add application**. Enter **unique ID** and in the handle registration choose TTn handler eu and add the application

STEP 20:Now **register the devices** .In that page enter the **device ID and click register.**

STEP 21:Unplug the wire and in windows select à **device manager** and check the **port**.

Step 22:comeback to arduino sketch choose port à and select the port mentioned in **device manager**.

STEP 23:In the tera term use the command to configure sketch with lorawan. For that it checks the id, if it is true ok will be printed in terminal

STEP 24:Using tera term choose **Setupàterminalànewlineàreceiveàauto**

Step 25:use command** 

**Fram reset hard, lorawan configure deveui, lorawan configure appeui, lorawan configure appkey and lorawan configure join 1.**

**System configure syseui,system configure platforguid and system configure operatingflags 1 and reset.**

STEP 26:In lorawan console page click data and that data is in the encode format .

STEP 27:To **decode** the information, choose **payload option** and paste the decode format code .

STEP 28:Finally, the information of sensor values given.


