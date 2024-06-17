---
icon: material/wifi
---

# Wi-Fi

!!! failure

    This page is under construction.

## Creating a Wi-Fi Access Point

```arduino
#include <WiFi.h>

void setup() {
  Serial.begin(115200);
  
  // Start the Access Point with a default SSID and password
  WiFi.softAP("ESP32_AP", "12345678");

  Serial.println("Access Point Started");
  Serial.print("IP Address: ");
  Serial.println(WiFi.softAPIP());
}

void loop() {
}
```

## Connecting to an Existing Access Point

```arduino
#include <WiFi.h>

const char* ssid = "<ssid>";
const char* password = "<password>";

void setup() {
  Serial.begin(115200);
  delay(10);

  Serial.print("Connecting to ");
  Serial.println(ssid);

  WiFi.begin(ssid, password);

  while (WiFi.status() != WL_CONNECTED) {
    delay(1000);
    Serial.print(".");
  }

  Serial.println("");
  Serial.println("WiFi connected.");
  Serial.println("IP address: ");
  Serial.println(WiFi.localIP());
}

void loop() {
}
```
