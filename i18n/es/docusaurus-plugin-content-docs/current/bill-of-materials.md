---
sidebar_position: 2
---

# Lista de Materiales

El WSPR Beakon está diseñado como un sistema modular con diferentes configuraciones para adaptarse a varias necesidades y capacidades. Antes de comenzar el ensamblaje, revise las configuraciones disponibles y seleccione los componentes necesarios para su configuración elegida.

## Componentes de Configuración Principal

La versión más básica se alimenta desde el conector USB del módulo ESP32 y contiene todo lo esencial para operar el transmisor. Para esta versión básica, se necesitan los siguientes elementos:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-base.webp').default} alt="PCB Principal WSPR Beakon" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Identificación Visual de Componentes Principales

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-pcb.webp').default} alt="PCB Principal" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>PCB Principal</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-esp32.webp').default} alt="ESP32 Dev Kit C V4" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>ESP32 Dev Kit C V4</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-si5351.webp').default} alt="Módulo RF Si5351" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Módulo RF Si5351</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-encoder-hw40.webp').default} alt="Codificador Rotatorio HW-40" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Codificador Rotatorio HW-40</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-lcd-1602-i2c.webp').default} alt="Pantalla LCD 16x2 I2C" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Pantalla LCD 16x2 I2C</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-ceramic-capacitor.webp').default} alt="Condensador Cerámico" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Condensador Cerámico</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-electrolitic-capacitor.webp').default} alt="Condensador Electrolítico" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Condensador Electrolítico</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-resistor.webp').default} alt="Resistencias 100Ω" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Resistencias 100Ω</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-dupont-cable-fem-fem.webp').default} alt="Cables Dupont" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Cables Dupont</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-4-pin.webp').default} alt="Socket Hembra 4 pines" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Socket Hembra 4 pines</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-7-pin.webp').default} alt="Socket Hembra 7 pines" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Socket Hembra 7 pines</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-19-pin.webp').default} alt="Socket Hembra 19 pines" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Socket Hembra 19 pines</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-male-4-pin.webp').default} alt="Tira de Pines Macho 4 pines" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Tira de Pines Macho 2.54</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screw-separators.webp').default} alt="Separadores Metálicos" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Separadores Metálicos</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screws.webp').default} alt="Tornillos M2.5" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Tornillos M2.5</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-filter-pcbs.webp').default} alt="PCB de Filtro" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>PCB de Filtro</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-axial-inductor.webp').default} alt="Inductores para el Filtro" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Inductores para el Filtro</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-ceramic-capacitor-1.webp').default} alt="Condensadores para el Filtro" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Condensadores para el Filtro</div>
  </div>
</div>

### Tabla Detallada de Componentes Principales

