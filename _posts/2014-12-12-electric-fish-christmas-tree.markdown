---
author: Jason Gallant
author_profile: true
comments: false
date: 2014-12-12 18:46:11+00:00
title: Electric Fish Christmas Tree
tags: [news, outreach, fun, lab]
---

Perhaps the nerdiest of all Christmas decorations I've ever put up, here is the official electric fish christmas tree!


This christmas tree is not "powered" by electric fish, rather it is controlled by an electric fish.  Weakly electric fish continuously produce pulses of electricity for communication and navigation in their environments-- every time the fish produces a pulse, the tree lights up.

This is done with a little RadioShack magic-- an Arduino board with a  relay shield is all you need!


(1) Arduino Uno (or equivalent)
(2) [Seed Studios Relay Shield](http://www.seeedstudio.com/wiki/Relay_Shield_V2.0)
(3) Old extension cable (two-prong)
(4) Amplifier & Electrode (great info [here](http://mormyrids.lifedesks.org/node/822) on some low cost DIY options )
(5) Code below (suggestions for improvement are welcome!)

Take an old indoor extension cable, and carefully splice it and connect one of the relays.  Next, a simple amplifier is connected to an electrode and dropped in the water with the electric fish.  The amplifier output is connected to the analog input pin and ground of the Arduino board.  Fire up your Arduino editor, and load the following code:




    /*
      Analog Input with prescale change (thanks to jmknapp)
      http://www.arduino.cc/cgi-bin/yabb2/YaBB.pl?num=1208715493/11
      Reading a 1 kHz sine wave, 0 to 5 volts
      Using analog 0
      Results stored in memory for highest speed
     */

    #define FASTADC 1
    // defines for setting and clearing register bits
    #ifndef cbi
    #define cbi(sfr, bit) (_SFR_BYTE(sfr) &= ~_BV(bit))
    #endif
    #ifndef sbi
    #define sbi(sfr, bit) (_SFR_BYTE(sfr) |= _BV(bit))
    #endif

    int value[5];   // variable to store the value coming from the sensor
    //int i=0;
    int relay_pin = 5;
    int randNumber;
    boolean relay_on = false; // the current state of the light

    void setup()
    {
     //Serial.begin(9600) ;
     int i ;
     pinMode(relay_pin, OUTPUT);
    #if FASTADC
      // set prescale to 16
      sbi(ADCSRA,ADPS2) ;
      cbi(ADCSRA,ADPS1) ;
      cbi(ADCSRA,ADPS0) ;
    #endif
    }

    void loop()
    {
      int value=analogRead(0);
      digitalWrite(relay_pin, relay_on);
      //float voltage = sensorValue * (5.0 / 1023.0);
      if (value > 3) {
        relay_on= !relay_on;
    }   
    }
