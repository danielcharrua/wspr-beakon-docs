---
sidebar_position: 4
---

# Filters

This section covers the design, construction, and tuning of filters for your WSPR Beakon system.

## Filter Design Philosophy

Since operation will be conducted at very low power, we attempted to build filters with common and inexpensive components: axial inductors (their appearance is similar to resistors with a green body) and normal low-voltage capacitors (50 volts). We believed that avoiding the need to wind toroids and obtaining high-quality NP0 type capacitors (which is obviously a better option) would make the construction of these filters more feasible for a wider audience. This does not prevent the same support (PCB) from being used to build them with higher quality components than those proposed here.

Several filter units were built for each band, verifying that in most cases they are replicable without major modifications; logically this will depend on the tolerance of the different components and in some cases fine adjustment may be necessary, generally by varying the value of some capacitor, and especially for centering the working frequency of units that incorporate notch filters; adjustment of the center frequency of these "notch" filters is much faster and simpler if an adjustment trimmer with a value slightly higher than that of the corresponding fixed capacitor(s) is used, which it would replace. Its use is therefore recommended (see the "Notes" section in the filter components table).

## Mandatory Testing Requirements

It should be emphasized that the component table for each filter is only a starting point, so each constructed unit must be **OBLIGATORILY VERIFIED** individually with measuring equipment, for example a nanoVNA, in order to verify that:

- The **second harmonic** (double frequency of the one to be used) is at a level between **35 and 40 dB below** the level of the use frequency
- The **third harmonic** (triple frequency of the one to be used) is between **45 and 50 dB below** the level of the use frequency
- Frequencies higher than the third harmonic should also be maintained at around **50 dB (or more) below** the level of the use frequency

:::warning Filter Verification Required
Each filter unit must be individually tested and verified with appropriate measuring equipment before use. The component values provided are starting points and may require adjustment for optimal performance.
:::

## HF Filter Component Values

The component values that will be used as starting points for the construction of the different HF filters are as follows:

