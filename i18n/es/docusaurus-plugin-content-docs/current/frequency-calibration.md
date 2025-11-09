---
sidebar_position: 7
---

# Calibración de Frecuencia para Cada Banda

Esta sección cubre el proceso de calibración de frecuencia requerido para cada banda de su sistema WSPR Beakon.

## Por Qué se Requiere Calibración

Una vez que el código inicial se carga en el conjunto, cada banda de interés debe calibrarse individualmente (este proceso no es necesario para bandas que no usará). Hay variaciones entre bandas y también variaciones entre diferentes módulos Si5351. Si necesita reemplazar un módulo Si5351 debido a falla, el proceso de calibración debe repetirse.

El código inicial establece la frecuencia del cristal para cada banda en 25000000 Hz. Esta frecuencia debe ajustarse para centrar correctamente la transmisión en el segmento WSPR, que es bastante estrecho. **Este paso es obligatorio y debe realizarse rigurosamente**, ya que colocar su transmisión fuera del segmento asignado impedirá que alguien reporte sus tramas.

:::warning Importancia Crítica
La calibración adecuada de frecuencia es esencial para el funcionamiento WSPR. Las señales fuera del segmento WSPR designado no serán decodificadas por otras estaciones.
:::

## Equipo Necesario

Para calibración, necesitará:

- Un transceptor (o receptor) que sea razonablemente preciso en frecuencia con conexión PC
- Cualquier equipo moderno usado para modos digitales debería ser suficiente
- Software WSJT-X (descargable del sitio web oficial)
- Acceso al calculador de calibración en línea

## Procedimiento de Calibración

### Configuración Inicial

1. **Configure intervalo de transmisión**: Configure el conjunto para transmitir cada 4 minutos (opcional, pero reduce el tiempo de espera entre transmisiones)

2. **Instale filtro apropiado**: Instale el filtro para la banda que desea calibrar

3. **Conecte carga ficticia**: Instale una carga ficticia en el conector SMA de la placa principal (o una antena como alternativa)

4. **Encienda el conjunto**: Aplique energía para iniciar el sistema

5. **Seleccione banda objetivo**: Use el codificador para seleccionar la banda de interés (igual que el filtro instalado). Nota: Los cambios de banda no son posibles durante períodos de TX o calentamiento

### Período de Estabilización

6. **Espere estabilización**: Permita 10 minutos para que el módulo Si5351 se estabilice en temperatura y frecuencia

:::info Sensibilidad de Temperatura
El Si5351 es muy sensible a ligeras corrientes de aire que causan cambios de temperatura y deriva de frecuencia. Si el conjunto está expuesto, cúbralo (incluso con una caja de cartón) para prevenir inestabilidad de frecuencia. La frecuencia inestable causa que las tramas WSPR aparezcan visiblemente "inclinadas" en pantallas de cascada y previene la decodificación adecuada.
:::

### Configuración del Receptor

