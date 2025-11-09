---
sidebar_position: 6
---

# Uso de Pantalla LCD y Codificador

Esta sección cubre la información de la pantalla LCD y el funcionamiento del codificador para su sistema WSPR Beakon.

## Secuencia de Arranque del Sistema

### Proceso de Arranque Inicial

Cuando se aplica energía al conjunto, ocurre la siguiente secuencia:

- **"Connecting Wifi"** aparece en el LCD. Si no puede conectarse a ninguna de las redes WiFi preconfiguradas, procederá a verificar la señal GPS
- **"Reading GPS"** aparece en el LCD. El sistema alternará entre ambos mensajes hasta que logre un resultado de sincronización válido

:::info Adquisición de Señal GPS
La adquisición de señal GPS puede tomar varios minutos. Para un rendimiento óptimo:
- Posicione el conjunto en un área despejada con una vista amplia del cielo
- Si usa la antena GPS integrada y el conjunto está dentro de una carcasa, asegúrese de que la carcasa esté hecha de material no metálico
:::

### Mensajes de Estado de Conexión

- **"Wifi Connected" + "Reading GPS"**: Indica que una red WiFi está conectada pero no tiene acceso a internet, impidiendo la calibración de tiempo vía WiFi
- **"Time not synced"**: Aparece cuando el conjunto ha estado tratando de sincronizar por más de media hora sin éxito vía WiFi o GPS

### Fase de Prueba de Señal

Una vez que se detecta una red WiFi válida o señal GPS:
- LCD muestra **"Testing signal"**
- El equipo comienza una transmisión de prueba de 30 segundos

## Pantalla de Funcionamiento Normal

### Pantalla de Información

Después de la transmisión de prueba, el LCD muestra:

**Línea Superior**: Mensaje deslizante que contiene:
- Indicativo
- Localizador
- Frecuencia
- Banda
- Potencia transmitida (en dBm)
- Intervalo de tiempo configurado entre transmisiones

**Línea Inferior**: Cuenta regresiva numérica que muestra el tiempo restante hasta la próxima transmisión WSPR

### Secuencia de Transmisión

1. **30 segundos antes de la transmisión**: El sistema comienza a transmitir una portadora de calentamiento para estabilizar la temperatura y frecuencia del módulo RF
2. **Durante la transmisión WSPR**: LCD muestra **"Transmitting WSPR message"**
3. **Después de la transmisión**: Regresa a la pantalla de información deslizante y temporizador de cuenta regresiva

## Funcionamiento del Codificador

### Proceso de Selección de Banda

El codificador rotatorio se usa para cambiar bandas y solo puede operarse durante los períodos de descanso de transmisión:

1. **Presione el codificador** - **"Select Freq"** aparece el mensaje
2. **Gire el codificador** - Navegue por las bandas disponibles en cualquier dirección
3. **Presione el codificador nuevamente** cuando se muestre la banda deseada - **"Frequency Set"** aparece el mensaje y se selecciona la nueva banda

:::warning Recordatorio Crítico
**¡Siempre recuerde insertar el filtro apropiado para la nueva banda después de cambiar la frecuencia!**
:::

### Memoria de Banda

- La última banda seleccionada se almacena en memoria cuando se quita la energía
- El sistema iniciará en la misma banda cuando se restaure la energía

## Referencia de Mensajes de Pantalla

| Mensaje | Significado |
|---------|-------------|
| "Connecting Wifi" | Intentando conectar a redes WiFi preconfiguradas |
| "Reading GPS" | Intentando adquirir señal GPS |
| "Wifi Connected" + "Reading GPS" | WiFi conectado pero sin acceso a internet |
| "Time not synced" | Sincronización falló después de 30+ minutos |
| "Testing signal" | Realizando transmisión de prueba de 30 segundos |
| "Transmitting WSPR message" | Transmisión WSPR activa en progreso |
| "Select Freq" | Modo de selección de banda activo |
| "Frequency Set" | Nueva banda ha sido seleccionada |

## Solución de Problemas de Pantalla

Si la pantalla muestra comportamiento inesperado:
- Asegúrese del voltaje adecuado de la fuente de alimentación
- Verifique las conexiones del LCD
- Verifique el cableado del codificador
- Confirme que el sistema ha sido correctamente inicializado después de la carga del firmware