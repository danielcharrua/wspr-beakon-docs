---
sidebar_position: 3
---

# Guía de Ensamblaje

Esta guía proporciona instrucciones paso a paso para ensamblar componentes en la PCB principal de su WSPR Beakon. Siga estas instrucciones cuidadosamente para asegurar un ensamblaje y funcionamiento adecuados.

## Ensamblaje de Componentes de la PCB Principal

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-front-modules.webp').default} alt="Ensamblaje de módulos" style={{maxWidth: '800px', width: '100%'}} />
</div>

Al ensamblar los diversos componentes en la placa principal, se recomienda seguir este orden:

## 1. Verificación Inicial

- Verifique que la serigrafía de pines de los diferentes módulos coincida con la serigrafía de la placa principal, ya que puede haber diferentes versiones de módulos con diferentes distribuciones de pines

## 2. Instalación de Zócalos para Filtros

- Suelde los dos zócalos hembra de 4 pines para los filtros, presionándolos contra la placa durante la soldadura para que estén correctamente asentados y formen 90 grados con respecto a la placa

## 3. Instalación de Socket ESP32

- Suelde los zócalos de pines hembra para el ESP32, cuidando que estén correctamente asentados y por tanto formen 90 grados con respecto a la placa

## 4. Instalación de Socket del Módulo RF Si5351

- Suelde los zócalos de pines hembra para el módulo RF (Si5351), cuidando que estén correctamente asentados y por tanto formen 90 grados con respecto a la placa

## 5. Instalación de Pines del Módulo Si5351

- Suelde la tira de pines macho de siete pines en el módulo Si5351. Estos pines se insertan desde la parte inferior de la placa (soldar por arriba) y la parte larga de los pines debe quedar visible. Cuide que formen un ángulo de 90 grados con la placa

## 6. Mejora de Estabilidad de Frecuencia

Una vez soldados los pines en el módulo Si5351, suelde 3 resistencias de 100 ohmios y 1 vatio, en paralelo, en los pines marcados como "VIN" y "GND". Estas resistencias quedarán a 1 o 2 milímetros por encima de los componentes de la placa para actuar como "calentador" de los mismos y así minimizar la deriva de frecuencia del módulo.

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-si5351-stability-1.webp').default} alt="Módulo RF con resistencias de calefacción" style={{maxWidth: '500px', width: '100%'}} />
</div>
<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginTop: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-si5351-stability-2.webp').default} alt="Módulo RF con resistencias de calefacción" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-si5351-stability-3.webp').default} alt="Módulo RF con resistencias de calefacción" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

### Carcasa de Estabilización de Temperatura Opcional

Si se quiere mejorar aún más la deriva de frecuencia, se puede preparar una pequeña caja para el módulo Si5351 que lo encierre junto con las resistencias para mantener el calor interno. Se puede utilizar una chapa metálica estañada para hacer esta caja (la chapa de las latas de leche condensada de una conocida marca alimentaria es óptima por su facilidad para ser soldada con estaño). En este caso es necesario montar los separadores en el módulo antes de soldar la carcasa en la parte inferior de la placa en cuatro puntos, y generalmente suelen ser suficientes dos resistencias en lugar de las tres previstas si el módulo no queda "encerrado".

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-si5351-stability-4.webp').default} alt="Carcasa del módulo RF" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-si5351-stability-5.webp').default} alt="Carcasa del módulo RF" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>
<div style={{textAlign: 'center', marginTop: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-si5351-stability-6.webp').default} alt="Carcasa del módulo RF" style={{maxWidth: '500px', width: '100%'}} />
</div>

### Verificación de Deriva de Frecuencia

La deriva final del módulo se puede comprobar (preferiblemente en 10 metros por ser la banda más alta y por tanto más crítica), después de tenerlo encendido durante 10 minutos, recibiéndonos nosotros mismos, o también en el sitio web "wsprnet.org", sección "Database", buscando nuestros reportes enviados por otras estaciones (en "Call" pondremos nuestro indicativo). Si la sección "Drift" muestra valores de -1, 0, o 1, todo va razonablemente bien.

- **Valores positivos** (2, 3, o 4): Indica que estamos sobrecalentando el módulo; quitar una resistencia o separarlas un poco de los componentes de la placa
- **Valores negativos** (-4, -3, o -2): Indica que el módulo requiere más calor; añadir una tercera resistencia (si hubiera solo dos) o acercarlas
- **Desviaciones** de ±5 o más: Serán tramas indecodificables y aparecerán claramente inclinadas en la "Cascada" de programas como WSJT-X

## 7. Instalación de Pines para el Cableado

- Suelde las tiras de pines macho (lado corto apoyado en la placa) correspondientes a "LCD" (4 pines) y "Encoder" (5 pines)

## 8. Instalación de Condensadores

- Suelde los condensadores C1 (100 nF) y C2 (1000 μF), respetando la polaridad de este último

## 9. Conector de Salida RF

- Suelde el conector SMA de salida (RF OUT) si tiene previsto usarlo en la posición habilitada para ello en la placa; en caso contrario deberá reconducir la RF, con un cable coaxial, hasta la posición donde se encuentre el conector de salida de RF empleado

## 10. Instalación de Módulos

- Inserte el módulo ESP32 en su socket respectivo (su conector USB quedará hacia fuera de la placa; verifique que la nomenclatura de pines del ESP32 y de la placa principal coincidan)
- Inserte el módulo Si5351 (asegúrelo con separadores M2.5 x 11mm a la placa principal)
- Inserte el filtro correspondiente a la banda donde se usará el transmisor WSPR (oriéntelo correctamente en la placa; el lado "IN" debe mirar hacia el Si5351)

## 11. Cableado de Pantalla y Codificador

- Conecte el LCD y el codificador a sus respectivos zócalos con cables "Dupont" hembra-a-hembra, respetando la nomenclatura de pines mostrada en la serigrafía de las placas correspondientes

## Verificación del Progreso del Ensamblaje

La placa debería verse aproximadamente así:

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-base-partial.webp').default} alt="Ensamblaje básico" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-base.webp').default} alt="Ensamblaje básico" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