7. **Configure transceptor de referencia**: 
   - Encienda el transceptor a usar como referencia
   - Sintonice a la frecuencia WSPR para la banda siendo calibrada (siempre modo USB, independientemente de la banda)
   - **Frecuencias de bandas clásicas (160-10m)**: 1.836600, 3.568600, 7.038600, 14.095600, 21.094600, y 28.124600 MHz
   - Lista completa de frecuencias disponible en: [Frecuencias WSPR](http://wsprnet.org/drupal/wsprnet/spots)

8. **Configuración de acoplamiento**: Conecte el transceptor a:
   - Una carga ficticia colocada cerca del conjunto, o
   - Un cable corto con conector abierto colocado cerca (pero sin tocar) el conjunto
   - Objetivo: Recibir la transmisión del conjunto sin interferencia externa

:::tip Alternativa de Conexión de Antena
Si usa antenas tanto para el transceptor como para el conjunto (mejor opción para identificación de señal), active el atenuador y/o reduzca la ganancia RF para prevenir problemas de sobrecarga RF.
:::

### Configuración de WSJT-X

9. **Lance WSJT-X**: 
   - Seleccione modo WSPR
   - Seleccione la banda siendo calibrada
   - Si el control CAT está configurado, el programa establecerá automáticamente la frecuencia correcta

10. **Abra pantalla de cascada**: 
    - Seleccione menú "View" → "Wide Graph (Waterfall)"
    - Las señales WSPR deben aparecer entre 1400 y 1600 Hz (solo ventana de 200 Hz)

### Análisis de Señal

<div style={{display: 'flex', justifyContent: 'space-around', gap: '20px', marginBottom: '20px'}}>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-signals-example.webp').default} alt="Señales WSPR correctas dentro de la banda 1400-1600 Hz" style={{maxWidth: '300px', width: '100%'}} />
    <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
      Señales WSPR dentro de la banda de paso correcta, entre 1400 y 1600 Hz
    </p>
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-signals-incorrect.webp').default} alt="Señal WSPR incorrecta fuera de la banda de paso" style={{maxWidth: '300px', width: '100%'}} />
    <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
      Señal WSPR fuera de la banda de paso correcta. Esta señal nunca será decodificada
    </p>
  </div>
  <div style={{textAlign: 'center', flex: 1}}>
    <img src={require('@site/static/img/wspr-beakon-signals-correct.webp').default} alt="Señal WSPR correcta" style={{maxWidth: '300px', width: '100%'}} />
    <p style={{fontSize: '14px', color: '#666', marginTop: '10px', fontStyle: 'italic'}}>
      Señal WSPR dentro de la banda de paso correcta
    </p>
  </div>
</div>

### Medición y Corrección de Frecuencia

11. **Verifique posición de señal**:
    - **Si la señal está dentro de 1400-1600 Hz** (preferiblemente no cerca de los bordes): Calibración completa para esta banda
    - **Si la señal está fuera de la ventana**: Continúe con el proceso de corrección

12. **Localice su señal**:
    - Use el dial del transceptor para moverse arriba o abajo hasta encontrar su señal
    - Posiciónela dentro de la porción correcta del espectro (evite extremos debido a variaciones potenciales de frecuencia)

13. **Registre frecuencia real**: Anote la frecuencia (en Hz) donde tuvo que sintonizar el transceptor para recibir correctamente su señal

### Calcular Nueva Frecuencia de Cristal

14. **Use calculador en línea**: Acceda al calculador de calibración en:
    - **URL**: [https://danielpcostas.dev/how-to-calibrate-the-si5351-oscillator-crystal-without-expensive-instruments/](https://danielpcostas.dev/how-to-calibrate-the-si5351-oscillator-crystal-without-expensive-instruments/)

15. **Ingrese parámetros**:
    - **Frecuencia deseada**: Frecuencia WSPR oficial para la banda (en Hz, sin comas o separadores decimales)
    - **Frecuencia obtenida**: Frecuencia que sintonizó en el transceptor para centrar su señal (en Hz)
    - **Frecuencia inicial del cristal**: 25000000 (valor por defecto cargado en el código ESP32)

16. **Calcule resultado**: Haga clic en "Calculate" para obtener la nueva frecuencia del cristal (ej., "Adjusted Crystal Frequency: 25008771 Hz")

:::info Manejo de Decimales
Si el resultado incluye decimales (ej., 25008771.24 Hz), ignore la porción decimal y use solo el número entero.
:::

## Completar Calibración

### Repetir para Todas las Bandas

17. **Repita proceso**: Realice este procedimiento de calibración para todas las bandas de interés

### Actualizar Código

18. **Modifique frecuencias de cristal**: 
    - Regrese a la página de carga de código
    - Reemplace el valor por defecto 25000000 con el valor calculado para cada banda calibrada
    - Deje bandas no calibradas (que no se usarán) con el valor por defecto

19. **Ajuste intervalo de transmisión**: Modifique períodos de transmisión de 4 minutos a un intervalo más típico (8-10 minutos; siempre números pares)

20. **Cargue nuevo código**: Cargue el código actualizado al ESP32

### Inicialización Final

21. **Paso crítico post-carga**: Después de cargar nuevo código, **debe seleccionar una banda usando el codificador** (ver sección anterior) para la inicialización adecuada del microcontrolador. De lo contrario, el conjunto funcionará erráticamente.

## Verificación

Después de completar todas las calibraciones:
- Su conjunto debería estar correctamente calibrado para todas las bandas de interés
- El sistema está listo para funcionamiento WSPR normal
- Verifique que cada banda produzca señales dentro de la banda de paso WSPR correcta