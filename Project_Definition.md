# Análisis de Definición de Proyecto: Sistema de Autoservicio CGRH – UADY

---

## 1. Relevancia Social

La Coordinación General de Recursos Humanos de la UADY busca ofrecer al personal activo y jubilado acceso autónomo a CFDI, el Fondo de Ahorro para el Retiro (FAR) y la Caja de Ahorro (RF10, RF20 y RF30). La ausencia de un canal digital centralizado *obliga* actualmente a los empleados a depender de trámites presenciales o intermediados, generando ineficiencias operativas que un sistema de autoservicio bien diseñado eliminaría.

El análisis HCI se enfocará en jubilados mayores de 60 años, segmento que concentra la mayor densidad de barreras de acceso tecnológico. Esta delimitación es metodológicamente ventajosa: los criterios de diseño derivados del perfil más exigente benefician al sistema en su totalidad, partiendo de que si un usuario de la tercera edad puede utilizarlo, la gran mayoría del resto podrá también.

La pertinencia de esta segmentación se respalda con evidencia estadística. Según la ENDUTIH 2023 del INEGI, solo el 43.7% de la población entre 55 y 64 años usó internet en el último año, frente al 82.8% del grupo de 25 a 34 años. Esta brecha estructural justifica que los flujos RF02 (recuperación de contraseña) y RF03 (inicio de sesión) sean diseñados con criterios de accesibilidad cognitiva en lugar de convenciones para usuarios con alta competencia digital. Adicionalmente, los jubilados carecen de presencia cotidiana en instalaciones universitarias, lo que amplifica su dependencia de un canal autónomo para acceder a información financiera crítica para su planeación posactiva.

---

## 2. Innovación

Los sistemas de recursos humanos en instituciones de educación superior mexicanas asumen implícitamente un usuario con competencia digital media-alta, priorizando densidad funcional sobre claridad de navegación. Este proyecto quiere invertir esa premisa: la arquitectura de información se deriva del perfil de menor competencia dentro de la población, lo que tiene consecuencias concretas desde la estructura del menú principal (RF05) hasta la granularidad de los mensajes de error en autenticación.

La manifestación más clara de esta orientación es tratar RF02 como requerimiento de primer nivel. Fisk et al. en *Designing for Older Adults* (3a ed., 2018) documentan que la gestión de contraseñas es una de las barreras más frecuentes que conduce al abandono del canal digital. Diseñar este flujo con pasos reducidos, retroalimentación explícita en cada estado y sin terminología técnica lo diferencia de los desarrollos institucionales comparables donde la recuperación de contraseña es un flujo secundario mal documentado.

La apuesta por escritorio sobre mobile-first concentra el esfuerzo de diseño en una sola superficie de visualización amplia, que habilita tipografía aumentada, espaciado generoso y baja densidad informativa por pantalla: factores directamente vinculados a la usabilidad para usuarios con posible disminución visual. Finalmente, centralizar CFDI, FAR y Caja de Ahorro en una plataforma con navegación de máximo dos niveles de profundidad es una condición de usabilidad que elimina la dispersión actual de datos y reduce la carga cognitiva del usuario.

---

## 3. Factibilidad

**Argumentos que respaldan el éxito del desarrollo.** Los requerimientos se limitan a autenticación, gestión de sesión y consulta de datos: patrones de desarrollo web convencionales sin procesamiento en tiempo real ni integraciones externas. Los datos de CFDI, FAR y Caja de Ahorro residen en bases institucionales de la CGRH, cuya jurisdicción directa elimina dependencias de autorización entre unidades. La UADY provee infraestructura de servidores sin necesidad de hosting externo. Al ser un sistema de consulta pura —los usuarios visualizan información sin modificarla— la superficie de riesgo de seguridad se reduce y el alcance de las pruebas de regresión queda acotado. La restricción a escritorio simplifica adicionalmente la capa de presentación a un solo entorno de renderizado.

**Fortalezas y debilidades del equipo.**

| Dimensión | Fortaleza | Debilidad |
|---|---|---|
| Técnica | Familiaridad con desarrollo web y patrones de autenticación estándar | Experiencia limitada en integración con sistemas legados institucionales |
| Metodológica | Enfoque HCI con segmento de usuario definido y justificado | Experiencia reducida en pruebas de usabilidad con adultos mayores |
| Organizacional | Acceso al contexto institucional de la UADY y vinculación con la CGRH | Dependencia de tiempos y disponibilidad de la unidad para validar datos |
| Alcance | Requerimientos funcionales acotados y bien delimitados | Riesgo de expansión si la CGRH solicita funcionalidades adicionales |

**Retos desde la perspectiva HCI y de producto.** El principal desafío es la validación con usuarios reales: reclutar jubilados mayores de 60 años para pruebas de usabilidad requiere coordinación activa con la CGRH y una logística adaptada a las condiciones de movilidad y disponibilidad de este perfil, que además ya no tiene presencia regular en las instalaciones universitarias. Los sustitutos de perfil más joven invalidan la señal específica que justifica la segmentación del proyecto.

Desde el diseño de producto, el flujo de registro (RF01) es el punto más crítico: concentra las principales decisiones de alfabetización digital y un diseño deficiente en él genera abandono temprano antes de que el usuario experimente el valor de los módulos de consulta. El equipo deberá planificar al menos dos ciclos de evaluación con el segmento objetivo antes de considerarlo estable.