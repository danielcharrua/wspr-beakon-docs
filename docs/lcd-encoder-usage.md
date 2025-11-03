---
sidebar_position: 6
---

# LCD Display and Encoder Usage

This section covers the LCD display information and encoder operation for your WSPR Beakon system.

## System Startup Sequence

### Initial Boot Process

When power is applied to the assembly, the following sequence occurs:

- **"Connecting Wifi"** message appears on the LCD. If it cannot connect to any of the preconfigured WiFi networks, it will proceed to check the GPS signal
- **"Reading GPS"** message appears on the LCD. The system will alternate between both messages until it achieves a valid synchronization result

:::info GPS Signal Acquisition
GPS signal acquisition can take several minutes. For optimal performance:
- Position the assembly in a clear area with a wide view of the sky
- If using the integrated GPS antenna and the assembly is inside an enclosure, ensure the enclosure is made of non-metallic material
:::

### Connection Status Messages

- **"Wifi Connected" + "Reading GPS"**: Indicates a WiFi network is connected but has no internet access, preventing time calibration via WiFi
- **"Time not synced"**: Appears when the assembly has been trying to synchronize for more than half an hour without success via either WiFi or GPS

### Signal Testing Phase

Once a valid WiFi network or GPS signal is detected:
- LCD displays **"Testing signal"**
- Equipment begins a 30-second test transmission

## Normal Operation Display

### Information Display

After the test transmission, the LCD shows:

**Upper Line**: Scrolling message containing:
- Callsign
- Locator
- Frequency
- Band
- Transmitted power (in dBm)
- Configured time interval between transmissions

**Lower Line**: Numerical countdown showing time remaining until next WSPR transmission

### Transmission Sequence

1. **30 seconds before transmission**: System starts transmitting a warm-up carrier to stabilize the RF module temperature and frequency
2. **During WSPR transmission**: LCD displays **"Transmitting WSPR message"**
3. **After transmission**: Returns to scrolling information display and countdown timer

## Encoder Operation

### Band Selection Process

The rotary encoder is used to change bands and can only be operated during transmission rest periods:

1. **Press the encoder** - **"Select Freq"** message appears
2. **Rotate the encoder** - Navigate through available bands in either direction
3. **Press the encoder again** when desired band is displayed - **"Frequency Set"** message appears and new band is selected

:::warning Critical Reminder
**Always remember to insert the appropriate filter for the new band after changing frequency!**
:::

### Band Memory

- The last selected band is stored in memory when power is removed
- The system will start on the same band when power is restored

## Display Message Reference

| Message | Meaning |
|---------|---------|
| "Connecting Wifi" | Attempting to connect to preconfigured WiFi networks |
| "Reading GPS" | Attempting to acquire GPS signal |
| "Wifi Connected" + "Reading GPS" | WiFi connected but no internet access |
| "Time not synced" | Synchronization failed after 30+ minutes |
| "Testing signal" | Performing 30-second test transmission |
| "Transmitting WSPR message" | Active WSPR transmission in progress |
| "Select Freq" | Band selection mode active |
| "Frequency Set" | New band has been selected |

## Troubleshooting Display Issues

If the display shows unexpected behavior:
- Ensure proper power supply voltage
- Check LCD connections
- Verify encoder wiring
- Confirm system has been properly initialized after firmware upload