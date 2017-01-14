# Introducción a la programación

<img src="ElCableAmarillo.png" /><br>
*Fondo Europeo de Desarrollo Regional - Una manera de hacer Europa*



***



En este apartado verás una introducción a los lenguajes de programación de placas de Arduino para utilizar en el aula con tus alumnos.

- [Scratch 4 Arduino](#scratch-4-arduino)
    - [Instrucciones de control](#instrucciones-de-control)
    - [Instrucciones de operación](#instrucciones-de-operación)
    - [Instrucciones de movimiento](#instrucciones-de-movimiento)
    - [Variables](#variables)
- [Arduino IDE](#arduino-ide)
    - [Sintaxis de Processing](#sintaxis-de-processing)
    - [Estructura de un programa en Arduino](#estructura-de-un-programa-en-arduino)
        - [Definición de una variable](#definición-de-una-variable)
        - [Función setup()](#función-setup())
        - [Función loop()](#función-loop())
    - [Instrucciones propias de processing](#instrucciones-propias-de-processing)
        - [Visualización de datos en pantalla](#visualización-de-datos-en-pantalla)
        - [Pausas y retardos](#pausas-y-retardos)
        - [Estructura condicional](#estructura-condicional)
    - [Instrucciones de control de pines](#instrucciones-de-control-de-pines)
    - [Declaración de librerías](#declaración-de-librerías)




***



## Scratch 4 Arduino
### Instrucciones de control
### Instrucciones de operación
### Instrucciones de movimiento
### Variables


<br /><br />


## Arduino IDE

Arduino IDE es un entorno basado en Processing que nos permite programar tarjetas Arduino. Incluye instrucciones y librerías propias que facilita el proceso de programación.

Al ser un lenguaje de programación basado en código (sin entorno visual), tenemos que aprender bien la semántica del lenguaje para minimizar los errores por fallos de escritura. Igualmente debemos tener claros cuales son los errores de sintaxis más comunes para solventar los problemas con celeridad.

<br />

### Sintaxis de Processing

Es importante tener claros las siguientes reglas del lenguaje de programación:
- Las instrucciones son sensibles a las mayúsculas y las minúsculas. Es decir, si una instrucción está definida dentro de processing con una letra en mayúsucla o minúscula debemos respetarlo o por el contrario nos devolverá un mensaje de error.
- Toda línea termina en un ; (punto y coma) excepto las estructuras de control que se acompañan con unas {} (llaves).

Para familiarizarnos con la sintaxis vamos a realizar un repaso por las instrucciones más habituales con sencillos ejemplos.

<br />

### Estructura de un programa en Arduino

Todo programa para Arduino realizado en Processing, consta de la siguiente estructura:

```
//Decclaración de variables 
Variable 1
Variable 2
...
Variable N

//La función setup() es la primera función en ejecutarse, una sola vez
void setup (){
    Instrucción 1
    Instrucción 2
    ...
    Instrucción N
}

// La función loop() se ejecuta repetidamente en bucle infinito
void loop (){
    Instrucción 1
    Instrucción 2
    ...
    Instrucción N
}
```


#### Definición de variables

En la realización de nuestros programas puede ser de utilidad el uso de *variables*, por ejemplo, para almacenar datos proporcionados por sensores.

Una variable es una zona de memoria donde vamos a guardar un valor. A esta variable le asignaremos un nombre para poder acceder al valor encualquier parte de nuestro código. Los tipos de datos que vamos a utilizar en esta introducción a la programación son los siguientes:

```
int numero_entero = 13;

float numero_decimal = 3.141516;

boolean numero_bool = true;

String cadena = “¡Hola Mundo!”
```

NOTA: Para más información sobre tipos de datos primitivos en Arduino, visita el siguiente [link](http://playground.arduino.cc/ArduinoNotebookTraduccion/Datatypes).


#### Función setup()

La función *setup()* es la primera función que se ejecuta en nuestro programa, ejecutándose sólo una vez, y se utiliza para `configurar la comunicación` con nuestro equipo, `inicializar los pines` de nuestra tarjeta de Arduino e `inicialización de las variables`.

```
void setup (){
    Serial.begin(9600);
    pinMode(13, OUTPUT);
    mi_variable = 18;
}
```


#### Función loop()

La función *loop()* se ejecuta repetidamente después de la función setup(). Dentro de la misma vamos a introducir el programa que queremos ejecutar dentro de la placa de Arduino. 

```
void loop (){
    Serial.println("¡Hola mundo!");
    digitalWrite(13, HIGH);
    delay(1000);
}
```

<br />

### Instrucciones propias de processing
#### Visualización de datos en pantalla
#### Pausas y retardos
#### Estructura condicional
### Instrucciones de control de pines
### Declaración de librerías



<br /><br />



***



#### Licencia

<img src="http://i.creativecommons.org/l/by-sa/4.0/88x31.png" /> Esta obra se distribuye bajo licencia [Reconocimiento-CompartirIgual 4.0 Internacional (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.es_ES).
