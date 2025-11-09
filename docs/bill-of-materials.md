---
sidebar_position: 2
---

# Bill of Materials

:::info
For convenience, pre-selected component kits are available to simplify the build process. See [Kit Options](/docs/kit-options) for details. This helps ensure you have all compatible parts, even if some individual links become outdated over time.
:::

The WSPR Beakon is designed as a modular system with different configuration flavors to suit various needs and capabilities. Before beginning assembly, review the available flavors and select the components needed for your chosen configuration.

## Core Configuration Components

The most basic version is powered from the USB connector of the ESP32 module and contains everything essential to operate the transmitter. For this basic version, the following elements are needed:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-base.webp').default} alt="WSPR Beakon PCB Core" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Visual Identification of Core Components

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-pcb.webp').default} alt="Main PCB" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Main PCB</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-esp32.webp').default} alt="ESP32 Dev Kit C V4" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>ESP32 Dev Kit C V4</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-si5351.webp').default} alt="Si5351 RF Module" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Si5351 RF Module</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-encoder-hw40.webp').default} alt="Rotary Encoder HW-40" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Rotary Encoder HW-40</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-lcd-1602-i2c.webp').default} alt="LCD Display 16x2 I2C" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>LCD Display 16x2 I2C</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-ceramic-capacitor.webp').default} alt="Ceramic Capacitor" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Ceramic Capacitor</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-electrolitic-capacitor.webp').default} alt="Electrolytic Capacitor" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Electrolytic Capacitor</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-resistor.webp').default} alt="Resistors 100Ω" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Resistors 100Ω</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-dupont-cable-fem-fem.webp').default} alt="Dupont Cables" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Dupont Cables</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-4-pin.webp').default} alt="4-pin Female Socket" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>4-pin Female Socket</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-7-pin.webp').default} alt="7-pin Female Socket" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>7-pin Female Socket</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-19-pin.webp').default} alt="19-pin Female Socket" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>19-pin Female Socket</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-male-4-pin.webp').default} alt="4-pin Male Header" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>2.54 Male Header</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screw-separators.webp').default} alt="Metal Standoffs" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Metal Standoffs</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screws.webp').default} alt="Screws M2.5" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Screws M2.5</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-filter-pcbs.webp').default} alt="Filter PCB" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Filter PCB</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-axial-inductor.webp').default} alt="Filter Inductors" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Filter Inductors</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-ceramic-capacitor-1.webp').default} alt="Filter Capacitors" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Filter Capacitors</div>
  </div>
</div>

### Detailed Table of Core Components

| Component | Qty | Notes | Link |
|-----------|-----|-------|------|
| **Main PCB** | 1 | Gerber file provided for manufacturing | [Download](https://github.com/danielcharrua/wspr-beakon/tree/main/pcb) |
| **ESP32 Dev Kit C V4** | 1 | 38 pins, Type C | [AliExpress](https://es.aliexpress.com/item/1005007820190456.html) |
| **Si5351 RF Module** | 1 | | [AliExpress](https://es.aliexpress.com/item/1005006233803174.html) |
| **Rotary Encoder HW-40** | 1 | | [AliExpress](https://es.aliexpress.com/item/1005006771313967.html) |
| **LCD Display** | 1 | 16x2 I2C | [AliExpress](https://es.aliexpress.com/item/1005006100081942.html) |
| **Ceramic Capacitor** | 1 | 100nF 50V, non-critical values | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=213004009&cPath=952) |
| **Electrolytic Capacitor** | 1 | 1000μF 25V, non-critical values | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=211004075&cPath=968) |
| **Resistors** | 3 | 100Ω 1W | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=514310001&cPath=921) |
| **Dupont Cables** | 9 | Female-female, for LCD and encoder | [AliExpress](https://es.aliexpress.com/item/1005006263457745.html) |
| **4-pin Female Socket** | 2 | | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **7-pin Female Socket** | 1 | | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **19-pin Female Socket** | 2 | | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **4-pin Male Header** | 1 | Cut to size | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |
| **5-pin Male Header** | 1 | Cut to size | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |
| **Metal Standoffs** | 7 | M2.5 x 11mm female-female | [AliExpress](https://es.aliexpress.com/item/1005001478301407.html) |
| **Screws** | 14 | M2.5 x 5mm | [AliExpress](https://es.aliexpress.com/item/1005006674754845.html) |
| **Filter PCB** | As needed | PCB has 10 units to cut, minimum 1 needed | [Download](https://github.com/danielcharrua/wspr-beakon/tree/main/pcb) |
| **Filter Inductors** | As needed | Axial, according to band choice | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=999208848&cPath=1335) |
| **Filter Capacitors** | As needed | According to band choice | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=213004001&cPath=952) |

:::warning Important Note about Filter Components
The filter inductors and capacitors values depend on the specific amateur radio band you plan to use for WSPR transmission. Before purchasing these components, please refer to the technical documentation included with the project to determine the exact values needed for your chosen frequency band. See the section [Filter Design and Values](/docs/filters) for details.
:::

## Enhancement 1: GPS

With this upgrade we provide the capability to not depend on a WiFi network for precise time synchronization of the assembly, as a GPS module is added that has an integrated antenna, in addition to an SMA-type input for an external antenna. If you want to use it with the integrated antenna, obviously the box where the assembly is located cannot be metallic. For this enhancement, the following elements need to be added:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-gps.webp').default} alt="WSPR Beakon PCB GPS" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Visual Identification of GPS Components

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-gps-neo-7m.webp').default} alt="GPS Module NEO-7M" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>GPS Module NEO-7M</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-5-pin.webp').default} alt="5-pin Female Socket" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>5-pin Female Socket</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screw-separators.webp').default} alt="Metal Standoffs" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Metal Standoffs</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screws.webp').default} alt="Screws M2.5" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Screws M2.5</div>
  </div>
