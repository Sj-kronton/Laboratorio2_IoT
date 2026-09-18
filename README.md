# Curso: IoT + Cloud + Sistemas Distribuidos Integrantes:

Juan Alejandro Sierra — U00178520
Maria Herrera — U00173188

Repositorio del Laboratorio 2: extensión de la flota del Laboratorio 1 a 8 dispositivos bajo una misma plantilla de Azure IoT Central ("Sensores de calidad del paciente"), incorporando dos nodos de generación de datos por código propio: un script en Python ejecutado en una máquina virtual y un firmware para ESP32 simulado en Wokwi.


## Inventario de la flota
        Dispositivo	Tipo	Origen del dato	Variables
* 1-6	Sim-01 … Sim-06	Simulado nativo	Motor de simulación de IoT Central	HeartRate, Temperature, SPO2, BreathRate
* 7	Sensores de calidad del paciente - físico	Python en VM (Azure)	IoTCentralSender.py	HeartRate, Temperature, SPO2
* 8	65sxptcib	ESP32 (Wokwi)	Sensor virtual DHT22 + lógica propia	Temperature, HeartRate, BreathRate + comando setAlertLed

## Estructura del repositorio
.
├── README.md                     # Este archivo
│── IoTCentralSender.py        # Script de telemetría ejecutado en la VM
├── README.md                  # Instrucciones de despliegue en la VM
├── main.py                    # Firmware del ESP32 (MicroPython)
├── diagram.json               # Diagrama del circuito (ESP32 + DHT22)
└── evidencias/
    └── Fotos
