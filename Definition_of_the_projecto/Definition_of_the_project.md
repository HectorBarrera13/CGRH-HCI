# ANÁLISIS DEL PROYECTO
*Evaluación de Relevancia Social · Innovación · Factibilidad*

> *CGRH — Coordinación General de Recursos Humanos*  

---

## 1. Relevancia Social

El proyecto aborda la brecha digital para todos los empleados de la UADY, pero mayormente enfocado hacia los adultos mayores, un grupo socialmente vulnerable que enfrenta barreras significativas para acceder a servicios esenciales (financieros, laborales) debido al diseño de sistemas digitales que no consideran sus capacidades cognitivas, físicas y tecnológicas.

### Argumento Principal

No se trata simplemente de un problema de usabilidad general, sino de inclusión social y acceso a derechos. El equipo colaborativo esta enfocado en la asognatura hacia los empleados mayores de 60 años con nivel básico de alfabetización digital.

### Puntos de Fricción Críticos Identificados

- *RF01 – RF03:* El manejo de credenciales es el punto de mayor fricción identificado en el sistema.
- *Impacto real:* No poder iniciar sesión bloquea el acceso a información financiera personal: CFDI, FAR, Caja de Ahorro.
- *Consecuencia social:* Genera estrés y dependencia de terceros (familiares, ventanillas físicas), erosionando la autonomía del jubilado.

### Validación en Campo

El plan de User Research contempla entrevistas con aproximadamente 5 adultos mayores de la UADY y pruebas con 15 participantes del perfil objetivo. Esto no es un plan futuro: el equipo ya tiene acceso a la comunidad afectada, lo que valida la relevancia desde la fase de investigación.

*Conclusión:* El CGRH no es solo un sistema de RH. Es un mecanismo para garantizar la autonomía, la dignidad y la inclusión financiera de un grupo etario que, de otro modo, quedaría relegado en la transición digital de la universidad.

---

## 2. Innovación

La innovación no radica en crear nuevas funcionalidades, sino en un enfoque de diseño radicalmente centrado en la fragilidad digital del usuario. La diferencia clave es pasar de diseñar para el usuario promedio a diseñar para la persona mayor no experta como eje central desde los requerimientos no funcionales.

### Enfoque Basado en Atributos, no solo en Funciones

La mayoría de los sistemas existentes (banca en línea, portales de gobierno) se enfocan en cumplir funciones. El sistema CGRH, por el contrario, prioriza atributos de usabilidad específicos:

| Atributo | Descripción |
|---|---|
| *Accesibilidad* | Diseño adaptado a limitaciones visuales y motoras del adulto mayor |
| *Legibilidad* | Tipografía, contraste y espaciado pensados para facilitar la lectura |
| *Baja Carga Cognitiva* | Flujos cortos, máximo 5 opciones por pantalla (RNF-05) |
| *Confianza* | Confirmaciones explícitas (RNF-08) y mensajes sin tecnicismos (RNF-04) |

*Conclusión:* La innovación del CGRH es metodológica y de principios. Su valor diferencial es aplicar el marco teórico de Nielsen e ISO 9241 de manera rigurosa para resolver un problema de exclusión generacional, diseñando para la fragilidad en lugar de para la capacidad.

---

## 3. Factibilidad

El proyecto es altamente factible porque su alcance está delimitado por el perfil de usuario, las tareas críticas están identificadas, y las métricas de éxito son claras y medibles. El equipo cuenta con un plan de investigación que mitiga riesgos antes de la implementación.

### Argumentos de Éxito

- *Alcance acotado:* El sistema se enfoca en un conjunto pequeño de tareas de alto valor: Consulta de CFDI, FAR y Caja de Ahorro. No es un sistema monolítico, lo que facilita el desarrollo y la curva de aprendizaje.
- *Validación temprana:* Las actividades de User Research (entrevistas, pruebas) están planificadas antes del diseño, garantizando que el desarrollo se base en datos reales y no en suposiciones.

### Fortalezas del Equipo

- *Conocimiento del usuario:* El equipo demuestra capacidad para hacer user research y tiene acceso directo a la muestra de usuarios.
- *Enfoque teórico sólido:* La fundamentación en Nielsen e ISO 9241 demuestra que el equipo aplica estándares reconocidos de HCI, no improvisa.
- *Identificación de riesgos:* Señalar RF01–RF03 como puntos de fricción demuestra que el equipo sabe exactamente dónde enfocar los esfuerzos de diseño.

### Desafíos y Riesgos

| Tipo | Desafío | Descripción |
|---|---|---|
| *HCI* | Reto Cognitivo | Lograr que RF02 (recuperación de contraseña) sea completable por un usuario con poca memoria y ansiedad tecnológica, sin ayuda externa. El wording, botones y timing son un reto de diseño mayúsculo. |
| *Producto* | Reto de Confianza | Los adultos mayores temen "equivocarse" y "romper algo". El mayor reto es diseñar una interfaz que no solo sea usable, sino que inspire calma y confianza desde el primer momento. |
| *Técnico* | Accesibilidad Android | Implementar RNF-02 (áreas táctiles 48×48) y RNF-01 (contraste 4.5:1) en Android con diferentes versiones y personalizaciones de fabricante requiere pruebas extensivas en dispositivos reales. |
| *Equipo* | Brecha Generacional | Los desarrolladores son probablemente nativos digitales y pueden caer en la trampa de "diseñar para uno mismo", ignorando las necesidades reales del usuario de 67 años. |

*Conclusión:* La combinación de alcance delimitado, métricas claras y validación temprana con usuarios reales hace del CGRH un proyecto con alta probabilidad de éxito, siempre que el equipo mantenga al jubilado como el centro de cada decisión de diseño.