| Componente | Cant | Notas | Enlace |
|------------|------|-------|--------|
| **PCB Principal** | 1 | Archivo Gerber proporcionado para fabricación | [Descargar](https://github.com/danielcharrua/wspr-beakon/tree/main/pcb) |
| **ESP32 Dev Kit C V4** | 1 | 38 pines, Tipo C | [AliExpress](https://es.aliexpress.com/item/1005007820190456.html) |
| **Módulo RF Si5351** | 1 | | [AliExpress](https://es.aliexpress.com/item/1005006233803174.html) |
| **Codificador Rotatorio HW-40** | 1 | | [AliExpress](https://es.aliexpress.com/item/1005006771313967.html) |
| **Pantalla LCD** | 1 | 16x2 I2C | [AliExpress](https://es.aliexpress.com/item/1005006100081942.html) |
| **Condensador Cerámico** | 1 | 100nF 50V, valores no críticos | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=213004009&cPath=952) |
| **Condensador Electrolítico** | 1 | 1000μF 25V, valores no críticos | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=211004075&cPath=968) |
| **Resistencias** | 3 | 100Ω 1W | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=514310001&cPath=921) |
| **Cables Dupont** | 9 | Hembra-hembra, para LCD y codificador | [AliExpress](https://es.aliexpress.com/item/1005006263457745.html) |
| **Socket Hembra 4 pines** | 2 | | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **Socket Hembra 7 pines** | 1 | | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **Socket Hembra 19 pines** | 2 | | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **Tira de Pines Macho 4 pines** | 3 | Cortar a medida | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |
| **Tira de Pines Macho 5 pines** | 1 | Cortar a medida | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |
| **Separadores Metálicos** | 7 | M2.5 x 11mm hembra-hembra | [AliExpress](https://es.aliexpress.com/item/1005001478301407.html) |
| **Tornillos** | 14 | M2.5 x 5mm | [AliExpress](https://es.aliexpress.com/item/1005006674754845.html) |
| **PCB de Filtro** | Según necesidad | La PCB tiene 10 unidades para cortar, mínimo 1 necesaria | [Descargar](https://github.com/danielcharrua/wspr-beakon/tree/main/pcb) |
| **Inductores de Filtro** | Según necesidad | Axiales, según elección de banda | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=999208848&cPath=1335) |
| **Condensadores de Filtro** | Según necesidad | Según elección de banda | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=213004001&cPath=952) |

:::warning Nota Importante sobre Componentes de Filtro
Los valores de inductores y condensadores de filtro dependen de la banda específica de radioaficionado que planea usar para transmisión WSPR. Antes de comprar estos componentes, consulte la documentación técnica incluida con el proyecto para determinar los valores exactos necesarios para su banda de frecuencia elegida. Ver la sección [Diseño y Valores de Filtros](/docs/filters) para detalles.
:::

## Mejora 1: GPS

Con esta mejora proporcionamos la capacidad de no depender de una red WiFi para sincronización de tiempo precisa del conjunto, ya que se añade un módulo GPS que tiene una antena integrada, además de una entrada tipo SMA para una antena externa. Si desea usarlo con la antena integrada, obviamente la caja donde esté ubicado el conjunto no puede ser metálica. Para esta mejora, es necesario añadir los siguientes elementos:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-gps.webp').default} alt="PCB GPS WSPR Beakon" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Identificación Visual de Componentes para GPS

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-gps-neo-7m.webp').default} alt="Módulo GPS NEO-7M" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Módulo GPS NEO-7M</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-5-pin.webp').default} alt="Socket Hembra 5 pines" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Socket Hembra 5 pines</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screw-separators.webp').default} alt="Separadores Metálicos" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Separadores Metálicos</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screws.webp').default} alt="Tornillos M2.5" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Tornillos M2.5</div>
  </div>
</div>

### Tabla Detallada de Componentes para GPS

| Componente | Cant | Notas | Enlace |
|------------|------|-------|--------|
| **Módulo GPS NEO-7M** | 1 | Con antena integrada y conector SMA para antena externa | [AliExpress](https://es.aliexpress.com/item/1005006152967959.html) |
| **Socket Hembra 5 pines** | 1 | Para el nuevo módulo GPS | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **Separadores Metálicos** | 2 | M2.5 x 11mm hembra-hembra, para asegurar placa principal a carcasa y placa módulo RF sobre placa principal | [AliExpress](https://es.aliexpress.com/item/1005001478301407.html) |
| **Tornillos** | 4 | M2.5 x 5mm para separadores metálicos | [AliExpress](https://es.aliexpress.com/item/1005006674754845.html) |

## Mejora 2: Fuente de Alimentación 12V

Con esta mejora proporcionamos la capacidad de alimentar el circuito a 12 (o 13.8) voltios, como con una de las fuentes de alimentación que normalmente se encuentran en la sala de radio. Para esta mejora, es necesario añadir los siguientes elementos:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-12v.webp').default} alt="PCB 12V WSPR Beakon" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Identificación Visual de Componentes para Fuente de Alimentación 12V

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-diode.webp').default} alt="Diodo 1N5819" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Diodo 1N5819</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-buck-converter.webp').default} alt="Convertidor Buck DC-DC" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Convertidor Buck DC-DC</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-dupont-cable-fem-fem.webp').default} alt="Cables Dupont" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Cables Dupont</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-fem-4-pin.webp').default} alt="Socket Hembra 4 pines" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Sockets Hembra 4 pines</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-male-pin.webp').default} alt="Tira de Pines Macho 2 pines" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Tira de Pines Macho 2.54</div>
  </div>
</div>

### Tabla Detallada de Componentes para Fuente de Alimentación 12V

