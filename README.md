# Simulación y Monitoreo de Variables Cardiovasculares y Hemodinámicas

Samuel Joel Peña Rojas

Vanessa Vera Caro

Daniel Leonardo López Castillo


## Monitor de signos vitales uMEC 100

El Mindray uMEC 100 es un monitor multiparámetro de signos vitales con una configuración robusta y portátil, diseñado para la monitorización continua y ambulatoria de pacientes adultos, pediátricos y neonatales, tanto en entornos hospitalarios como durante el traslado de pacientes.

<div align="center">
<img width="413" height="304" alt="image" src="https://github.com/user-attachments/assets/8fe99d7a-ab0e-47ac-b050-c1e52ed2f835" />
</div>

Este equipo es capaz de procesar múltiples señales bioeléctricas y fisiológicas en tiempo real, permitiendo la medición de variables como el electrocardiograma (ECG), la respiración por impedancia, la presión arterial, la temperatura y la frecuencia de pulso. Adicionalmente, incorpora algoritmos de filtrado digital destinados a la extracción de la señal fotopletismográfica (PPG), cuya tecnología se encuentra optimizada para minimizar los principales artefactos que afectan la calidad de la lectura clínica, tales como el movimiento del paciente y la baja perfusión tisular.

Un aspecto destacado de este monitor es su sistema inteligente de alarmas, el cual integra alertas visuales y acústicas clasificadas en tres niveles de criticidad: alta, media y baja. Estas alarmas se dividen en dos categorías principales:

- *Alarmas fisiológicas:* Se activan cuando los parámetros fisiológicos del paciente exceden los límites configurados, como en casos de bradicardia o desaturación de oxígeno.
- *Alarmas técnicas:* Corresponden a eventos relacionados con fallas del sistema, incluyendo problemas de hardware, desconexión de sensores o interferencias en la adquisición de la señal.


## Simulador de parámetros hemodinámicos Pronk OxSim OX-1

El Pronk OxSim OX-1 es un analizador metrológico y simulador óptico miniaturizado de oximetría de pulso (SpO₂), diseñado específicamente para la verificación funcional, el mantenimiento preventivo y la calibración de monitores de signos vitales, tanto en entornos clínicos como de laboratorio.

<div align="center">
<img width="371" height="421" alt="image" src="https://github.com/user-attachments/assets/72f40dd7-b815-4e4b-9b93-74ff39f12bfd" />
</div>

Este dispositivo incorpora un bloque de prueba óptico permanente con forma de “dedo índice”, el cual intercepta activamente los destellos de luz infrarroja emitidos por los LED del sensor del Mindray uMEC 100. Posteriormente, procesa electrónicamente la señal para calcular la sincronía del pulso y devuelve pulsos de luz controlados hacia el fotodetector del sensor, con el propósito de simular la absorción óptica característica de un tejido biológico vivo.

La tecnología implementada por el Pronk OxSim OX-1 permite identificar automáticamente las características ópticas del sensor conectado, incluyendo tecnologías como Masimo, Nellcor y Mindray. Gracias a ello, el equipo ajusta de manera automática las curvas internas de calibración y simulación, garantizando una alta precisión sin necesidad de adaptadores externos.

Adicionalmente, el dispositivo posee un chasis de policarbonato de alta resistencia y una interfaz de usuario minimalista, controlada mediante dos botones ubicados en el panel frontal: el botón *Mode* y el botón *Sensor*. Estos permiten alternar entre diferentes modos de simulación fisiológica y patológica.

# PARTE A

## Colocación del uMEC 100 en modo "monitor"

El modo “Monitor” del Mindray uMEC 100 corresponde al estado operativo predeterminado del equipo al momento de su encendido. Dependiendo de la condición previa en la que se encuentre el monitor dentro del laboratorio, es necesario realizar distintos procedimientos antes de iniciar su utilización, tales como:

<div align="center">
<img width="400" height="250" alt="image" src="https://github.com/user-attachments/assets/9f94c2df-a964-4763-9e7a-4e62a92ba332" />
</div>

**1. Estado de apagado (inicio normal)**

Para iniciar el funcionamiento del equipo, se debe presionar el botón físico de encendido/apagado ubicado en la parte inferior derecha del monitor. Posteriormente, el indicador de encendido se iluminará, el sistema emitirá un sonido correspondiente a la autocomprobación y la pantalla mostrará de manera inmediata la interfaz principal de usuario.

