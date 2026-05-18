# PULL-REQUEST-PUNTO-DE-VENTA-CASTILLO-NOEL-
Mejoras para un proyecto ya implementado 
# 🌴 Blender Island Walking Project

## Proyecto de graficación y simulación en Blender 5.x

---

# 📖 Introducción

Este proyecto consiste en el desarrollo de un entorno interactivo en Blender 5.x utilizando Python y la API de Blender (`bpy`). El objetivo principal fue crear un escenario compuesto por múltiples islas flotantes conectadas mediante puentes, donde un personaje animado puede desplazarse libremente utilizando controles de teclado.

A lo largo del desarrollo del proyecto se implementaron distintos sistemas fundamentales para la interacción del personaje dentro del entorno 3D, incluyendo:

- Movimiento del personaje
- Rotación
- Animación de caminata
- Gravedad
- Respawn automático
- Detección de superficies transitables
- Puentes funcionales
- Colisiones básicas
- Sistema de salto

El proyecto fue desarrollado completamente dentro de Blender, utilizando modelado 3D, programación en Python y sistemas básicos de simulación para generar una experiencia interactiva similar a la lógica de un videojuego.

---

#  Objetivo del proyecto

El objetivo principal del proyecto fue desarrollar un escenario interactivo que permitiera:

- Diseñar un entorno 3D compuesto por múltiples islas.
- Conectar las islas mediante puentes transitables.
- Implementar un personaje controlable mediante teclado.
- Integrar animaciones de caminata.
- Simular gravedad y caída.
- Crear un sistema de respawn automático.
- Experimentar con colisiones básicas utilizando geometría invisible.
- Integrar scripting mediante Python dentro de Blender.

---

#  Tecnologías utilizadas

Durante el desarrollo del proyecto se utilizaron las siguientes herramientas y tecnologías:

| Tecnología | Descripción |
|---|---|
| Blender 5.x | Software principal de modelado y simulación |
| Python | Lenguaje utilizado para la programación |
| bpy | API oficial de Blender para scripting |
| Armature System | Sistema de huesos para animación |
| Ray Casting | Técnica utilizada para detectar superficies |
| Colliders invisibles | Geometría utilizada para limitar movimiento |

---

#  Conceptos aplicados

Este proyecto involucró múltiples conceptos relacionados con graficación computacional y simulación interactiva:

- Modelado 3D
- Transformaciones espaciales
- Animación esquelética
- Sistemas de coordenadas
- Simulación de gravedad
- Colisiones
- Detección de superficies
- Programación orientada a eventos
- Control mediante teclado
- Física básica

---

#  Diseño del escenario

El escenario principal del proyecto está compuesto por:

- Una isla central.
- Cuatro islas secundarias.
- Cuatro puentes conectores.
- Un personaje animado.
- Superficies invisibles para detección de movimiento.
- Paredes invisibles utilizadas como colisiones.

El entorno fue diseñado con el objetivo de simular un pequeño mapa explorable donde el personaje pudiera desplazarse entre distintas zonas.

---

#  Imagen del escenario principal

COLOCAR IMAGEN DEL MAPA GENERAL AQUÍ

---

# <img width="1122" height="697" alt="Captura de pantalla 2026-05-17 a la(s) 20 19 11" src="https://github.com/user-attachments/assets/3a6571ca-ff1f-4cc5-a294-fb728e22e6cb" />
 Construcción de las islas

Las islas fueron modeladas directamente dentro de Blender utilizando primitivas básicas y herramientas de edición de malla.

Durante esta etapa se realizaron procesos como:

- Escalado de geometría.
- Extrusión.
- Modificación de superficies.
- Aplicación de materiales.
- Organización de objetos dentro de la escena.

Cada isla fue diseñada para funcionar como una zona transitable dentro del entorno.

---

