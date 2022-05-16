# Practica-8-Rafael-Moncayo-Palate

## Codi de la pràctica 

```cpp

#include <Arduino.h>
 
 
void setup() {
 
 Serial.begin(115200);
  Serial2.begin(115200);
}
 
void loop() { //Choose Serial1 or Serial2 as required
 while (Serial.available()) {
   Serial2.print(char(Serial.read()));
 }
 while (Serial2.available()) {
   Serial.print(char(Serial2.read()));
 }
}

```

## Explicació de la pràctica.

Aquesta pràctica ens ajuda a entendre els busos de comunicació UART.
El codi comença amb un void setup amb 2 serial.begin(); perquè necessitarem 2 serials perquè es puguen comunicar entre ells. El primer serial és el que ens ajuda a escriure i el segon ens ajuda a llegir. En el loop tenim 2 whiles, el primer que ens ajuda a escriure através del segon serial el que li arribi al primer serial.read, amb la condició que el primer serial estiga disponible. I viceversa amb el segon while.