En dicha interfaz se presentan los espacios destinados a la visualización de las ondas bioeléctricas y los valores numéricos asociados a los diferentes parámetros fisiológicos. Una vez conectados los sensores correspondientes, el monitor inicia automáticamente el proceso de adquisición, procesamiento y análisis de señales en tiempo real.

**2. Estado de espera (Sandby)**

El modo de espera se utiliza para pausar la monitorización sin necesidad de apagar el equipo. En este estado, la pantalla permanece apagada mientras el indicador de energía continúa activo. Para retornar al modo monitor, se debe girar la perilla de navegación o presionar cualquier tecla física del panel frontal; posteriormente, el equipo saldrá inmediatamente del estado de espera y volverá de forma automática a la interfaz principal de monitorización.

**3. Estado de demostración (Demo)**

En caso de que el monitor se encuentre mostrando ondas simuladas pregrabadas, identificadas mediante la palabra “DEMO” en pantalla, se debe realizar el siguiente procedimiento:

- Presionar la tecla física correspondiente al menú principal.
- Seleccionar la opción de mantenimiento o configuración del sistema.
- Acceder a la sección de mantenimiento de usuario e ingresar la contraseña de fábrica del sistema del Mindray uMEC 100.
- Dentro del menú desplegado, ubicar la opción “Modo Demo” y cambiar su estado a “Desactivado”.

## Parámetros y variables fisiológicas simuladas con el Pronk OxSim OX-1

El OxSim OX-1 posee un bloque óptico activo (dedo de prueba) y a través de él es capaz de simular tres parámetros o variables fisiológicas controlando la atenuación de la luz en tiempo real.

<div align="center">
<img width="250" height="350" alt="image" src="https://github.com/user-attachments/assets/97dbf281-c784-4b6c-bc19-c21062692e8f" />
</div>

1. Saturación Periférica de Oxigeno (SPO2)

Esta variable simula el porcentaje de hemoglobina unida de manera reversible al oxígeno en la sangre arterial del paciente, a partir de la relación de absorción de luz roja (660 nm) e infrarroja (940 nm) a través del tejido perfundido. Para ello, el Pronk OxSim OX-1 recibe las dos longitudes de onda emitidas por el sensor del Mindray uMEC 100 y modifica electrónicamente la cantidad de luz devuelta al fotodetector, permitiendo simular valores de saturación fijos y precisos.

Esto posibilita la evaluación de las alarmas de hipoxia y la verificación de la exactitud del monitor de signos vitales. Los puntos de simulación disponibles en el OX-1 corresponden a valores de 85 %, 95 %, 98 % y 99 % de saturación de oxígeno.

<div align="center">
<img width="443" height="273" alt="image" src="https://github.com/user-attachments/assets/9c7901aa-dd15-4f57-b362-96baf3377f1b" />
</div>

2. Frecuencia de pulso (PR)/ frecuencia cardíaca (HR)

Este parámetro representa la cantidad de pulsaciones de la onda de presión arterial por minuto (bpm), originadas por la sístole ventricular izquierda y propagadas hacia el lecho capilar periférico. Para simular este comportamiento fisiológico, el Pronk OxSim OX-1 genera variaciones cíclicas en la intensidad de la luz devuelta al sensor del Mindray uMEC 100, donde cada ciclo corresponde a un pulso arterial volumétrico.

Mediante la modificación del intervalo temporal entre dichas variaciones, el simulador puede reproducir con precisión distintos estados de ritmo cardíaco, permitiendo evaluar la respuesta del monitor ante condiciones de bradicardia o taquicardia. Los puntos fijos de simulación disponibles corresponden a frecuencias de 40, 80 y 140 bpm.

<div align="center">
<img width="436" height="273" alt="image" src="https://github.com/user-attachments/assets/731c2c1c-eb55-494b-80ab-0633e078c2e4" />
</div>

3. Índice de perfusión tisular (Modo de baja perfusión)

El parámetro de índice de perfusión corresponde a la relación entre el componente pulsátil de la sangre arterial y el componente estático asociado a los tejidos, el hueso y la sangre venosa presentes en el sitio de medición. En condiciones normales de perfusión, la señal pulsátil (componente AC) presenta una amplitud robusta; sin embargo, en estados de baja perfusión, el tamaño de esta onda disminuye considerablemente.

En el modo de baja perfusión, el Pronk OxSim OX-1 reduce la amplitud de la señal pulsátil a niveles críticamente bajos respecto al componente estático, manteniendo constantes la frecuencia cardíaca y la saturación de oxígeno, configuradas por defecto en 99 % y 80 bpm, respectivamente.

