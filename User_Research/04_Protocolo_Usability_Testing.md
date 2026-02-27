# Protocolo de Usability Testing
## Actividad 4: Pruebas de Usabilidad — CGRH UADY

**Elaborado por:** Héctor Barrera
**Fecha:** 27 de febrero de 2026
**Perfil objetivo:** Empleados jubilados de la UADY, mayores de 60 años

---

## 1. Objetivos de la Evaluación

Las pruebas de usabilidad tienen como fin evaluar la facilidad de uso del sistema CGRH con usuarios representativos del perfil primario definido (jubilados mayores de 60 años con nivel básico de alfabetización digital). Los objetivos específicos son:

- Identificar los errores más frecuentes durante la ejecución de tareas críticas (registro, inicio de sesión, recuperación de contraseña, consulta de información).
- Medir el tiempo promedio necesario para completar cada tarea sin asistencia.
- Detectar problemas de comprensión en etiquetas, mensajes de error y flujos de navegación.
- Obtener evidencia empírica para justificar decisiones de diseño en los requerimientos RF01–RF30.
- Validar o refutar los supuestos establecidos en las proto-personas (Armando, Concepción, Feliciano).

| Campo | Detalle |
|---|---|
| **Duración por sesión** | 20 – 35 minutos |
| **Modalidad** | Presencial (en domicilio del participante o sala habilitada) |
| **Perfil del participante** | Jubilado UADY, 60+ años, nivel básico de alfabetización digital |
| **Número de participantes** | 5 participantes (mínimo viable para detectar el 85% de problemas de usabilidad, Nielsen 1993) |
| **Roles** | 1 facilitador + 1 observador/tomador de notas |
| **Material requerido** | Prototipo en computadora de escritorio, fichas de tareas, hoja de registro, lápiz |
| **Criterio de éxito por tarea** | Completada sin asistencia en el tiempo límite establecido |

---

## 2. Tareas de Evaluación

Cada tarea se presenta al participante en una ficha impresa con lenguaje sencillo y sin terminología técnica. El facilitador **no da instrucciones** sobre cómo realizarla; solo describe el objetivo.

| # | Tarea | Escenario presentado al usuario | Tiempo límite | RF |
|---|---|---|:---:|---|
| T1 | Registro en el sistema | *"Imagine que va a entrar al sistema de la CGRH por primera vez. Por favor, cree una cuenta nueva."* | 8 min | RF01 |
| T2 | Inicio de sesión | *"Ya tiene una cuenta. Por favor, entre al sistema con su usuario y contraseña."* | 3 min | RF03 |
| T3 | Recuperación de contraseña | *"Olvidó su contraseña. Por favor, intente recuperarla para poder entrar."* | 5 min | RF02 |
| T4 | Consulta de CFDI | *"Necesita su recibo de nómina del mes pasado para entregarlo en el banco. Búsquelo y descárguelo."* | 5 min | RF10 |
| T5 | Consulta del FAR | *"Quiere saber cuánto tiene en su Fondo de Ahorro para el Retiro. Búsquelo."* | 4 min | RF20 |
| T6 | Consulta de Caja de Ahorro | *"Quiere ver el saldo de su Caja de Ahorro. Encuéntrelo en el sistema."* | 4 min | RF30 |
| T7 | Cierre de sesión | *"Ya terminó lo que necesitaba. Por favor, salga del sistema."* | 2 min | RF04 |

---

## 3. Guión del Facilitador

### 3.1 Introducción (5 min)

**Texto sugerido:**

> "Buenos días/tardes. Gracias por venir. Hoy vamos a probar una página de internet que está en desarrollo. Quiero aclarar que no estamos evaluando cómo usa usted la computadora: estamos evaluando si la página está bien diseñada. Si algo no le queda claro o no sabe qué hacer, eso nos dice que hay algo que mejorar en el diseño. Le pediré que piense en voz alta mientras trabaja: que me diga qué ve, qué espera que pase, y qué le confunde. ¿Tiene alguna pregunta antes de comenzar?"

### 3.2 Reglas durante la sesión

- No dar pistas, sugerencias ni confirmar si el usuario va bien o mal.
- Si el usuario pregunta "¿Está bien así?", responder: *"Haga lo que le parezca natural."*
- Si el usuario está bloqueado por más de 2 minutos, registrar el abandono de tarea y pasar a la siguiente.
- Si el usuario expresa frustración intensa, reconocerla brevemente: *"Entiendo, está bien, eso es justo lo que queremos identificar."*
- Mantener un tono neutro y calmado durante toda la sesión.

### 3.3 Cierre (10 min)

Al terminar todas las tareas, realice las siguientes preguntas:

