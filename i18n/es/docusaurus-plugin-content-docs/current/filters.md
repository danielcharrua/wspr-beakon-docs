---
sidebar_position: 4
---

# Filtros

Esta sección cubre el diseño, construcción y ajuste de filtros para su sistema WSPR Beakon.

## Filosofía de Diseño de Filtros

Dado que el funcionamiento se realizará a muy baja potencia, intentamos construir filtros con componentes comunes y económicos: inductores axiales (su apariencia es similar a resistencias con cuerpo verde) y condensadores normales de bajo voltaje (50 voltios). Creímos que evitar la necesidad de enrollar toroides y obtener condensadores de tipo NP0 de alta calidad (que obviamente es una mejor opción) haría que la construcción de estos filtros fuera más factible para una audiencia más amplia. Esto no impide que el mismo soporte (PCB) se use para construirlos con componentes de mayor calidad que los propuestos aquí.

Se construyeron varias unidades de filtro para cada banda, verificando que en la mayoría de los casos son replicables sin modificaciones mayores; lógicamente esto dependerá de la tolerancia de los diferentes componentes y en algunos casos puede ser necesario un ajuste fino, generalmente variando el valor de algún condensador, y especialmente para centrar la frecuencia de trabajo de unidades que incorporan filtros de muesca; el ajuste de la frecuencia central de estos filtros de "muesca" es mucho más rápido y simple si se usa un trimmer de ajuste con un valor ligeramente superior al del condensador(es) fijo(s) correspondiente, que reemplazaría. Por tanto se recomienda su uso (ver la sección "Notas" en la tabla de componentes de filtros).

## Requisitos de Prueba Obligatorios

Debe enfatizarse que la tabla de componentes para cada filtro es solo un punto de partida, por lo que cada unidad construida debe ser **OBLIGATORIAMENTE VERIFICADA** individualmente con equipo de medición, por ejemplo un nanoVNA, para verificar que:

- El **segundo armónico** (doble frecuencia de la que se va a usar) esté a un nivel entre **35 y 40 dB por debajo** del nivel de la frecuencia de uso
- El **tercer armónico** (triple frecuencia de la que se va a usar) esté entre **45 y 50 dB por debajo** del nivel de la frecuencia de uso
- Las frecuencias superiores al tercer armónico también deben mantenerse alrededor de **50 dB (o más) por debajo** del nivel de la frecuencia de uso

:::warning Verificación de Filtro Requerida
Cada unidad de filtro debe ser probada y verificada individualmente con equipo de medición apropiado antes del uso. Los valores de componentes proporcionados son puntos de partida y pueden requerir ajuste para un rendimiento óptimo.
:::

## Valores de Componentes de Filtros HF

Los valores de componentes que se usarán como puntos de partida para la construcción de los diferentes filtros HF son los siguientes:

<table>
  <thead>
    <tr>
      <th rowspan="2">BANDA</th>
      <th colspan="4" style={{backgroundColor: '#e6f6e6'}}>INDUCTORES (μH)</th>
      <th colspan="7" style={{backgroundColor: '#eef9fd'}}>CONDENSADORES (pF)</th>
      <th rowspan="2">NOTAS TIPO DE FILTRO</th>
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
      <td>5 polos con muesca. El C de 15 pF puede ser sustituido por un trimmer para ajuste fino de la muesca de 56.3 MHz</td>
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
      <td>5 polos con muesca. Capacitancia inicial formada por dos condensadores en paralelo. Los C de 27 pF + 1 pF pueden ser sustituidos por un solo trimmer para ajuste fino de la muesca de 42.2 MHz</td>
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
      <td>5 polos con 2 muescas. Los C de 18 pF + 1.2 pF pueden ser sustituidos por un solo trimmer para ajuste fino de la muesca de 42.28 MHz. Los C de 39 pF + 5.6 pF pueden ser sustituidos por un solo trimmer para ajuste fino de la muesca de 28.19 MHz</td>
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
      <td>7 polos, con inductancia central formada por dos inductores en serie</td>
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
      <td>5 polos con 2 muescas. El C de 12 pF puede ser sustituido por un trimmer para ajuste fino de la muesca de 10.7 MHz. El C de 18 pF puede ser sustituido por un trimmer para ajuste fino de la muesca de 7.14 MHz</td>
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
      <td>7 polos con muesca. El C de 220 pF ajusta la muesca de 3.67 MHz</td>
    </tr>
  </tbody>
</table>

### Notas sobre Componentes

- **Inductores**: Inductores axiales con cuerpo verde (apariencia similar a resistencias)
- **Condensadores**: Condensadores normales de bajo voltaje (clasificación de 50V)
- **Trimmers**: Pueden ser sustituidos por condensadores específicos para permitir el ajuste fino de frecuencias de muesca
- **Combinaciones serie/paralelo**: Algunos valores se logran combinando múltiples componentes

:::info Recomendaciones de Trimmers
Para un ajuste más fácil de las frecuencias de muesca, considere usar condensadores trimmer con valores ligeramente superiores a los condensadores fijos que reemplazan. Esto permite el centrado preciso de frecuencia durante las pruebas.
:::