<img width="1792" height="1120" alt="Captura de pantalla 2026-05-17 a la(s) 20 19 03" src="https://github.com/user-attachments/assets/8dcf99d9-520f-4897-bbc5-435bf30e530b" />


---

#  Construcción de los puentes

Los puentes fueron creados para conectar las distintas islas del escenario.

Cada puente fue diseñado considerando:

- Distancia entre islas.
- Altura uniforme.
- Superficie transitable.
- Integración visual con el entorno.

Además, los puentes se utilizaron posteriormente como superficies válidas para el sistema de colisiones y gravedad.

---

#  Imagen de los puentes

<img width="1041" height="599" alt="Captura de pantalla 2026-05-17 a la(s) 20 21 03" src="https://github.com/user-attachments/assets/f62f6e1d-1be2-489e-a9e6-cd3671a655c1" />


---

#  Integración del personaje

El personaje utilizado en el proyecto fue importado dentro de Blender junto con un sistema de huesos (Armature).

Este sistema permitió:

- Aplicar animaciones.
- Controlar movimiento corporal.
- Simular caminata.
- Mantener una estructura esquelética funcional.

El personaje se convirtió posteriormente en el objeto principal controlado mediante teclado.

---

#  Imagen del personaje

<img width="697" height="613" alt="Captura de pantalla 2026-05-17 a la(s) 20 22 06" src="https://github.com/user-attachments/assets/e31077a2-9e5a-4d5a-a7cc-201382a6ebca" />


---

#  Sistema de animación

El proyecto implementa una animación de caminata que se reproduce únicamente cuando el personaje está en movimiento.

Para lograr esto se utilizó:

- Evaluación de keyframes.
- Interpolación de animaciones.
- Manipulación de huesos mediante Python.
- Control de reproducción por frames.

El sistema analiza constantemente si el jugador se encuentra caminando para activar o desactivar la animación.

---

#  Programación del controlador

El controlador principal fue desarrollado completamente en Python utilizando la API `bpy`.

Este controlador se encarga de:

- Detectar teclas presionadas.
- Mover al personaje.
- Rotar el personaje.
- Activar animaciones.
- Detectar colisiones.
- Aplicar gravedad.
- Ejecutar saltos.
- Realizar respawn automático.

El sistema funciona mediante un operador modal que se ejecuta constantemente mientras el proyecto está activo.

---

#  Controles implementados

| Tecla | Acción |
|---|---|
| W | Avanzar |
| S | Retroceder |
| A | Girar izquierda |
| D | Girar derecha |
| SPACE | Saltar |
| ESC | Salir del controlador |

---

#  Sistema de movimiento

El movimiento del personaje fue implementado utilizando cálculos matemáticos basados en:

- Rotación en eje Z.
- Funciones trigonométricas.
- Transformaciones espaciales.

El personaje puede avanzar y girar libremente dentro del escenario.

La dirección del movimiento depende de la orientación actual del personaje.

---

#  Cálculos matemáticos utilizados

Para el movimiento se utilizaron funciones trigonométricas:

- `sin()`
- `cos()`

Estas funciones permiten calcular correctamente el desplazamiento del personaje según su rotación.

Ejemplo conceptual:

```python
x += -sin(rotacion) * velocidad
y +=  cos(rotacion) * velocidad
```

---

#  Sistema de gravedad

Uno de los sistemas más importantes implementados fue la gravedad.

La gravedad permite que:

- El personaje permanezca sobre las superficies.
- El personaje caiga si sale de una zona válida.
- Exista una simulación básica de física.

La gravedad funciona mediante una velocidad vertical acumulativa:

```python
VERTICAL_VELOCITY += GRAVITY * dt
```

Esto genera un efecto de aceleración hacia abajo.

---

#  Imagen del personaje cayendo

<img width="1792" height="1120" alt="Captura de pantalla 2026-05-17 a la(s) 20 27 16" src="https://github.com/user-attachments/assets/ed70773a-1c54-4175-b6bb-fa7b69b38c89" />


