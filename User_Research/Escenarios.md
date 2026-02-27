# Escenarios de Uso

## Sistema CGRH – UADY

**Elaborado por:** Damián Villares, Héctor Castro  
**Fecha:** 27 de febrero de 2026

> **Nota metodológica:** Los escenarios presentados son **escenarios preliminares de diseño**, derivados del análisis de requerimientos funcionales (RF01–RF30), del perfil de usuario definido y de fuentes secundarias sobre comportamiento digital de adultos mayores. Su función es orientar decisiones de diseño y servir como base para la creación de requerimientos, no como resultado de sesiones de campo. Serán ajustados y enriquecidos una vez que la investigación primaria (entrevistas, contextual inquiry, pruebas de usabilidad) aporte evidencia directa del comportamiento de los usuarios.

---

## Escenario 1 — Descarga de CFDI para trámite bancario

**Persona:** Don Armando Cetina Pech, 67 años, jubilado docente  
**Contexto:** Mañana en casa, sentado frente a su computadora de escritorio  
**Requerimientos relacionados:** RF03 (Inicio de sesión), RF10 (Consultar CFDI)

---

Armando necesita presentar sus últimos tres recibos de nómina ante una institución financiera para tramitar un crédito. Un sobrino le comentó que desde hace un tiempo puede descargarlos directamente desde el sistema de la CGRH sin ir a la universidad.

Abre el navegador que tiene en su escritorio y escribe la dirección que le anotó su sobrino en un papel. Llega a la pantalla de inicio de sesión. Ingresa su nombre de usuario — lo tiene anotado en una hoja pegada al monitor — y teclea su contraseña intentando recordar si usó mayúsculas o no. El sistema le indica que la contraseña es incorrecta. Armando intenta una segunda vez con otra variante que recuerda. El segundo intento falla también.

Ve un enlace que dice **"¿Olvidaste tu contraseña?"** y hace clic. El sistema le pide su correo institucional. Armando no sabe de memoria cuál es su correo; busca en sus anotaciones y lo encuentra. Lo escribe, pulsa continuar y el sistema le indica que recibirá un correo con instrucciones.

Armando abre su cliente de correo y espera. Después de unos minutos encuentra el mensaje en la carpeta de correo no deseado. Sigue el enlace, establece una nueva contraseña y vuelve al inicio de sesión. Esta vez accede correctamente.

Desde el menú principal, identifica la opción **"Mis CFDI"**. El sistema muestra una lista de recibos ordenados por fecha. Armando selecciona los tres más recientes y descarga cada uno en PDF haciendo clic en el botón correspondiente. Los archivos se guardan en su carpeta de descargas. Cierra sesión.

**Puntos de fricción identificados:**
- Recordar o localizar las credenciales de acceso
- Reconocer el correo de recuperación en carpeta de spam
- Asociar el término "CFDI" con "recibo de nómina"

**Criterios de diseño derivados:**
- RF02 debe incluir indicación explícita de revisar carpeta de correo no deseado
- RF10 debe mostrar los recibos con etiqueta "Recibo de Nómina (CFDI)" en lugar de solo la sigla
- El botón de descarga en PDF debe ser el elemento más prominente en cada registro

---

## Escenario 2 — Recuperación de contraseña sin asistencia

**Persona:** Doña Concepción Dzul Rosado, 63 años, jubilada administrativa  
**Contexto:** Tarde en casa, usando la laptop de su hija mientras ella trabaja  
**Requerimientos relacionados:** RF02 (Recuperar contraseña), RF03 (Inicio de sesión)

---

Concepción quiere revisar su saldo de Caja de Ahorro antes de una reunión familiar este fin de semana. Su hija le dejó la laptop antes de salir al trabajo. Concepción recuerda que ya tiene cuenta en el sistema pero no recuerda la contraseña; la última vez que entró fue hace cuatro meses.

Accede a la plataforma y en la pantalla de inicio de sesión escribe lo que cree que es su usuario. El sistema no lo reconoce: no sabe si su usuario es su número de empleado, su nombre o su correo. Intenta con las tres variantes que se le ocurren y ninguna funciona.

Encuentra el enlace de recuperación. El sistema le pide su correo institucional. Concepción no está segura de cuál es, pero recuerda que terminaba en `@correo.uady.mx`. Lo escribe y hace clic. El sistema confirma que se ha enviado un correo.

Concepción abre el correo que tiene en el teléfono de su hija — donde sí sabe acceder— y encuentra el mensaje. Sigue el enlace desde el teléfono, establece una contraseña nueva usando una que ya tiene memorizada de otra cuenta, y regresa a la laptop para iniciar sesión con las nuevas credenciales.

El sistema la recibe en el menú principal. Busca la sección de **Caja de Ahorro**, localiza su saldo actual y toma una foto a la pantalla con su teléfono para tenerlo de referencia.

**Puntos de fricción identificados:**
- Ambigüedad sobre qué campo usar como "usuario"
- Flujo de recuperación que cruza dispositivos (laptop → teléfono → laptop)
- No sabe cómo "guardar" la información; fotografia la pantalla como alternativa