| Componente | Cant | Notas | Enlace |
|------------|------|-------|--------|
| **Diodo 1N5819** | 1 | Diodo Schottky para protección de polaridad | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=71-1N5819&cPath=970) |
| **Convertidor Buck DC-DC** | 1 | Convertidor DC-DC salida 5V | [AliExpress](https://es.aliexpress.com/item/1005008678729834.html) |
| **Cables Dupont** | 2 | Con extremo hembra para cableado de entrada 12V a placa principal | [AliExpress](https://es.aliexpress.com/item/1005006263457745.html) |
| **Sockets Hembra 4 pines** | 2 | | [AliExpress](https://es.aliexpress.com/item/1005001418544370.html) |
| **Pines Macho 1 pin** | 4 | Cortar a medida | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |
| **Tira de Pines Macho 2 pines** | 1 | Cortar a medida | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |

## Mejora 3: Control de Relés Externos

Para habilitar esta mejora, debemos haber implementado previamente la mejora número 2. Con esta mejora incorporamos siete salidas de relé (nivel alto, 12 voltios) configurables según la banda de trabajo (pines marcados como 12, 14, 27, 26, 25, 33 y 32), y una octava salida de relé (pin marcado como 13) controlada por los períodos TX del circuito y que está "secuenciada" para evitar conmutación con RF (va a nivel alto, 12 voltios, medio segundo antes de ir a TX y va a nivel bajo medio segundo después de que cese TX). Para esta mejora, es necesario añadir los siguientes elementos:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-ext-filters.webp').default} alt="PCB Filtro WSPR Beakon" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Identificación Visual de Componentes para Control de Relés Externos

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-udn2981.webp').default} alt="IC UDN2981" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>IC UDN2981</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-ic-socket-18pin.webp').default} alt="Socket IC 18 pines" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Socket IC 18 pines</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-dupont-cable-fem-fem.webp').default} alt="Cables Dupont" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Cables Dupont</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-male-pin.webp').default} alt="Tira de Pines Macho 2.54" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Tira de Pines Macho 8 pines</div>
  </div>
</div>

### Tabla Detallada de Componentes para Banco de Filtros Externo

