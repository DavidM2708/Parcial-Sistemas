# Parcial-Sistemas
David Esteban Mesa Gonzalez

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

* S = 010 - Y2 = D


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
2. Se agrupan los valores en bloques
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

- 1 compuerta NOT para B
- 1 compuerta AND de 3 entradas




## Logica circuito en Tinkercad 
 
 Componentes:
   - 3 interruptores (A, B, C)
   - 1 compuerta NOT
   - 1 compuerta AND de 3 entradas 
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

En 2026, los semiconductores se han convertido en el corazón de la revolución digital. La demanda de tecnologías como la inteligencia artificial, el Internet de las cosas, los autos autónomos y la nube está empujando a crear chips cada vez más pequeños, potentes y eficientes.

Al mismo tiempo, la investigación busca ir más allá del silicio, explorando nuevos materiales y arquitecturas innovadoras, como los chips tridimensionales.

Pero no todo es avance: la industria enfrenta retos serios, desde la escasez de insumos y las tensiones geopolíticas, hasta la necesidad de cadenas de suministro más sólidas. Por eso, tanto países como empresas están apostando por construir más fábricas en distintas regiones, buscando asegurar su independencia tecnológica y reducir riesgos.


## 2. Empresas más relevantes del sector y su impacto en los sistemas digitales

En el mundo de los semiconductores, algunas compañías marcan el rumbo de la innovación y el desarrollo tecnológico. Intel, TSMC, NVIDIA, Samsung y AMD son protagonistas clave que hacen posible que los sistemas digitales funcionen con la velocidad y eficiencia que hoy damos por sentada.

Intel sigue siendo referente en procesadores para computadoras y servidores, impactando directamente en el rendimiento de la informática. TSMC, se ha convertido en el gran fabricante de chips avanzados para múltiples empresas, sosteniendo gran parte de la cadena global de producción. NVIDIA se ha consolidado como líder en GPUs, fundamentales para inteligencia artificial y gráficos complejos. Samsung no solo fabrica memorias, también impulsa avances en móviles y soluciones de almacenamiento. AMD compite con fuerza en el mercado de procesadores de alto rendimiento, ofreciendo alternativas eficientes para la computación avanzada.

El aporte de estas compañías es enorme, gracias a sus tecnologías, los sistemas digitales logran procesar más rápido, consumir menos energía y manejar cantidades masivas de datos con mayor facilidad.


## Código del Chatbot (Python)

```python
import requests

API_KEY = '     '
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
            print("Chatbot: Hasta luego")
            break

        respuesta = enviar_mensaje(mensaje)

        print("\nChatbot:")
        print(respuesta)
        print("-" * 50)


if __name__ == "__main__":
    main()
```

