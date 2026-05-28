# Simulación y Monitoreo de Variables Cardiovasculares y Hemodinámicas

Samuel Joel Peña Rojas

Paula Vanessa Vera Caro

Daniel Leonardo López Castillo


## Monitor de signos vitales uMEC 100

El mindray uMEC 100 es un monitor de signos vitales multiparámetro de configuración robusta y portátil, diseñado para la monitorización continua o ambulatoria de pacientes adultos, pediatricos y neonatales en entornos hospitalarios y de traslado. 

<div align="center">
<img width="413" height="304" alt="image" src="https://github.com/user-attachments/assets/8fe99d7a-ab0e-47ac-b050-c1e52ed2f835" />
</div>

Este equipo procesa múltiples señales bioeléctricas y fisiológicas en tiempo real, midiendo electrocardiograma (ECG), Respiraciones por Impedancia, Presión arterial, Temperatura y Frecuencia de pulso. Además, incorpora algoritmos de filtrado digital para extraer la señal fotopletismográfica (PPG) y su tecnología está optimizada para contrarrestar los dos principales artefactos que degradan la lectura clínica: el movimiento del paciente y la baja perfusión tisular.

Algo muy importante de este equipo es el sistema de alarmas inteligente, contando con un sistema de alarmas visuales y acústicas, las cuales son clasificadas en tres niveles de criticidad (alta, media y baja). Estas se dividen en:

- *Alarmas fisiológicas:* Cuando los parámetros del paciente se encuentran fuera de los límites programados, como bradicardia o desaturación.

- *Alarmas técnicas:* Cuando hay fallas en el sistema, en cuanto a hardware, desconexión de sensores o interferencias en la señal.

## Simulador de parámetros hemodinámicos Pronk OxSim OX-1

