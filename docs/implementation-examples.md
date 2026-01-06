---
sidebar_position: 2
---

# Implementation Examples

This section showcases the versatility and modularity of the WSPR Beakon project through different implementation examples. The basic design can be enhanced and adapted for various use cases while maintaining the core functionality.

## Basic WSPR Beakon

The core WSPR Beakon system with GPS synchronization represents the fundamental implementation. This setup provides all essential WSPR functionality in a compact, standalone package.

### Basic PCB Assembly

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '600px', width: '100%'}} />
  <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
    Core PCB assembly showing all available enhancement modules installed
  </p>
</div>

### 3D Printed Enclosure Option

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-core-7.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '600px', width: '100%'}} />
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-5.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-6.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-1.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-2.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-4.webp').default} alt="WSPR Beakon - Core with case" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

**Features:**
- GPS-based or NTP (WiFi) time synchronization
- Multi-band operation with manual filter selection
- LCD display and user interface with encoder
- Compact design suitable for portable operation
- Optional 3D printed enclosure available

## "Mad Max" Enhanced Version

This implementation demonstrates how easily the basic design can be enhanced with an RF amplifier for increased output power. This example operates in single-band configuration and showcases the project's modularity without requiring a formal enclosure.

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-mad-max.webp').default} alt="WSPR Beakon - Mad Max Version" style={{maxWidth: '600px', width: '100%'}} />
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-mad-max-1.webp').default} alt="WSPR Beakon - Mad Max Version" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-mad-max-2.webp').default} alt="WSPR Beakon - Mad Max Version" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-mad-max-3.webp').default} alt="WSPR Beakon - Mad Max Version" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-mad-max-4.webp').default} alt="WSPR Beakon - Mad Max Version" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-mad-max-5.webp').default} alt="WSPR Beakon - Mad Max Version" style={{maxWidth: '600px', width: '100%'}} />
</div>

**Features:**
- All basic WSPR Beakon functionality
- Integrated RF amplifier for higher output power
- Multi-band operation with manual intervention
- Open construction for easy modifications
- Demonstrates modular enhancement approach

## Advanced Multi-Band System

This implementation represents the most complete version, featuring automatic filter bank selection and integrated amplification. The system operates from a 220V AC or 12V DC power source and includes automatic relay control for seamless band switching.

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-enhanced-unit.webp').default} alt="WSPR Beakon - Enhanced unit" style={{maxWidth: '600px', width: '100%'}} />
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-1.webp').default} alt="WSPR Beakon - Enhanced unit" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-2.webp').default} alt="WSPR Beakon - Enhanced unit" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-3.webp').default} alt="WSPR Beakon - Enhanced unit" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-4.webp').default} alt="WSPR Beakon - Enhanced unit" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-5.webp').default} alt="WSPR Beakon - Enhanced unit" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-6.webp').default} alt="WSPR Beakon - Enhanced unit" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

**Features:**

- Integrated RF amplifier
- 220V AC or 12V DC power supply operation
- GPS integration for precise timing
- Relay control system for automatic filter switching
- Commercial enclosure with custom machining
- Multi-band operation without manual intervention

## Project Modularity

These examples demonstrate the inherent modularity of the WSPR Beakon design:

- **Core functionality** remains consistent across all implementations
- **Enhancement modules** can be added as needed
- **Mechanical integration** adapts to different use cases
- **Scalable power requirements** based on needs
- **Control systems** maintain the same user interface

Whether you need a simple portable beacon or a sophisticated multi-band station, the WSPR Beakon architecture provides a solid foundation for your specific requirements.