## Mejora 1: Instalación del Módulo GPS

Si desea actualizar la placa con la "Mejora 1" (GPS), siga estos pasos:

### 12. Instalación de Socket GPS

- Suelde un socket hembra de 5 pines en la posición correspondiente en la placa principal, cuidando que esté correctamente asentado y por tanto forme 90 grados con respecto a la placa

### 13. Preparación de Pines del Módulo GPS

La placa GPS viene con pines que sobresalen paralelos a la placa, y deben doblarse para que sobresalgan a 90 grados. Esta es una operación simple pero debe hacerse con cierto cuidado para evitar romper algún pin.

:::warning Procedimiento de Doblado de Pines
**HAGA ESTO PIN POR PIN, NO TODOS A LA VEZ.** Agarre cada pin lo más cerca posible de la parte plástica con alicates de punta fina y dóblelo suavemente para que quede a 90 grados con respecto a la placa. Repita con los cinco pines. Una vez hecho, verifique que estén todos razonablemente alineados y ajuste si es necesario.
:::

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-gps-module-mod-1.webp').default} alt="Modificación del módulo GPS" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-gps-module-mod-2.webp').default} alt="Modificación del módulo GPS" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>
<div style={{textAlign: 'center', marginTop: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-gps-module-mod-3.webp').default} alt="Modificación del módulo GPS" style={{maxWidth: '500px', width: '100%'}} />
</div>

### 14. Recorte de Pines GPS

Los pines, una vez enderezados, son más largos de lo necesario y por tanto no se asientan completamente en el socket hembra. Córtelos a aproximadamente 6 milímetros, midiendo desde la pieza plástica.

### 15. Instalación del Módulo GPS

- Inserte el módulo GPS en su socket y asegúrelo con separadores M2.5 x 11mm a la placa principal

Esta área de la placa debería verse aproximadamente así:

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-gps-module-mod-4.webp').default} alt="Modificación del módulo GPS" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-gps.webp').default} alt="Modificación del módulo GPS" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

## Mejora 2: Fuente de Alimentación Externa de 12V

Si desea actualizar la placa con la "Mejora 2" (alimentación externa de 12V), siga estos pasos:

### 16. Entrada de Alimentación

- Suelde la tira de pines macho de 2 pines (lado corto apoyado en la placa) en la posición marcada como "GND" y "12V"

### 17. Zócalos del Convertidor DC-DC

- Suelde los dos zócalos hembra de 4 pines en la posición correspondiente para el convertidor DC-DC, cuidando que estén correctamente asentados y formen 90 grados con respecto a la placa

### 18. Instalación de Pines en las Esquinas

- Inserte solo 4 pines macho (desde el lado largo) en las 4 esquinas del rectángulo formado por ambos zócalos hembra (posiciones marcadas en la placa como GND, 12V, GND, 5V). Los dos pines centrales de cada socket hembra de 4 pines no se usan

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-12v-1.webp').default} alt="Modificación 12v" style={{maxWidth: '500px', width: '100%'}} />
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-pcb-12v-2.webp').default} alt="Modificación 12v" style={{maxWidth: '500px', width: '100%'}} />
  </div>
</div>

### 19. Instalación del Convertidor DC-DC

- Coloque la placa del convertidor DC-DC sobre los cuatro pines macho (cuidado: verifique que la serigrafía "IN" y "OUT" de la placa convertidora mire hacia abajo hacia la placa principal y coincida con la serigrafía "12V" (para "IN") y "5V" (para "OUT") de la placa principal)
- Asegúrese de que se asiente correctamente y suelde los 4 pines macho

