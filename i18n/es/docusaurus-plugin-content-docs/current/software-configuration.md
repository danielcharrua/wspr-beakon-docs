---
sidebar_position: 5
---

# Flasheo y Configuración de Software

Esta sección cubre la instalación del firmware y la configuración de parámetros para tu sistema WSPR Beakon.

:::info Repositorio del Código Fuente
El código fuente completo, librerías y documentación para el proyecto WSPR Beakon están disponibles en:

**[https://github.com/danielcharrua/wspr-beakon](https://github.com/danielcharrua/wspr-beakon)**

Asegúrate de descargar o clonar el repositorio para acceder a todos los archivos necesarios antes de proceder con la instalación.
:::

## Instalación del Software

### Prerrequisitos

1. Arduino IDE: Descargar e instalar desde [arduino.cc](https://www.arduino.cc/en/software)
2. Paquete ESP32: Instalar soporte para ESP32 en Arduino IDE

### Configuración del Arduino IDE

Configura Arduino IDE con las siguientes opciones:

- Placa: ESP32 Dev Module
- Velocidad de Subida: 921600
- Frecuencia CPU: 240MHz (WiFi/BT)
- Frecuencia Flash: 80MHz
- Modo Flash: QIO
- Tamaño Flash: 4MB (32Mb)
- Esquema de Partición: Default 4MB with spiffs
- Nivel Debug Core: None
- PSRAM: Disabled
- Programador: Esptool

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-arduino-esp32-devkit-c-v4-config.png').default} alt="Configuración ESP32 Arduino" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Instalación de Librerías

1. Descarga todos los archivos ZIP de librerías desde la [carpeta lib/ del repositorio de GitHub](https://github.com/danielcharrua/wspr-beakon/tree/main/lib)
2. Copia las carpetas extraídas a tu directorio de librerías de Arduino:
   - Windows: `Documents\Arduino\libraries\`
   - macOS: `~/Documents/Arduino/libraries/`
   - Linux: `~/Arduino/libraries/`

**Librerías requeridas:**

- [Etherkit Si5351 (v2.1.4)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/Etherkit_Si5351-2.1.4.zip)
- [JTEncode (v1.2.0)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/JTEncode-1.2.0.zip)
- [LiquidCrystal I2C (v1.1.4)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/LiquidCrystal_I2C-1.1.4.zip)
- [NTPClient (v3.1.0)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/NTPClient-3.1.0.zip)
- [RotaryEncoder (v1.5.2)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/RotaryEncoder-1.5.2.zip)
- [Time (v1.5)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/Time-1.5.zip)
- [TinyGPSPlus (v1.1.0)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/TinyGPSPlus-1.1.0.zip)

### Subida del Firmware

:::warning Seguridad de Alimentación
Si estás alimentando el circuito desde una fuente externa, es **ALTAMENTE RECOMENDADO** que esta fuente se apague antes de conectar un PC al módulo ESP32. **NO HACERLO PUEDE DAÑAR IRREPARABLEMENTE EL PC.**
:::

1. Conecta tu ESP32 a tu computadora vía cable USB
2. Abre `wspr-beakon.ino` en Arduino IDE
3. Configura los parámetros requeridos (ver sección Configuración abajo)
4. Selecciona el puerto COM correcto en Arduino IDE
5. Haz clic en "Subir" para flashear el firmware

## Configuración del Software

Antes de subir el firmware, debes modificar las variables de configuración en la sección `USER CONFIGURATION` del código según tu configuración elegida:

### Configuración del Modo de Desarrollo

```cpp
#define DEVMODE // Debug del puerto serie
```

:::warning Modo de Desarrollo

- **Desarrollo**: Mantén `#define DEVMODE` descomentado para depuración y resolución de problemas
- **Producción**: Comenta esta línea (`// #define DEVMODE`) para rendimiento óptimo en despliegue final
:::

### Configuración Básica WSPR

```cpp
// Configuración del transmisor WSPR
#define WSPR_CALL "EA1REX"  // Tu indicativo de 4-6 caracteres
#define WSPR_LOC "IN53"     // Tu localizador de cuadrícula de 4 caracteres
#define WSPR_DBM 10         // Nivel de potencia mostrado en trama WSPR (0, 3, 7, 10 dBm)
#define WSPR_TX_EVERY 4     // Transmitir cada X minutos (2, 4, 6, 8, 10, etc.)
```

### Nivel de Potencia Si5351

```cpp
// Opciones disponibles: SI5351_DRIVE_2MA, SI5351_DRIVE_4MA, SI5351_DRIVE_6MA, SI5351_DRIVE_8MA
// Potencia de salida (valores probados): 2mA = 1mW, 4mA = 2mW, 6mA = 5mW, 8mA = 10mW
#define SI5351_DRIVE_LEVEL SI5351_DRIVE_4MA
```

### Configuración de Redes WiFi

Para **configuración base** (sincronización NTP):

```cpp
const WiFiNetwork wifiNetworks[] = {
  {"Tu_SSID_1", "contraseña1"},
  {"Tu_SSID_2", "contraseña2"},
  {"Tu_SSID_3", "contraseña3"}
};
```

:::info SSID
"Tu_SSID_1" es el nombre de tu red Wifi
:::

### Configuración de Bandas

Configura frecuencias, calibración del cristal y pines de relé para cada banda:

```cpp
} wsprFrequencies[] = {
  // Frecuencia(Hz), Freq_Cristal(Hz), Etiqueta, Pin_Relé
  {144489000UL, 25000000UL, "144.489 MHz 2m",  0},    // banda 2m (no soportada por el Si5351)
  {70105048UL,  25000000UL, "70.091 MHz 4m",   0},    // banda 4m (no soportada por el Si5351)
  {50303500UL,  25000000UL, "50.293 MHz 6m",   0},    // banda 6m (no soportada por el Si5351)
  {28131120UL,  25000000UL, "28.124 MHz 10m",  12},   // banda 10m
  {24924600UL,  25000000UL, "24.924 MHz 12m",  12},   // banda 12m
  {21099330UL,  25000000UL, "21.094 MHz 15m",  14},   // banda 15m
  {18104600UL,  25000000UL, "18.104 MHz 17m",  14},   // banda 17m
  {14099615UL,  25000000UL, "14.095 MHz 20m",  27},   // banda 20m
  {10142033UL,  25000000UL, "10.138 MHz 30m",  27},   // banda 30m
  {7041356UL,   25000000UL, "7.038 MHz 40m",   26},   // banda 40m
  {5364700UL,   25000000UL, "5.364 MHz 60m",   26},   // banda 60m
  {3570732UL,   25000000UL, "3.568 MHz 80m",   25},   // banda 80m
  {1838426UL,   25000000UL, "1.836 MHz 160m",  33},   // banda 160m
  {475786UL,    25000000UL, "0.474 MHz 630m",  32},   // banda 630m
  {136000UL,    25000000UL, "0.136 MHz 2200m", 32}    // banda 2200m
};
```

### Asignación de Pines de Relé

Los siguientes pines del ESP32 se usan para control de relés de banda:

- **Pin 12**: bandas 10m, 12m
- **Pin 14**: bandas 15m, 17m  
- **Pin 25**: banda 80m
- **Pin 26**: bandas 40m, 60m
- **Pin 27**: bandas 20m, 30m
- **Pin 32**: bandas 630m, 2200m
- **Pin 33**: banda 160m

:::warning Notas Importantes de Configuración

1. **Frecuencia Inicial del Cristal**: Para la primera subida, configura todas las frecuencias del cristal a `25000000UL` (25 MHz)
2. **Calibración Requerida**: Después de la subida inicial, necesitarás calibrar cada banda para precisión de frecuencia
3. **Frecuencias Personalizadas**: Las frecuencias proporcionadas son ejemplos - debes calcular las tuyas basadas en tu cristal Si5351 específico

:::

:::danger Paso Crítico Post-Subida
**Muy Importante**: Una vez que se sube el nuevo código al ESP32, es necesario hacer una selección de banda usando el encoder (ver siguiente sección) para que el microcontrolador se inicialice correctamente. De lo contrario, el funcionamiento del ensamblaje será errático.
:::