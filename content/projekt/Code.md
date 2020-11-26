---
title: "Code"
date: 2020-11-26T07:54:37+01:00
draft: false
---

## Programmcode

```c++
// http://arduino.esp8266.com/stable/package_esp8266com_index.json

/*** INCLUDES ***/
#include <DHT.h>
#include <Wire.h>
#include <Adafruit_BMP085.h>
#include <ESP8266WiFi.h>
#include <ESP8266HTTPClient.h>


/*** DEFINES ***/
#define DHTPIN 14
#define DHTTYPE DHT22
#define MQ5PIN A0

const char* ssid     = "INSERT_WLAN_SSID";
const char* password = "INSERT_WLAN_PASSWORD";
const int sensorMin = 0;
const int sensorMax = 1024;
Adafruit_BMP085 bmp;
DHT dht(DHTPIN, DHTTYPE);
long lastSensorRead;
long lastFireRead;
bool fireDetected = false;
bool fireReportSend = false;


/*** SETUP ***/
void setup() {

    // set serial for monitoring
    Serial.begin(9600);

    // WIFI Setup
    WiFi.begin(ssid, password);
    Serial.print("Connecting to ");
    Serial.print(ssid); Serial.println(" ...");

    int i = 0;
    while (WiFi.status() != WL_CONNECTED) {
        delay(1000);
        Serial.print(++i); Serial.print(' ');
    }

    Serial.println('\n');
    Serial.println("Connection established!");
    Serial.print("IP address:\t");
    Serial.println(WiFi.localIP());

    // MQ5 PIN
    pinMode(MQ5PIN, INPUT);

    // BMP start
    Wire.begin (13, 12);
    if(!bmp.begin()) {
        Serial.println("BMP Sensor konnte nicht gestartet werden!");
        return;
    }

    // DHT start
    dht.begin();

    // time init for sensor reads
    lastSensorRead = millis();
    lastFireRead = millis();
}


/*** LOOP ***/
void loop() {
    // Sensor Data every minute
    if (millis() - lastSensorRead >= 60000) {
        readValuesAndSendToServer();
    }

    // Fire every 5 seconds
    if (millis() - lastFireRead >= 5000) {
        fireDetection();
    }
}


/*** FIRE DETECTION ***/
void fireDetection() {
    int sensorReading = analogRead(4);
    Serial.println(sensorReading);
    if (!(sensorReading > 0)) {
        Serial.println("FEUER");
        fireDetected = true;
    } else {
      fireDetected = false;
      fireReportSend = false;
    }

    if(fireDetected && !fireReportSend) {
        Serial.println("Sende Feuermeldung an Server");

            /*** POST TO SERVER ***/

            //Check WiFi connection status
            if(WiFi.status()== WL_CONNECTED){
                HTTPClient http;

                char* serverName = "API_ROUTE_GOES_HERE";
                http.begin(serverName);

                http.addHeader("Content-Type", "application/json");
                int httpResponseCode = http.POST(POST_CONTENT_GOES_HERE);

                Serial.print("Serverantwort: ");
                Serial.println(httpResponseCode);

                http.end();
            } else {
                Serial.println("Nicht mit dem Internet verbunden");
            }

        fireReportSend = true;
    }

    lastFireRead = millis();
}


/*** SENSORS AND SERVER POST ***/
void readValuesAndSendToServer() {

    // get the gas value from the MQ5
    float gas_value = analogRead(MQ5PIN);
    Serial.print("Gas: ");
    Serial.println(gas_value);

    /*** DHT  ***/
    // read from the sensors
    float h = dht.readHumidity();
    float t = dht.readTemperature();

    // check if the values are correctly received
    if (isnan(h) || isnan(t)) {
        Serial.println("Fehler beim auslesen des Sensors!");
        return;
    }


    // BMP
    float pressure = bmp.readPressure();
    Serial.print("Luftdruck = ");
    Serial.print(pressure);
    Serial.print(" Pa");
    Serial.print("\t");

    Serial.print("Hoehe = ");
    Serial.print(bmp.readAltitude());
    Serial.println(" meters");


    // DHT
    Serial.print("Luftfeuchtigkeit: ");
    Serial.print(h);
    Serial.print("%\t");
    Serial.print("Temperatur: ");
    Serial.print(t);
    Serial.write("Grad");
    Serial.println("C");


    /*** POST TO SERVER ***/
    //Check WiFi connection status
    if(WiFi.status()== WL_CONNECTED){
        HTTPClient http;

        char* serverName = "API_ROUTE_GOES_HERE";
        http.begin(serverName);

        http.addHeader("Content-Type", "application/json");
        int httpResponseCode = http.POST(POST_CONTENT_GOES_HERE);

        Serial.print("Serverantwort: ");
        Serial.println(httpResponseCode);

        http.end();
    } else {
        Serial.println("Nicht mit dem Internet verbunden");
    }

    lastSensorRead = millis();
}
```
