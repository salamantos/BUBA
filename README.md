# BUBA
BUBA is a 36-key wireless keyboard

# Build guide
## PCB part list
| Part | Count | Notes |
| :--- | :---: | :---- |
| Nice!Nano V2 | 2 | Analog on [aliexpress](https://aliexpress.ru/item/1005001621678794.html?spm=a2g2w.orderdetail.0.0.7c724aa6qcxqjh&sku_id=12000016846541261&_ga=2.130299407.1493609630.1750741411-1399833778.1733553955) |
| Kailh Choc 1350 switches | 36 | [aliexpress](https://aliexpress.ru/item/1005005446722280.html?spm=a2g2w.orderdetail.0.0.42454aa6ibGAXx&sku_id=12000033116056002&_ga=2.226769437.1493609630.1750741411-1399833778.1733553955) |
| Kailh Choc 1350 sockets | 36 | [aliexpress](https://aliexpress.ru/item/1005006007846154.html?spm=a2g2w.orderdetail.0.0.1d204aa6P8AFYT&sku_id=12000035295576732&_ga=2.172020259.1493609630.1750741411-1399833778.1733553955) |
| Keycaps | 36 | Should be 1.65x1.65 cm, for example [aliexpress](https://aliexpress.ru/item/1005004558099208.html?spm=a2g2w.orderdetail.0.0.2f794aa6PMRDgN&sku_id=12000029606982948&_ga=2.226769437.1493609630.1750741411-1399833778.1733553955) |
| Blind keycaps | 2 | Optionally, you can buy 2 blind keycaps, like this [one](https://aliexpress.ru/item/1005005801849639.html?spm=a2g2w.orderdetail.0.0.6dd84aa6mOQywq&sku_id=12000034400650844&_ga=2.126899725.1493609630.1750741411-1399833778.1733553955) |
| Reset button YD-3414 | 2 | [aliexpress](https://aliexpress.ru/item/32898212708.html?spm=a2g2w.orderdetail.0.0.26d14aa6C22wnv&sku_id=65744827973&_ga=2.133255566.1493609630.1750741411-1399833778.1733553955) |
| Power switcher MSK-12C02 | 2 | [aliexpress](https://aliexpress.ru/item/4000685483225.html?spm=a2g2w.orderdetail.0.0.13724aa634mmE9&sku_id=12000037044894570&_ga=2.133255566.1493609630.1750741411-1399833778.1733553955) |
| LIPO battery | 2 | [401230](https://aliexpress.ru/item/32332620628.html?spm=a2g2w.orderdetail.0.0.58144aa6yRwDMa&sku_id=10000011118733382&_ga=2.253442569.1493609630.1750741411-1399833778.1733553955) or 301230 (last one is smaller, but will also work) |
| PH2.0 connector for batteries | 2 | You can buy [kit](https://aliexpress.ru/item/1005004689621192.html?spm=a2g2w.orderdetail.0.0.44ed4aa69hGHGt&sku_id=12000030109246019&_ga=2.164294975.1493609630.1750741411-1399833778.1733553955) |
| PH2.0 angled connectors for PCB | 2 | [aliexpress](https://aliexpress.ru/item/1005006058022917.html?spm=a2g2w.orderdetail.0.0.2d864aa6y3ekFd&sku_id=12000035557145316&_ga=2.164294975.1493609630.1750741411-1399833778.1733553955) |
| MCU sockets | 4 ||
| MCU pins |  ||

## Case part list
| Part | Count | Notes |
| :--- | :---: | :---- |
| 3D printed top | 2 ||
| 3D printed bottom | 2 ||
| 3D printed MCU cover | 2 ||
| Flat head screw M2x4x4 | 8 | [aliexpress](https://aliexpress.ru/item/4001248931159.html?sku_id=12000034160900192&spm=a2g2w.productlist.search_results.2.6d274144mNMv3y) |
| Threaded inserts M2xL3xOD3.2 | 8 | [aliexpress](https://aliexpress.ru/item/1005006201944599.html?spm=a2g2w.orderdetail.0.0.36434aa6refYqW&sku_id=12000036250301731&_ga=2.172046627.1493609630.1750741411-1399833778.1733553955) |

## PCB assembly
### Microcontroller
> **Warning**
> First flash the microcontroller to make sure it works, before soldering it in

Both the left and right halves of the keyboard use **identical PCBs**, so the steps below apply to each side

#### 1. Solder special pads on PCB

* Solder the **special pads** to the **top side** of each PCB
  These pads will connect PCB traces to the correct side of microcontroller
![telegram-cloud-document-2-5393216297880284355](https://github.com/user-attachments/assets/f9b4c933-4e1c-4618-932f-15645e7638aa)
![telegram-cloud-document-2-5393216297880284359](https://github.com/user-attachments/assets/7653aee6-0a40-46a8-8b70-a422cfc44761)

#### 2. Attach the sockets

* Solder **two 12-pin sockets** to each PCB, directly onto the header pins you just installed
![telegram-cloud-document-2-5393216297880284303](https://github.com/user-attachments/assets/da764ef8-de23-41a3-839b-8d1d30c82fc1)
![telegram-cloud-document-2-5393216297880284304](https://github.com/user-attachments/assets/e12ecc0d-d51a-44c0-8ffa-1d857c04e3c0)

#### 3. Prepare to socket the MCU

You have two options for socketing the microcontroller (MCU):

* Use **dedicated socketing pins**, or
* Improvise using **resistor or diode legs** (trimmed leads)

#### 4. Set up for soldering

* Insert the socketing pins (or trimmed leads) into the 12-pin sockets
* **Tape down** the sockets to prevent the pins from getting accidentally soldered to them
* Place the **microcontroller** on top of the inserted pins
* Make sure everything is aligned correctly

#### 5. Solder the MCU

* Carefully solder each pin to the corresponding pad on the microcontroller
* Take your time and ensure each connection is clean and solid

#### 6. Remove the MCU

* Once soldered, you can gently remove the microcontroller using **tweezers**
* This gives you a removable, socketed setup — useful for reprogramming or replacing the MCU later
* This step is necessary because you’ll need to place the battery underneath the MCU later on
![telegram-cloud-document-2-5393321584708578374](https://github.com/user-attachments/assets/4c5be719-772e-40e8-8f5a-7f58a4c74096)
![telegram-cloud-document-2-5391176433227823066](https://github.com/user-attachments/assets/1b376bab-78ca-43f8-8397-e5587f7f9ef6)

### Switch sockets
With the microcontroller in place, it's time to install the **hot-swap switch sockets**

#### 1. Orient the socket

* Take one **hot-swap socket** and place it into a switch footprint on the PCB
* Make sure the **sharp corner** of the socket is facing **bottom-left** of the switch position
  ⚠️ Orientation is important for proper electrical contact
![telegram-cloud-document-2-5393216297880284455](https://github.com/user-attachments/assets/7632bcd7-4773-4d7f-b4c7-92fccbe135e4)
![telegram-cloud-document-2-5393216297880284457](https://github.com/user-attachments/assets/9bd165f1-5132-40c5-ae88-8dac1e654bd3)

#### 2. Solder one socket at a time

* Solder **each socket individually** to ensure it sits flush and properly aligned
* After inserting the socket:

  * Hold it firmly in place
  * Solder one pad, then check alignment
  * Once it's aligned and flat, solder the second pad

#### 3. Repeat for all sockets

* Continue socket-by-socket until all switch positions are filled
![telegram-cloud-document-2-5393216297880284524](https://github.com/user-attachments/assets/7a821110-fb47-4053-8ed8-a76c09df6464)


### Reset button and power switch

With the sockets in place, let’s finish the essential components: the **reset button** and **power switch**

#### 1. Solder the Reset Button

* Insert the **reset button** into the holes. Make sure it sits flat against the board
* Solder all 4 legs

> The reset button is used to put the microcontroller into bootloader mode when flashing firmware

#### 2. Solder the Power Switch

* Insert the **power switch**, ensuring proper alignment
* Solder the switch legs to the PCB (3 pins and 4 case legs for stability)

Once both components are soldered, you're ready for the **final hardware steps** like installing key switches and assembling the case — or move on to **flashing the firmware** if you're testing before final assembly. Let me know how you'd like to continue!


### Battery socket

In this step, you’ll solder the **angled PH male connector** and prepare the battery connection

#### 1. Solder the angled PH male connector

* Insert the **angled PH male connector** into the battery pads on the PCB
* Make sure it faces upward
* Solder the pins securely on the underside of the board
![telegram-cloud-document-2-5393216297880284525](https://github.com/user-attachments/assets/1401cb67-1d2a-452c-a701-2e9c629c1740)

#### 2. Prepare the battery plug

* Take a **PH 2.0 female connector** and insert the battery wires into it:

  * **Red wire** → Positive (BAT+)
  * **Black wire** → Ground (GND)
* Crimp and insert the wires into the correct slots
![telegram-cloud-document-2-5393216297880284528](https://github.com/user-attachments/assets/9ecb7e1a-508e-43fa-9d41-07218b48d316)

#### 3. Check orientation (important!)

* The required polarity is **different for the left and right halves**:

  * On the **right half**, the **positive wire must be on the right** (when viewed from the front of the board)
  * On the **left half**, the **positive wire must be on the left**

> **Warning**
> Getting this wrong can damage your microcontroller or charging circuit. Double-check before plugging anything in

#### 4. Connect the Battery

* Carefully plug the battery’s female PH connector into the male socket you just soldered
* Place battery underneath the microcontroller
* Tuck the battery and wires neatly in place
* Put microcontroller back in place
![telegram-cloud-document-2-5393216297880284529](https://github.com/user-attachments/assets/a6019e73-484e-45d1-b18c-4a6f0bc4aa5c)
![telegram-cloud-document-2-5393216297880284164](https://github.com/user-attachments/assets/91624fd1-3671-4abb-9552-3fb2c94e2ba3)

> **Repeat all the steps to the other side of the PCB**

You're now finished with all soldering! Next step: **assemble the keyboard case and install mechanical switches**