---

#  Sistema de respawn

Cuando el personaje cae fuera del mapa, el sistema automáticamente:

1. Detecta la caída.
2. Reinicia la posición.
3. Coloca nuevamente al personaje sobre la isla principal.

Esto evita que el personaje continúe cayendo infinitamente.

---

#  Sistema de salto

Posteriormente se implementó un sistema de salto utilizando fuerza vertical.

El salto funciona aplicando una velocidad positiva momentánea:

```python
VERTICAL_VELOCITY = JUMP_FORCE
```

Después de esto, la gravedad vuelve a actuar sobre el personaje.

---

#  Sistema de colisiones

Para limitar el movimiento del personaje se utilizaron colliders invisibles.

Estos colliders fueron creados utilizando:

- Planos invisibles.
- Cubos invisibles.
- Superficies auxiliares.

El objetivo principal fue:

- Evitar que el personaje salga de ciertas zonas.
- Simular barandales en los puentes.
- Definir áreas transitables.

---

#  Colliders invisibles

Los colliders invisibles son objetos que no forman parte visual del escenario, pero sí participan en las detecciones de colisión.

Se utilizaron dos tipos principales:

## 1. Floor Colliders

Detectan superficies caminables:

- Islas
- Puentes

## 2. Wall Colliders

Impiden que el personaje atraviese ciertas zonas.

---

#  Imagen de colliders invisibles

<img width="973" height="636" alt="Captura de pantalla 2026-05-17 a la(s) 20 30 15" src="https://github.com/user-attachments/assets/b9da18e5-029a-4065-9725-00ddd1ce4f2b" />


---

#  Detección mediante Ray Casting

Para detectar superficies válidas se utilizó ray casting.

El ray casting consiste en lanzar un rayo invisible desde cierta posición hacia una dirección determinada.

En este caso:

- El rayo se lanza hacia abajo.
- Si golpea una superficie válida, el personaje permanece sobre ella.
- Si no detecta superficie, el personaje cae.

---

#  Problemas encontrados durante el desarrollo

Durante el desarrollo surgieron distintos problemas técnicos:

## Problemas principales

- El personaje atravesaba puentes.
- La gravedad detectaba objetos incorrectos.
- El personaje aparecía debajo del mapa.
- Los colliders no siempre funcionaban correctamente.
- Conflictos entre teclas y shortcuts de Blender.
- Errores relacionados con keyframes.

---

#  Soluciones implementadas

Para resolver los problemas anteriores se realizaron múltiples ajustes:

- Uso de superficies invisibles específicas.
- Corrección de posiciones en eje Z.
- Aplicación de gravedad controlada.
- Implementación de respawn.
- Separación entre pisos y paredes invisibles.
- Aplicación de transformaciones (`CTRL + A`).
- Mejora en la detección de colisiones.

---

#  Evolución del proyecto

El proyecto evolucionó gradualmente desde un escenario estático hasta un entorno interactivo funcional.

## Etapas del desarrollo

1. Creación de las islas.
2. Construcción de puentes.
3. Importación del personaje.
4. Integración de animaciones.
5. Programación del movimiento.
6. Implementación de gravedad.
7. Implementación de respawn.
8. Sistema de salto.
9. Colisiones básicas.

---
<img width="1068" height="629" alt="Captura de pantalla 2026-05-17 a la(s) 20 31 14" src="https://github.com/user-attachments/assets/7da62dd7-d654-415f-94b2-73fd13beb41f" />


---

#  Aprendizajes obtenidos

Durante el desarrollo del proyecto se fortalecieron conocimientos relacionados con:

- Blender
- Python
- Programación interactiva
- Sistemas de físicas básicas
- Graficación computacional
- Detección de colisiones
- Animación 3D
- Simulación de movimiento



#  Autor

Nombre: Noel Castillo Villanueva

Proyecto desarrollado en Blender 5.x utilizando Python y la API bpy.