## Obtención de Componentes

Por favor consulte la [tabla de lista de materiales al final](/docs/bill-of-materials#tabla-detallada-de-componentes-principales).

## Ubicación de Componentes y Diseño de PCB

La posición de cada componente en las diferentes placas de filtro es la siguiente:

<table>
  <thead>
    <tr>
      <th>BANDA</th>
      <th>Lado Superior</th>
      <th>Lado Inferior</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>10M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-10m-t.webp').default} alt="Filtro 10M - Lado Superior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-10m-b.webp').default} alt="Filtro 10M - Lado Inferior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>15M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-15m-t.webp').default} alt="Filtro 15M - Lado Superior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-15m-b.webp').default} alt="Filtro 15M - Lado Inferior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>20M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-20m-t.webp').default} alt="Filtro 20M - Lado Superior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-20m-b.webp').default} alt="Filtro 20M - Lado Inferior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>40M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-40m-t.webp').default} alt="Filtro 40M - Lado Superior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-40m-b.webp').default} alt="Filtro 40M - Lado Inferior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>80M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-80m-t.webp').default} alt="Filtro 80M - Lado Superior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-80m-b.webp').default} alt="Filtro 80M - Lado Inferior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
    <tr>
      <td><strong>160M</strong></td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-160m-t.webp').default} alt="Filtro 160M - Lado Superior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
      <td style={{textAlign: 'center'}}>
        <img src={require('@site/static/img/wspr-beakon-filters-160m-b.webp').default} alt="Filtro 160M - Lado Inferior" style={{maxWidth: '300px', width: '100%'}} />
      </td>
    </tr>
  </tbody>
</table>

## Guía de Identificación de Componentes

Para mayor claridad de ensamblaje, se proporciona la identificación usual de los diferentes componentes que componen los filtros:

### Tabla de Identificación de Componentes

<table>
  <thead>
    <tr>
      <th colspan="2" style={{textAlign: 'center'}}>INDUCTORES AXIALES</th>
      <th colspan="2" style={{textAlign: 'center'}}>CONDENSADORES</th>
    </tr>
    <tr>
      <th style={{backgroundColor: '#e6f6e6'}}>VALOR</th>
      <th style={{backgroundColor: '#e6f6e6'}}>BANDAS DE COLOR</th>
      <th style={{backgroundColor: '#eef9fd'}}>VALOR</th>
      <th style={{backgroundColor: '#eef9fd'}}>SERIGRAFÍA</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>0.33 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>NARANJA - NARANJA - PLATA - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>1 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>1.0 o 1p0</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>0.47 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>AMARILLO - VIOLETA - PLATA - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>1.2 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>1.2 o 1p2</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>0.68 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>AZUL - GRIS - PLATA - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>5.6 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>5.6 o 5p6</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>1 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>MARRÓN - NEGRO - DORADO - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>12 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>12</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>1.5 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>MARRÓN - VERDE - DORADO - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>15 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>15</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>2.2 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>ROJO - ROJO - DORADO - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>18 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>18</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>4.7 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>AMARILLO - VIOLETA - DORADO - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>22 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>22</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>5.6 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>VERDE - AZUL - DORADO - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>27 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>27</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}>8.2 μH</td>
      <td style={{backgroundColor: '#e6f6e6'}}>GRIS - ROJO - DORADO - PLATA</td>
      <td style={{backgroundColor: '#eef9fd'}}>39 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>39</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>100 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>101 o n10</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>120 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>121 o n12</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>220 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>221 o n22</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>270 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>271 o n27</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>470 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>471 o n47</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>680 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>681 o n68</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>820 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>821 o n82</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>1500 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>152 o 1n5</td>
    </tr>
    <tr>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#e6f6e6'}}></td>
      <td style={{backgroundColor: '#eef9fd'}}>2200 pF</td>
      <td style={{backgroundColor: '#eef9fd'}}>222 o 2n2</td>
    </tr>
  </tbody>
</table>

## Diseño y Construcción de PCB de Filtros