El Pronk OxSim OX-1 es un analizador metrológico y simulador óptico miniaturizado de oximetría de pulso (SPO2, el cual está diseñado específicamente para la verificación funcional, el mantenimiento preventivo y la calibración de monitores de signos vitales en campo o laboratorio.

<div align="center">
<img width="371" height="421" alt="image" src="https://github.com/user-attachments/assets/72f40dd7-b815-4e4b-9b93-74ff39f12bfd" />
</div>

Este dispositivo cuenta con un bloque de prueba óptico permanente en forma de "dedo index", donde intercepta de manera activa los destellos de luz infrarroja por los LEDs del sensor del uMEC 100, procesa la señal electrónicamente para calcular la sincronía del pulso y devuelve los pulsos de luz controlador hacia el fotodetector del sensor para imitar la absorción de un tejido vivo.

La tecnología que implementa el OX-1 es para identificar de manera automatica las caracteristicas ópticas del sensor que se le conecte (Masimo, Nellcor, Mindray, etc). Esto permite que ajuste autmáticamente las curvas de calibración de simulación interna para garantizar la máxima precisión sin necesidad de adaptadores externos. Además, su chasis de policarbonato de alta resistencia opera mediante una interfaz de usuario minimalista controlada por solo dos botones en el panel frontal: Botón de mode y botón de sensor, los cuales permiten alternar diferentes modos de simulación fisiológica/patológica.

# PARTE A

## Colocación del uMEC 100 en modo "monitor"

El modo "monitor" del uMEC 100 es el estado operativo por defecto del equipo al momento de encenderlo y dependiendo del estado previo en el que se encuentre el equipo en el laboratorio, se debe proceder de varias formas, tales como:

<div align="center">
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/9f94c2df-a964-4763-9e7a-4e62a92ba332" />
</div>

**1. Estado de apagado (inicio normal)**

Se debe presionar el botón físico de Encendido/apagado ubicado en la parte derecha inferior del equipo. Luego de esto, el indicador de encendido se iluminará, el monitor emitirá un sonido de autocomprobación y la pantalla mostrará de manera inmediata la interfaz de usuario principal con los espacios asignados para las ondas bioleéctricas, los valores numéricos de los parámetros y al momento de conectar los sensores, el monitor comenzará de manera automática la adquisición y análisis de señales en tiempo real.

**2. Estado de espera (Sandby)**

El modo de espera se utiliza para pausar la monitorización sin apagar el equipo. Aquí la pantalla estará apagada pero el indicador de energía seguirá activo. Para retornarlo a modo monitor, se debe girar la perilla de navegación o presionar cualquier tecla física del panel frontal y así el monitor daldrá inmediatamente del estado de espera y regresará de forma directa a la pantalla principal.

**3. Estado de demostración (Demo)**

En caso de que el monitor esté mostrando ondas simuladas pregrabadas (marcadas con la palabra DEMO en pantalla), se debe seguir el siguiente procedimiento:

- Presionar la tecla física del menú principal
- Seleccionar la opción de mantenimiento o configuración de sistema
- Seleccionar la sección de mantenimiento de usuario e introducir la contraseña de fábrica del sistema uMEC 100.
- En el menú desplegado, buscar la opción de "Modo Demo" y cambiar su estado a "Desactivar"

## Parámetros y variables fisiológicas simuladas con el Pronk OxSim OX-1

El OxSim OX-1 posee un bloque óptico activo (dedo de prueba) y a través de él es capaz de simular tres parámetros o variables fisiológicas controlando la atenuación de la luz en tiempo real.


<div align="center">
<img width="250" height="350" alt="image" src="https://github.com/user-attachments/assets/97dbf281-c784-4b6c-bc19-c21062692e8f" />
</div>


1. Saturación Periférica de Oxigeno (SPO2)

Esta variable simula el porcentaje de hemoglobina que se encuentra unida de forma reversible al oxígeno en la sangre arterial del paciente, basado en la relación de absorción de luz roja (660 nm) e infrarroja (940 nm) a través del tejido hidratado. Aquí el simulador toma las dos longitudes de onda emitidas por el sensor del monitor de signos vitales y altera electrónicamente la cantidad de luz que devuelve al fotodetector del sensor, permitiendo simular valores de saturación fijos y precisos para evaluar alarma de hipoxia y la exactitud del monitor. Los puntos de simulación del OX-1 son 85%, 95%, 98% y 99%

<div align="center">
<img width="443" height="273" alt="image" src="https://github.com/user-attachments/assets/9c7901aa-dd15-4f57-b362-96baf3377f1b" />
</div>

2. Frecuencia de pulso (PR)/ frecuencia cardíaca (HR)

Este parámetro representa la cantidad de pulsaciones de la onda de presión arterial por minuto (bpm) causadas por la sístole ventricular izquierda del corazón, propagas hacia el lecho capilar periférico. Lo que hará el simulador será generar variaciones cíclicas en la intensidad de la luz que simula retornar al sensor del monitor, donde cada ciclco será un pulso arterial volumétrico y modificando el intervalo de tiempo entre estas variaciones el OX-1 simulará con precisión diferente estados de ritmo cardíaco para evaluar alarmas de bradicardia o taquicardia. Los puntos fijos de simulación son 40, 80 y 140 bpm

<div align="center">
<img width="436" height="273" alt="image" src="https://github.com/user-attachments/assets/731c2c1c-eb55-494b-80ab-0633e078c2e4" />
</div>

3. Índice de perfusión tisular (Modo de baja perfusión)

El parámetro del índice de perfusión es la relación entre el componente pulsátil de la sangre arterial y el componente estático de los tejidos. Hueso y sangre venosa en el sitio del sensor. Una perfusión normal tiene una señal AC robusta, mientras que una mala perfusión reduce el tamaño de la onda de pulso AC. El OX-1 en el modo de baja perfusión, reducirá la amplitud de la señal pulsátil a niveles críticamente bajos en comparación con el nivel estático, manteniendo la consistencia de la frecuencia y la saturación, la cual está ajustada por defecto a 99% y 80 bpm. Esto verificará la eficacia en los algoritmos de amplificación de señal y sensibilidad de filtrado en el sistema del monitor de signos vitales frente a un paciente con compromiso hemodinámico extremo.

<div align="center">
<img width="445" height="273" alt="image" src="https://github.com/user-attachments/assets/d63cff13-c441-43cc-aac2-1129d9b3db63" />
</div>

## Tolerancias o errores permitidos para cada parámetro

Para poder obtener los errores máximos permitidos del equipo, se deben verificar las especificaciones técnicas del fabricante. Al contrastar las normas internacionales de la industría médica (ISO 80601-2-61 para oximetría de pulso) con los valores de diseño declarados en las epecificaciones de medición del manual de usuario del monitor de la serie uMEC, se definen los siguientes errores permitidos:

1. Saturación Periférica de Oxigeno (SPO2): El error máximo permitido (EMP) para la saturación de oxígeno varía segun el tipo de tecnología integrada en el sensor configurado y el grupo aterio del paciente. De acuerdo al manual de Mindray menciona los siguientes (EMP) en el rango útil del 70% al 100%:

- Pacientes adultos y pediátricos: **$\pm$ 2%**
- Pacientes Neonatales: **$\pm$ 3%**

Es importante mencionar que el fabricante menciona que para valores inferiores al 70%, declara la exactitud como "No especificada", lo que a nivel clínico se debe a que no está permitido por comités de ética médica someter a pacientes humanos a niveles de hipoxia tan extremos para calibrar o validar de forma absoluta las curvas ópticas.

2. Frecuencia de pulso

Las toelrancias de diseño electrónico del monitor de signos vitales establecen un margen sumamente estricto para este parámetros hemodinámico.

- Error Máximo Permitido: **$\pm$ 2bpm** o **$\pm$ 2%**

Esto quiere decir que si el simulador entrega una frecuencia de 40 bpm, el monitor puede mostrar valores entre 38 y 42 bpm. Si simula una taquicardia de 140 bpm, el 2% equivale a $\pm$2.8bpm, por lo que si el monitor se encuentra dentro de la tolerancia va a registrar valores entre 137 y 143 bpm.

3. Índice de perfusión tisular (mmodo de baja perfusión)

A nivel metrológico, la tolerancia ante condiciones de baja perfusión no se evalúa como un error numérico, sino como la capacidad del equipo para mantener la exactitud de los otros dos parámetros bajo estados de señal degradada, por lo cual su tolerancia en baja perfusión se mantiene en $\pm$ 2% para el SPO2 y la frecuencia de pulso.

Para un monitor como el uMEC 100 se garantiza que, a pesar que el simulador Pronk reduzca drasticamente la amplitud de la onda pulsatil para imitar un choque hemodinámico, los algoritmos internos de filtrado digital aislarán el ruido lo suficienteme bien como para no comprometer ni inflar el error de diganóstico.

