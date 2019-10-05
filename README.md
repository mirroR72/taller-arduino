# Como Empezar

## Instalar Software

1. Windows/OSX: Instalar [drivers de USB CH340G](drivers/) (Linux vienen por defecto)
2. Instalar [Arduino IDE](https://www.arduino.cc/en/main/software)

## Conectar el Arduino

1. Conectar el Arduino por USB
2. Ir a Herramientas y selecionar `Arduino Nano`, `ATMEGA328P`, y el puerto que corresponda.

![img/herramientas.png](img/herramientas.png)

## Para subir un codigo basico al Arduino

1. Ir a Fichero > Ejemplos > Basics > Blink
2. 'Subir' codigo al Arduino

![img/examples.blink.png](img/examples.blink.png)
![img/subir.png](img/subir.png)

# Herramientas: Arduino Nano

El nano **tiene un LED ya conectado** con el pin 13 con la letra 'L', se puede cambiar la velocidad con el programa de 'blink'

![img/blink.jpg](img/blink.jpg)

# Herramientas: Placa

Se usa para conectar componentes. Se puedan crear **varias conexiones en cada uno de los pines**.

![img/breadboard.front-back.jpg](img/breadboard.front-back.jpg)

# Primer Circuito: Blink

1. Conectar LED al pin D13: *PATA LARGA* es *POSITIVO* y va hacia el ARDUINO
2. La *PATA CORTA* del LED se conecta con el *NEGATIVO* y as su vez, con el pin GND (Groud = Tierra = Negativo).
3. Se puede usar una resistencia de 330 Ohm en el LED D13 pero es opcional, ya que el Arduino ya lleva una internamente.

![img/1.blink.jpg](img/1.blink.jpg)

# Segundo Circuito: Fotoresistencia

![img/examples.analoginoutserial.png](img/examples.analoginoutserial.png)

1. Conectar Fotoresistencia a cualquier pin A0-A7.
2. Usar `int valor = analogRead(A0);` para leer el valor de la fotoresistencia.
3. Abrir `Herramientas > Monitor de Serie` para ver los valores que manda la fotoresistencia al PC por USB

![img/2.photoresistor.gif](img/2.photoresistor.gif)

# Tercer Circuito: Zumbador (Buzzer)

![img/examples.tonepitchfollower.png](img/examples.tonepitchfollower.png)

1. Conectar el Zumbador a un pin con PWM (Ver [#pinout](#Pinout))
2. Usar `tone(PIN, FREQUENCY, DURATION)` para generar un tono basado en la fotoresistencia.

![img/3.buzzer.png](img/3.buzzer.png)

## Pinout

![img/nano.pinout.jpg](img/nano.pinout.jpg)
