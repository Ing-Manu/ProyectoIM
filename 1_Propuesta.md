---
layout: page
title: Propuesta de mejora
---


Debido a que Cast-Metal es una empresa de tamaño pequeño y es de creación muy reciente, tiene oportunidades de mejora sencillas y de bajo costo.
A continuación se presentan tales oportunidades de mejora:

* Diseño de los moldes:
El proceso de fabricación de los moldes actualmente se lleva a cabo sin tener en cuenta los ángulos de extracción de la pieza, la presencia del pozo, de las mazarotas ni de los rebosaderos. Por lo tanto se propone hacer los moldes teniendo en cuenta los elementos anteriormente mencionados con el fin de mejorar la calidad de las piezas y su repetibilidad.

* Control de calidad de la arena:
En el momento, la arena se adquiere a granel y a diferentes proveedores. Entonces, se propone adquirir la arena de un único proveedor y, además, realizar pruebas de humedad de la arena con el fin de mantener su permeabilidad y que todos los moldes tengan la misma calidad.
La prueba de humedad se lleva a cabo así:

Tomar de 20 a 50 g de arena lista para el molde.

Calentar la muestra hasta que se evapore todo el contenido de agua.

Pesar la muestra sin humedad y calcular:

![EcHum](/assets/img/EcHum.jpg)


La prueba se lleva a cabo teniendo en cuenta que la arena debería tener un contenido de humedad de entre el 30 % y el 35 %.

* Sistema de control de los hornos:
El proceso de fundición se lleva a cabo sin poder usar ambos hornos a la vez y sin control de la temperatura, en consecuencia se propone un sistema de control basado en el PLC Siemens LOGO! 8 (Ver la sección x de la página).

* Seguridad industrial:
Durante el tiempo que ha estado funcionando la empresa, al operario de los hornos no se le ha proporcionado los elementos de protección personal necesarios para llevar a cabo tal labor. Así pues, la propuesta es adquirir tal dotación para prevenir accidentes que puedan resultar en costos económicos y legales, los cuales serían muy superiores al precio de tal dotación.

# Sistema de control

El sistema propuesto para controlar la temperatura de los hornos y automatizar su uso es el siguiente:

Tal sistema tiene el siguiente funcionamiento:
* Entradas:
  + Parada de emergencia:
    Este botón tiene la finalidad de ser utilizado en caso de emergencia. Al ser accionado por una persona interrumpe toda la actividad que el PLC esté llevando a cabo, en consecuencia apagando los hornos.
  + Sensores de temperatura:
    Estos sensores tienen el objetivo de sensar la temperatura de los hornos para que el PLC pueda controlar el paso de gas y su ignición.
* Control:
  + El PLC Siemens LOGO! 8 es el encargado de recibir las señales de entrada y procesarlas para posteriormente enviar las respectivas señales de salida.
  + La HMI Siemens LOGO! TDE es la interfaz mediante la cual el operario podrá configurar los hornos.
* Salidas:
  + Luz de emergencia:
    Esta luz se activará cuando el botón de parada de emergencia sea accionado, emitiendo luz roja y sonido. Es particularmente útil porque el entorno de la empresa puede ser ruidoso, así que tener una señal visual es acertado.
  + Contactores:
    Estos actuadores son los encargados de encender o apagar los sopladores de los hornos si están o no en servicio.
  + Bujías:
    Estos son los actuadores encargados de iniciar el proceso de combustión del gas natural cuando se abra el paso del mismo hacia los hornos.
  + Válvulas solenoide:
    Estas válvulas son las encargadas de regular el paso del gas natural hacia los hornos según sea requerido para mantener la temperatura de forma controlada y en el valor requerido por el proceso.

El sistema de control expuesto anteriormente tiene aproximadamente los siguientes costos:

![CostosC](/assets/img/CostosControl.jpg)

Estos costos son aproximados ya que hace falta el cableado, los rieles DIN y en gabinete para el tablero.
