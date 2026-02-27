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

## Escenario 3 — Consulta del Fondo de Ahorro para el Retiro

**Persona:** Don Mauricio Sansores Herrera, 71 años, jubilado técnico  
**Contexto:** Primer día del mes, en casa, desde su computadora de escritorio con zoom aumentado al 150%  
**Requerimientos relacionados:** RF03 (Inicio de sesión), RF05 (Menú principal), RF20 (FAR)

---

Mauricio tiene el hábito de revisar mensualmente el estado de su Fondo de Ahorro para el Retiro. Ya tiene cuenta en el sistema y recuerda bien su usuario y contraseña porque los anotó en la libreta que tiene junto a su computadora.

Abre el navegador con el zoom configurado al 150%, que es el nivel que le permite leer con comodidad. Accede al sistema, escribe sus credenciales sin dificultad y entra al menú principal.

La pantalla del menú muestra tres secciones claramente diferenciadas: **Mis CFDI**, **Fondo de Ahorro para el Retiro** y **Caja de Ahorro**. Mauricio hace clic en **Fondo de Ahorro para el Retiro**.

La vista del FAR le presenta una tarjeta con su saldo total, sus aportaciones del mes en curso y un resumen de rendimientos. Mauricio revisa los números, confirma que el monto corresponde a lo esperado y descarga el PDF del estado de cuenta mensual para archivarlo en su computadora.

Cierra la sección, regresa al menú principal y cierra sesión usando el botón visible en la esquina superior.

**Puntos de fricción identificados:**
- Si el diseño no es responsivo al zoom, los elementos se desplazan o superponen al 150%
- Terminología financiera ("rendimientos", "aportaciones ordinarias") puede resultar opaca sin etiquetas explicativas

**Criterios de diseño derivados:**
- RF05 y RF20 deben mantener su estructura y usabilidad a niveles de zoom de hasta 200%
- RF20 debe presentar cada campo numérico con una etiqueta explicativa en lenguaje llano (ej. "Lo que ahorraste este mes:")
- El botón de descarga PDF debe estar visible sin necesidad de scroll en la resolución y zoom habituales del perfil objetivo

---

## Síntesis de escenarios

| Escenario | Persona | Flujos involucrados | Puntos de diseño críticos |
|---|---|---|---|
| 1 — Descarga de CFDI | Don Armando | RF02, RF03, RF10 | Correo recuperación spam, etiquetado CFDI, botón PDF prominente |
| 2 — Recuperación de contraseña | Doña Concepción | RF02, RF03, RF30 | Ambigüedad de usuario, flujo cross-device, descarga como alternativa a fotografia |
| 3 — Consulta FAR mensual | Don Mauricio | RF03, RF05, RF20 | Responsividad al zoom, lenguaje financiero llano, visibilidad PDF sin scroll |

---

## Relación con requerimientos funcionales

Los tres escenarios confirman que **RF01, RF02 y RF03** concentran la mayor fricción para el usuario primario, en línea con lo establecido en los requerimientos del producto. Adicionalmente, los escenarios aportan criterios de diseño concretos para RF05, RF10, RF20 y RF30 que complementan las especificaciones funcionales ya documentadas.

---

## Referencias

- Fisk, A. D., Rogers, W. A., Charness, N., Czaja, S. J., & Sharit, J. (2018). *Designing for Older Adults: Principles and Creative Human Factors Approaches* (3a ed.). CRC Press.
- Carroll, J. M. (2000). *Making Use: Scenario-Based Design of Human-Computer Interactions*. MIT Press.
- INEGI. (2023). *Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de la Información en los Hogares (ENDUTIH 2023)*. Instituto Nacional de Estadística y Geografía.