Esta función permite evaluar la eficacia de los algoritmos de amplificación y filtrado implementados en el Mindray uMEC 100 frente a condiciones de compromiso hemodinámico severo, verificando la capacidad del sistema para mantener mediciones precisas aun en escenarios de perfusión periférica reducida.

<div align="center">
<img width="445" height="273" alt="image" src="https://github.com/user-attachments/assets/d63cff13-c441-43cc-aac2-1129d9b3db63" />
</div>

## Tolerancias o errores permitidos para cada parámetro

Para determinar los errores máximos permitidos del equipo, es necesario verificar las especificaciones técnicas proporcionadas por el fabricante. Al contrastar los lineamientos establecidos en las normas internacionales para dispositivos médicos, particularmente la norma ISO 80601-2-61 para equipos de oximetría de pulso, con los valores de diseño especificados en el manual de usuario de la serie Mindray uMEC 100, se establecen los siguientes límites de error permitidos:

**1. Saturación periférica de oxígeno (SpO₂):** El error máximo permitido (EMP) para la medición de la saturación de oxígeno varía según la tecnología integrada en el sensor configurado y el grupo etario del paciente. De acuerdo con el manual de Mindray uMEC 100, se establecen los siguientes valores de EMP para el rango operativo comprendido entre 70 % y 100 % de saturación:

- Pacientes adultos y pediátricos: **$\pm$ 2%**
- Pacientes Neonatales: **$\pm$ 3%**

Es importante mencionar que el fabricante establece que, para valores inferiores al 70 % de saturación, la exactitud de la medición se considera “no especificada”. Desde el punto de vista clínico, esto se debe a que los comités de ética médica no permiten someter a pacientes humanos a niveles de hipoxia tan severos con el propósito de calibrar o validar de manera absoluta las curvas ópticas empleadas en los sistemas de oximetría de pulso.

2. Frecuencia de pulso

Las tolerancias de diseño electrónico del monitor de signos vitales establecen un margen sumamente estricto para este parámetros hemodinámico.

- Error Máximo Permitido: **$\pm$ 2bpm** o **$\pm$ 2%**

Esto significa que, si el simulador entrega una frecuencia cardíaca de 40 bpm, el monitor puede registrar valores comprendidos entre 38 y 42 bpm sin exceder el margen de error permitido. De igual manera, si se simula un estado de taquicardia de 140 bpm, el 2 % de tolerancia corresponde a un margen de ±2.8 bpm; por lo tanto, el monitor se considerará dentro de especificación si presenta lecturas entre 137 y 143 bpm.

3. Índice de perfusión tisular (mmodo de baja perfusión)

Desde el punto de vista metrológico, la tolerancia en condiciones de baja perfusión no se evalúa mediante un error numérico independiente, sino a partir de la capacidad del equipo para conservar la exactitud de los demás parámetros bajo condiciones de señal degradada. Por esta razón, las tolerancias especificadas en estado de baja perfusión se mantienen en ±2 % para la medición de SpO₂ y para la frecuencia de pulso.

En el caso del Mindray uMEC 100, se garantiza que, aun cuando el Pronk OxSim OX-1 reduzca drásticamente la amplitud de la onda pulsátil con el fin de simular un estado de choque hemodinámico, los algoritmos internos de filtrado digital serán capaces de aislar el ruido de manera eficiente, evitando comprometer o incrementar el error diagnóstico del sistema.

# PARTE B
En esta parte B se muestran los resultados obtenidos tras seguir el paso a paso de la guía de laboratorio.

| Prueba | Límite              | Valor Simulado bpm | Valor Simulado SpO2 | Valor Medido bpm | Valor Medido SpO2 | Alarma Activa | Tiempo de Respuesta (s) | Error Absoluto SpO2 | Error Absoluto bpm | Error Porcentual SpO2 | Error Porcentual bpm |
|--------|----------------------|--------------------|---------------------|------------------|-------------------|----------------|--------------------------|----------------------|--------------------|------------------------|----------------------|
| 1 |  | 40  | 95 | 40  | 96 | No |  | 1 | 0 | 1% | 0% |
| 2 | Inferior SpO₂ = 90% | 80  | 85 | 80  | 85 | Sí | 4,3 | 0 | 0 | 0% | 0% |
| 3 | Superior SpO₂ = 97% |  | 99 |  | 100 | Sí | 3 | 1 |  | 1% |  |
| 4 |  | 140 | 98 | 140 | 99 | Sí | 4,6 | 0 | 0 | 0% | 0% |


