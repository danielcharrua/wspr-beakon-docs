---
sidebar_position: 1
---

# Descripción del Proyecto

Bienvenido a la documentación completa del **WSPR Beakon**, un transmisor baliza WSPR (Weak Signal Propagation Reporter) modular y expandible basado en microcontrolador ESP32 con generador de reloj Si5351.

## ¿Qué es WSPR?

WSPR (Weak Signal Propagation Reporter) es un protocolo digital y programa de computadora usado para comunicación de radio de señal débil entre radioaficionados. El protocolo fue desarrollado por el físico ganador del Premio Nobel Joe Taylor (K1JT).

WSPR es un modo de radio cuyo uso principal es el estudio de propagación a través de diferentes bandas de radioaficionados, y también permite efectivamente la comparación directa de diferentes antenas o ubicaciones. Utiliza períodos de transmisión de dos minutos y típicamente emplea muy baja potencia, siendo el rango más común entre un milivatio (1 mW) y un vatio (1 W). En términos muy generales, se podría decir que una transmisión de 1 vatio en WSPR es equivalente a 10 vatios en FT8, 100 vatios en CW, o 1000 vatios en SSB.

Existe una gran red de estaciones receptoras WSPR distribuidas mundialmente en diferentes bandas, y muchas de estas estaciones suben sus reportes al sitio web WSPR: [https://www.wsprnet.org/drupal/wsprnet/map](https://www.wsprnet.org/drupal/wsprnet/map). Este sitio web presenta inicialmente un mapa de reportes donde puedes filtrar por banda, indicativo, período de tiempo, etc. El mismo sitio web, en la sección "Database", permite obtener un listado de texto detallado con información comprensiva en la que también se pueden aplicar filtros de búsqueda.

Para más información sobre WSPR, puedes visitar: [https://en.wikipedia.org/wiki/WSPR_(amateur_radio_software)](https://en.wikipedia.org/wiki/WSPR_(amateur_radio_software))

## Acerca del WSPR Beakon

El ensamblaje propuesto está diseñado para transmitir en bandas HF, MF y LF. El WSPR Beakon está diseñado con un **enfoque modular** que permite implementar diferentes configuraciones según las necesidades del usuario, desde una versión básica hasta un sistema completamente equipado.

<div style={{textAlign: 'center', marginBottom: '20px'}}>
  <img src={require('@site/static/img/wspr-beakon-pcb.webp').default} alt="PCB WSPR Beakon" style={{maxWidth: '600px', width: '100%'}} />
</div>

### Características Principales

- **Operación multibanda**: Desde 2200m hasta 2m (limitado por hardware a 10m)
- **Diseño modular**: Sistema expandible con mejoras opcionales
- **Sincronización de tiempo vía WiFi**: Requerimiento esencial para el modo de transmisión WSPR, con soporte para múltiples configuraciones de red simultáneas
- **Sincronización de tiempo vía módulo GPS**: Incluye antena integrada con opción de conectar antena externa
- **Pantalla LCD**: Muestra varios parámetros del equipo e información de estado
- **Encoder rotatorio**: Para seleccionar la banda de operación
- **Zócalos para filtros incorporados**: Zócalos montados en PCB para inserción de filtros pasa-bajos
- **Potencia de salida configurable**: Control de potencia de cuatro pasos entre 1 y 10 milivatios
- **Siete salidas de relé**: Salidas de alto nivel configurables según la banda de operación
- **Salida de relé TX/RX**: Salida de alto nivel que se activa/desactiva con cambios de transmisión
- **Período de calentamiento de transmisión**: Período previo a la transmisión para estabilizar la deriva de frecuencia del módulo RF, especialmente importante en frecuencias más altas
- **Bloqueo de transmisión**: Previene la transmisión si no se puede lograr sincronización de tiempo válida vía WiFi o GPS

:::caution Limitación de Hardware
Aunque el software soporta frecuencias hasta 2m (144 MHz), la implementación actual de hardware usando el módulo generador de reloj Si5351 está prácticamente limitada a frecuencias hasta 10m (28 MHz) debido a las características de respuesta de frecuencia del módulo.
:::

## Antes de Empezar

:::danger Se Requiere Licencia de Radioaficionado
Para usar este ensamblaje en la práctica conectándolo a una antena real, **DEBES** tener una licencia de radioaficionado válida o autorización administrativa que te permita hacerlo, es decir, tener un indicativo de radioaficionado oficialmente asignado.
:::

:::danger Filtrado RF Obligatorio
**EL USO DE UN FILTRO EN LA SALIDA DEL TRANSMISOR ES ABSOLUTAMENTE IMPERATIVO.** El módulo RF genera múltiples armónicos que deben ser eliminados antes de poner una señal al aire. La placa del circuito incluye zócalos para insertar un filtro pasa-bajos, que generalmente opera en modo de banda única, por lo que la experimentación en múltiples bandas usualmente requiere sustituir un filtro por otro. **SE REITERA EL USO OBLIGATORIO DE ELEMENTOS DE FILTRADO RF.**
:::

:::warning Seguridad de Alimentación
Si estás alimentando el circuito desde una fuente externa, es **ALTAMENTE RECOMENDADO** que esta fuente se apague antes de conectar un PC al módulo ESP32. **NO HACERLO PUEDE DAÑAR IRREPARABLEMENTE EL PC.**
:::

:::info Uso Responsable de Potencia
WSPR es un modo altamente efectivo diseñado para el uso de niveles de potencia muy moderados, generalmente por debajo de 1 vatio, siendo muy común el uso de unos pocos milivatios. Tengamos esto en mente al hacer uso responsable del espectro.
:::

## Consideraciones Importantes del Ensamblaje

Este montaje, aunque pueda parecer lo contrario por la fotografía inicial, involucra más que solo ensamblar los diferentes módulos que lo componen. Incluso en la versión más básica, se deben construir filtros (soldando componentes) y necesitas conocimiento para ajustarlos con equipo de medición (por ejemplo, un nanoVNA), y la frecuencia de salida también debe ser calibrada con equipo de medición apropiado o con un receptor (o transceptor) razonablemente ajustado en frecuencia. **En esencia, este no es un proyecto plug-and-play.**

Se recomienda una lectura completa de esta documentación antes de comenzar el ensamblaje propuesto, ya que hay algunos elementos que se sueldan o no dependiendo de la opción de operación elegida, y podría pasar que algo innecesario para nuestras intenciones haya sido soldado o adquirido. Una lectura completa y cuidadosa nos dará una visión general para elegir la opción de ensamblaje que mejor se ajuste a nuestras expectativas.

La documentación es bastante extensa para proporcionar descripciones exhaustivas y aclarar todas las posibles dudas que puedan surgir. La parte más compleja del ensamblaje son los filtros, pero nada que no se pueda abordar con un poco de paciencia y enfocándose en las bandas de interés, por lo que probablemente no sea necesario hacer los seis filtros propuestos.
