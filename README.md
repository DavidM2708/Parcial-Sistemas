# Parcial-Sistemas

# Parcial de Sistemas Digitales


## Latch vs Flip-Flop

### Latch

* Dispositivo sensible al nivel de una señal de control.
* Mientras está activo, la salida sigue la entrada.
* Es rápido pero menos controlado.

### Flip-Flop

* Dispositivo sensible al flanco del reloj.
* Cambia solo en un instante específico.
* Más estable en sistemas digitales.

### Tipos

**Latches:**

* SR
* D

**Flip-Flops:**

* SR
* D
* JK
* T


## Multiplexor y Demultiplexor

### Multiplexor 

Selecciona una entrada entre varias y la envía a una sola salida.

**Ejemplo 8:1**

* Entradas: D0–D7
* Selectores: S0, S1, S2
* Salida: Y

Funcionamiento:

* S = 101 - Y = D5


### Demultiplexor 

Distribuye una entrada hacia una de varias salidas.

**Ejemplo 1:8**

* Entrada: D
* Selectores: S0, S1, S2
* Salidas: Y0–Y7

Funcionamiento:

* S = 010 → Y2 = D


## Sumadores y Circuitos Secuenciales

### Sumador Medio

* Suma 2 bits
* Salidas:

  * Suma (S)
  * Acarreo (C)


### Sumador Completo

* Suma 3 bits (A, B, Cin)
* Salidas:

  * Suma (S)
  * Acarreo (Cout)


### Circuitos Secuenciales

* Dependen del estado anterior
* Utilizan memoria (latches y flip-flops)
* Ejemplos:

  * Contadores
  * Registros
  * Máquinas de estado


## Mapa de Karnaugh

### ¿Qué es?

Es una herramienta gráfica para simplificar funciones booleanas.

### ¿Para qué sirve?

* Reducir expresiones lógicas
* Minimizar compuertas
* Optimizar circuitos digitales

### Funcionamiento

1. Se llena con la tabla de verdad
2. Se agrupan los valores (1) en bloques
3. Se obtiene una expresión simplificada


# Análisis de Ecuación Lógica

## Ejercicio 2.a

Se analiza la siguiente ecuación booleana:

X = [ A B̅ ((C + BD) + A̅B̅) ] C


## Simplificación paso a paso

### 1. Expandir la expresión interna

(C + BD) + A̅B̅

= C + BD + A̅B̅


### 2. Multiplicar por A B̅

A B̅ (C + BD + A̅B̅)

Distribuyendo:

= A B̅ C + A B̅ BD + A B̅ A̅B̅


### 3. Simplificar términos

- A B̅ BD = 0  (porque B·B̅ = 0)  
- A B̅ A̅B̅ = 0 (porque A·A̅ = 0)

Entonces:

= A B̅ C



### 4. Multiplicar por C

X = (A B̅ C) C

X = A B̅ C


## Resultado final simplificado

X = A B̅ C


## Circuito lógico

La ecuación final requiere:

- 1 compuerta NOT (para B)
- 1 compuerta AND de 3 entradas


## Imagen del circuito

_Agrega aquí la captura de tu circuito desde Tinkercad_

![Circuito lógico](ruta_de_la_imagen.png)


## 🛠️ Construcción del circuito en Tinkercad (Paso a paso)

1. Ingresar a Tinkercad → Circuits  
2. Crear un nuevo circuito  
3. Agregar los siguientes componentes:
   - 3 interruptores (A, B, C)
   - 1 compuerta NOT
   - 1 compuerta AND de 3 entradas  
     (o 2 AND de 2 entradas)
   - 1 LED
   - 1 resistencia de 220Ω



### 🔧 Conexiones

**Paso 1: Invertir B**
- B → NOT → B̅

**Paso 2: Compuerta AND**
- A → AND  
- B̅ → AND  
- C → AND  

**Paso 3: Salida**
- Salida AND → LED



### ✅ Funcionamiento

El LED se enciende únicamente cuando:

A = 1  
B = 0  
C = 1  



## 📊 Tabla de verdad

| A | B | C | D | B̅ | X |
|---|---|---|---|----|---|
| 0 | 0 | 0 | 0 | 1  | 0 |
| 0 | 0 | 1 | 0 | 1  | 0 |
| 0 | 1 | 0 | 0 | 0  | 0 |
| 0 | 1 | 1 | 0 | 0  | 0 |
| 1 | 0 | 0 | 0 | 1  | 0 |
| 1 | 0 | 1 | 0 | 1  | 1 |
| 1 | 1 | 0 | 0 | 0  | 0 |
| 1 | 1 | 1 | 0 | 0  | 0 |