1. En general, ¿cómo describiría su experiencia con el sistema?
2. ¿Hubo alguna parte que le resultara muy confusa o frustrante?
3. ¿Hay algo que el sistema haga especialmente bien?
4. Si pudiera cambiar una sola cosa, ¿qué sería?
5. ¿Usaría este sistema de manera regular si estuviera disponible?

---

## 4. Métricas de Usabilidad

| Métrica | Definición | Método de registro |
|---|---|---|
| **Tasa de completación** | % de participantes que completan la tarea sin asistencia | Ficha de registro: Completada / No completada / Abandonada |
| **Tiempo en tarea** | Tiempo transcurrido desde que se presenta la tarea hasta que el usuario la da por terminada | Cronómetro; registrar en segundos |
| **Número de errores** | Clics incorrectos, navegación hacia atrás, repetición de pasos | Observador registra en tiempo real |
| **Solicitudes de ayuda** | Número de veces que el usuario pregunta al facilitador cómo proceder | Conteo por tarea |
| **Puntuación SUS** | System Usability Scale: 10 ítems en escala Likert 1-5 | Cuestionario post-sesión (ver Sección 6) |
| **Problemas cualitativos** | Verbalizaciones de confusión, errores de comprensión, reacciones emocionales | Notas textuales del observador |

---

## 5. Ficha de Registro por Tarea

*Complete una fila por tarea. Use una ficha por participante.*

| Tarea | Estado | Tiempo (seg) | # Errores | # Ayudas | Observaciones |
|:---:|---|:---:|:---:|:---:|---|
| T1 | ☐ Completa ☐ No completa ☐ Abandonada | | | | |
| T2 | ☐ Completa ☐ No completa ☐ Abandonada | | | | |
| T3 | ☐ Completa ☐ No completa ☐ Abandonada | | | | |
| T4 | ☐ Completa ☐ No completa ☐ Abandonada | | | | |
| T5 | ☐ Completa ☐ No completa ☐ Abandonada | | | | |
| T6 | ☐ Completa ☐ No completa ☐ Abandonada | | | | |
| T7 | ☐ Completa ☐ No completa ☐ Abandonada | | | | |

---

## 6. Cuestionario SUS (System Usability Scale)

**Instrucciones para el participante:** A continuación hay 10 afirmaciones sobre el sistema. Por favor indique qué tan de acuerdo está con cada una:

*1 = Totalmente en desacuerdo — 5 = Totalmente de acuerdo*

| # | Afirmación | 1 | 2 | 3 | 4 | 5 |
|:---:|---|:---:|:---:|:---:|:---:|:---:|
| 1 | Creo que me gustaría usar este sistema con frecuencia | ☐ | ☐ | ☐ | ☐ | ☐ |
| 2 | Encontré el sistema innecesariamente complejo | ☐ | ☐ | ☐ | ☐ | ☐ |
| 3 | Pensé que el sistema era fácil de usar | ☐ | ☐ | ☐ | ☐ | ☐ |
| 4 | Creo que necesitaría el apoyo de alguien para poder usar este sistema | ☐ | ☐ | ☐ | ☐ | ☐ |
| 5 | Las diferentes partes del sistema estaban bien integradas | ☐ | ☐ | ☐ | ☐ | ☐ |
| 6 | Había demasiadas inconsistencias en el sistema | ☐ | ☐ | ☐ | ☐ | ☐ |
| 7 | Imagino que la mayoría de personas aprendería a usar este sistema muy rápidamente | ☐ | ☐ | ☐ | ☐ | ☐ |
| 8 | El sistema fue muy difícil de manejar | ☐ | ☐ | ☐ | ☐ | ☐ |
| 9 | Me sentí muy seguro/a usando el sistema | ☐ | ☐ | ☐ | ☐ | ☐ |
| 10 | Necesité aprender muchas cosas antes de poder empezar a usar el sistema | ☐ | ☐ | ☐ | ☐ | ☐ |

---

## 7. Criterios de Priorización de Hallazgos

Los problemas identificados durante las pruebas serán clasificados según la escala de severidad de Nielsen (1993):

| Nivel | Severidad | Criterio |
|---|---|---|
| **4 – Crítico** | Catastrófico | El usuario no puede completar la tarea; genera abandono inmediato del sistema |
| **3 – Alto** | Mayor | El usuario completa la tarea con dificultad significativa o requiere ayuda |
| **2 – Medio** | Menor | Causa confusión o retraso notable pero el usuario llega al objetivo |
| **1 – Bajo** | Cosmético | Molestia menor; no impide la completación de la tarea |
| **0 – Sin impacto** | No es un problema | Observado pero sin efecto en la experiencia del usuario |
