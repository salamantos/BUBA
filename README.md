# BUBA
BUBA is a 36-key wireless keyboard

# Build guide
### PCB part list
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

### Case part list
| Part | Count | Notes |
| :--- | :---: | :---- |
| 3D printed top | 2 ||
| 3D printed bottom | 2 ||
| 3D printed MCU cover | 2 ||
| Flat head screw M2x4x4 | 8 | [aliexpress](https://aliexpress.ru/item/4001248931159.html?sku_id=12000034160900192&spm=a2g2w.productlist.search_results.2.6d274144mNMv3y) |
| Threaded inserts M2xL3xOD3.2 | 8 | [aliexpress](https://aliexpress.ru/item/1005006201944599.html?spm=a2g2w.orderdetail.0.0.36434aa6refYqW&sku_id=12000036250301731&_ga=2.172046627.1493609630.1750741411-1399833778.1733553955) |

### PCB assembly
#### Microcontroller
> **Warning**
> First flash the microcontroller to make sure it works, before soldering it in.

Both the left and right halves of the keyboard use **identical PCBs**, so the steps below apply to each side.

#### 1. Solder special pads on PCB

* Solder the **special pads** to the **top side** of each PCB.
  These pads will connect PCB traces to the correct side of microcontroller.
![telegram-cloud-document-2-5393216297880284355](https://github.com/user-attachments/assets/f9b4c933-4e1c-4618-932f-15645e7638aa)
![telegram-cloud-document-2-5393216297880284359](https://github.com/user-attachments/assets/7653aee6-0a40-46a8-8b70-a422cfc44761)

#### 2. Attach the sockets

* Solder **two 12-pin sockets** to each PCB, directly onto the header pins you just installed.
![telegram-cloud-document-2-5393216297880284303](https://github.com/user-attachments/assets/da764ef8-de23-41a3-839b-8d1d30c82fc1)
![telegram-cloud-document-2-5393216297880284304](https://github.com/user-attachments/assets/e12ecc0d-d51a-44c0-8ffa-1d857c04e3c0)

#### 3. Prepare to socket the MCU

You have two options for socketing the microcontroller (MCU):

* Use **dedicated socketing pins**, or
* Improvise using **resistor or diode legs** (trimmed leads).

#### 4. Set up for soldering

* Insert the socketing pins (or trimmed leads) into the 12-pin sockets.
* **Tape down** the sockets to prevent the pins from getting accidentally soldered to them.
* Place the **microcontroller** on top of the inserted pins.
* Make sure everything is aligned correctly.

#### 5. Solder the MCU

* Carefully solder each pin to the corresponding pad on the microcontroller.
* Take your time and ensure each connection is clean and solid.

#### 6. Remove the MCU

* Once soldered, you can gently remove the microcontroller using **tweezers**.
* This gives you a removable, socketed setup — useful for reprogramming or replacing the MCU later.
* This step is necessary because you’ll need to place the battery underneath the MCU later on
![telegram-cloud-document-2-5393321584708578374](https://github.com/user-attachments/assets/4c5be719-772e-40e8-8f5a-7f58a4c74096)
![telegram-cloud-document-2-5391176433227823066](https://github.com/user-attachments/assets/1b376bab-78ca-43f8-8397-e5587f7f9ef6)

