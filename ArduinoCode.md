# SmartSwitchesArduino
This repository provides Arduino source code for running smart switches mobile app using HC-05 Bluetooth module. Connect relays coressponding to switches 1 and 2 on pin 13 and 12 respectively.


int state=0;
void setup() {
  // put your setup code here, to run once:
pinMode(13,OUTPUT);
pinMode (12,OUTPUT);
digitalWrite(13,LOW);
digitalWrite(12,LOW);
Serial.begin(9600);
}

void loop() {
  // put your main code here, to run repeatedly:
if (Serial.available()>0){
  state=Serial.read();
  Serial.println(state);
  if (state==65){digitalWrite(13,HIGH);
    }
  if (state==66){digitalWrite(13,LOW);}
  if (state==67){digitalWrite(12,HIGH);
    }
  if (state==68){digitalWrite(12,LOW);}}
