#include <Wire.h>
int x;
void setup()
{
  Serial.begin(9600);
  while (!Serial) {
    ; // wait for serial port to connect. Needed for Leonardo only
  }
  Wire.begin(); // join i2c bus (address optional for master)
  Wire.onReceive(handler);
  Wire.onRequest(handlerb);
}

void loop()
{
  Serial.print("I2Csend: ");
  Serial.println("0xC2 0x02 0x3C");
  Wire.beginTransmission(0x50); // transmit to device #4
  Wire.write(0xC2);
  Wire.write(0x02);
  Wire.write(0x3C);
  x=Wire.endTransmission();    // stop transmitting
  delay(200);
  Serial.print("x:\t");
  Serial.println(x);
    Wire.requestFrom(0x50, 8); 
 getData();
 
 Serial.print("I2Csend: ");
 Serial.println("0xCF ");
  Wire.beginTransmission(0x50); // transmit to device #4
  Wire.write(0xCF);
  x=Wire.endTransmission();    // stop transmitting
  delay(200);
  Serial.print("x:\t");
  Serial.println(x);
    Wire.requestFrom(0x50, 8); 
 getData();
 
 Serial.print("I2Csend: ");
 Serial.println("0x71 0x01 0x8E");
  Wire.beginTransmission(0x50); // transmit to device #4
  Wire.write(0x71);
  Wire.write(0x01);
  Wire.write(0x8E);
  x=Wire.endTransmission();    // stop transmitting
  delay(200);
  Serial.print("x:\t");
  Serial.println(x);
    Wire.requestFrom(0x50, 8); 
 getData();
  
  Serial.print("I2Csend: ");
  Serial.println("0x71 0x00 0x8F");
  Wire.beginTransmission(0x50); // transmit to device #4
  Wire.write(0x71);
  Wire.write(0x00);
  Wire.write(0x8F);
  x=Wire.endTransmission();    // stop transmitting
  delay(200);
  Serial.print("x:\t");
  Serial.println(x);
    Wire.requestFrom(0x50, 8); 
 getData();
 
 while(1);
}


void getData(){
  while(Wire.available())    // slave may send less than requested
  { 
    char c = Wire.read(); // receive a byte as character
    Print(c);
  }
   Serial.println(" ");
}

void Print(char ch){
  switch (ch){
      case  0x80:
        Serial.print("CMD_ACK");         // print the character
      break;
      case  0x82:
        Serial.print("CMD_NACK");         // print the character
      break;
      case  0x84:
        Serial.print("CMD_CSUM_ERR");         // print the character
      break;
    default:
        Serial.print(ch,HEX);         // print the character
      break; 
  }
  Serial.print(" ");
}

void handler(int numBytes){
  Serial.println("handler(int numBytes)");
}

void handlerb(){
  Serial.println("handlerb");
}
