# Arduino library for the HP303B
### Installation
- Clone this repository  or download&unzip [zip file](https://github.com/wemos/LOLIN_HP303B_Library/archive/master.zip) into Arduino/libraries
### Usage
- Temperature and pressure values returned by the library functions are multiplied by 100, so fractional part is included into integer return value. This is done to avoid using of floating point types, which aren't supported by ESP8266 and software emulation is bulky and slow.
- /100 result to get inteder part and %100 to get fractional part:
 ```c
 Serial.println("Temperature: %d.%d", t/100, (t > 0) ? (t%100) : (-t%100));
 Serial.println("Pressure: %d.%d", p/100, p%100);
 ```
