# PRACTICA-ESP32-con-DHT11
Este repositorio muestra como podemos programar una ESP32 con el sensor DHT11.

## INTRODUCCION

### DESCRIPCION

La Esp32 la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (DTH11) para adquirir temperatura y humedad del entorno; Cabe aclarar que esta practica se usara un simulador llamado WOKWI.

## MATERIAL NECESARIO

Para realizar esta practica necesitas lo siguiente:

-WOKWI

-Tarjeta ESP 32

-Sensor DHT11

## INSTRUCCIONES

### REQUISITOS PREVIOS

Para poder usar este repositorio necesitas entrar a la plataforma WOKWI.

### INSTRUCCIONES DE PREPARACION DE ENTORNO

1. Abrir la terminal de programación y colocar la siguente programación:

```
#include "DHTesp.h"

const int DHT_PIN = 15;
DHTesp dhtSensor;


void setup() {

  Serial.begin(115200);
  dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
  Serial.println("Temp: " + String(data.temperature, 1) + "°C");
  Serial.println("Humidity: " + String(data.humidity, 1) + "%");
  Serial.println("---");
  delay(1000);
}
```
2. Instalar la libreria de DHT sensor library for ESPx como se muestra en la siguente imagen.

![](https://github.com/OSCAROV2058/PRACTICA-ESP32-con-DHT11/blob/main/WhatsApp%20Image%202025-06-06%20at%208.06.19%20PM.jpeg?raw=true)

3. Hacer la conexion de DHT11 con la ESP32 como se muestra en la siguente imagen.

![](https://github.com/OSCAROV2058/PRACTICA-ESP32-con-DHT11/blob/main/WhatsApp%20Image%202025-06-06%20at%208.11.14%20PM.jpeg?raw=true)

### INSTRUCCIONES DE OPERACION

1. Iniciar simulador.
2. Visualizar los datos en el monitor serial.
3. Colocar la temperatura y humedad dando doble click al sensor DHT11.

## RESULTADOS

Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen.

![]()

EN ESTA PRACTICA UTILIZAREMOS EL SENSOR DHT11 PARA SIMULAR LA TEMPERATURA Y HUMEDAD DEL ENTORNO
