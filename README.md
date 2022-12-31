# ATmega168P_Arduino_FSK_RFID_Reader  
clone and port to atmega168p, modified source code get rid of some memory constraints.    


source code copt from, https://gist.github.com/rgerganov/c8cec1f2c498c1e0786084bfdc1240b7  
design copy from, https://playground.arduino.cc/Main/DIYRFIDReader/  
it says GNU license  

uses Arduino IDE to complie, mini core used, add 168P support  
download and install the latest timerOne form github, Arduino library is not the latest one.  
https://github.com/PaulStoffregen/TimerOne  
install to C:\Users\user0\Documents\Arduino\libraries\TimerOne  
edit C:\Users\user0\Documents\Arduino\libraries\TimerOne\config\known_16bit_timers.h
add 168p support,  
```
//    Uno, Duemilanove, LilyPad, etc
//    Nano, some uses 168P , by xiaolaba
//    #elif defined (__AVR_ATmega168__) || (__AVR_ATmega168P__) || defined (__AVR_ATmega328P__) || defined (__AVR_ATmega328__) ||  defined (__AVR_ATmega8__)add atmega168P to support TIMER1_PINA

```

or copy [known_16bit_timers.h](known_16bit_timers.h) of this repo to patch.  

### testing done,
![burn_hex_ok.JPG](burn_hex_ok.JPG)  

### [143KHz_LC_tank_testing](143KHz_LC_tank_testing)  
![143KHz_LC_tank_testing/143KHZ_OSC.JPG](143KHz_LC_tank_testing/143KHZ_OSC.JPG)  
