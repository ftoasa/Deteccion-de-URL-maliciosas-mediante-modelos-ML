# Retroalimentación de la práctica 3

El Random Forest fue el mejor modelo porque combina muchos árboles de decisión y aprovecha el voto de cada uno para reducir errores. Sus puntos claves son: maneja muy bien datos con muchas variables y relaciones no lineales, es robusto frente al ruido y a los outliers, evita el sobreajuste gracias al bagging y la aleatoriedad en la selección de atributos, y ofrece la ventaja adicional de calcular la importancia de cada característica, lo que ayuda a entender qué factores del dataset influyen más en la clasificación de URLs maliciosas. 

## Dicho esto se explica los puntos clave para considerar que Random Forest fue el Mejor Modelo para este Dataset:

### 1. ¿Qué es Random Forest?

Es un ensemble (conjunto) de muchos árboles de decisión.
 - Cada árbol se entrena con un subconjunto aleatorio de datos y características.
 - Luego, todos los árboles votan y el resultado final es la mayoría de votos.

Esto lo hace mucho más estable y preciso que un único árbol de decisión.

### 2. Ventajas que explican su buen desempeño

    1. Manejo del desbalance de datos
    - En tu dataset, hay muchísimas URLs benignas y muchas menos de malware.
    - Un árbol de decisión puede sesgarse hacia la clase mayoritaria.
    - Random Forest, al combinar varios árboles entrenados con distintas muestras, reduce ese sesgo y mejora el recall en clases minoritarias (malware, defacement).

    2.	Capacidad de capturar relaciones no lineales
    -	Las features (url_len, número de símbolos, HTTPS, IP) no se combinan de manera lineal.
    -	Random Forest divide el espacio de características en múltiples regiones y detecta patrones complejos, como: “Si la URL no tiene HTTPS y contiene IP y es corta → sospechosa”.

### 3.	Resistencia al overfitting

    - Un solo árbol puede memorizar demasiado los datos de entrenamiento.
    - Random Forest introduce aleatoriedad (submuestras y selección aleatoria de features por árbol).
    - Esto le da mejor generalización a datos nuevos (como tu X_test).

### 4.	Robustez frente a ruido

    - Algunas URLs legítimas pueden parecer sospechosas (ej: acortadores válidos).
    - Random Forest promedia los errores de los árboles individuales, lo que lo hace menos sensible a ejemplos atípicos.

### 5.	Manejo automático de importancia de features

Random Forest internamente calcula qué features son más útiles para clasificar. o En este caso, probablemente encontró que cosas como:
    1. having_ip_address
    2. Shortining_Service
    3. url_len
    4. símbolos como @ o //
Son los que más pesan para diferenciar phishing de benign.
