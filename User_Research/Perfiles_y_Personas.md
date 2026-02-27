# Perfiles de Usuario y Proto-Personas

## Sistema CGRH – UADY

**Elaborado por:** Damián Villares, Héctor Castro  
**Fecha:** 27 de febrero de 2026

> **Nota metodológica:** Las personas presentadas en este documento son **proto-personas de supuesto** (*assumption personas*), construidas a partir de datos secundarios (ENDUTIH 2023, INEGI), análisis de dominio institucional y los requerimientos funcionales definidos para el sistema CGRH. No se derivan de investigación primaria formal, sino que la preceden y la orientan. Serán refinadas y validadas conforme avance la investigación primaria planeada (entrevistas, encuestas, pruebas de usabilidad). Esta práctica es metodológicamente estándar cuando la investigación de campo se encuentra en fase de diseño o no ha concluido (Cooper, 2004; Gothelf & Seiden, 2016).

---

## 1. Perfil General de Usuario

### 1.1 Usuarios Primarios

Los **usuarios primarios** son aquellos que interactúan directamente con el sistema CGRH para consultar su información financiera y administrativa.

| Atributo | Descripción |
|---|---|
| **Segmento** | Empleados jubilados de la UADY |
| **Rango de edad** | 60 años en adelante |
| **Ocupación previa** | Personal docente, administrativo o de servicios de la UADY |
| **Nivel de alfabetización digital** | Básico (43.7% de la población de 55–64 años usó internet en el último año, ENDUTIH 2023, INEGI) |
| **Dispositivo de acceso predominante** | Computadora de escritorio (especificaciones low-end) |
| **Contexto de uso** | Hogar; sin presencia cotidiana en instalaciones universitarias |
| **Frecuencia de uso estimada** | Mensual o esporádica (consulta de CFDI, FAR, Caja de Ahorro) |
| **Dependencia de canal presencial** | Alta — actualmente dependen de trámites presenciales o intermediados por terceros |

**Barreras identificadas en la literatura y el dominio:**
- Dificultad para recordar y gestionar contraseñas (Fisk et al., *Designing for Older Adults*, 3a ed., 2018)
- Posible disminución visual que afecta la lectura de texto pequeño
- Tendencia a abandonar flujos digitales ante mensajes de error poco claros
- Baja exposición a plataformas institucionales digitales

### 1.2 Usuarios Secundarios

Los **usuarios secundarios** interactúan con el sistema de manera indirecta o en contextos específicos.

| Segmento | Relación con el sistema |
|---|---|
| Personal administrativo CGRH | Atiende consultas de jubilados que no pudieron completar el flujo de manera autónoma |
| Familiares o asistentes del jubilado | En algunos casos apoyan al usuario primario en tareas como inicio de sesión o descarga de documentos |
| Personal activo UADY (docentes y administrativos) | Comparten la plataforma pero presentan menor nivel de fricción digital |

---

## 2. Proto-Personas

---

### Proto-Persona 1 — "Don Armando"

> *Jubilado docente que necesita sus CFDI para trámites externos*

| Campo | Detalle |
|---|---|
| **Nombre** | Armando Cetina Pech |
| **Edad** | 67 años |
| **Ocupación previa** | Profesor de tiempo completo, Facultad de Ingeniería, UADY (35 años de servicio) |
| **Lugar de residencia** | Mérida, Yucatán |
| **Dispositivo** | Computadora de escritorio con Windows 10; pantalla de 19" |
| **Conexión** | Internet en casa (servicio básico) |
| **Competencia digital** | Básica-media — usa WhatsApp y YouTube, pero nunca ha descargado un PDF de manera autónoma |

**Objetivos:**
- Descargar sus recibos de nómina (CFDI) para presentarlos como comprobante de ingresos ante una institución financiera
- Acceder a la información de su Fondo de Ahorro para el Retiro para planear un gasto mayor
- Hacer estos trámites sin tener que trasladarse a las instalaciones de la UADY

**Frustraciones:**
- "Nunca sé si estoy haciendo bien el proceso; cuando sale un mensaje de error no entiendo qué significa"
- Olvida su contraseña regularmente porque no la anota y no tiene un método de recuperación claro
- Las instrucciones en pantalla le parecen pequeñas y usan términos que no reconoce (RFC, XML, CURP)

**Cita representativa:**  
*"Antes iba a ventanilla y en diez minutos ya tenía mi recibo. Ahora me dicen que lo puedo hacer desde la computadora, pero cada vez que lo intento me trabo en algo diferente."*

**Relación con requerimientos:**  
Principalmente RF01 (registro), RF02 (recuperar contraseña), RF03 (inicio de sesión), RF10 (consulta de CFDI), RF20 (FAR).

