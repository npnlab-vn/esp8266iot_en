# ESP8266_IoT package

The ESP8266_IoT library is developed to support programming, including the following main features:
1. Connect to Wifi network
2. Upload data to Thingspeak Server
The library is optimized for connection to the ChiPi Base Shield circuit.
Documentation: [Textbook] Kết nối vạn vật với Microbit


![](https://github.com/elecfreaks/pxt-esp8266iot/blob/master/ESP8266.png)


## Hardware Setup

1. Insert the [OLED display](http://www.elecfreaks.com/estore/iic-oled.html) into the I2C ports on the [ELECFREAKS Octopus:bit](http://www.elecfreaks.com/estore/elecfreaks-micro-bit-breakout-board.html).


## Basic usage

1. Open [Microsoft Makecode/microbit](https://pxt.microbit.org) and create a new project 
2. Search and add the `ESP8266` package
3. Use the `ESP8266` drawer in the editor to drag out and arrange the blocks
4. Click `Download` to move your program to the micro:bit


## Example

### set wifi
Set pin RX and pin TX for ESP8266 Serial Wifi Module, Baud rate: 115200.
```blocks
ESP8266_IoT.initwifi(SerialPin.P2, SerialPin.P8)
```

### connet wifi
Connectwifi，please fill in your ssid and your key.
```blocks
ESP8266_IoT.connectwifi("your ssid", "your key")
```

### connect thingspeak
Connect thingspeak IoT TCP server.
```blocks
ESP8266_IoT.connectthingspeak()
```

### set data to be send 
Set data to be sent. Firstly, you should fill in your write api key.
```blocks
ESP8266_IoT.tosendtext(
"your write api key",
0,
0,
0,
0,
0,
0,
0,
0
)
``` 

### senddata
Send data to thingspeak.
```blocks
ESP8266_IoT.senddata()
```


## License

MIT


## Supported targets

* for PXT/microbit
(The metadata above is needed for package search.)

```package
esp8266=github:elecfreaks/pxt-esp8266iot
```



