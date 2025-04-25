# Measure-Humidity-and-Temperature-using-DHT11

DHT11 Temperature & Humidity Monitoring with Blynk IoT

This project reads temperature and humidity data using a DHT11 sensor connected to an ESP8266 (NodeMCU) and sends the data to the Blynk IoT platform in real-time.

Components Used: 1.ESP8266 NodeMCU 2.DHT11 Temperature & Humidity Sensor 3.Wi-Fi connection 4.Blynk IoT App

Features:     Measures temperature and humidity every 15 seconds
              Displays live data on Blynk mobile dashboard (V0 → Temperature, V1 → Humidity)
              Serial Monitor prints sensor values for debugging

How to Use:       1.Connect DHT11's VCC, GND, and DATA to NodeMCU (e.g., DATA → D3).
                  2.Update Wi-Fi credentials and Blynk Auth Token in the code.
                  3.Upload the code to NodeMCU using Arduino IDE.
                  4.Open Blynk App, add two Value Display widgets (linked to V0 and V1).
                  5.Power up and monitor your environment remotely!