---

### Proto-Persona 2 — "Doña Concepción"

> *Jubilada administrativa con mínima experiencia digital que depende de apoyo externo*

| Campo | Detalle |
|---|---|
| **Nombre** | Concepción Dzul Rosado |
| **Edad** | 63 años |
| **Ocupación previa** | Asistente administrativa, Dirección General de Administración Escolar, UADY (28 años de servicio) |
| **Lugar de residencia** | Mérida, Yucatán |
| **Dispositivo** | Computadora portátil de su hija, que le presta cuando la necesita |
| **Conexión** | Internet compartido con su familia |
| **Competencia digital** | Básica — usa su teléfono principalmente para llamadas y mensajes de texto; el uso de computadora es esporádico |

**Objetivos:**
- Verificar el saldo de su Caja de Ahorro antes de un pago
- Obtener sus recibos de nómina sin necesitar que un familiar la lleve a la CGRH

**Frustraciones:**
- No recuerda cuál es su "usuario" ni tiene claro si es su nombre, número de empleado o correo institucional
- Cuando intenta registrarse, los formularios le parecen largos y confusos (RFC, CURP, CAPTCHA)
- Siente que "va a romper algo" si hace clic en el lugar equivocado

**Cita representativa:**  
*"Le pido a mi hija que me ayude porque yo sola no puedo. Pero tampoco quiero estar molestándola cada vez que necesito un papel."*

**Relación con requerimientos:**  
Principalmente RF01 (registro con múltiples campos — punto de mayor fricción para este perfil), RF03 (inicio de sesión), RF04 (cerrar sesión), RF30 (Caja de Ahorro).

---

### Proto-Persona 3 — "Don Mauricio"

> *Jubilado con algo más de experiencia digital, pero que enfrenta barreras visuales*

| Campo | Detalle |
|---|---|
| **Nombre** | Mauricio Sansores Herrera |
| **Edad** | 71 años |
| **Ocupación previa** | Técnico de laboratorio, Facultad de Medicina, UADY (32 años de servicio) |
| **Lugar de residencia** | Mérida, Yucatán |
| **Dispositivo** | Computadora de escritorio; monitor de 24" con resolución aumentada |
| **Conexión** | Internet en casa |
| **Competencia digital** | Media — usó computadora durante toda su vida laboral para registro de datos; sabe navegar en internet pero no está familiarizado con plataformas institucionales recientes |

**Objetivos:**
- Revisar sus aportaciones al Fondo de Ahorro para el Retiro cada mes
- Descargar su CFDI en PDF sin necesitar ayuda
- Que el sistema funcione bien con el tamaño de letra aumentado que usa en su computadora

**Frustraciones:**
- Muchas plataformas institucionales rompen su diseño cuando aumenta el zoom del navegador
- Ha intentado acceder al sistema anterior pero los mensajes de error no indican claramente qué debe corregir
- Los correos de confirmación de registro a veces llegan a correo no deseado y no sabe cómo encontrarlos

**Cita representativa:**  
*"Sí sé usar la computadora, pero los sistemas de la universidad siempre tienen algo que no funciona como esperas. Le sodo zoom a todo y luego los botones desaparecen."*

**Relación con requerimientos:**  
Principalmente RF02 (recuperar contraseña — correo de confirmación), RF05 (menú principal — accesibilidad visual), RF10 (consulta de CFDI), RF20 (FAR).

---

## 3. Síntesis — Patrones del Perfil Primario

| Patrón | Presente en |
|---|---|
| Dificultad con contraseñas y credenciales | Don Armando, Doña Concepción, Don Mauricio |
| Dependencia de apoyo externo (familiar o CGRH) | Doña Concepción, Don Armando |
| Necesidad de tipografía aumentada y baja densidad informativa | Don Mauricio, Don Armando |
| Terminología técnica como barrera (RFC, CURP, CAPTCHA, XML) | Don Armando, Doña Concepción |
| Uso esporádico que incrementa la curva de memoria | Los tres perfiles |
| Canal principal: escritorio | Los tres perfiles |

---

## Referencias

- Fisk, A. D., Rogers, W. A., Charness, N., Czaja, S. J., & Sharit, J. (2018). *Designing for Older Adults: Principles and Creative Human Factors Approaches* (3a ed.). CRC Press.
- INEGI. (2023). *Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de la Información en los Hogares (ENDUTIH 2023)*. Instituto Nacional de Estadística y Geografía.
- Cooper, A., Reimann, R., & Cronin, D. (2004). *About Face 3: The Essentials of Interaction Design*. Wiley.
- Gothelf, J., & Seiden, J. (2016). *Lean UX: Applying Lean Principles to Improve User Experience* (2a ed.). O'Reilly Media.
