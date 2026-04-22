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


## Simplificación

### 1.

(C + BD) + A̅B̅

= C + BD + A̅B̅


### 2. Multiplicar por A B̅

A B̅ (C + BD + A̅B̅)

Distribuyendo:

= A B̅ C + A B̅ BD + A B̅ A̅B̅


### 3. Simplificar los términos

- A B̅ BD = 0  (porque B·B̅ = 0)  
- A B̅ A̅B̅ = 0 (porque A·A̅ = 0)

Entonces:

= A B̅ C



### 4. Multiplicar por C

X = (A B̅ C) C

X = A B̅ C


## Resultado final 

X = A B̅ C


## Circuito lógico

La ecuación final requiere:

- 1 compuerta NOT (para B)
- 1 compuerta AND de 3 entradas




## Construcción del circuito en Tinkercad (Paso a paso)
 
 Componentes:
   - 3 interruptores (A, B, C)
   - 1 compuerta NOT
   - 1 compuerta AND de 3 entradas  
     (o 2 AND de 2 entradas)
   - 1 LED
   - 1 resistencia de 220Ω



### Conexiones

**Paso 1: Invertir B**
- B - NOT - B̅

**Paso 2: Compuerta AND**
- A - AND  
- B̅ - AND  
- C - AND  

**Paso 3: Salida**
- Salida AND - LED



### Funcionamiento

El LED se enciende únicamente cuando:

A = 1  
B = 0  
C = 1  

## Imagen del circuito

_Agrega aquí la captura de tu circuito desde Tinkercad_

![Circuito lógico](ruta_de_la_imagen.png)

## Tabla de verdad

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


# Chatbot de Sistemas Digitales y Semiconductores

## 1. Análisis de la temática de los semiconductores en el año 2026

En el año 2026, los semiconductores se consolidan como la base fundamental de la transformación digital global. La creciente demanda de tecnologías como la inteligencia artificial, el Internet de las cosas (IoT), los vehículos autónomos y la computación en la nube ha impulsado el desarrollo de chips más potentes, eficientes y pequeños.

Además, se observa una fuerte inversión en investigación para superar los límites físicos del silicio, explorando materiales alternativos y nuevas arquitecturas como los chips 3D.

Asimismo, la industria enfrenta desafíos importantes como la escasez de materiales, tensiones geopolíticas y la necesidad de cadenas de suministro más resilientes. En este contexto, los países y empresas buscan mayor independencia tecnológica, lo que ha incrementado la construcción de fábricas de semiconductores en distintas regiones del mundo.


## 2. Empresas más relevantes del sector y su impacto en los sistemas digitales

Entre las empresas más influyentes del sector destacan Intel, TSMC, NVIDIA, Samsung y AMD. Estas compañías lideran el diseño y fabricación de semiconductores que hacen posible el funcionamiento de los sistemas digitales modernos.

Intel continúa desarrollando procesadores para computadoras y servidores, influyendo directamente en el rendimiento de los sistemas informáticos. TSMC es clave en la fabricación de chips avanzados para múltiples empresas tecnológicas, siendo un pilar en la cadena de producción global. NVIDIA se ha posicionado como líder en el desarrollo de GPUs para inteligencia artificial y procesamiento gráfico, esenciales en sistemas digitales complejos. Samsung, además de fabricar chips de memoria, impulsa la innovación en dispositivos móviles y almacenamiento. AMD compite en el mercado de procesadores de alto rendimiento, ofreciendo soluciones eficientes para computación avanzada.

El impacto de estas empresas en los sistemas digitales es significativo, ya que sus tecnologías permiten mayor velocidad de procesamiento, eficiencia energética y capacidad de manejo de grandes volúmenes de datos.

## Código del Chatbot (Python)

```python
import requests

API_KEY = 'TU_API_KEY_AQUI'
API_URL = 'https://api.deepseek.com/v1/chat/completions'


def clasificar_pregunta(mensaje):
    mensaje = mensaje.lower()

    if "innovacion" in mensaje or "innovación" in mensaje:
        return "innovacion"
    elif "impacto" in mensaje or "proyectos" in mensaje:
        return "impacto"
    elif "futuro" in mensaje:
        return "futuro"
    else:
        return "general"


def generar_contexto(tipo):
    if tipo == "innovacion":
        return (
            "Explica cómo los semiconductores y sistemas digitales impulsan la innovación en la educación. "
            "Incluye ejemplos como inteligencia artificial, plataformas virtuales, realidad aumentada y dispositivos inteligentes."
        )
    elif tipo == "impacto":
        return (
            "Describe el impacto de proyectos de sistemas digitales en la educación. "
            "Incluye ejemplos como laboratorios virtuales, simuladores, plataformas educativas y beneficios en el aprendizaje."
        )
    elif tipo == "futuro":
        return (
            "Explica el futuro de los sistemas digitales y semiconductores en la educación. "
            "Incluye tendencias como computación cuántica, inteligencia artificial avanzada y educación personalizada."
        )
    else:
        return (
            "Responde de forma general sobre sistemas digitales aplicados a la educación."
        )


def enviar_mensaje(mensaje_usuario):
    tipo = clasificar_pregunta(mensaje_usuario)
    contexto = generar_contexto(tipo)

    headers = {
        'Authorization': f'Bearer {API_KEY}',
        'Content-Type': 'application/json'
    }

    mensajes = [
        {
            "role": "system",
            "content": (
                "Actúa como un profesor experto en sistemas digitales aplicado a la educación. "
                "Responde de forma clara, organizada y con ejemplos fáciles de entender."
            )
        },
        {
            "role": "user",
            "content": mensaje_usuario + "\n\n" + contexto
        }
    ]

    data = {
        "model": "deepseek-chat",
        "messages": mensajes,
        "temperature": 0.7
    }

    try:
        respuesta = requests.post(API_URL, headers=headers, json=data)

        if respuesta.status_code == 200:
            contenido = respuesta.json()
            return contenido['choices'][0]['message']['content']
        else:
            return f"Error HTTP: {respuesta.status_code}"

    except Exception as e:
        return f"Error: {e}"


def main():
    print("===== Chatbot Educativo de Sistemas Digitales =====")
    print("Preguntas sobre innovación, impacto o futuro en educación.")
    print("Escribe 'salir' para terminar.\n")

    while True:
        mensaje = input("Tú: ")

        if mensaje.lower() == "salir":
            print("Chatbot: Hasta luego 👋")
            break

        respuesta = enviar_mensaje(mensaje)

        print("\nChatbot:")
        print(respuesta)
        print("-" * 50)


if __name__ == "__main__":
    main()
```

