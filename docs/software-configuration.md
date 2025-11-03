---
sidebar_position: 5
---

# Software Flashing & Config

This section covers the firmware installation and parameter configuration for your WSPR Beakon system.

:::info Source Code Repository
The complete source code, libraries, and documentation for the WSPR Beakon project are available at:

**[https://github.com/danielcharrua/wspr-beakon](https://github.com/danielcharrua/wspr-beakon)**

Make sure to download or clone the repository to access all necessary files before proceeding with the installation.
:::

## Software Installation

### Prerequisites

1. Arduino IDE: Download and install from [arduino.cc](https://www.arduino.cc/en/software)
2. ESP32 Package: Install ESP32 support in Arduino IDE

### Arduino IDE Configuration

Configure Arduino IDE with the following settings:

- Board: ESP32 Dev Module
- Upload Speed: 921600
- CPU Frequency: 240MHz (WiFi/BT)
- Flash Frequency: 80MHz
- Flash Mode: QIO
- Flash Size: 4MB (32Mb)
- Partition Scheme: Default 4MB with spiffs
- Core Debug Level: None
- PSRAM: Disabled
- Programmer: Esptool

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src="/img/wspr-beakon-arduino-esp32-devkit-c-v4-config.png" alt="Arduino ESP32 Configuration" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Library Installation

1. Download all library ZIP files from the [GitHub repository lib/ folder](https://github.com/danielcharrua/wspr-beakon/tree/main/lib)
2. Copy the extracted folders to your Arduino libraries directory:
   - Windows: `Documents\Arduino\libraries\`
   - macOS: `~/Documents/Arduino/libraries/`
   - Linux: `~/Arduino/libraries/`

**Required libraries:**

- [Etherkit Si5351 (v2.1.4)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/Etherkit_Si5351-2.1.4.zip)
- [JTEncode (v1.2.0)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/JTEncode-1.2.0.zip)
- [LiquidCrystal I2C (v1.1.4)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/LiquidCrystal_I2C-1.1.4.zip)
- [NTPClient (v3.1.0)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/NTPClient-3.1.0.zip)
- [RotaryEncoder (v1.5.2)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/RotaryEncoder-1.5.2.zip)
- [Time (v1.5)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/Time-1.5.zip)
- [TinyGPSPlus (v1.1.0)](https://github.com/danielcharrua/wspr-beakon/raw/main/lib/TinyGPSPlus-1.1.0.zip)

### Firmware Upload

1. Connect your ESP32 to your computer via USB cable
2. Open `wspr-beakon.ino` in Arduino IDE
3. Configure the required parameters (see Configuration section below)
4. Select the correct COM port in Arduino IDE
5. Click "Upload" to flash the firmware

## Software Configuration

Before uploading the firmware, you must modify the configuration variables in the `USER CONFIGURATION` section of the code according to your chosen configuration:

### Development Mode Configuration

```cpp
#define DEVMODE // Serial port debug
```

:::warning Development Mode
- **Development**: Keep `#define DEVMODE` uncommented for debugging and troubleshooting
- **Production**: Comment out this line (`// #define DEVMODE`) for optimal performance in final deployment
:::

### Basic WSPR Configuration

```cpp
// WSPR transmitter configuration
#define WSPR_CALL "EA1REX"  // Your 4-6 character callsign
#define WSPR_LOC "IN53"     // Your 4-character grid locator
#define WSPR_DBM 20         // Power level shown in WSPR frame (0, 3, 7, 10 dBm)
#define WSPR_TX_EVERY 4     // Transmit every X minutes (2, 4, 6, 8, 10, etc.)
```

### Si5351 Power Level

```cpp
// Available options: SI5351_DRIVE_2MA, SI5351_DRIVE_4MA, SI5351_DRIVE_6MA, SI5351_DRIVE_8MA
// Power output (tested values): 2mA = 1mW, 4mA = 2mW, 6mA = 5mW, 8mA = 10mW
#define SI5351_DRIVE_LEVEL SI5351_DRIVE_4MA
```

### WiFi Networks Configuration

For **base configuration** (NTP synchronization):

```cpp
const WiFiNetwork wifiNetworks[] = {
  {"Your_SSID_1", "password1"},
  {"Your_SSID_2", "password2"},
  {"Your_SSID_3", "password3"}
};
```

### Band Configuration

Configure frequencies, crystal calibration, and relay pins for each band:

```cpp
} wsprFrequencies[] = {
  // Frequency(Hz), Crystal_Freq(Hz), Label, Relay_Pin
  {144489000UL, 25000000UL, "144.489 MHz 2m",  0},    // 2m band (not supported by the Si5351)
  {70105048UL,  25000000UL, "70.091 MHz 4m",   0},    // 4m band (not supported by the Si5351)
  {50303500UL,  25000000UL, "50.293 MHz 6m",   0},    // 6m band (not supported by the Si5351)
  {28131120UL,  25000000UL, "28.124 MHz 10m",  12},   // 10m band
  {24924600UL,  25000000UL, "24.924 MHz 12m",  12},   // 12m band
  {21099330UL,  25000000UL, "21.094 MHz 15m",  14},   // 15m band
  {18104600UL,  25000000UL, "18.104 MHz 17m",  14},   // 17m band
  {14099615UL,  25000000UL, "14.095 MHz 20m",  27},   // 20m band
  {10142033UL,  25000000UL, "10.138 MHz 30m",  27},   // 30m band
  {7041356UL,   25000000UL, "7.038 MHz 40m",   26},   // 40m band
  {5287200UL,   25000000UL, "5.287 MHz 60m",   26},   // 60m band
  {3570732UL,   25000000UL, "3.568 MHz 80m",   25},   // 80m band
  {1838426UL,   25000000UL, "1.836 MHz 160m",  33},   // 160m band
  {475786UL,    25000000UL, "0.474 MHz 630m",  32},   // 630m band
  {136000UL,    25000000UL, "0.136 MHz 2200m", 32}    // 2200m band
};
```

### Relay Pin Assignment

The following ESP32 pins are used for band relay control:

- **Pin 12**: 10m, 12m bands
- **Pin 14**: 15m, 17m bands  
- **Pin 25**: 80m band
- **Pin 26**: 40m, 60m bands
- **Pin 27**: 20m, 30m bands
- **Pin 32**: 630m, 2200m bands
- **Pin 33**: 160m band

:::warning Important Configuration Notes
1. **Initial Crystal Frequency**: For the first upload, set all crystal frequencies to `25000000UL` (25 MHz)
2. **Calibration Required**: After initial upload, you'll need to calibrate each band for frequency accuracy
3. **Custom Frequencies**: The provided frequencies are examples - you must calculate your own based on your specific Si5351 crystal
:::

:::danger Critical Post-Upload Step
**Very Important**: Once new code is uploaded to the ESP32, it is necessary to make a band selection using the encoder (see next section) for the microcontroller to initialize correctly. Otherwise, the assembly operation will be erratic.
:::
