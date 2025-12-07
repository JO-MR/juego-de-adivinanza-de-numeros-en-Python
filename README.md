#  Juego de Adivinanza de Números en Python

Este proyecto implementa un **juego interactivo de adivinanza** desarrollado en Python, diseñado para demostrar buenas prácticas de programación, control de flujo, manejo de errores y gestión de datos.  
El juego permite jugar en **modo solitario**, **modo 2 jugadores** y consultar un módulo de **estadísticas**, ofreciendo una experiencia completa y personalizable.

---

##  Funcionalidades principales

###  Partida en modo solitario
- El sistema genera automáticamente un número secreto entre **1 y 1000**.
- El jugador intenta adivinarlo con un número limitado de intentos según la dificultad seleccionada.

###  Partida en modo 2 jugadores
- Un jugador introduce el número objetivo.
- El segundo jugador intenta adivinarlo bajo las mismas reglas de dificultad.
- El número elegido puede mantenerse oculto para no mostrarlo en pantalla (según implementación).

###  Módulo de estadísticas
- El sistema registra automáticamente, para cada partida:
  - Nombre del jugador  
  - Resultado (victoria / derrota)  
  - Número secreto  
  - Intentos utilizados  
  - Dificultad seleccionada  
  - Fecha de la partida  
- Los datos se almacenan en un **archivo Excel** y pueden visualizarse desde el menú de estadísticas.

###  Salir
- Finaliza la ejecución del programa de forma segura.

---

##  Niveles de dificultad

Cada modo de juego permite elegir entre tres niveles:

| Dificultad | Intentos permitidos |
|------------|---------------------|
| Fácil      | 20 intentos         |
| Medio      | 12 intentos         |
| Difícil    | 5 intentos          |

Todas las opciones de menú se validan para evitar entradas incorrectas y mejorar la robustez de la aplicación.

---

##  Características técnicas

- Diseño modular con funciones separadas para:
  - Menú principal  
  - Lógica del juego  
  - Selección de dificultad  
  - Gestión de estadísticas  
  - Validación de entradas  
- Gestión de errores y entradas no válidas mediante bucles y comprobaciones explícitas.
- Persistencia de la información de las partidas en un fichero Excel para su consulta posterior.

---

##  Estructura del proyecto

```text
juego-adivina-el-numero/
│
├── juego_de_adivinanza_de_numeros.ipynb   # Notebook principal
├── resultados.xlsx                         # Archivo con el histórico de partidas (se genera al jugar)
├── README.md                               # Documentación del proyecto
└── src/                                    # (Opcional) versión en script .py si se extrae del notebook

## Tecnologías utilizadas
Python 3.x
Pandas – para la lectura y escritura del fichero Excel
OpenPyXL – motor de soporte para Excel
Estructuras de control (if, while, for) y manejo de excepciones
