---
title: Proyectos
description: Casos de estudio y proyectos de ingeniería electrónica, diseño de hardware y firmware desarrollados por Edgar Vela.
---

# Proyectos de Ingeniería

A continuación se presentan proyectos representativos que abarcan desde el diseño esquemático y ruteo de PCB multicapa hasta el desarrollo de firmware embebido y la validación en banco de pruebas.

---

## Proyecto 1: Nodo Sensor IoT Industrial Ultra-Low Power

!!! info "Resumen del Proyecto"
    Diseño integral de un dispositivo autónomo de monitoreo ambiental y de vibración industrial de bajo consumo, con comunicación inalámbrica de largo alcance (LoRaWAN) y conectividad local BLE para diagnóstico y parametrización mediante aplicación móvil.

### :material-cogs: Especificaciones Técnicas

- **Unidad de Procesamiento**: Microcontrolador STM32L4 (ARM Cortex-M4 @ 80 MHz con FPU).
- **Conectividad**: Módulo LoRaWAN SX1262 (bandas 868 MHz / 915 MHz) y transceptor Bluetooth Low Energy (nRF52832).
- **Sensores Integrados**:
    - Acelerómetro triaxial de precisión (SPI, FIFO integrado para detección de anomalías de vibración).
    - Sensor ambiental de alta precisión (temperatura, humedad relativa y presión barométrica).
- **Alimentación**: Batería Li-SOCl2 (3.6 V) con regulador Buck nano-quiescent (< 1 µA de corriente estática).
- **Durabilidad Estimada**: > 5 años de operación con envíos periódicos cada 15 minutos.
- **Topología de PCB**: 4 capas (FR4 TG150, apilado SIG-GND-PWR-SIG, impedancia controlada a 50 Ω para línea RF).

### :material-code-tags: Stack Tecnológico

| Dominio | Herramientas & Tecnologías |
| :--- | :--- |
| **Diseño de Hardware** | Altium Designer, simulación SPICE de fuentes conmutadas, análisis DFM/DFA |
| **Firmware Embebido** | C (C99), STM32CubeIDE, FreeRTOS, stack LoRaWAN semtech, BLE GAP/GATT |
| **Validación & Test** | Otii Arc (Power Profiler), Osciloscopio Keysight InfiniiVision, Analizador de Espectro |

### :material-check-decagram: Resultados & Logros

- **Consumo en reposo (*Sleep Mode*)**: Se redujo la corriente de espera global a **4.2 µA**, superando el objetivo inicial de 8 µA.
- **Integridad RF**: Pérdidas de retorno (*Return Loss*) $S_{11} < -18 \text{ dB}$ en la banda de 868 MHz tras el ajuste de red de adaptación Pi.
- **Producción**: Fabricación y ensamble exitoso de un primer lote piloto de 50 unidades sin fallos de manufactura (DFT implementado con puntos de test de aguja).

---

## Proyecto 2: Controlador de Motor BLDC de Alta Eficiencia

!!! info "Resumen del Proyecto"
    Inversor trifásico compacto para accionamiento de motores BLDC/PMSM con control orientado al campo (FOC), diseñado para robótica móvil y actuadores de alta densidad de par.

### :material-cogs: Especificaciones Técnicas

- **Rango de Tensión de Entrada**: 18 V a 52 V DC (soporta paquetes Li-Ion hasta 12S).
- **Capacidad de Corriente**: 30 A continuos / 70 A pico con disipación pasiva optimizada.
- **Etapa de Potencia**: Medio puente trifásico con transistores MOSFET de baja $R_{DS(on)}$ (1.8 mΩ) y drivers de compuerta aislados con protección *shoot-through*.
- **Medición de Corriente**: Shunts triaxiales de bajo valor con amplificadores de sensado de corriente bidireccionales de bajo drift térmico.
- **Interfaces de Comunicación**: Bus CAN-FD aislado galvanicamente y puerto UART/USB para telemetría.
- **Frecuencia PWM**: 20 kHz a 40 kHz con muestreo de ADC sincronizado en el centro del período PWM.
- **Topología de PCB**: 6 capas con cobre de 2 oz en capas externas y 3 oz en capas internas para gestión de altas corrientes y disipación térmica.

### :material-code-tags: Stack Tecnológico

| Dominio | Herramientas & Tecnologías |
| :--- | :--- |
| **Diseño de Hardware** | KiCad 8.0, análisis térmico térmico FEA, modelado de planos de masa |
| **Algoritmos de Control** | Algoritmo FOC (Transformadas de Clarke/Park, PWM Vectorial Espacial - SVPWM), control de bucle cerrado de corriente y velocidad |
| **Entorno de Firmware** | C++ embebido moderno (C++17), CMSIS-DSP, arquitectura sin bloqueo |
| **Herramientas de Validación** | Banco de carga dinamométrica, sondas de corriente Hall, cámara termográfica FLIR |

### :material-check-decagram: Resultados & Logros

- **Eficiencia Energética**: Eficiencia pico del inversor del **96.8%** a plena carga nominal.
- **Respuesta Dinámica**: Bucle de corriente ejecutado a **20 kHz** en menos de 12 µs de tiempo de cómputo en el microcontrolador.
- **Seguridad**: Implementación de protecciones en hardware por sobrecorriente por ciclo de reloj (*Cycle-by-cycle trip*), sobretensión y desconexión por sobrecalentamiento.

---

## :material-folder-multiple: Plantilla para Nuevos Proyectos

Para agregar proyectos adicionales a este portafolio, utiliza la siguiente estructura estándar:

```markdown
## Nombre del Proyecto

!!! info "Resumen del Proyecto"
    Descripción general del objetivo y valor del diseño.

### :material-cogs: Especificaciones Técnicas
- **Parámetro 1**: Detalle.
- **Parámetro 2**: Detalle.

### :material-code-tags: Stack Tecnológico
| Dominio | Herramientas & Tecnologías |
| :--- | :--- |
| Hardware | Herramientas CAD, simulaciones |
| Firmware | Lenguaje, RTOS, librerías |

### :material-check-decagram: Resultados & Logros
- Métricas cuantificables obtenidas durante la validación.
```
