# Measure-Humidity-and-Temperature-using-DHT11
#define BLYNK_TEMPLATE_ID "TMPL8exwnkQi"
#define BLYNK_DEVICE_NAME "sensor data publish"
#define BLYNK_AUTH_TOKEN "qSfVTm7xAvZ8cvGrwFjVg1vENozMN0hC"


#define BLYNK_PRINT Serial
#include <ESP8266WiFi.h>
#include <BlynkSimpleEsp8266.h>
#include <DHT.h>

char auth[] = BLYNK_AUTH_TOKEN;

char ssid[] = "bandhu@PC";  // type your wifi name
char pass[] = "JoyNetai@67";  // type your wifi password

DHT dht;

void setup(){
Serial.begin(9600);
Blynk.begin(auth, ssid, pass);
dht.setup(D3);

}
void loop(){
  
float Temperature = dht.getTemperature();/* Get temperature value */
float Humidity = dht.getHumidity();/* Get humidity value */

Serial.println(Temperature);
Serial.println(Humidity);

  Blynk.virtualWrite(V1,Humidity );
  Blynk.virtualWrite(V0,Temperature );

delay(15000);
  Blynk.run();
  }