En la tabla anterior se muestran los valores simulados con el simulador de parámetros hemodinámicos Pronk OxSim OX-1 y los valores medidos con el monitor de signos vitales uMEC 100, así como también sus respectivos tiempos de respuesta y errores obtenidos. Posteriormente, se realizará una breve explicación de cada una de las pruebas, además de adjuntar las imágenes de evidencia correspondientes.

## Prueba 1
Inicialmente, en la primera prueba se configuró el simulador Pronk OxSim OX-1 para representar un paciente con bradicardia, estableciendo una frecuencia cardíaca de 40 bpm y una saturación de oxígeno de 95%.

<div align="center">
<img width="500" height="400" alt="image" src="https://github.com/user-attachments/assets/882b0e4b-c188-492a-ace1-002bd6dece8b" />
</div>

Posteriormente, se verificaron en el monitor uMEC 100 los valores mostrados y se compararon con los valores simulados para calcular el error absoluto y porcentual de cada variable.

$$
\text{Error absoluto SpO}_2 = |95 - 96| = 1
$$

$$
\text{Error porcentual SpO}_2 =
\frac{|95 - 96|}{95}\times100 = 1{,}05\%
$$

$$
\text{Error absoluto bpm} = |40 - 40| = 0
$$

$$
\text{Error porcentual bpm} =
\frac{|40 - 40|}{40}\times100 = 0\%
$$

Además de esto, en la onda fotopletismográfica se puede observar que la señal se vuelve mucho más lenta, lo cual coincide con la baja frecuencia cardíaca simulada. También se evidenció la activación de la alarma “FP < 50”, indicando una frecuencia cardíaca baja. Es importante mencionar que este límite de alarma no fue configurado durante la práctica, sino que ya venía preestablecido en el equipo.

## Prueba 2

En la segunda prueba se configuró el monitor con un límite inferior de alarma de SpO₂ de 90%. Posteriormente, el simulador se ajustó a una frecuencia cardíaca de 80 bpm y una saturación de oxígeno de 85%. Luego, el equipo registró valores de 80 bpm y 85% respectivamente, por lo que tanto el error absoluto como el error porcentual fueron iguales a 0, como se observa en la tabla.

<div align="center">
<img width="200" height="300" alt="image" src="https://github.com/user-attachments/assets/ac340bd9-fa18-4b33-925d-68e8ecc576e1" />
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/7ed02675-db92-4a95-8565-67b38f5004fd" />
</div>

En las imágenes anteriores se aprecia que, en esta prueba, la señal fotopletismográfica se visualiza un poco más rápida en comparación con la prueba anterior, lo cual indica el aumento de la frecuencia cardíaca. Además, en la siguiente imagen se puede observar la activación de la alarma visual configurada de “SpO₂ < 90%”, lo cual es coherente, ya que el valor de saturación simulado fue de 85%.

<div align="center">
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/a62e5cfb-337f-47ab-8373-9b5b848c3dfa" />
</div>

## Prueba 3

En la tercera prueba se configuró el monitor con un límite superior de alarma de SpO₂ de 97%. Posteriormente, el simulador se ajustó a una saturación de oxígeno de 99% en modo *Low Perfusion*. Se verificó la activación de la alarma visual del monitor y se registraron los valores mostrados por el equipo para calcular los errores absoluto y porcentual.

De acuerdo con los resultados obtenidos, el monitor registró una saturación de oxígeno de 100%, mientras que el valor simulado fue de 99%. Esto generó un error absoluto de 1 y un error porcentual aproximado de 1%, como se muestra en la tabla.

<div align="center">
<img width="350" height="250" alt="image" src="https://github.com/user-attachments/assets/71c6551c-1683-423e-9e33-a5ae8a8004d6" />
<img width="380" height="250" alt="image" src="https://github.com/user-attachments/assets/42cf0535-0262-49fd-aaf0-ff2478156653" />
</div>

En las imágenes anteriores, la primera corresponde a los valores registrados por el monitor durante la simulación, donde se puede observar una saturación de oxígeno de 100%. Respecto a la evidencia de la alarma visual configurada para esta prueba, lamentablemente no se tomó una fotografía en el momento de su activación.

