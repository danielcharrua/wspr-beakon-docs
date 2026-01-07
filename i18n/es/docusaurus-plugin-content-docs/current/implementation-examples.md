---
sidebar_position: 2
---

# Ejemplos de Implementación

Esta sección muestra la versatilidad y modularidad del proyecto WSPR Beakon a través de diferentes ejemplos de implementación. El diseño básico puede ser mejorado y adaptado para varios casos de uso mientras mantiene la funcionalidad central.

## WSPR Beakon Básico

El sistema central WSPR Beakon con sincronización GPS representa la implementación fundamental. Esta configuración proporciona toda la funcionalidad WSPR esencial en un paquete compacto e independiente.

### Ensamblaje PCB Básico

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb.webp').default} alt="WSPR Beakon - Núcleo con carcasa" style={{maxWidth: '600px', width: '100%'}} />
  <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
    Ensamblaje PCB central mostrando todos los módulos de mejora disponibles instalados
  </p>
</div>

### Opción de Carcasa Impresa en 3D

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-core-7.webp').default} alt="WSPR Beakon - Núcleo con carcasa" style={{maxWidth: '600px', width: '100%'}} />
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-5.webp').default} alt="WSPR Beakon - Núcleo con carcasa" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-6.webp').default} alt="WSPR Beakon - Núcleo con carcasa" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-1.webp').default} alt="WSPR Beakon - Núcleo con carcasa" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-2.webp').default} alt="WSPR Beakon - Núcleo con carcasa" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core.webp').default} alt="WSPR Beakon - Núcleo con carcasa" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-core-4.webp').default} alt="WSPR Beakon - Núcleo con carcasa" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

**Características:**

- Sincronización de tiempo basada en GPS o NTP (WiFi)
- Operación multibanda con selección manual de filtros
- Pantalla LCD e interfaz de usuario con encoder
- Diseño compacto adecuado para operación portátil
- Carcasa impresa en 3D opcional disponible

## Versión Mejorada "Mad Max"

Esta implementación demuestra lo fácilmente que el diseño básico puede mejorarse mediante un amplificador de RF para obtener una mayor potencia de salida. Este ejemplo funciona con una configuración de conmutación manual de filtros y pone de manifiesto la modularidad del proyecto sin necesidad de una carcasa formal.

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-mad-max.webp').default} alt="WSPR Beakon - Versión Mad Max" style={{maxWidth: '600px', width: '100%'}} />
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-mad-max-1.webp').default} alt="WSPR Beakon - Versión Mad Max" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-mad-max-2.webp').default} alt="WSPR Beakon - Versión Mad Max" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-mad-max-3.webp').default} alt="WSPR Beakon - Versión Mad Max" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-mad-max-4.webp').default} alt="WSPR Beakon - Versión Mad Max" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-mad-max-5.webp').default} alt="WSPR Beakon - Versión Mad Max" style={{maxWidth: '600px', width: '100%'}} />
</div>

**Características:**

- Toda la funcionalidad básica de WSPR Beakon
- Amplificador RF integrado para mayor potencia de salida
- Operación multibanda con intervención manual
- Construcción abierta para modificaciones fáciles
- Demuestra el enfoque de mejora modular

## Sistema Multibanda Avanzado

Esta implementación representa la versión más completa, con selección automática de banco de filtros y amplificación integrada. El sistema opera desde fuente AC 220V o DC 12V e incluye control automático de relés para cambio de banda sin interrupciones.

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-enhanced-unit.webp').default} alt="WSPR Beakon - Unidad mejorada" style={{maxWidth: '600px', width: '100%'}} />
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-1.webp').default} alt="WSPR Beakon - Unidad mejorada" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-2.webp').default} alt="WSPR Beakon - Unidad mejorada" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-3.webp').default} alt="WSPR Beakon - Unidad mejorada" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-4.webp').default} alt="WSPR Beakon - Unidad mejorada" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-5.webp').default} alt="WSPR Beakon - Unidad mejorada" style={{maxWidth: '400px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-enhanced-unit-6.webp').default} alt="WSPR Beakon - Unidad mejorada" style={{maxWidth: '400px', width: '100%'}} />
  </div>
</div>

**Características:**

- Amplificador RF integrado
- Operación con fuente AC 220V o DC 12V
- Integración GPS para temporización precisa
- Sistema de control de relés para cambios automáticos de filtros
- Carcasa comercial con mecanización personalizada
- Operación multibanda sin intervención manual

## Modularidad del Proyecto

Estos ejemplos demuestran la modularidad inherente del diseño WSPR Beakon:

- **Funcionalidad central** permanece consistente en todas las implementaciones
- **Módulos de mejora** pueden añadirse según se necesite
- **Integración mecánica** se adapta a diferentes casos de uso
- **Requerimientos de potencia** escalables según necesidades
- **Sistemas de control** mantienen la misma interfaz de usuario

Ya sea que necesites una baliza portátil simple o una estación multibanda sofisticada, la arquitectura WSPR Beakon proporciona una base sólida para tus requerimientos específicos.