</div>

### Detailed Table of GPS Components

| Component | Qty | Notes | Link |
|-----------|-----|-------|------|
| **GPS Module NEO-7M** | 1 | With integrated antenna and SMA connector for external antenna | [AliExpress](https://es.aliexpress.com/item/1005006152967959.html) |
| **5-pin Female Socket** | 1 | For the new GPS module | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **Metal Standoffs** | 2 | M2.5 x 11mm female-female, for securing main board to case and RF module board over main board | [AliExpress](https://es.aliexpress.com/item/1005001478301407.html) |
| **Screws** | 4 | M2.5 x 5mm for metal standoffs | [AliExpress](https://es.aliexpress.com/item/1005006674754845.html) |

## Enhancement 2: 12V Power Supply

With this upgrade we provide the capability to power the circuit at 12 (or 13.8) volts, such as with one of the power supplies normally found in the radio room. For this enhancement, the following elements need to be added:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-12v.webp').default} alt="WSPR Beakon PCB 12V" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Visual Identification of 12V Power Supply Components

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-diode.webp').default} alt="Diode 1N5819" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Diode 1N5819</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-buck-converter.webp').default} alt="Buck DC-DC Converter" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Buck DC-DC Converter</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-dupont-cable-fem-fem.webp').default} alt="Dupont Cables" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Dupont Cables</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-4-pin.webp').default} alt="4-pin Female Socket" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>4-pin Female Sockets</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-male-pin.webp').default} alt="2-pin Male Header Strip" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>2.54 Male Header Strip</div>
  </div>
</div>

### Detailed Table of 12V Power Supply Components

| Component | Qty | Notes | Link |
|-----------|-----|-------|------|
| **Diode 1N5819** | 1 | Schottky diode for polarity protection | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=71-1N5819&cPath=970) |
| **Buck DC-DC Converter** | 1 | DC-DC 5V output converter | [AliExpress](https://es.aliexpress.com/item/1005008678729834.html) |
| **Dupont Cables** | 2 | With female end for 12V input wiring to main board | [AliExpress](https://es.aliexpress.com/item/1005006263457745.html) |
| **4-pin Female Sockets** | 2 | | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **1-pin Male Headers** | 4 | Cut to size | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |
| **2-pin Male Header Strip** | 1 | Cut to size | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |

## Enhancement 3: External Filter Bank

To enable this enhancement, we must have previously implemented enhancement number 2. With this improvement we incorporate seven relay outputs (high level, 12 volts) configurable according to the working band (pins marked as 12, 14, 27, 26, 25, 33 and 32), and an eighth relay output (pin marked as 13) controlled by the TX periods of the circuit and which is "sequenced" to avoid switching with RF (it goes high level, 12 volts, half a second before going to TX and goes low level half a second after TX ceases). For this enhancement, the following elements need to be added:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-ext-filters.webp').default} alt="WSPR Beakon PCB Filter" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Visual Identification of External Filter Bank Components

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-udn2981.webp').default} alt="UDN2981 IC" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>UDN2981 IC</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-ic-socket-18pin.webp').default} alt="18-pin IC Socket" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>18-pin IC Socket</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-dupont-cable-fem-fem.webp').default} alt="Dupont Cables" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Dupont Cables</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-male-pin.webp').default} alt="2.54 Male Header Strip" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>8-pin Male Header Strip</div>
  </div>
</div>

### Detailed Table of External Filter Bank Components