### 20. Instalación del Diodo

- Suelde el diodo D1 (1N5819) respetando la posición ánodo-cátodo como se muestra en la serigrafía de la placa

Esta área de la placa debería verse aproximadamente así:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-12v.webp').default} alt="Modificación 12v" style={{maxWidth: '600px', width: '100%'}} />
</div>

## Mejora 3: Control de Relé Externo

Si desea actualizar la placa con la "Mejora 3" (control de relé externo), siga estos pasos:

:::warning Prerrequisito
Para que esta parte funcione, es necesario haber implementado previamente la "Mejora 2"
:::

### 21. Socket del IC UDN2981

- Suelde el socket de 18 pines para el IC UDN2981 (con la "muesca" orientada como se muestra en la serigrafía de la placa principal)

### 22. Conectores de salida de relé

- Suelde la tira de pines macho de 8 pines (lado corto apoyado en la placa) que forma las salidas a los diferentes relés

### 23. Conectores de Tierra Opcional

- Opcionalmente suelde la tira de pines macho de 4 pines (lado corto apoyado en la placa) en la posición marcada como GND cerca del IC, para facilitar un punto de conexión de tierra común para periféricos que puedan necesitarlo (por ejemplo, una placa de relés para un filtro multibanda externo)

### 24. Instalación del IC UDN2981

- Inserte el IC UDN2981 en su socket (con la "muesca" orientada como se muestra en la serigrafía de la placa principal)

Esta área de la placa debería verse aproximadamente así:

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb-ext-filters.webp').default} alt="Modificación 12v" style={{maxWidth: '600px', width: '100%'}} />
</div>

## Ensamblaje de la Carcasa 3D

Con el ensamblaje de la PCB completo, es hora de instalar todo en la carcasa impresa en 3D.

### 25. Instalación de Insertos

- Instale los insertos roscados (M2.5) en los agujeros designados de la carcasa
- Use un soldador para calentar los insertos y presionarlos en el plástico hasta que queden al ras con la superficie
- Deje enfriar completamente antes de continuar

### 26. Montaje de la PCB Base

- Asegure la PCB principal a la base de la carcasa usando tornillos M2.5
- Asegúrese de que la PCB se asiente plana y todos los agujeros de montaje se alineen correctamente
- No apriete demasiado los tornillos para evitar agrietar el plástico

### 27. Ensamblaje del Panel Frontal

- Monte la pantalla LCD en la abertura del panel frontal
- Instale el codificador rotatorio (HW-040) en su posición designada
- Asegure ambos componentes con sus respectivos tornillos (LCD) y tuerca + arandela (encoder)

### 28. Ensamblaje del Panel Trasero

- Instale el conector SO-239 (PL hembra de chasis) en el panel trasero
- Asegúrese de que el conector esté correctamente asentado y apretado
- Uno de los tornillos, por la parte interior de la caja, deberá llevar un terminal de tierra para poder soldar la malla del cable coaxial de RF

### 29. Conexión RF

- Conecte la salida RF de la PCB al conector SO-239 trasero usando cable coaxial RG-316
- Suelde las conexiones cuidadosamente, asegurando una buena continuidad RF
- Mantenga la longitud del cable lo más corta posible para minimizar las pérdidas

### 30. Verificación del Cableado

- Verifique doblemente todas las conexiones del codificador a la PCB
- Verifique que las conexiones del LCD coincidan con las asignaciones de pines
- Asegúrese de que todos los cables Dupont estén correctamente asentados y seguros

### 31. Ensamblaje Final de la Carcasa

- Posicione cuidadosamente el panel frontal con LCD y codificador
- Enrute todos los cables ordenadamente dentro de la carcasa para evitar pellizcos
- Inserte los paneles frontal y trasero en sus respectivas ranuras de la base
- Inserte la tapa deslizante en las guías internas de la carcasa superior, teniendo cuidado de que la muesca quede hacia el exterior y hacia delante. La parte delantera de la carcasa tiene un borde ligeramente inclinado
- Inserte la carcasa superior de tal modo que las partes frontal y trasera asienten en sus correspondientes ranuras
- Realice una inspección visual final de todas las conexiones

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-core.webp').default} alt="WSPR Beakon ensamblado" style={{maxWidth: '600px', width: '100%'}} />
</div>

## Ensamblaje Completo

Su WSPR Beakon está ahora completamente ensamblado y listo para la instalación del firmware y las pruebas. El siguiente paso es proceder con la configuración del software y las pruebas iniciales.

:::tip Consejos de Ensamblaje
- Tome fotos durante el desensamblaje como referencia si necesita hacer modificaciones más tarde
- Pruebe la unidad antes del cierre final de la carcasa para asegurar que todo funcione correctamente
:::