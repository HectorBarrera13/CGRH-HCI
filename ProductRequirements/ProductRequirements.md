# Punto 4 — Requerimientos del Producto

**Universidad Autónoma de Yucatán — Facultad de Matemáticas | Ingeniería en Software**  
**Entregable HCI — Sistema CGRH (Coordinación General de Recursos Humanos)**  
*Mérida, Yucatán, 2026*

---

## Tabla de Contenidos

1. [Introducción y Contexto del Sistema](#1-introducción-y-contexto-del-sistema)
2. [Resumen de Requerimientos Funcionales](#2-resumen-de-requerimientos-funcionales)
3. [Requerimientos Funcionales — Descripción Detallada](#3-requerimientos-funcionales--descripción-detallada)
   - [RF01 — Registro de Empleado](#31-rf01--registro-de-empleado--alta-fricción)
   - [RF02 — Recuperar Contraseña](#32-rf02--recuperar-contraseña--alta-fricción)
   - [RF03 — Iniciar Sesión](#33-rf03--iniciar-sesión--alta-fricción)
   - [RF04 — Finalizar Sesión](#34-rf04--finalizar-sesión)
   - [RF05 — Menú Principal](#35-rf05--menú-principal)
   - [RF10 — Consultar CFDIs](#36-rf10--consultar-cfdis--alta-frecuencia)
   - [RF20 — Fondo de Ahorro para el Retiro](#37-rf20--fondo-de-ahorro-para-el-retiro--alta-frecuencia)
   - [RF30 — Caja de Ahorro](#38-rf30--caja-de-ahorro--alta-frecuencia)
4. [Requerimientos No Funcionales de Usabilidad](#4-requerimientos-no-funcionales-de-usabilidad)
5. [Relación RF — RNF](#5-relación-rf--rnf)
6. [Criterios de Aceptación Globales (HCI)](#6-criterios-de-aceptación-globales-hci)
7. [Referencias](#7-referencias)

---

## 1. Introducción y Contexto del Sistema

El Sistema para la CGRH (Coordinación General de Recursos Humanos) de la Universidad Autónoma de Yucatán es una plataforma digital de autoservicio que permite a empleados y jubilados UADY consultar su información económica: recibos de nómina (CFDI), Fondo de Ahorro para el Retiro (FAR) y Caja de Ahorro.

El contexto de uso más crítico desde la perspectiva de HCI involucra a **empleados jubilados mayores de 60 años** con nivel básico de alfabetización digital, acceso predominante desde dispositivos Android básicos y posibles limitaciones visuales y cognitivas. Este perfil define las prioridades de diseño de todos los requerimientos aquí descritos.

> **Usuarios objetivo primarios:** Jubilados UADY, 60+ años, alfabetización digital básica, computadoras con especificaciones low-end.

---

## 2. Resumen de Requerimientos Funcionales

El sistema contempla 8 requerimientos funcionales agrupados en dos categorías desde la perspectiva HCI:

- **Autenticación y acceso (RF01–RF05):** Puntos de mayor fricción para el usuario objetivo.
- **Consulta de prestaciones (RF10, RF20, RF30):** Mayor frecuencia de uso y valor directo para el jubilado.

| ID | Nombre | Prioridad HCI | Datos Involucrados | Nivel de Fricción (usuario 60+) |
|---|---|---|---|---|
| RF01 | Registro de Empleado | Alta | Clave, RFC, CURP, correo institucional, contraseña, teléfono | **Alto** — múltiples campos, CAPTCHA, flujo en 2 pasos |
| RF02 | Recuperar Contraseña | Alta | Correo institucional → enlace temporal → nueva contraseña | **Alto** — memoria de credenciales, gestión de correo |
| RF03 | Iniciar Sesión | Alta | Usuario + contraseña → acceso al sistema | **Alto** — punto de entrada, bloqueo = sin acceso a todo |
| RF04 | Finalizar Sesión | Media | Botón de cerrar sesión en menú | **Bajo**, acción clara y visible |
| RF05 | Menú Principal | Alta | Vista de opciones disponibles tras login | **Medio** — navegación y orientación del usuario |
| RF10 | Consultar CFDI | Muy Alta | Lista de recibos con filtros, descarga PDF/XML | **Medio** - lectura de datos financieros, descarga |
| RF20 | Fondo de Ahorro para el Retiro | Muy Alta | Tarjeta con saldos, aportaciones, rendimientos, descarga PDF | **Medio** — información financiera crítica |
| RF30 | Caja de Ahorro | Muy Alta | Resumen de cuenta de caja de ahorro, descarga PDF | **Medio** — información financiera crítica |

> **Nota:** Los requerimientos RF01, RF02 y RF03 representan los **puntos de mayor fricción** para el usuario de 60+ años. Un fallo en cualquiera de estos bloquea el acceso a toda la plataforma.

---

## 3. Requerimientos Funcionales — Descripción Detallada

---

### 3.1 RF01 — Registro de Empleado - Alta Fricción

| Campo | Detalle |
|---|---|
| **Actor** | Empleado / Jubilado UADY |
| **Descripción** | El empleado podrá registrarse a la plataforma para consultar sus documentos de nómina, fondos y administrar sus prestaciones. |
| **Precondición** | El usuario tiene acceso a internet, conoce su correo institucional UADY, RFC y CURP. |

**Flujo Principal:**
1. Usuario accede a la opción de registro.
2. Sistema muestra formulario — Paso 1: Clave de empleado, RFC, CURP, correo institucional, confirmación de correo, CAPTCHA.
3. Usuario completa datos y pulsa **"Continuar"**.
4. Sistema valida y muestra Paso 2: nombre (no editable, recuperado del sistema de nómina), usuario (auto-asignado), contraseña, confirmación, teléfono.
5. Usuario completa y pulsa **"Registrar"**.
6. Sistema envía correo de confirmación con enlace.
7. Usuario confirma y puede iniciar sesión.

**Flujos Alternativos:**
- **Alt. 1:** Correo con formato inválido → mensaje de error en el campo.
- **Alt. 2:** Enlace de confirmación caducado → mensaje y opción de re-registro.
- **Alt. 3:** Correos no coinciden → campo en rojo con mensaje descriptivo.
- **Alt. 4:** Usuario ya registrado → mensaje informativo con enlace a login.

> **Consideraciones HCI/Usabilidad:** Flujo en 2 pasos necesario pero complejo para adultos mayores. Recomendaciones: instrucciones claras antes de cada campo, indicador de progreso visible ("Paso 1 de 2"), mensajes de error en lenguaje sencillo sin tecnicismos, CAPTCHA accesible, tamaño de fuente mínimo 16pt, botones táctiles grandes (≥ 48×48 dp). Considerar guía visual o tutorial para el primer acceso.

---

### 3.2 RF02 — Recuperar Contraseña - Alta Fricción

| Campo | Detalle |
|---|---|
| **Actor** | Empleado / Jubilado UADY registrado |
| **Descripción** | El empleado registrado que olvidó su contraseña puede recuperar el acceso a través de su correo institucional. |
| **Precondición** | El usuario está registrado en el sistema y tiene acceso a su correo institucional (@correo.uady.mx). |

**Flujo Principal:**
1. Usuario selecciona "¿Recuperar contraseña?" en pantalla de login.
2. Sistema solicita correo institucional.
3. Usuario ingresa correo y confirma.
4. Sistema envía enlace temporal al correo.
5. Usuario abre el enlace.
6. Sistema presenta formulario de nueva contraseña.
7. Usuario crea y confirma nueva contraseña.
8. Sistema confirma el cambio y redirige al login.

**Flujos Alternativos:**
- **Alt. 1:** Correo no registrado → mensaje "Correo no encontrado".
- **Alt. 2:** Enlace caducado → mensaje y opción de reenvío.
- **Alt. 3:** Nueva contraseña no cumple requisitos → indicación visual de reglas.

> **Consideraciones HCI/Usabilidad:** Este es el flujo más crítico del sistema para adultos mayores: implica recordar contraseña, acceder a correo y crear una nueva contraseña compleja. Recomendaciones: mostrar requisitos de contraseña en tiempo real con indicador visual (débil/media/fuerte), permitir ver la contraseña ingresada (ícono ojo), mensajes de error extremadamente claros, tiempo de expiración del enlace no menor a 30 minutos, y siempre mostrar el número de RRHH como alternativa de soporte.

---

### 3.3 RF03 — Iniciar Sesión - Alta Fricción

| Campo | Detalle |
|---|---|
| **Actor** | Empleado / Jubilado UADY registrado |
| **Descripción** | El empleado registrado inicia sesión con su usuario y contraseña para acceder al sistema. |
| **Precondición** | El usuario está registrado en el sistema. |

**Flujo Principal:**
1. Usuario accede a la pantalla de inicio de sesión.
2. Sistema muestra: logo institucional, campos de usuario y contraseña, botón "Iniciar Sesión" y enlace "¿Recuperar contraseña?".
3. Usuario ingresa usuario y contraseña.
4. Sistema valida credenciales.
5. Sistema muestra el menú principal (RF05).

**Flujos Alternativos:**
- **Alt. 1:** Usuario o contraseña incorrectos → mensaje "El usuario o la contraseña son incorrectos", limpia los campos.
- **Ext. 1:** Usuario selecciona "Recuperar contraseña" → flujo RF02.

> **Consideraciones HCI/Usabilidad:** El login es la puerta de entrada al sistema. Recomendaciones: campo de usuario pre-llenado si el dispositivo lo permite, botón de mostrar/ocultar contraseña, mensaje de error descriptivo sin revelar qué campo es incorrecto (seguridad), enlace de recuperación muy visible, no bloquear cuenta automáticamente sin aviso previo. Considerar opción "Recordarme" para dispositivos de confianza.

---

### 3.4 RF04 — Finalizar Sesión

| Campo | Detalle |
|---|---|
| **Actor** | Empleado / Jubilado UADY con sesión activa |
| **Descripción** | El empleado puede cerrar su sesión de forma explícita y segura. |
| **Precondición** | El usuario tiene una sesión activa en el sistema. |

**Flujo Principal:**
1. Usuario localiza y selecciona la opción "Cerrar sesión" en el menú.
2. Sistema invalida la sesión del usuario.
3. Sistema redirige a la pantalla de inicio de sesión.

**Flujos Alternativos:** Sin flujos alternativos significativos. La sesión también puede expirar por tiempo de inactividad.

> **Consideraciones HCI/Usabilidad:** Elemento de cierre de sesión siempre visible y claramente etiquetado como "Cerrar sesión" (no íconos ambiguos). Considerar confirmación antes de cerrar para evitar cierres accidentales. Tiempo de inactividad antes del cierre automático debe ser generoso (mínimo 15 minutos) dado el perfil de usuario.

---

### 3.5 RF05 — Menú Principal

| Campo | Detalle |
|---|---|
| **Actor** | Empleado / Jubilado UADY autenticado |
| **Descripción** | Tras el inicio de sesión, el usuario ve el menú principal que le da acceso a todas las funciones disponibles. |
| **Precondición** | El usuario ha iniciado sesión exitosamente (RF03). |

**Flujo Principal:**
1. Sistema muestra pantalla principal con las opciones disponibles: CFDI, Fondo de Ahorro para el Retiro, Caja de Ahorro.
2. Usuario selecciona la opción deseada.
3. Sistema navega a la sección correspondiente.

**Flujos Alternativos:** Sin flujos alternativos. El menú es el punto de distribución principal.

> **Consideraciones HCI/Usabilidad:** Punto de orientación clave. Recomendaciones: máximo 4–5 opciones visibles para evitar sobrecarga cognitiva, íconos representativos acompañados **siempre** de texto descriptivo, jerarquía visual clara, bienvenida personalizada con nombre del usuario, y número de soporte de RRHH siempre visible en esta pantalla.

---

### 3.6 RF10 — Consultar CFDIs - Alta Frecuencia

| Campo | Detalle |
|---|---|
| **Actor** | Empleado / Jubilado UADY autenticado |
| **Descripción** | El empleado puede visualizar y descargar sus Comprobantes Fiscales Digitales por Internet (recibos de nómina). |
| **Precondición** | El usuario ha iniciado sesión. El sistema cuenta con CFDIs del empleado. |

**Flujo Principal:**
1. Usuario selecciona "CFDI" en menú principal.
2. Sistema muestra tabla con CFDIs del mes/año actual: folio, departamento, quincena, fechas de pago, días pagados, botones de descarga (PDF/XML).
3. Filtros disponibles: año y mes de fecha de pago.
4. Usuario puede descargar PDF individual, XML individual, o seleccionar varios/todos para descarga masiva (.zip).
5. Sistema genera y descarga el archivo solicitado.

**Flujos Alternativos:**
- **Alt. 1:** Sin filtros aplicados → muestra todos los CFDIs del año actual.
- **Alt. 2:** Usuario cancela descarga del .zip → sistema cierra la ventana de guardado.

> **Consideraciones HCI/Usabilidad:** Función de mayor uso del sistema. Recomendaciones: mostrar primero el CFDI más reciente, usar términos familiares ("Recibo de Nómina" junto a "CFDI"), botones de descarga PDF grandes y visibles (PDF es más familiar que XML para adultos mayores), filtros simples con listas desplegables, paginación clara con números de página visibles, etiquetas de quincena en formato comprensible ("1a quincena enero" no solo "01/01/2026").

---

### 3.7 RF20 — Fondo de Ahorro para el Retiro - Alta Frecuencia

| Campo | Detalle |
|---|---|
| **Actor** | Empleado / Jubilado UADY autenticado |
| **Descripción** | El empleado puede ver un resumen de su cuenta del Fondo de Ahorro para el Retiro (FAR) administrado por Banco Santander. |
| **Precondición** | El usuario ha iniciado sesión. El sistema tiene datos del FAR del empleado (cargados por RRHH). |

**Flujo Principal:**
1. Usuario selecciona "Fondo de Ahorro para el Retiro".
2. Sistema muestra tarjeta con:
   - Datos generales: clave y nombre del empleado, fecha del último reporte.
   - Resumen financiero: Saldo inicial, Aportaciones, Retiros, Rendimientos, Saldo Final, Derechos Adquiridos.
   - Nota sobre Banco Santander.
   - Botón "Descargar" reporte PDF.
3. Usuario puede descargar el reporte completo en PDF.

**Flujos Alternativos:** Sin flujos alternativos (datos son de solo lectura).

> **Consideraciones HCI/Usabilidad:** Información financiera de alto valor emocional para el jubilado. Recomendaciones: presentar el Saldo Final de forma prominente en tipografía grande, usar tarjeta bien delimitada visualmente, explicar brevemente cada concepto ("Rendimientos: intereses generados por tu ahorro"), indicar claramente la fecha del dato para evitar confusión sobre vigencia, botón de descarga PDF grande y claramente etiquetado.

---

### 3.8 RF30 — Caja de Ahorro - Alta Frecuencia

| Campo | Detalle |
|---|---|
| **Actor** | Empleado / Jubilado UADY autenticado |
| **Descripción** | El empleado puede ver el resumen de su cuenta de Caja de Ahorro. |
| **Precondición** | El usuario ha iniciado sesión. El sistema tiene datos de caja de ahorro del empleado. |

**Flujo Principal:**
1. Usuario selecciona "Caja de Ahorro".
2. Sistema muestra tarjeta con resumen de la cuenta: datos del empleado, saldos, movimientos del período.
3. Usuario puede descargar reporte en PDF.

**Flujos Alternativos:** Sin flujos alternativos (datos son de solo lectura).

> **Consideraciones HCI/Usabilidad:** Mismas consideraciones que RF20. Presentación visual clara con énfasis en saldo actual y descarga de reporte. La **consistencia visual con RF20** es importante para reducir la curva de aprendizaje del usuario.

---

## 4. Requerimientos No Funcionales de Usabilidad

Los siguientes RNF se derivan del perfil de usuario objetivo y se fundamentan en los principios heurísticos de Nielsen (1994) y la norma ISO 9241-11:2018. Se priorizan cuatro dimensiones: **accesibilidad visual, legibilidad, carga cognitiva y confianza/soporte**.

| ID | Atributo de Usabilidad | Descripción / Criterio de Aceptación | RFs Relacionados | Heurística Nielsen |
|---|---|---|---|---|
| RNF-01 | Legibilidad — Tamaño de fuente | Tamaño mínimo de fuente **16pt** en toda la interfaz. Encabezados ≥ 20pt. Sin texto menor a 14pt en ningún elemento. | Todos los RF | H8 — Estética y diseño minimalista |
| RNF-02 | Accesibilidad táctil | Áreas táctiles mínimas de **48×48 dp** para todos los botones e ítems interactivos. Sin botones de menos de 9mm de alto. | Todos los RF | H7 — Flexibilidad y eficiencia |
| RNF-03 | Contraste visual | Relación de contraste mínima de **4.5:1 (WCAG AA)** entre texto y fondo. Nunca usar gris claro sobre blanco. | Todos los RF | H8 — Estética y diseño minimalista |
| RNF-04 | Mensajes de error claros | Mensajes en lenguaje cotidiano, sin códigos de error, con indicación clara de qué hacer. Máximo 2 oraciones. | RF01, RF02, RF03 | H9 — Ayuda a reconocer y recuperarse de errores |
| RNF-05 | Reconocimiento sobre recuerdo | Todas las opciones visibles; nunca depender de que el usuario recuerde rutas. Breadcrumbs visibles en navegación. | RF05, RF10, RF20, RF30 | H6 — Reconocimiento sobre recuerdo |
| RNF-06 | Tiempo de respuesta | Carga ≤ **3 segundos** en redes 3G típicas. Indicador de carga visible si la operación tarda más de 1 segundo. | RF10, RF20, RF30 | H1 — Visibilidad del estado del sistema |
| RNF-07 | Flujos cortos | El número de pasos para completar cualquier tarea de consulta no debe superar **3 interacciones** desde el menú principal. | RF10, RF20, RF30 | H7 — Flexibilidad y eficiencia |
| RNF-08 | Prevención de errores | Botones destructivos deben incluir confirmación explícita. Formularios validan en tiempo real antes del envío. | RF01, RF02, RF04 | H5 — Prevención de errores |
| RNF-09 | Soporte humano visible | Número de contacto de RRHH **siempre visible** en el menú principal y en pantallas de error. Alternativa analógica siempre presente. | RF05, pantallas de error RF01–RF03 | H10 — Ayuda y documentación |
| RNF-10 | Consistencia visual | Mismo esquema de color, tipografía, iconografía y patrones de interacción en toda la aplicación. Mismos términos para mismos conceptos. | Todos los RF | H4 — Consistencia y estándares |
| RNF-11 | Compatibilidad de dispositivos | Funciona correctamente en dispositivos **Android 8.0+** con pantallas de 5–6 pulgadas y resolución mínima 720×1280px. | Todos los RF | H7 — Flexibilidad y eficiencia |
| RNF-12 | Tasa de éxito de tareas | ≥ **80%** de usuarios del perfil objetivo completan cada tarea sin asistencia. Tiempo en tareas de consulta ≤ **90 segundos**. | RF10, RF20, RF30 | ISO 9241-11 — Eficacia |

---

## 5. Relación RF — RNF

Matriz de criticidad: **✓✓** = Crítico para este RF | **✓** = Relevante para este RF

| RF | Legibilidad | Táctil | Contraste | Errores | Reconoc. | Flujos Cortos | Soporte Visible | Prevención |
|---|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| RF01 | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓✓ |
| RF02 | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓✓ |
| RF03 | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓ | ✓✓ | ✓ |
| RF04 | ✓ | ✓✓ | ✓ | ✓ | ✓ | ✓ | ✓ | ✓✓ |
| RF05 | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓ | ✓✓ | ✓ |
| RF10 | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓ | ✓ |
| RF20 | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓ | ✓ |
| RF30 | ✓✓ | ✓✓ | ✓✓ | ✓ | ✓✓ | ✓✓ | ✓ | ✓ |

---

## 6. Criterios de Aceptación Globales (HCI)

Los siguientes criterios definen el mínimo de calidad de usabilidad que el sistema debe alcanzar antes de considerarse apto para los usuarios objetivo:

| # | Criterio | Métrica | RF Objetivo |
|---|---|---|---|
| T1 | **Tasa de éxito de tareas** | ≥ 80% de usuarios del perfil objetivo completan cada tarea sin asistencia externa. | Todos |
| T2 | **Tiempo en tareas de consulta** | ≤ 90 segundos desde el menú principal hasta visualizar el dato clave. | RF10, RF20, RF30 |
| T3 | **Tasa de abandono** | ≤ 10% en las tareas críticas durante las pruebas de usabilidad. | RF01, RF02, RF03 |
| T4 | **Puntuación SUS** | ≥ 70 en la escala SUS adaptada con lenguaje simplificado para el perfil objetivo. | Todos |
| T5 | **Errores de usabilidad severos** | 0 errores de nivel 4–5 (escala Nielsen) en revisión heurística por ≥ 3 evaluadores. | Todos |
| T6 | **Conformidad WCAG AA** | Contraste mínimo 4.5:1 en todos los elementos de texto. Verificado con herramienta automatizada. | Todos |

---

## 7. Referencias

- Nielsen, J. (1994). *10 Usability Heuristics for User Interface Design*. Nielsen Norman Group.
- ISO 9241-11:2018. *Ergonomics of human-system interaction — Part 11: Usability: Definitions and concepts*.
- WCAG 2.1 — *Web Content Accessibility Guidelines*. W3C, 2018.
- Brooke, J. (1996). *SUS: A 'quick and dirty' usability scale*. Usability Evaluation in Industry.
- UADY CGRH — Documentos de requerimientos funcionales RF01–RF30, Sistema de Prestaciones UADY, 2025–2026.

---

*Interacción Humano-Computadora — Ingeniería en Software, UADY | 2026*
