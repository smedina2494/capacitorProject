#include <CapacitiveSensor.h>


CapacitiveSensor   bottomRight = CapacitiveSensor(3,2);        // 10M resistor between pins 3 & 2, pin 2 is sensor pin, add a wire and or foil if desired
CapacitiveSensor   bottomLeft = CapacitiveSensor(5,4);        // 10M resistor between pins 5 & 4, pin 4 is sensor pin, add a wire and or foil
CapacitiveSensor   topRight = CapacitiveSensor(7,6);        // 10M resistor between pins 7 & 6, pin 6 is sensor pin, add a wire and or foil
CapacitiveSensor   topLeft = CapacitiveSensor(10,9);        // 10M resistor between pins 10 & 9, pin 9 is sensor pin, add a wire and or foil
CapacitiveSensor   center = CapacitiveSensor(13,12);        // 10M resistor between pins 13 & 12, pin 12 is sensor pin, add a wire and or foil

void setup()                    
{
   bottomRight.set_CS_AutocaL_Millis(0xFFFFFFFF);     // turn off autocalibrate on channel 1 - just as an example
   Serial.begin(9600);
}

void loop()                    
{
    long start = millis();
    long total1 =  bottomRight.capacitiveSensor(30);
    long total2 =  bottomLeft.capacitiveSensor(30);
    long total3 =  topRight.capacitiveSensor(30);
    long total4 =  topLeft.capacitiveSensor(30);
    long total5 =  center.capacitiveSensor(30);

    Serial.print(millis() - start);        // check on performance in milliseconds
    Serial.print("\t");                    // tab character for debug windown spacing

    Serial.println(total1);                  // print sensor output 1
    Serial.print("\t");
    Serial.print(total2);                  // print sensor output 2
    Serial.print("\t");
    Serial.print(total3);                // print sensor output 3
    Serial.print("\t");
    Serial.print(total4);                // print sensor output 4
    Serial.print("\t");
    Serial.print(total5);                // print sensor output 5

    delay(10);                             // arbitrary delay to limit data to serial port 
}