**Criterios de diseño derivados:**
- RF03 debe indicar explícitamente bajo el campo de usuario qué formato se espera (ej. "Ingresa tu número de empleado o correo institucional")
- RF02 debe mostrar una vista de confirmación clara y breve, sin presuponer que el usuario sabe revisar correo en el mismo dispositivo
- RF30 debe ofrecer opción de descarga en PDF como mecanismo de captura de información alternativo a la fotografia

---

## Escenario 3 — Registro asistido por primera vez

**Persona:** Don Feliciano Canul Tzuc, 69 años, jubilado de servicios generales  
**Contexto:** Tarde en casa de un vecino, usando su computadora; el vecino actúa como guía durante el proceso  
**Requerimientos relacionados:** RF01 (Registro), RF03 (Inicio de sesión), RF10 (Consultar CFDI)

---

Feliciano necesita presentar un recibo de nómina ante el IMSS para un trámite de pensión complementaria. Un familiar le explicó que puede descargarlo desde el sistema de la CGRH sin ir a la universidad, pero que primero tiene que registrarse.

Va a casa de su vecino Ernesto, quien tiene computadora e internet. Ernesto accede al sistema desde el navegador. La pantalla de inicio muestra las opciones para iniciar sesión o registrarse. Feliciano no tiene cuenta, así que Ernesto le ayuda a encontrar el botón de registro.

El formulario de registro muestra varios campos: clave de empleado, RFC, CURP, correo institucional y confirmación de correo. Feliciano saca de su cartera una copia de su credencial de ex-empleado donde tiene anotada su clave. El RFC y la CURP los tiene escritos en un papel doblado que carga consigo. Los dicta en voz alta y Ernesto los escribe.

Al llegar al campo de correo institucional, Feliciano no recuerda cuál es. Ernesto sugiere llamar a la CGRH para preguntarlo. Después de una llamada breve, obtienen el correo y lo escriben. El sistema pide crear una contraseña; Ernesto le sugiere una combinación simple basada en su fecha de nacimiento y la anota en un papel para que Feliciano la guarde.

El sistema muestra un mensaje de que se ha enviado un enlace de confirmación al correo. Ernesto abre el correo institucional desde la misma computadora, encuentra el mensaje y hace clic en el enlace. Feliciano ya tiene cuenta activa.

Inician sesión con las credenciales recién creadas. El menú principal aparece con tres opciones. Ernesto lee en voz alta: "Mis CFDI, Fondo de Ahorro, Caja de Ahorro". Feliciano reconoce la primera opción. Ernesto hace clic, aparece la lista de recibos más recientes y descarga el PDF correspondiente al mes que pide el IMSS. Lo imprimen en la tienda de servicios camino a casa.

**Puntos de fricción identificados:**
- El proceso completo requirió asistencia total de un tercero; Feliciano no pudo operar la computadora por sí solo
- Múltiples campos de datos que el usuario no tiene memorizados ni digitalizados (RFC, CURP, correo)
- El flujo de confirmación por correo supone que el usuario tiene acceso y sabe operar su correo institucional
- Sin papel y lápiz para anotar la contraseña, el próximo acceso sería imposible

**Criterios de diseño derivados:**
- RF01 debe minimizar el número de campos en el paso inicial y ofrecer texto de ayuda en cada campo (ej. "Tu clave de empleado está en tu credencial UADY")
- El flujo de confirmación de RF01 debe contemplar que la cuenta de correo sea accedida por el mismo usuario; mensajes claros y paso a paso
- RF03 debe tolerar accesos infrecuentes sin penalizar al usuario con bloqueos rápidos por intentos fallidos
- RF10 debe identificar los recibos con lenguaje llano ("Recibo de Nómina — Enero 2026") además del folio técnico

---

## Síntesis de escenarios

| Escenario | Persona | Flujos involucrados | Puntos de diseño críticos |
|---|---|---|---|
| 1 — Descarga de CFDI | Don Armando | RF02, RF03, RF10 | Correo recuperación spam, etiquetado CFDI, botón PDF prominente |
| 2 — Recuperación de contraseña | Doña Concepción | RF02, RF03, RF30 | Ambigüedad de usuario, flujo cross-device, descarga como alternativa a fotografía |
| 3 — Registro asistido | Don Feliciano | RF01, RF03, RF10 | Cantidad de campos en registro, dependencia de correo institucional, lenguaje llano en recibos |

---

## Relación con requerimientos funcionales

Los tres escenarios confirman que **RF01, RF02 y RF03** concentran la mayor fricción para el usuario primario, en línea con lo establecido en los requerimientos del producto. Adicionalmente, los escenarios aportan criterios de diseño concretos para RF05, RF10, RF20 y RF30 que complementan las especificaciones funcionales ya documentadas.

---

## Referencias

- Fisk, A. D., Rogers, W. A., Charness, N., Czaja, S. J., & Sharit, J. (2018). *Designing for Older Adults: Principles and Creative Human Factors Approaches* (3a ed.). CRC Press.
- Carroll, J. M. (2000). *Making Use: Scenario-Based Design of Human-Computer Interactions*. MIT Press.
- INEGI. (2023). *Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de la Información en los Hogares (ENDUTIH 2023)*. Instituto Nacional de Estadística y Geografía.
