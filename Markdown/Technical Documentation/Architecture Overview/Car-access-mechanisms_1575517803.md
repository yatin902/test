# BloXmove Dev : Car access mechanisms

Car access can be either controlled via the Virtual Car Wallet connected to a Telematics Gateway, or using a Hardware Car Wallet directly in the car.

Together with different options for gathering telematics data from the car, this results in the following three scenarios (also see original slides as attachment to this page):


## 1) Virtual Car Wallet for Access Control, Hardware Wallet for Telematics Data
![This is an image](https://github.com/yatin902/test/blob/main/1812397679.png)
## 2) No Telematics Gateway, Mobile App directly interacting with Hardware Wallet for Access Control
![This is an image](https://github.com/yatin902/test/blob/main/1812332143.png)
# 3) Virtual Car Wallet for Access Control and Telematics Data, no Hardware Wallet
![This is an image](https://github.com/yatin902/test/blob/main/1812168301.png)
The favoured approach is scenario 2, however due to restrictions in terms of in-car security the “mixed” scenario 1 is likely for the European Union. For testing and development, we currently employ scenario 3 with a simulated/mocked telematics gateway and telematics box.

![This is an image](https://github.com/yatin902/test/blob/main/1812233848.jpg)