Por esta razón, se recurrió a una imagen obtenida durante la prueba 4, la cual se describirá posteriormente. En dicha prueba, la saturación simulada fue de 98%, valor que también supera el límite de alarma establecido de 97%, permitiendo evidenciar el correcto funcionamiento y la activación visual de la alarma configurada.

## Prueba 4

En la cuarta y última prueba se configuró el simulador para generar una taquicarda, estableciendo una frecuencia cardíaca de 140 bpm y una saturación de oxígeno de 98%. En este caso, el monitor registró valores de 140 bpm y 98% respectivamente, por lo que tanto el error absoluto como el error porcentual fueron iguales a 0, como se observa en la tabla.

<div align="center">
<img width="500" height="350" alt="image" src="https://github.com/user-attachments/assets/fe477e8b-297d-4df0-85f2-d2e04744fe7d" />
</div>


Finalmente, como se aprecia en la imagen, se evidencia la activación de la alarma por frecuencia cardíaca elevada. El monitor estaba configurado con un límite superior de 140 bpm, pero como el simulador no permitía superar ese valor, se ajustó el umbral a 120 bpm para poder comprobar su funcionamiento. Con este cambio, se verificó que la alarma responde correctamente, ya que al simular una frecuencia de 140 bpm, esta se activó de manera adecuada.

Además, se puede ver que la señal fotopletismográfica va tomando una forma cada vez más parecida a una onda senoidal. Esto pasa porque a esta frecuencia tan alta los latidos o pulsos ocurren muy seguidos entre sí, casi sin tiempo de separación. Por esta razón, ya no es fácil distinguir detalles característicos de la señal como el nodo dicrótico o la forma típica que normalmente se observa en condiciones de más baja frecuencia.

# Parte C

## 1. ¿Cuál es el principio de operación del Pronk OxSim OX-1 para simular una onda pulsátil?

El Pronk OxSim OX-1 simula la onda pulsátil mediante un principio de interacción óptica con el sensor del monitor. El dispositivo intercepta la luz emitida por los LED rojo e infrarrojo del pulsioxímetro y regula electrónicamente la cantidad de luz que regresa al fotodetector. Al generar variaciones cíclicas en esta señal luminosa, reproduce un patrón equivalente al comportamiento de la sangre arterial, haciendo que el monitor interprete estos cambios como pulsaciones reales.

## 2. ¿Por qué la SpO₂ baja puede ser un falso positivo (falsa alarma) en una situación de mala perfusión?

En condiciones de mala perfusión, el flujo sanguíneo en la zona de medición disminuye, lo que debilita la señal pulsátil utilizada por el pulsioxímetro para calcular la saturación de oxígeno. Esto dificulta que el equipo distinga correctamente la señal arterial del ruido o de otras componentes no pulsátiles.

Como resultado, el monitor puede interpretar de forma incorrect la señal y mostrar valores de SpO₂ más bajos de lo real, generando una falsa alarma de desaturación aunque la oxigenación del paciente no esté realmente comprometida.

## Conclusión

Finalmente, se logró utilizar de manera correcta tanto el simulador Pronk OxSim OX-1 como el monitor de signos vitales uMEC 100, permitiendo comprender su funcionamiento conjunto en la simulación de variables hemodinámicas. A través de las diferents pruebas realizadas, se evidenció que el sistema responde adecuadamente a cambios en frecuencia cardíaca, saturación de oxígeno y condiciones de perfusión, así como la correcta activación de las alarmas configuradas.

Además, se verificó la precisión del equipo al comparar los valores simulados con los medidos, obteniendo errores dentro de los rangos permitidos según la normativa. En general, la práctica permitió reforzar el uso adecuado del simulador y del monitor, así como la interpretación de señales fisiológicas en un entorno controlado.


# REFERENCIAS

[1]	Shenzhen Mindray Bio-Medical Electronics Co., Ltd., uMEC 60/uMEC 70/uMEC 80/uMEC 100/uMEC 120/uMEC 150 Patient Monitor Operator's Manual, rev. 2.0, P/N 046-026551-00(2.0), Shenzhen, China, 2023.

[2]	Pronk Technologies, "OxSim OX-1 Optical SpO2 Pulse Oximeter Tester," pronktech.com. https://www.pronktech.com/product/ox-1-oxsim-miniaturized-optical-spo2-pulse-oximeter-tester/ (accedido el 28 de mayo, 2026).

[3]	Medical Electrical Equipment - Part 2-61: Particular Requirements for Basic Safety and Essential Performance of Pulse Oximeter Equipment, ISO Standard 80601-2-61:2017(E), 2017.