<table>
  <thead>
    <tr>
      <th rowspan="2">BAND</th>
      <th colspan="4" style={{backgroundColor: '#e6f6e6'}}>INDUCTORS (μH)</th>
      <th colspan="7" style={{backgroundColor: '#eef9fd'}}>CAPACITORS (pF)</th>
      <th rowspan="2">FILTER TYPE NOTES</th>
    </tr>
    <tr>
      <th style={{backgroundColor: '#e6f6e6'}}>L1</th>
      <th style={{backgroundColor: '#e6f6e6'}}>L2</th>
      <th style={{backgroundColor: '#e6f6e6'}}>L3</th>
      <th style={{backgroundColor: '#e6f6e6'}}>L4</th>
      <th style={{backgroundColor: '#eef9fd'}}>C1</th>
      <th style={{backgroundColor: '#eef9fd'}}>C2</th>
      <th style={{backgroundColor: '#eef9fd'}}>C3</th>
      <th style={{backgroundColor: '#eef9fd'}}>C4</th>
      <th style={{backgroundColor: '#eef9fd'}}>C5</th>
      <th style={{backgroundColor: '#eef9fd'}}>C6</th>
      <th style={{backgroundColor: '#eef9fd'}}>C7</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>10M</strong></td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.33</td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.33</td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.47</td>
      <td style={{backgroundColor: '#e6f6e6'}}>-</td>
      <td style={{backgroundColor: '#eef9fd'}}>100</td>
      <td style={{backgroundColor: '#eef9fd'}}>220</td>
      <td style={{backgroundColor: '#eef9fd'}}>100</td>
      <td style={{backgroundColor: '#eef9fd'}}>15</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td>5-pole with notch. The 15 pF C can be substituted by a trimmer for fine adjustment of the 56.3 MHz notch</td>
    </tr>
    <tr>
      <td><strong>15M</strong></td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.47</td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.47</td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.47</td>
      <td style={{backgroundColor: '#e6f6e6'}}>-</td>
      <td style={{backgroundColor: '#eef9fd'}}>120</td>
      <td style={{backgroundColor: '#eef9fd'}}>22</td>
      <td style={{backgroundColor: '#eef9fd'}}>270</td>
      <td style={{backgroundColor: '#eef9fd'}}>120</td>
      <td style={{backgroundColor: '#eef9fd'}}>27</td>
      <td style={{backgroundColor: '#eef9fd'}}>1</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td>5-pole with notch. Initial capacitance formed by two capacitors in parallel. The 27 pF + 1 pF C can be substituted by a single trimmer for fine adjustment of the 42.2 MHz notch</td>
    </tr>
    <tr>
      <td><strong>20M</strong></td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.68</td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.47</td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.47</td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.68</td>
      <td style={{backgroundColor: '#eef9fd'}}>18</td>
      <td style={{backgroundColor: '#eef9fd'}}>1.2</td>
      <td style={{backgroundColor: '#eef9fd'}}>220</td>
      <td style={{backgroundColor: '#eef9fd'}}>470</td>
      <td style={{backgroundColor: '#eef9fd'}}>220</td>
      <td style={{backgroundColor: '#eef9fd'}}>39</td>
      <td style={{backgroundColor: '#eef9fd'}}>5.6</td>
      <td>5-pole with 2 notches. The 18 pF + 1.2 pF C can be substituted by a single trimmer for fine adjustment of the 42.28 MHz notch. The 39 pF + 5.6 pF C can be substituted by a single trimmer for fine adjustment of the 28.19 MHz notch</td>
    </tr>
    <tr>
      <td><strong>40M</strong></td>
      <td style={{backgroundColor: '#e6f6e6'}}>1.5</td>
      <td style={{backgroundColor: '#e6f6e6'}}>1</td>
      <td style={{backgroundColor: '#e6f6e6'}}>0.68</td>
      <td style={{backgroundColor: '#e6f6e6'}}>1.5</td>
      <td style={{backgroundColor: '#eef9fd'}}>270</td>
      <td style={{backgroundColor: '#eef9fd'}}>680</td>
      <td style={{backgroundColor: '#eef9fd'}}>680</td>
      <td style={{backgroundColor: '#eef9fd'}}>270</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td>7-pole, with central inductance formed by two inductors in series</td>
    </tr>
    <tr>
      <td><strong>80M</strong></td>
      <td style={{backgroundColor: '#e6f6e6'}}>1</td>
      <td style={{backgroundColor: '#e6f6e6'}}>2.2</td>
      <td style={{backgroundColor: '#e6f6e6'}}>2.2</td>
      <td style={{backgroundColor: '#e6f6e6'}}>2.2</td>
      <td style={{backgroundColor: '#eef9fd'}}>220</td>
      <td style={{backgroundColor: '#eef9fd'}}>12</td>
      <td style={{backgroundColor: '#eef9fd'}}>680</td>
      <td style={{backgroundColor: '#eef9fd'}}>1500</td>
      <td style={{backgroundColor: '#eef9fd'}}>680</td>
      <td style={{backgroundColor: '#eef9fd'}}>220</td>
      <td style={{backgroundColor: '#eef9fd'}}>18</td>
      <td>5-pole with 2 notches. The 12 pF C can be substituted by a trimmer for fine adjustment of the 10.7 MHz notch. The 18 pF C can be substituted by a trimmer for fine adjustment of the 7.14 MHz notch</td>
    </tr>
    <tr>
      <td><strong>160M</strong></td>
      <td style={{backgroundColor: '#e6f6e6'}}>8.2</td>
      <td style={{backgroundColor: '#e6f6e6'}}>4.7</td>
      <td style={{backgroundColor: '#e6f6e6'}}>5.6</td>
      <td style={{backgroundColor: '#e6f6e6'}}>4.7</td>
      <td style={{backgroundColor: '#eef9fd'}}>220</td>
      <td style={{backgroundColor: '#eef9fd'}}>820</td>
      <td style={{backgroundColor: '#eef9fd'}}>2200</td>
      <td style={{backgroundColor: '#eef9fd'}}>2200</td>
      <td style={{backgroundColor: '#eef9fd'}}>820</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td style={{backgroundColor: '#eef9fd'}}>-</td>
      <td>7-pole with notch. The 220 pF C adjusts the 3.67 MHz notch</td>
    </tr>
  </tbody>