| Componente | Cant | Notas | Enlace |
|------------|------|-------|--------|
| **IC UDN2981** | 1 | Circuito integrado driver de 8 canales | [AliExpress](https://es.aliexpress.com/item/1005006888538620.html) |
| **Socket IC 18 pines** | 1 | Para el circuito integrado UDN2981 | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=999127304&cPath=1380) |
| **Cables Dupont** | 8 | Con extremo hembra para cableado de salidas a relés externos | [AliExpress](https://es.aliexpress.com/item/1005006263457745.html) |
| **Cables Dupont de Tierra Extra** | 4 | Opcional, con extremo hembra para conexiones de tierra a periféricos externos | [AliExpress](https://es.aliexpress.com/item/1005006263457745.html) |
| **Tira de Pines Macho 8 pines** | 1 | Para salidas de relé, cortar a medida | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |
| **Tira de Pines Macho 4 pines** | 1 | Opcional, para conexión de tierra común a periféricos externos, cortar a medida | [AliExpress](https://es.aliexpress.com/item/1005006034877497.html) |

### Otras Posibles Mejoras para Investigación del Experimentador

Aprovechando las siete salidas de relé disponibles (nivel alto, 12 voltios) que se activan según la banda de trabajo configurada, se podría hacer un banco de filtros externo automáticamente conmutable, de manera que cuando se elige una banda en el menú, se selecciona el filtro correspondiente. Estas salidas de relé también podrían usarse para manejar automáticamente un conmutador de antena para diferentes bandas.

La octava salida de relé disponible, controlada por cambios TX/RX, podría usarse para enrutar la antena a un receptor externo durante los momentos de inactividad TX (en este caso, debe tenerse en cuenta el aislamiento de dicho relé para no "freír" el receptor cuando esté funcionando el transmisor); esta última salida de relé también podría usarse como PTT externo para manejar cualquier periférico que necesite esta señal.

El modo WSPR es altamente eficiente y requiere muy poca potencia, pero si desea usarlo con más energía, podría experimentar, por ejemplo, con uno de los módulos amplificadores de banda ancha populares que vienen de Asia y tienen alta ganancia (entre 30 y 40 dB), siendo capaces de entregar entre 1.5 y 2 vatios de potencia de salida; aun así, y en vista de algunas pruebas realizadas, se recomienda encarecidamente usarlo a un nivel conservador, digamos unos 300-400 milivatios máximo, siendo potencia más que suficiente en WSPR para la mayoría de circunstancias y que resulta en salida más limpia; como ventaja, a ese nivel de potencia, el módulo es muy tolerante a antenas moderadamente desadaptadas, si ese fuera el caso.

Debe añadirse que estos amplificadores tienen ganancia desigual en diferentes bandas, por lo que se recomienda altamente el uso de un atenuador variable entre el conjunto descrito aquí y el amplificador mismo para unificar, y mantener dentro de márgenes razonables, la potencia de salida si se va a hacer uso multibanda del mismo.

:::warning Requisito Obligatorio de Filtro Pasa-Bajos
El amplificador debe conectarse OBLIGATORIAMENTE en su salida a un filtro pasa-bajos, que puede ser externo o puede ser el integrado en la placa haciendo un ligero recableado de la parte RF. Esto es esencial para prevenir emisiones espurias y asegurar funcionamiento adecuado.
:::

Los filtros descritos más adelante han sido usados durante días en regímenes de salida de 500 milivatios sin observar calentamiento o deterioro en su curva de respuesta.

## Carcasa Impresa en 3D para Sistema Principal

Una carcasa impresa en 3D personalizada está disponible para el sistema principal básico WSPR Beakon. Esta carcasa proporciona apariencia profesional y protección mientras mantiene fácil acceso a todos los controles y conexiones.

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-core-7.webp').default} alt="WSPR Beakon - Principal con carcasa" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Identificación Visual de Componentes de Carcasa 3D

<div style={{display: 'flex', flexWrap: 'wrap', justifyContent: 'center', gap: '32px', marginBottom: '32px'}}>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-3d-case.webp').default} alt="Carcasa Impresa en 3D" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Carcasa Impresa en 3D</div>
    <div style={{fontSize: '13px', color: '#666'}}>Archivos STL disponibles</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-insert.webp').default} alt="Insertos Roscados M2.5" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Insertos Roscados M2.5</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-so-239.webp').default} alt="Conector SO-239" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Conector SO-239</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-rg-316.webp').default} alt="Cable Coaxial" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Cable Coaxial</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screws.webp').default} alt="Tornillos M2.5 x 5mm" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Tornillos M2.5 x 5mm</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-screws-m3.webp').default} alt="Tornillos M3 x 8mm" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Tornillos M3 x 8mm</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-nuts-m3.webp').default} alt="Tuercas M3" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Tuercas M3</div>
  </div>
  <div style={{width: '160px', textAlign: 'center'}}>
    <img src={require('@site/static/img/parts/wspr-beakon-ground-terminal.webp').default} alt="Terminal de Tierra" style={{maxWidth: '120px', marginBottom: '8px'}} />
    <div style={{fontWeight: 'bold'}}>Terminal de Tierra</div>
  </div>
</div>

### Tabla Detallada de Componentes de Carcasa 3D

| Componente | Cant | Notas | Enlace |
|------------|------|-------|--------|
| **Carcasa Impresa en 3D** | 1 | Archivos STL disponibles para descarga | [Descargar](https://github.com/danielcharrua/wspr-beakon/tree/main/3D) |
| **Insertos Roscados M2.5** | 13 | 5mm de longitud, para fundir en plástico | [AliExpress](https://es.aliexpress.com/item/1005007653131713.html) |
| **Conector SO-239** | 1 | Tipo montaje en panel de 4 agujeros | [AliExpress](https://es.aliexpress.com/item/1005004896899844.html) |
| **Cable Coaxial** | 1 | RG316 o similar, 10-15cm de longitud para conexión RF interna | [AliExpress](https://es.aliexpress.com/item/1005003618138960.html) |
| **Tornillos M2.5 x 5mm** | 13 | Para uso con insertos roscados | [AliExpress](https://es.aliexpress.com/item/1005006674754845.html) |
| **Tornillos M3 x 8mm** | 4 | Para montaje del conector SO-239 | [AliExpress](https://es.aliexpress.com/item/1005006674754845.html) |
| **Tuercas M3** | 4 | Para asegurar conector SO-239 | [AliExpress](https://es.aliexpress.com/item/1005006470779106.html) |
| **Terminal de Tierra** | 1 | Tipo tornillo 3mm para conexión de blindaje coaxial | [Cetronic](https://www.cetronic.es/sqlcommerce/disenos/plantilla1/seccion/producto/DetalleProducto.jsp?idIdioma=&idTienda=93&codProducto=999208192&cPath=1162) |