| Component | Qty | Notes | Link |
|-----------|-----|-------|------|
| **UDN2981 IC** | 1 | 8-channel driver integrated circuit | [AliExpress](https://es.aliexpress.com/item/1005006888538620.html) |
| **18-pin IC Socket** | 1 | For the UDN2981 integrated circuit | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=999127304&cPath=1380) |
| **Dupont Cables** | 8 | With female end for wiring outputs to external relays | [AliExpress](https://es.aliexpress.com/item/1005006263457745.html) |
| **Extra Ground Dupont Cables** | 4 | Optional, with female end for ground connections to external peripherals | [AliExpress](https://es.aliexpress.com/item/1005006263457745.html) |
| **8-pin Male Header Strip** | 1 | For relay outputs, cut to size | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |
| **4-pin Male Header Strip** | 1 | Optional, for common ground connection to external peripherals, cut to size | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |

### Other Possible Improvements for Experimenter Investigation

Taking advantage of the seven available relay outputs (high level, 12 volts) that are activated according to the configured working band, an external filter bank could be made automatically switchable, so that when a band is chosen in the menu, the corresponding filter is selected. These relay outputs could also be used to automatically handle an antenna switch for different bands.

The eighth available relay output, controlled by TX/RX changes, could be used to route the antenna to an external receiver during TX idle moments (in this case, the isolation of said relay must be taken into account so as not to "fry" the receiver when the transmitter is running); this last relay output could also be used as an external PTT to handle any peripheral that needs this signal.

The WSPR mode is highly efficient and requires very little power, but if you want to use it with more energy, you could experiment, for example, with one of the popular broadband amplifier modules that come from Asia and have high gain (between 30 and 40 dB), being capable of delivering between 1.5 and 2 watts of output power; even so, and in view of some tests carried out, it is strongly recommended to use it at a conservative level, say about 300-400 milliwatts maximum, being more than sufficient power in WSPR for most circumstances and which results in cleaner output; as an advantage, at that power level, the module is very tolerant of moderately mismatched antennas, if that were the case.

It should be added that these amplifiers have uneven gain on different bands, so the use of a variable attenuator between the assembly described here and the amplifier itself is highly recommended in order to unify, and keep within reasonable margins, the output power if multiband use is to be made of it.

:::warning Mandatory Low-Pass Filter Requirement
The amplifier must OBLIGATORILY be connected at its output to a low-pass filter, which can be external or can be the one integrated in the board by doing a slight rewiring of the RF part. This is essential to prevent spurious emissions and ensure proper operation.
:::

The filters described later have been used for days at 500 milliwatt output regimes without observing heating or deterioration in their response curve.

## 3D Printed Enclosure for Core System

A custom 3D printed enclosure is available for the basic WSPR Beakon core system. This enclosure provides professional appearance and protection while maintaining easy access to all controls and connections.

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-core-7.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Visual Identification of 3D Case Components

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-3d-case.webp').default} alt="3D Printed Case" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>3D Printed Case</div>
    <div style={{fontSize: '13px', color: '#666'}}>STL files available</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-insert.webp').default} alt="Threaded Inserts M2.5" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Threaded Inserts M2.5</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-so-239.webp').default} alt="SO-239 Connector" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>SO-239 Connector</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-rg-316.webp').default} alt="Coaxial Cable" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Coaxial Cable</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screws.webp').default} alt="M2.5 x 5mm Screws" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>M2.5 x 5mm Screws</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screws-m3.webp').default} alt="M3 x 8mm Screws" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>M3 x 8mm Screws</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-nuts-m3.webp').default} alt="M3 Nuts" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>M3 Nuts</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-ground-terminal.webp').default} alt="Ground Terminal" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Ground Terminal</div>
  </div>
</div>

### Detailed Table of 3D Case Components

| Component | Qty | Notes | Link |
|-----------|-----|-------|------|
| **3D Printed Case** | 1 | STL files available for download | [Download](https://github.com/danielcharrua/wspr-beakon/tree/main/3D) |
| **Threaded Inserts M2.5** | 13 | 5mm length, for melting into plastic | [AliExpress](https://es.aliexpress.com/item/1005007653131713.html) |
| **SO-239 Connector** | 1 | 4-hole panel mount type | [AliExpress](https://es.aliexpress.com/item/1005004896899844.html) |
| **Coaxial Cable** | 1 | RG316 or similar, 10-15cm length for internal RF connection | [AliExpress](https://es.aliexpress.com/item/1005003618138960.html) |
| **M2.5 x 5mm Screws** | 13 | For use with threaded inserts | [AliExpress](https://es.aliexpress.com/item/1005006674754845.html) |
| **M3 x 8mm Screws** | 4 | For SO-239 connector mounting | [AliExpress](https://es.aliexpress.com/item/1005006674754845.html) |
| **M3 Nuts** | 4 | For SO-239 connector securing | [AliExpress](https://es.aliexpress.com/item/1005006470779106.html) |
| **Ground Terminal** | 1 | 3mm screw type for coaxial shield connection | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=999208192&cPath=1162) |