</table>

### Component Notes

- **Inductors**: Axial inductors with green body (similar appearance to resistors)
- **Capacitors**: Normal low-voltage capacitors (50V rating)
- **Trimmers**: Can be substituted for specific capacitors to allow fine-tuning of notch frequencies
- **Series/Parallel combinations**: Some values are achieved by combining multiple components

:::info Trimmer Recommendations
For easier adjustment of notch frequencies, consider using trimmer capacitors with values slightly higher than the fixed capacitor(s) they replace. This allows for precise frequency centering during testing.
:::

## Component Sourcing

Please see the [BOM table at the bottom](/docs/bill-of-materials#detailed-table-of-core-components).

## Component Placement and PCB Layout

The position of each component on the different filter boards is as follows:

<table>
  <thead>
    <tr>
      <th>BAND</th>
      <th>Top Side</th>
      <th>Bottom Side</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>10M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-10m-t.webp').default} alt="10M Filter - Top Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-10m-b.webp').default} alt="10M Filter - Bottom Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>15M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-15m-t.webp').default} alt="15M Filter - Top Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-15m-b.webp').default} alt="15M Filter - Bottom Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>20M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-20m-t.webp').default} alt="20M Filter - Top Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-20m-b.webp').default} alt="20M Filter - Bottom Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>40M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-40m-t.webp').default} alt="40M Filter - Top Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-40m-b.webp').default} alt="40M Filter - Bottom Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>80M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-80m-t.webp').default} alt="80M Filter - Top Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-80m-b.webp').default} alt="80M Filter - Bottom Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>160M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-160m-t.webp').default} alt="160M Filter - Top Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-160m-b.webp').default} alt="160M Filter - Bottom Side" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
  </tbody>
</table>

## Component Identification Guide

For greater clarity of assembly, the usual identification of the different components that make up the filters is provided:

### Component Identification Table

<table>
  <thead>
    <tr>
      <th colspan="2" style={{textAlign: 'center'}}>AXIAL INDUCTORS</th>
      <th colspan="2" style={{textAlign: 'center'}}>CAPACITORS</th>
    </tr>
    <tr>
      <th style={{backgroundColor: '#e6f6e6'}}>VALUE</th>
      <th style={{backgroundColor: '#e6f6e6'}}>COLOR BANDS</th>
      <th style={{backgroundColor: '#eef9fd'}}>VALUE</th>
      <th style={{backgroundColor: '#eef9fd'}}>SILKSCREEN</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>0.33 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>ORANGE - ORANGE - SILVER - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>1 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>1.0 or 1p0</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>0.47 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>YELLOW - VIOLET - SILVER - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>1.2 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>1.2 or 1p2</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>0.68 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>BLUE - GRAY - SILVER - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>5.6 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>5.6 or 5p6</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>1 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>BROWN - BLACK - GOLD - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>12 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>12</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>1.5 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>BROWN - GREEN - GOLD - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>15 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>15</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>2.2 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>RED - RED - GOLD - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>18 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>18</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>4.7 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>YELLOW - VIOLET - GOLD - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>22 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>22</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>5.6 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>GREEN - BLUE - GOLD - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>27 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>27</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>8.2 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>GRAY - RED - GOLD - SILVER</td>
      <td style={{backgroundColor: '#eef9fd'}}>39 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>39</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>100 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>101 or n10</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>120 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>121 or n12</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>220 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>221 or n22</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>270 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>271 or n27</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>470 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>471 or n47</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>680 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>681 or n68</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>820 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>821 or n82</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>1500 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>152 or 1n5</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>2200 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>222 or 2n2</td>
    </tr>
  </tbody>
</table>

## Filter PCB Design and Construction