La PCB propuesta, para la cual se proporciona un enlace de descarga de archivo Gerber para descargar y ordenar la fabricación ([ver la tabla de lista de materiales al final](/docs/bill-of-materials#tabla-detallada-de-componentes-principales)), consiste en 10 mini placas (que deben cortarse con sierra) para 10 posibles filtros. El diseño tuvo en cuenta que debería ser una placa muy versátil y podría contener filtros de 5 o 7 polos, incluso con algún "notch" asociado con una frecuencia específica. El formato elegido es para construcción estilo "Manhattan" (componentes soldados en "islas") debido a la enorme flexibilidad de diseño y tipo de componente que se puede usar.

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-pcb.webp').default} alt="PCBs de filtros" style={{maxWidth: '450px', width: '100%'}} />
</div>

## Instalación y Conexión de Filtros

Las placas de filtro se conectan a la placa principal de ensamblaje a través de pines insertables, haciéndolas muy fácilmente intercambiables. Una buena manera de asegurar que estos pines estén bien alineados al soldar y que las placas puedan ser fácilmente intercambiadas después es seguir estos pasos:

1. **Instalación de Socket**: Suelde los dos sockets hembra de 4 pines en la placa principal, presionándolos contra la placa durante la soldadura para que estén correctamente asentados y formen 90 grados con respecto a la placa

2. **Inserción de Pines**: Inserte las dos tiras de pines macho de 4 pines, a través de su lado largo, en los sockets hembra ya soldados

3. **Montaje de Placa de Filtro**: Coloque la placa de filtro sobre las tiras de pines macho (cuidado: verifique que la serigrafía "IN" y "OUT" de la placa de filtro mire hacia arriba y coincida con la serigrafía "RFIN" y "RFOUT" de la placa principal), asegurándose de que se asiente correctamente y proceda a soldar los ocho pines macho a la placa de filtro

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-filters-1.webp').default} alt="Instalación y Conexión de Filtros" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-filters-2.webp').default} alt="Instalación y Conexión de Filtros" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-filters-3.webp').default} alt="Instalación y Conexión de Filtros" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-filters.webp').default} alt="Instalación y Conexión de Filtros" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

## Configuración Alternativa de Conector SMA

Aunque las placas de filtro fueron inicialmente diseñadas para ser usadas en este proyecto y conectadas a través de tiras de pines, la disposición de las pistas de "tierra" y "RF" permite soldar conectores SMA para placas de circuito de 1.6mm (que requieren cortar dos de sus cuatro pines de "tierra") y así poder usarlas en cualquier otro proyecto que requiera este tipo de conectores.

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-calibration-1.webp').default} alt="Calibración de filtro" style={{maxWidth: '600px', width: '100%'}} />
</div>

## Prueba y Verificación de Filtros

### Opciones de Configuración de Pruebas

Para proceder con el ajuste y verificación de filtros (**OBLIGATORIO**), deben conectarse al equipo de medición, como un nanoVNA. Para esto podemos preparar un par de "transiciones" de conector de pin a SMA (cuidando que los pines del "vivo" del conector SMA se coloquen entonces en los correspondientes al "IN" y "OUT" de la placa de filtro):

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-calibration-2.webp').default} alt="Calibración de filtro" style={{maxWidth: '500px', width: '100%'}} />
</div>
<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginTop: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-filter-calibration-3.webp').default} alt="Calibración de filtro" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-filter-calibration-4.webp').default} alt="Calibración de filtro" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

### Método de Prueba Alternativo

Otra opción es usar un par de conectores SMA hembra que pueden ubicarse en la placa principal para conexión al equipo de medición: por un lado, el de salida marcado como "RF OUT", y por otro lado, uno que soldaremos temporalmente en la parte inferior de la placa principal, llevando su pin central a la posición "IN" de los filtros (formada por dos pines) y soldando sus dos pines laterales (tierra) al área proporcionada para este propósito en la placa.

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-filter-calibration-5.webp').default} alt="Calibración de filtro" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-filter-calibration-6.webp').default} alt="Calibración de filtro" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

:::warning Precauciones Importantes de Prueba
Si se va a usar esta última opción de conexión al equipo de medición, es altamente recomendable comenzar con la construcción de los filtros antes de soldar cualquier otro elemento en la placa principal, para evitar daños a componentes en una mala maniobra con el soldador. Si se va a usar esta opción de conexión cuando la placa principal ya tenga sus componentes soldados e instalados, es esencial desconectar el módulo RF Si5351 mientras se ajustan los filtros.
:::

## Respuesta Esperada del Filtro

Los gráficos que obtendremos en el equipo de medición, dependiendo del tipo de filtro usado, deberían ser similares a los siguientes ejemplos:

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-calibration-160m.jpg').default} alt="Respuesta del Filtro 160m" style={{maxWidth: '700px', width: '100%'}} />
  <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
    Filtro de 160 metros con una muesca en el segundo armónico (3.6 MHz) para mejorar su atenuación
  </p>
</div>

<div style={{textAlign: 'center', marginBottom: '30px'}}>
  <img src={require('@site/static/img/wspr-beakon-filter-calibration-15m.jpg').default} alt="Respuesta del Filtro 15m" style={{maxWidth: '700px', width: '100%'}} />
  <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
    Filtro de 15 metros con una muesca en el segundo armónico (42.3 MHz) para mejorar su atenuación
  </p>
</div>

:::warning Importante - Intercambio de Filtros
Al intercambiar filtros en la placa principal para cambiar bandas, se debe prestar especial atención para asegurar que la serigrafía "IN" del filtro mire hacia el módulo RF (y coincida con la serigrafía "RF IN" de la placa principal), y que insertemos los 4 pines de ambos sockets. Puede suceder, si no prestamos atención, que uno de los pines quede fuera de su socket, lo que llevaría a un comportamiento totalmente anómalo del conjunto.
:::