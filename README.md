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