The proposed PCB, for which a Gerber file link is provided for downloading and ordering manufacturing ([see the BOM table at the bottom](/docs/bill-of-materials#detailed-table-of-core-components)), consists of 10 mini boards (which must be cut with a saw) for 10 possible filters. The design took into account that it should be a very versatile board and could contain 5 or 7-pole filters, even with some "notch" associated with a specific frequency. The chosen format is for "Manhattan" style construction (components soldered on "islands") due to the enormous flexibility of design and type of component that can be used.

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-pcb.webp').default} alt="filters PCBs" style={{maxWidth: '450px', width: '100%'}} />
</div>

## Filter Installation and Connection

Filter boards are connected to the main assembly board via insertable pins, making them very easily interchangeable. A good way to ensure these pins are well aligned when soldering and that the boards can then be easily exchanged is to follow these steps:

1. **Socket Installation**: Solder the two 4-pin female sockets on the main board, pressing them against the board during soldering so they are properly seated and form 90 degrees with respect to the board

2. **Pin Insertion**: Insert the two 4-pin male strips, through their long side, onto the female sockets already soldered

3. **Filter Board Mounting**: Place the filter board on the male pin strips (careful: check that the "IN" and "OUT" silkscreen of the filter board faces up and matches the "RFIN" and "RFOUT" silkscreen of the main board), ensuring it seats properly and proceed to solder the eight male pins to the filter board

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-filters-1.webp').default} alt="Filter Installation and Connection" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-filters-2.webp').default} alt="Filter Installation and Connection" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-filters-3.webp').default} alt="Filter Installation and Connection" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-filters.webp').default} alt="Filter Installation and Connection" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

## Alternative SMA Connector Configuration

Although the filter boards were initially designed to be used in this project and connected via pin strips, the arrangement of the "ground" and "RF" tracks allows for soldering SMA connectors for 1.6mm circuit boards (which require cutting two of their four "ground" pins) and thus be able to use them in any other project that requires this type of connectors.

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-calibration-1.webp').default} alt="Filter calibration" style={{maxWidth: '600px', width: '100%'}} />
</div>

## Filter Testing and Verification

### Testing Setup Options

To proceed with filter adjustment and verification (**MANDATORY**), they must be connected to measuring equipment, such as a nanoVNA. For this we can prepare a pair of "transitions" from pin connector to SMA (taking care that the pins of the "live" of the SMA connector are then placed in those corresponding to the "IN" and "OUT" of the filter board):

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-calibration-2.webp').default} alt="Filter calibration" style={{maxWidth: '500px', width: '100%'}} />
</div>
<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginTop: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-filter-calibration-3.webp').default} alt="Filter calibration" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-filter-calibration-4.webp').default} alt="Filter calibration" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>
### Alternative Testing Method

Another option is to use a pair of female SMA connectors that can be located on the main board for connection to the measuring equipment: on one hand, the output one marked as "RF OUT", and on the other hand, one that we will temporarily solder on the bottom of the main board, taking its central pin to the "IN" position of the filters (formed by two pins) and soldering its two lateral pins (ground) to the area provided for this purpose on the board.

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-filter-calibration-5.webp').default} alt="Filter calibration" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-filter-calibration-6.webp').default} alt="Filter calibration" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

:::warning Important Testing Precautions
If this last connection option to the measuring equipment is going to be used, it is highly recommended to start with the construction of the filters before soldering any other element on the main board, to avoid damage to components in a bad maneuver with the soldering iron. If this connection option is going to be used when the main board already has its components soldered and installed, it is essential to disconnect the Si5351 RF module while adjusting the filters.
:::

## Expected Filter Response

The graphs we will obtain in the measuring equipment, depending on the type of filter used, should be similar to the following examples:

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-calibration-160m.jpg').default} alt="Filter Response 160m" style={{maxWidth: '700px', width: '100%'}} />
  <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
    160 meter filter with a notch at the second harmonic (3.6 MHz) to improve its attenuation
  </p>
</div>

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-calibration-15m.jpg').default} alt="Filter Response 15m" style={{maxWidth: '700px', width: '100%'}} />
  <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
    15 meter filter with a notch at the second harmonic (42.3 MHz) to improve its attenuation
  </p>
</div>

:::warning Important - Filter Exchange
When exchanging filters on the main board to change bands, special attention must be paid to ensure that the "IN" silkscreen of the filter faces towards the RF module (and matches the "RF IN" silkscreen of the main board), and that we insert all 4 pins of both sockets. It may happen, if we do not pay attention, that one of the pins remains outside its socket, which would lead to totally anomalous behavior of the assembly.
:::