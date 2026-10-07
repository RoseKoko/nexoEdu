# nexoEdu — Plan de Calidad del Proyecto, Etapa I: Gestión de Calidad

Sep 30, 2026 · @Dylan

## 1. Portada

| Campo | Contenido |
| --- | --- |
| Institución | Tecnológico Nacional de México — Instituto Tecnológico de Tijuana |
| Materia | Gestión de Proyectos de Software |
| Nombre del proyecto | nexoEdu — plataforma integral para la gestión escolar |
| Documento | Plan de Calidad del Proyecto — Etapa I: Gestión de Calidad |
| Versión del documento | 1.0 (línea base) |
| Integrantes | Dylan Alexis Padilla · Stephanie Ariana Medrano Vargas · Ricardo Alejandro Pineda Gómez |
| Docente | Mtra. María Guadalupe Rodríguez López |
| Periodo del proyecto | 23 de septiembre al 25 de noviembre de 2026 |
| Periodo de la etapa | 23 de septiembre al 6 de octubre de 2026 |
| Fecha de entrega | 5 de octubre de 2026 |

## 2. Introducción

Este Plan de Calidad define qué parte del sistema escolar se desarrollará durante el periodo académico y con qué criterios se juzgará su calidad. Es la línea base contra la que se medirán las siguientes etapas: planificación, presentación de avances, supervisión y entrega final.

El proyecto parte de una visión amplia: una plataforma que centralice la información académica, disciplinaria, administrativa y de comunicación de una escuela. Esa visión es demasiado grande para nueve semanas y tres integrantes. Por eso el plan separa con claridad lo que el equipo se compromete a entregar (la base operativa) de lo que queda como evolución futura.

Establecer la calidad desde el inicio evita dos errores comunes: descubrir al final que “terminado” significaba cosas distintas para cada integrante, y dejar que el alcance crezca sin control. Aquí la calidad se define como requisitos verificables, criterios de aceptación medibles, métricas simples, control de cambios y evidencias conservadas. La gestión del proyecto y la calidad del software se tratan como un mismo proceso: lo que no se planifica y registra no se puede demostrar.

## 3. Descripción del proyecto

El sistema es una plataforma de gestión escolar con un solo acceso mediante login y control de permisos por roles (RBAC). Su visión es centralizar la información académica, disciplinaria, administrativa y de comunicación entre escuela, docentes, prefectura, alumnos y padres o tutores.

**Necesidad que atiende:** facilitar el registro diario de información, el seguimiento de alumnos, la comunicación con las familias, la operación administrativa y la generación de reportes para la toma de decisiones.

**Principales usuarios:** alumno; padre, madre o tutor; docente; prefectura; dirección; administración y contaduría; administrador del sistema.

**Principios base del producto** (tomados del resumen ejecutivo):

- Un solo acceso al sistema mediante login con roles.
- Control de permisos basado en RBAC.
- Información organizada por ciclo escolar.
- Relación entre alumnos y uno o más padres/tutores.
- Bitácora para acciones sensibles.
- Desarrollo por fases para evitar construir todo al mismo tiempo.

**Escuela destinataria:** caso simulado de una preparatoria (nivel medio superior). El sistema no se desarrolla para una escuela específica; todos los datos de prueba serán ficticios.

## 4. Problemática

nexoEdu se plantea como un caso simulado: una preparatoria genérica, no una escuela específica. La problemática se deriva de la documentación del proyecto, a partir de lo que el sistema debe resolver. No se usan estadísticas ni datos externos.

**Situación actual (inferida):** la información de alumnos, asistencia, conducta y comunicación con las familias no está centralizada en un sistema único con control de acceso por rol.

**Problemas identificados:**

- El registro de asistencia, faltas y retardos no queda en un historial consultable por alumno, grupo o periodo.
- Los reportes de conducta y sus evidencias no llegan de forma directa a prefectura ni a los padres/tutores.
- Los padres/tutores no tienen un medio para consultar la asistencia y conducta de sus hijos.
- No existe un control formal de quién puede ver o modificar información sensible de alumnos y familias.
- No hay trazabilidad de quién creó o modificó un registro, lo que dificulta resolver aclaraciones o disputas.

**Consecuencias:** seguimiento tardío de ausencias e incidencias, información dispersa o duplicada, exposición de datos personales a personas no autorizadas y falta de evidencia ante reclamaciones.

**Necesidad de una solución:** un sistema que concentre el flujo escolar principal (alumnos, grupos, asistencia y conducta), restrinja el acceso según el rol y deje registro de las acciones sensibles.

## 5. Justificación

Construir primero la base operativa resuelve el flujo escolar más frecuente y deja lista la estructura sobre la que crecerán las demás fases.

| Aspecto | Qué aporta la primera versión |
| --- | --- |
| Centralización de información | Alumnos, padres/tutores, docentes, grados y grupos en una sola base, organizada por ciclo escolar. |
| Seguimiento de alumnos | Historial de asistencia y de reportes de conducta consultable por alumno. |
| Control de asistencia y conducta | Prefectura registra asistencia diaria; docentes registran reportes de conducta con evidencias. |
| Comunicación entre actores | Los padres/tutores consultan la asistencia y los reportes de conducta de sus hijos. Las notificaciones automáticas quedan para la Fase 2. |
| Seguridad y permisos | Login único con RBAC: cada rol ve y hace solo lo que le permite la matriz de permisos. |
| Trazabilidad | Bitácora de quién creó, modificó o eliminó información relevante, con fecha y hora. |
| Crecimiento futuro | Arquitectura modular y datos por ciclo escolar para agregar comunicación, académico, administración y reportes sin rehacer la base. |

El roadmap del proyecto recomienda esta misma base para “validar el flujo escolar principal antes de agregar calificaciones, pagos, inventario avanzado y dashboards”.

## 6. Objetivos

### 6.1 Objetivo general

Desarrollar, entre el 23 de septiembre y el 25 de noviembre de 2026, la primera versión funcional de la plataforma de gestión escolar (base operativa), que permita registrar alumnos, padres/tutores, docentes, grados y grupos, controlar la asistencia y los reportes de conducta con evidencias, y ofrecer consulta a padres/tutores, con acceso por roles y bitácora de acciones sensibles, verificando su cumplimiento mediante los criterios y métricas de este plan.

### 6.2 Objetivos específicos

1. Implementar un login único con control de acceso por roles conforme a la matriz de permisos del proyecto.
2. Permitir al administrador del sistema gestionar usuarios, roles, ciclos escolares, grados y grupos.
3. Registrar alumnos, padres/tutores y docentes, con sus asociaciones a grupos y entre alumno y tutor.
4. Permitir a prefectura registrar asistencias, faltas y retardos diarios por grupo.
5. Permitir a docentes y prefectura registrar reportes de conducta con evidencias adjuntas.
6. Permitir a los padres/tutores consultar asistencia, reportes de conducta y evidencias solo de sus hijos.
7. Registrar en bitácora las acciones sensibles del alcance inicial.
8. Verificar la primera versión con casos de prueba documentados, incluidas pruebas de permisos por rol.
9. Mantener control de cambios, métricas y evidencias durante todo el proyecto.

## 7. Alcance del proyecto

El compromiso de esta materia es la **Fase 1 — Base operativa** del roadmap. Las fases 2 a 5 son visión futura y no forman parte de la entrega.

### 7.1 Visión completa del sistema

A largo plazo, el sistema contempla 15 módulos: autenticación y acceso, docentes, alumnos, padres o tutores, prefectura, dirección, administración y contaduría, inventario de uniformes, académico, calendario escolar, comunicación y notificaciones, inscripciones y matrícula, pagos y colegiaturas, reportes y dashboards, y auditoría y bitácora.

### 7.2 Incluido (alcance de la primera versión)

| Área | Qué incluye |
| --- | --- |
| Autenticación y roles | Login con usuario y contraseña, cierre de sesión, menú según rol, restricción de módulos y acciones. |
| Gestión de usuarios | Crear, editar, desactivar y reactivar usuarios; asignar roles. |
| Estructura escolar mínima | Ciclo escolar, grados y grupos. |
| Comunidad escolar | Alumnos, padres/tutores (relación muchos a muchos) y docentes asignados a grupos. |
| Prefectura | Registro y consulta de asistencias, faltas y retardos. |
| Conducta | Reportes de conducta con evidencias, registrados por docentes y prefectura. |
| Padres/tutores | Consulta de datos, asistencia, reportes de conducta y evidencias de sus hijos. |
| Bitácora básica | Registro y consulta de acciones sensibles del alcance inicial. |

Los requisitos de prioridad **Alta** (sección 9) son el compromiso mínimo. Los de prioridad Media y Baja son los primeros en posponerse si el tiempo no alcanza, mediante control de cambios.

### 7.3 No incluido (fuera del alcance de esta entrega)

| Funcionalidad | Fase del roadmap |
| --- | --- |
| Notificaciones automáticas (correo, sistema, push) | Fase 2 |
| Justificación de faltas | Fase 2 |
| Permisos y autorizaciones de salida | Fase 2 |
| Avisos generales y mensajes | Fase 2 |
| Calendario escolar y horarios de clase | Fase 2 |
| Materias, planes de estudio, tareas, entregas, calificaciones, boletas y kardex | Fase 3 |
| Pagos, colegiaturas, adeudos, recibos, becas y recargos | Fase 4 |
| Inventario y ventas de uniformes | Fase 4 |
| Dashboards, reportes estadísticos y exportación a PDF/Excel | Fase 5 |
| Inscripciones, reinscripciones y control de documentación | Sin fase asignada (ver sección 21) |
| Aplicación móvil nativa o PWA | Trabajo futuro (solo web: D-05, D-06; PWA ligada a Fase 2: D-07) |

### 7.4 Trabajo futuro / evolución prevista del sistema

La Fase 2 añadiría comunicación y seguimiento (notificaciones, justificantes, permisos de salida, avisos y calendario). La Fase 3 incorporaría la operación académica, la Fase 4 la gestión económica e inventario, y la Fase 5 los reportes avanzados para dirección. La base de la primera versión (roles, ciclo escolar, alumnos, grupos y bitácora) está pensada para soportar esas fases. **Su mención aquí no es un compromiso de desarrollo durante la materia.**

## 8. Usuarios y actores

La visión general contempla siete roles; la primera versión involucra directamente a cinco. Alumno y Administración y contaduría quedan fuera de esta versión.

| Rol | Función en la visión general | Participación en el alcance inicial |
| --- | --- | --- |
| Administrador del sistema | Configura usuarios, roles, ciclos, grados, grupos, catálogos y consulta la bitácora. | **Directa.** Da de alta usuarios, roles y estructura escolar. |
| Prefectura | Asistencia, disciplina, permisos y control operativo de alumnos. | **Directa.** Registra asistencia y da seguimiento a la conducta. |
| Docente | Imparte clases, registra información académica y reporta situaciones de sus alumnos. | **Directa.** Registra reportes de conducta con evidencias de sus grupos. |
| Padre, madre o tutor | Da seguimiento académico, disciplinario, administrativo y de asistencia. | **Directa.** Consulta asistencia y conducta de sus hijos. |
| Dirección | Visión global de consulta y supervisión; reportes estratégicos. | **Directa, de consulta.** Consulta alumnos, asistencia, conducta y bitácora; puede crear y editar alumnos según la matriz. |
| Alumno | Consulta su información académica y escolar. | **Fuera del alcance inicial.** No tendrá cuenta propia en la primera versión (D-01); su información la consultan sus padres/tutores. |
| Administración y contaduría | Pagos, colegiaturas, ventas e inventario de uniformes. | **Fuera del alcance inicial** (Fase 4). La matriz le permite crear y editar alumnos; ver inconsistencia I-03. |

## 9. Requerimientos funcionales del alcance inicial

La primera versión compromete 26 requisitos, tomados de los módulos 1, 2, 3, 4, 5 y 15 de los requisitos funcionales y filtrados por la Fase 1 del roadmap. Los permisos citados provienen de la matriz de roles.

| ID | Requisito | Descripción | Prioridad | Criterio de aceptación |
| --- | --- | --- | --- | --- |
| RF-01 | Iniciar sesión | Todo usuario ingresa con usuario y contraseña por un login único. | Alta | Con credenciales válidas se accede; con inválidas se rechaza el acceso con mensaje y no se crea sesión. |
| RF-02 | Mantener sesión segura | El usuario puede cerrar sesión; las páginas protegidas exigen sesión activa. | Alta | Tras cerrar sesión, ninguna página protegida es accesible sin volver a autenticarse. |
| RF-03 | Menú según rol | El sistema muestra opciones diferentes según el rol del usuario. | Alta | Cada rol ve solo los módulos que la matriz le permite (verificado con un usuario de prueba por rol). |
| RF-04 | Restringir acciones según permisos | Las acciones no permitidas se bloquean aunque se intente acceder directamente (URL o petición). | Alta | 100 % de los intentos de acción no permitida en la matriz de pruebas de permisos son rechazados. |
| RF-05 | Restablecer contraseña | El administrador restablece la contraseña de un usuario. Sin recuperación por correo en la primera versión (D-04). | Baja | El usuario accede con la nueva contraseña y la anterior deja de funcionar. |
| RF-06 | Gestionar usuarios | El administrador crea y edita usuarios. | Alta | Un usuario creado puede iniciar sesión; no se permite un nombre de usuario duplicado. |
| RF-07 | Desactivar y reactivar usuarios | El administrador bloquea, desactiva o reactiva usuarios. | Media | Un usuario desactivado no puede iniciar sesión; al reactivarlo, sí. La acción queda en bitácora. |
| RF-08 | Asignar roles | El administrador asigna rol(es) a cada usuario. Un usuario puede tener varios roles (D-02). | Alta | Al cambiar el rol, cambian el menú y los permisos en el siguiente inicio de sesión. |
| RF-09 | Configurar ciclo escolar, grados y grupos | Administrador (y dirección para grupos) configuran la estructura escolar. | Alta | Todo grupo pertenece a un grado y a un ciclo escolar; no se permiten grupos duplicados en el mismo grado y ciclo. |
| RF-10 | Registrar alumnos | Registro de datos generales y matrícula del alumno (dirección, administrador). | Alta | El alumno se guarda con los datos obligatorios (nombre completo, matrícula, fecha de nacimiento, CURP y grupo; D-17); el sistema impide duplicados por matrícula. |
| RF-11 | Asociar alumno a grado, grupo y ciclo | Cada alumno queda inscrito en un grupo de un ciclo escolar. | Alta | El alumno aparece en la lista de su grupo y ciclo, y en ningún otro grupo del mismo ciclo. |
| RF-12 | Registrar padres/tutores y asociarlos | Un tutor puede tener varios alumnos y un alumno varios tutores. | Alta | Un tutor con dos hijos ve a ambos; un alumno con dos tutores es visible para los dos. |
| RF-13 | Registrar docentes y asignarlos a grupos | Alta de docentes y su asignación a uno o más grupos. | Alta | El docente ve únicamente los grupos asignados. |
| RF-14 | Editar alumnos | Edición por dirección y administrador; prefectura “limitado” \[POR DEFINIR\]. | Media | La edición se guarda y queda en bitácora con el valor anterior y el nuevo. |
| RF-15 | Registrar asistencia diaria | Prefectura marca asistencia, falta o retardo por alumno, por grupo y fecha. | Alta | Se guarda un solo registro por alumno y fecha; un segundo intento se rechaza o se trata como edición. |
| RF-16 | Modificar asistencia | Corrección de un registro de asistencia ya capturado. | Media | El cambio se guarda y la bitácora conserva quién, cuándo y qué cambió. |
| RF-17 | Consultar asistencia | Por alumno, grupo y fecha o periodo (prefectura, dirección; docente solo sus grupos). | Media | Los filtros devuelven exactamente los registros capturados en los datos de prueba. |
| RF-18 | Registrar reporte de conducta | Docente (sus grupos), prefectura y dirección registran reportes sobre un alumno. | Alta | Un docente solo puede elegir alumnos de sus grupos; el reporte queda asociado al alumno, autor y fecha. |
| RF-19 | Adjuntar evidencias | Se suben archivos como evidencia de un reporte de conducta. | Alta | El archivo se guarda y puede abrirse desde el reporte. Solo se aceptan JPG, PNG y PDF; el tamaño máximo está por confirmar (I-13). |
| RF-20 | Consultar reportes y evidencias | Prefectura y dirección ven todos; docente, los de sus grupos. | Alta | Cada rol ve exactamente los reportes que le corresponden en los datos de prueba. |
| RF-21 | Registrar incidencias disciplinarias | Prefectura registra incidencias y da seguimiento a reportes. Relación con “reporte de conducta” por confirmar (I-01). | Media | La incidencia queda asociada al alumno y es consultable por prefectura, dirección y sus tutores. |
| RF-22 | Padre/tutor consulta datos del alumno | Datos generales de sus hijos o tutorados. | Alta | Solo ve alumnos asociados; intentar abrir otro alumno (por ejemplo, cambiando el ID en la URL) es rechazado. |
| RF-23 | Padre/tutor consulta asistencia | Asistencias, faltas y retardos de sus hijos. | Alta | Los datos mostrados coinciden con lo capturado por prefectura. |
| RF-24 | Padre/tutor consulta conducta | Reportes de conducta y evidencias de sus hijos. | Alta | Ve los reportes y abre las evidencias de sus hijos; no ve los de otros alumnos. |
| RF-25 | Registrar bitácora | Quién creó, modificó o eliminó usuarios, roles, alumnos, asistencias y reportes de conducta, con fecha y hora. | Alta | Cada acción sensible de la lista genera exactamente un registro con usuario, acción, entidad y fecha/hora. |
| RF-26 | Consultar bitácora | Administrador y dirección consultan la bitácora con filtros básicos (usuario, fecha). | Media | Los filtros devuelven los registros esperados; ningún otro rol puede abrir la bitácora. |

**Cuentas de alumno:** quedan fuera de la primera versión (D-01). La consulta de asistencia propia del alumno (antes RF-27) pasa a trabajo futuro.

**Requisitos del documento general que no entran en esta versión:** justificar faltas, permisos de salida, notificaciones, mensajes a padres, tareas, calificaciones, historial académico, documentos entregados, estado administrativo y generación de reportes exportables (ver 7.3).

## 10. Requerimientos no funcionales

Los RNF-01 a RNF-08 vienen de los requisitos no funcionales iniciales del proyecto. RNF-09 y RNF-10 son añadidos del equipo, necesarios para poder medir la calidad; se marcan como tales.

| ID | Requisito | Descripción | Método de verificación |
| --- | --- | --- | --- |
| RNF-01 | Seguridad basada en roles y permisos | Toda función valida el rol del usuario en el servidor (reglas de seguridad de Firebase o backend), no solo ocultando botones. | Matriz de pruebas rol × acción ejecutada con un usuario por rol, incluyendo accesos directos por URL. |
| RNF-02 | Registro de auditoría | Las acciones sensibles del alcance inicial quedan en bitácora (RF-25). | Ejecutar cada acción sensible y comprobar su registro en la bitácora. |
| RNF-03 | Diseño para múltiples ciclos escolares | Grupos, inscripciones y asistencias se asocian a un ciclo escolar. | Crear dos ciclos con datos de prueba y verificar que las consultas de uno no muestran datos del otro. |
| RNF-04 | Interfaz responsiva | Uso en computadora, tablet y celular. | Revisar las pantallas principales en tres anchos de pantalla (herramientas del navegador) con una lista de verificación y capturas. |
| RNF-05 | Protección de datos personales | Datos de alumnos y familias solo visibles para roles autorizados; contraseñas almacenadas cifradas con hash. | Pruebas de acceso cruzado (tutor A intenta ver alumno de tutor B) y revisión de la tabla de usuarios en la base de datos. |
| RNF-06 | Respaldos de información | Procedimiento documentado para respaldar y restaurar la base de datos. Será manual (D-20): exportación de las colecciones de Firestore a archivos. | Ejecutar al menos un respaldo y una restauración completa antes de la entrega final; conservar evidencia. |
| RNF-07 | Validaciones contra duplicidad | Se evitan alumnos, usuarios y registros de asistencia duplicados. | Casos de prueba que intentan crear cada duplicado y esperan rechazo. |
| RNF-08 | Arquitectura modular | El código se organiza por módulos para agregar fases posteriores. | Revisión de la estructura del repositorio contra el diseño de arquitectura en cada cierre de iteración. |
| RNF-09 *(añadido)* | Tiempo de respuesta | Las operaciones principales responden en menos de 3 segundos en el entorno de pruebas con los datos de prueba del equipo. | Medición con las herramientas de red del navegador sobre RF-01, RF-15, RF-20 y RF-23. |
| RNF-10 *(añadido)* | Control de versiones | Todo el código y la documentación se versionan en el repositorio del proyecto. | Historial de commits con participación de los tres integrantes. |

El requisito “posibilidad de exportar reportes en formatos comunes” se pospone a la Fase 5 junto con los reportes avanzados.

## 11. Control de acceso y seguridad

La seguridad se trata como criterio de calidad central: un error de permisos en este sistema expone datos de menores y familias. Se aplican cinco reglas.

1. **Control de acceso basado en roles (RBAC).** Cada usuario tiene rol(es) y cada rol determina módulos y acciones permitidas, conforme a la matriz de permisos del proyecto.
2. **Restricción de módulos.** El menú muestra solo los módulos del rol (RF-03).
3. **Restricción de acciones.** El servidor valida cada acción; ocultar un botón no cuenta como control (RF-04, RNF-01).
4. **Mínimo privilegio por relación.** El docente solo accede a alumnos de sus grupos; el padre/tutor solo a sus hijos o tutorados. Estas reglas vienen de la matriz y de las reglas generales.
5. **Registro de acciones importantes.** Altas, cambios y bajas sobre usuarios, roles, alumnos, asistencia y conducta quedan en bitácora (RF-25).

**Matriz de permisos aplicable a la primera versión** (extracto literal de la matriz del proyecto; las filas de fases posteriores se omiten):

| Acción | Alumno | Padre/Tutor | Docente | Prefectura | Dirección | Administración | Administrador |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Consultar datos del alumno | Sí | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | Limitado | Sí |
| Crear alumnos | No | No | No | No | Sí | Sí | Sí |
| Editar alumnos | No | No | No | Limitado | Sí | Sí | Sí |
| Registrar asistencia | No | No | No | Sí | Sí | No | Sí |
| Consultar asistencia | Sí, propia | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Registrar reportes de conducta | No | No | Sí | Sí | Sí | No | Sí |
| Consultar reportes de conducta | Sí, propios si aplica | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Subir evidencias de conducta | No | No | Sí | Sí | Sí | No | Sí |
| Consultar evidencias de conducta | Sí, propias si aplica | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Gestionar materias y grupos | No | No | No | No | Sí | No | Sí |
| Consultar bitácora | No | No | No | No | Sí | Limitado | Sí |
| Administrar usuarios y roles | No | No | No | No | No | No | Sí |

**Valores por definir:** los permisos “Limitado” y “si aplica” no están definidos en la documentación. Mientras no se definan, la primera versión los tratará como **No** (mínimo privilegio), y se registrará en control de cambios cuando se decidan (D-10, D-16, I-12).

## 12. Criterios de calidad

La primera versión se considera de calidad solo si cumple los siete criterios siguientes, cada uno con evidencia.

| Criterio | Qué significa | Cómo se verificará | Evidencia generada |
| --- | --- | --- | --- |
| Funcionalidad | El sistema cumple los requisitos del alcance inicial. | Un caso de prueba por requisito con resultado esperado y obtenido. | Bitácora de pruebas; matriz de trazabilidad actualizada. |
| Seguridad | Cada usuario solo accede a lo que su rol permite. | Matriz de pruebas rol × acción y pruebas de acceso cruzado. | Registro de pruebas de permisos con capturas de accesos rechazados. |
| Usabilidad | Las funciones principales se completan sin ayuda. | Recorrido guiado: un integrante que no desarrolló la función completa las tareas clave (login, pasar lista, registrar reporte, consulta del tutor) sin instrucciones. | Lista de tareas con resultado (completada / con dificultad) y observaciones. |
| Integridad de datos | No hay registros duplicados ni inconsistentes. | Casos de prueba de duplicidad y de campos obligatorios (RNF-07). | Resultados de pruebas y capturas de los mensajes de validación. |
| Trazabilidad | Las acciones sensibles se pueden identificar. | Verificar que cada acción de RF-25 genera su registro. | Capturas de la bitácora con los registros generados en las pruebas. |
| Rendimiento | Respuesta ágil en las operaciones principales. | Medición de RNF-09 (menos de 3 s) con herramientas del navegador. | Tabla de mediciones con fecha y capturas. |
| Mantenibilidad | Las siguientes fases se pueden agregar sin rehacer la base. | Revisión de código por un integrante distinto al autor; estructura por módulos (RNF-08). | Revisiones registradas en el repositorio (pull requests o comentarios) y diagrama de arquitectura. |

## 13. Metodología de trabajo

El equipo usará **Scrum adaptado a un equipo de tres integrantes**, con iteraciones (sprints) de dos semanas alineadas a las etapas de la materia.

**Justificación:**

- La materia exige avances funcionales desde la Etapa II; las iteraciones cortas producen un incremento demostrable al final de cada sprint.
- El backlog priorizado (Alta, Media, Baja) permite posponer requisitos de forma ordenada cuando falta tiempo, que es el principal riesgo del proyecto.
- Las revisiones al cierre de cada sprint coinciden con los puntos de control de la materia y generan evidencia de seguimiento.
- Se descartan ceremonias que no aportan a un equipo de tres (por ejemplo, un Scrum Master dedicado): el líder del proyecto asume esa función.

**Aplicación (calendario tentativo; se detalla en el Plan del Proyecto de la Etapa II):**

| Sprint | Fechas | Objetivo del sprint |
| --- | --- | --- |
| Sprint 0 | 23 sep – 6 oct | Plan de calidad, repositorio, modelo de datos inicial, prototipos. |
| Sprint 1 | 7 – 20 oct | Autenticación, roles, usuarios, ciclo/grados/grupos, bitácora base (RF-01 a RF-09, RF-25). |
| Sprint 2 | 21 oct – 3 nov | Alumnos, tutores, docentes y asistencia (RF-10 a RF-17). |
| Sprint 3 | 4 – 17 nov | Conducta, evidencias, vista de padres/tutores y consulta de bitácora (RF-18 a RF-24, RF-26). |
| Cierre | 18 – 24 nov | Pruebas de regresión, correcciones, manual de usuario y entrega. |

**Prácticas y su relación con la calidad:**

| Práctica | Frecuencia | Aporte a la calidad |
| --- | --- | --- |
| Planeación del sprint | Inicio de cada sprint | Se revisan y aclaran los requisitos y criterios de aceptación antes de programar. |
| Reunión breve de seguimiento | 2 veces por semana | Detecta bloqueos a tiempo; se registra en la bitácora de participación. |
| Revisión del sprint | Cierre de cada sprint | Se demuestran las funciones terminadas y se calculan las métricas. |
| Retrospectiva | Cierre de cada sprint | Acciones de mejora registradas. |
| Definición de terminado | Cada requisito | Un requisito está terminado solo si su código fue revisado por otro integrante, su caso de prueba pasó y su permiso por rol fue verificado. |

**Gestión de cambios y avances:** todo cambio de alcance pasa por el procedimiento de la sección 18; el avance se mide con las métricas de la sección 16 en el tablero de gestión y el historial del repositorio.

## 14. Organización del equipo

**Roles confirmados por el equipo.** Stephanie y Ricardo desarrollan la aplicación y Dylan construye la base de datos; los tres deben poder explicar cualquier parte del sistema en las revisiones, y nadie prueba únicamente su propio trabajo.

| Integrante | Rol | Responsabilidades | Evidencias generadas |
| --- | --- | --- | --- |
| Stephanie Ariana Medrano Vargas | Líder del proyecto; desarrollo; diseño de interfaz | Coordinar sprints y tablero; controlar cambios y decisiones; diseñar prototipos y pantallas; desarrollar autenticación, roles, vista de padres/tutores y bitácora. | Registro de cambios, actas de revisión de sprint, prototipos, commits. |
| Dylan Alexis Padilla | Responsable de análisis y documentación; responsable de base de datos | Mantener requisitos y matriz de trazabilidad; redactar los documentos de cada etapa y el manual de usuario; diseñar el modelo de datos; crear scripts, datos de prueba ficticios y procedimiento de respaldo. | Plan de calidad, requisitos, matriz de permisos, modelo de datos, reglas de seguridad de Firebase, manual de usuario, commits. |
| Ricardo Alejandro Pineda Gómez | Responsable de pruebas y calidad; desarrollo | Diseñar casos de prueba; ejecutar la matriz de permisos; llevar la bitácora de pruebas y las métricas; desarrollar alumnos, tutores, docentes, asistencia y conducta. | Casos de prueba, bitácora de pruebas, registro de métricas, commits. |

**Reglas del equipo:**

- Cada integrante registra su trabajo en la **bitácora de participación** (fecha, actividad, responsable, evidencia, tiempo empleado, resultado).
- Todo cambio de código lo revisa un integrante distinto a su autor antes de integrarse.
- Las decisiones de alcance se toman por consenso de los tres; si no lo hay, decide el líder y queda registrado.

## 15. Tecnologías y herramientas

Las tecnologías principales están definidas. El framework, el reparto entre JavaScript y Python y el almacenamiento de evidencias quedan como decisiones futuras (CC-03), con fecha límite en la sección 20. La elección es libre según la materia, pero debe ser congruente con el proyecto y quedar decidida antes del cierre de la Etapa I (D-22).

| Categoría | Tecnología | Propósito |
| --- | --- | --- |
| Lenguaje de programación | JavaScript y Python (reparto entre frontend y backend \[POR DEFINIR\], I-14) | Desarrollo del sistema. |
| Framework | \[TECNOLOGÍA POR DEFINIR\]; el frontend usará las plantillas del framework (HTML, CSS y JavaScript) | Estructura de la aplicación web responsiva. |
| Base de datos | Firebase (Cloud Firestore, base de datos NoSQL de documentos) | Almacenamiento de usuarios, alumnos, asistencia, conducta y bitácora. |
| Almacenamiento de evidencias | \[DECISIÓN PENDIENTE\]: se eligió guardarlas dentro de la base de datos, pero Firestore admite como máximo 1 MiB por documento (I-13) | Archivos adjuntos a reportes de conducta. |
| Control de versiones | Git | Historial de cambios y evidencia de participación. |
| Repositorio remoto | GitHub — github.com/StephAmv/nexoEdu | Alojamiento del código y la documentación. |
| Gestión del proyecto | GitHub Projects | Backlog, tablero de sprints y seguimiento. |
| Diseño y prototipos | draw.io | Prototipos de interfaz y diagramas. |
| Pruebas | \[TECNOLOGÍA POR DEFINIR\] | Registro de casos de prueba; pruebas automatizadas si el equipo las adopta. |
| Documentación | \[TECNOLOGÍA POR DEFINIR\] | Plan de calidad, reportes y manual de usuario. |

**Restricción de plataforma:** nexoEdu será una aplicación web responsiva (D-05) y no tendrá app nativa en este periodo (D-06). El lenguaje y el framework deben elegirse para desarrollo web.

## 16. Métricas e indicadores de calidad

Nueve métricas, todas calculables con una hoja de cálculo, el tablero de gestión y el historial del repositorio. Se reportan al cierre de cada sprint.

| ID | Métrica | Fórmula | Meta | Frecuencia | Responsable | Evidencia |
| --- | --- | --- | --- | --- | --- | --- |
| M-01 | Requisitos cumplidos | RF aceptados / RF comprometidos × 100 | 100 % de RF Alta; ≥ 80 % del total | Cierre de sprint | Pruebas y calidad | Matriz de trazabilidad |
| M-02 | Pruebas satisfactorias | Casos aprobados / casos ejecutados × 100 | ≥ 90 % antes de la entrega final | Cierre de sprint | Pruebas y calidad | Bitácora de pruebas |
| M-03 | Cobertura de pruebas de permisos | Combinaciones rol × acción probadas / combinaciones definidas × 100 | 100 %, todas aprobadas | Cierre de sprint | Pruebas y calidad | Matriz de pruebas de permisos |
| M-04 | Errores detectados | Conteo por prioridad (alta, media, baja) | Seguimiento; sin meta numérica | Semanal | Pruebas y calidad | Bitácora de pruebas |
| M-05 | Errores corregidos | Errores cerrados / errores detectados × 100 | 100 % de prioridad alta; ≥ 80 % del total al cierre | Semanal | Líder del proyecto | Bitácora de pruebas; commits de corrección |
| M-06 | Cumplimiento de actividades | Tareas terminadas / tareas planificadas del sprint × 100 | ≥ 80 % por sprint | Cierre de sprint | Líder del proyecto | Tablero de gestión |
| M-07 | Cambios solicitados y aprobados | Conteo de solicitudes; aprobados / solicitados | 100 % de cambios con registro y decisión | Cierre de sprint | Líder del proyecto | Registro de cambios |
| M-08 | Incidencias abiertas y cerradas | Conteo de abiertas vs. cerradas | 0 incidencias de prioridad alta abiertas en la entrega final | Semanal | Pruebas y calidad | Tablero o bitácora de pruebas |
| M-09 | Participación del equipo | Horas y actividades por integrante / total del equipo | Cada integrante con actividades registradas en todos los sprints | Cierre de sprint | Análisis y documentación | Bitácora de participación; historial de commits |

El tiempo de respuesta (RNF-09) se mide como parte de las pruebas, no como métrica de seguimiento semanal.

## 17. Plan de aseguramiento y control de calidad

La calidad se revisa en cada paso del desarrollo, no solo al final. Estas son las actividades y su momento.

| Actividad | Momento | Responsable | Qué se revisa |
| --- | --- | --- | --- |
| Revisión de requisitos | Planeación de cada sprint | Todo el equipo | Que cada requisito sea claro, esté dentro del alcance y tenga criterio de aceptación. |
| Revisión de diseño | Antes de programar cada módulo | Autor + un revisor | Modelo de datos, relaciones (alumno–tutor, docente–grupo) y asociación con ciclo escolar. |
| Revisión de código | Antes de integrar cada cambio | Integrante distinto al autor | Legibilidad, estructura por módulos, validación de permisos en el servidor. |
| Pruebas funcionales | Al terminar cada requisito | Pruebas y calidad | Caso de prueba del requisito con resultado esperado y obtenido. |
| Validación de permisos | Cierre de cada sprint | Pruebas y calidad | Matriz rol × acción y accesos cruzados. |
| Validación de datos | Al terminar cada formulario | Pruebas y calidad | Campos obligatorios, formatos y duplicados. |
| Pruebas de regresión | Cierre (18–24 nov) | Todo el equipo | Todos los casos de prueba de nuevo sobre la versión final. |

**Flujo de manejo de errores:**

1. **Detectar** — Se encuentra un error al probar o revisar.
2. **Registrar** — Se anota en la bitácora de pruebas: funcionalidad probada, fecha, responsable, resultado esperado, resultado obtenido, error detectado, nivel de prioridad, acción correctiva y estado final (campos que pide la Etapa IV).
3. **Corregir** — El responsable asignado corrige y referencia el ID del error en el commit.
4. **Verificar** — Un integrante distinto al que corrigió repite la prueba.
5. **Cerrar** — Si la prueba pasa, el error se marca como cerrado; si no, vuelve al paso 3.

**Prioridad de errores:** alta (bloquea una función o expone datos a un rol no autorizado), media (la función opera con un defecto) y baja (detalle visual o de texto).

## 18. Control de cambios

Ningún cambio al alcance, a los requisitos o a este plan se implementa sin registro y decisión. Este plan (versión 1.0) es la línea base.

**Procedimiento:**

1. Cualquier integrante (o la docente) propone el cambio y se registra con un ID.
2. El líder analiza el impacto en tiempo, complejidad, recursos, requisitos, calidad y alcance.
3. El equipo decide: **aprobar**, **rechazar** o **posponer** (al backlog de trabajo futuro).
4. Si se aprueba, se actualizan los documentos afectados (requisitos, trazabilidad, plan) con nueva versión.
5. Se implementa y se verifica como cualquier requisito; luego se cierra.

**Reglas para proteger la viabilidad:**

- Un cambio que agregue funciones de las fases 2 a 5 se pospone por defecto.
- Un cambio que ponga en riesgo un requisito de prioridad Alta se rechaza o se compensa retirando un requisito de prioridad Media o Baja.
- Después del 17 de noviembre solo se aceptan correcciones de errores, no funciones nuevas.
- Resolver una decisión pendiente (sección 20) también se registra como cambio.

**Registro de cambios:**

| ID | Fecha | Cambio solicitado | Motivo | Impacto | Prioridad | Decisión | Responsable | Estado |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CC-00 | \[POR COMPLETAR\] | Establecer la línea base del alcance: Fase 1 del roadmap, RF-01 a RF-26 | Inicio del proyecto | Define el alcance comprometido | Alta | Aprobado | Líder del proyecto | Cerrado |
| CC-01 | 30 sep 2026 | Resolver D-01, D-02, D-03, D-05 y D-06 | Decisiones requeridas antes del cierre de la Etapa I | Sin cuentas de alumno (sale RF-27); modelo usuario–rol con varios roles; solo el Administrador crea usuarios; plataforma solo web responsiva | Alta | Aprobado | Líder del proyecto | Cerrado |
| CC-02 | 30 sep 2026 | Definir tecnologías y resolver D-04, D-11, D-15, D-17 a D-21 y D-23 (tipos) | Completar el Plan de Calidad | Firebase como base de datos; datos obligatorios de alumno y tutor; sin recuperación por correo; respaldo manual; consultas sin reportes adicionales. Abre I-13 e I-14 | Alta | Aprobado | Líder del proyecto | Cerrado |
| CC-03 | 6 oct 2026 | Posponer I-13 (almacenamiento y tamaño de evidencias) e I-14 (framework y reparto JavaScript/Python) | Requieren analizar opciones fuera de la Etapa I | I-14 bloquea el inicio del código; I-13 bloquea RF-19 | Alta | Pospuesto | Líder del proyecto | Abierto |
| CC-04 |  |  |  |  |  |  |  |  |

## 19. Riesgos relacionados con la calidad

Los dos riesgos más altos son el crecimiento del alcance y la falta de tiempo: el alcance inicial ya es exigente para tres personas en nueve semanas.

| ID | Riesgo | Probabilidad | Impacto | Nivel | Mitigación | Responsable |
| --- | --- | --- | --- | --- | --- | --- |
| R-01 | Crecimiento excesivo del alcance (agregar funciones de otras fases) | Alta | Alto | Alto | Línea base CC-00; reglas de control de cambios; posponer por defecto. | Líder del proyecto |
| R-02 | Falta de tiempo para completar el alcance | Alta | Alto | Alto | Prioridades Alta/Media/Baja; entregar primero los RF Alta; revisión de M-06 en cada sprint. | Líder del proyecto |
| R-03 | Decisiones pendientes sin resolver bloquean el desarrollo | Media | Alto | Alto | Fecha límite por decisión (sección 20); valor por defecto de mínimo privilegio mientras tanto. | Líder del proyecto |
| R-04 | Errores de permisos que exponen datos a roles no autorizados | Media | Alto | Alto | Validación en servidor; matriz de pruebas de permisos al 100 % (M-03). | Pruebas y calidad |
| R-05 | Manejo incorrecto de datos sensibles (contraseñas, datos de alumnos, evidencias) | Media | Alto | Alto | Contraseñas con hash; solo datos de prueba ficticios; evidencias accesibles solo por rol. | Base de datos |
| R-06 | Requisitos ambiguos (“Limitado”, “si aplica”, reporte vs. incidencia) | Alta | Medio | Alto | Registro de inconsistencias (sección 21); criterio de aceptación por requisito. | Análisis y documentación |
| R-07 | Falta de pruebas por dejarlas al final | Media | Alto | Alto | Definición de terminado exige caso de prueba aprobado. | Pruebas y calidad |
| R-08 | Problemas de integración entre módulos (roles, alumnos, asistencia, conducta) | Media | Medio | Medio | Modelo de datos revisado antes de programar; integración continua en la rama principal. | Base de datos |
| R-09 | Dependencia excesiva de una persona | Media | Alto | Alto | Revisión cruzada de código y de base de datos; cada integrante documenta su parte; bitácora de participación. | Líder del proyecto |
| R-10 | Cambios tardíos que desestabilizan la versión final | Media | Alto | Alto | Congelamiento de funciones después del 17 de noviembre. | Líder del proyecto |
| R-11 | Tecnologías elegidas tarde o poco conocidas por el equipo | Media | Medio | Medio | Decidir el framework antes del Sprint 1 (7 de octubre) y el almacenamiento de evidencias antes del Sprint 3 (4 de noviembre), priorizando lo que el equipo ya domina. | Todo el equipo |

Nivel = combinación de probabilidad e impacto (probabilidad Alta con impacto Alto o Medio, o probabilidad Media con impacto Alto = Alto; Media/Medio = Medio).

## 20. Decisiones pendientes

Estas decisiones vienen del documento de decisiones pendientes y **no se resuelven en este plan**. Solo se fija cuándo deben decidirse según su impacto en la primera versión; las que afectan solo a fases futuras no bloquean esta entrega.

| ID | Decisión | Impacto sobre el proyecto | Fecha límite | Responsable | Estado |
| --- | --- | --- | --- | --- | --- |
| D-01 | ¿Los alumnos tendrán cuenta propia desde la primera versión? | Define si RF-27 entra al alcance y si se prueba el rol Alumno. | 6 oct 2026 | Equipo (validar con docente/escuela) | Resuelta: no (CC-01) |
| D-02 | ¿Un usuario podrá tener más de un rol? | Cambia el modelo de datos de usuarios y roles (RF-08). | 6 oct 2026 | Base de datos | Resuelta: sí (CC-01) |
| D-03 | ¿Quién podrá crear usuarios: dirección, administrador o ambos? | Cambia permisos de RF-06 (ver I-04). | 6 oct 2026 | Equipo | Resuelta: solo el Administrador (CC-01) |
| D-04 | ¿Recuperación de contraseña por correo desde la primera versión? | Requeriría envío de correo; si no, RF-05 queda como restablecimiento por el administrador. | 20 oct 2026 | Equipo | Resuelta: no; el Administrador restablece (CC-02) |
| D-05 | ¿Será solo una plataforma web responsiva? | Condiciona lenguaje, framework y pruebas de RNF-04. | 6 oct 2026 | Equipo | Resuelta: solo web responsiva (CC-01) |
| D-06 | ¿Se requiere aplicación móvil nativa? | Si sí, el alcance no es viable en el periodo; se propone como trabajo futuro. | 6 oct 2026 | Equipo | Resuelta: no, trabajo futuro (CC-01) |
| D-07 | ¿Se desarrollará como PWA para notificaciones push? | Ligado a notificaciones (Fase 2); no bloquea la primera versión. | Fase 2 | Equipo | \[PENDIENTE\] |
| D-08 | Canales de notificación iniciales (correo, sistema, push) | Fuera del alcance inicial (Fase 2). | Fase 2 | Equipo | \[PENDIENTE\] |
| D-09 | Pagos: registro manual o pasarela, validez fiscal, becas, descuentos y recargos | Fuera del alcance inicial (Fase 4). | Fase 4 | Equipo | \[PENDIENTE\] |
| D-10 | ¿Qué información disciplinaria podrá ver el alumno? | Afecta RF-27 y el permiso “si aplica”. Mientras tanto: no ve conducta. | Junto con D-01 | Equipo | No aplica en la primera versión (D-01) |
| D-11 | ¿Qué información disciplinaria solo podrá ver el padre/tutor? | Afecta RF-24. | 20 oct 2026 | Equipo | Resuelta: reportes y evidencias completos (CC-02) |
| D-12 | ¿Qué personal puede validar justificantes? | Justificantes en Fase 2. | Fase 2 | Equipo | \[PENDIENTE\] |
| D-13 | ¿Qué personal puede autorizar permisos de salida? | Permisos de salida en Fase 2. | Fase 2 | Equipo | \[PENDIENTE\] |
| D-14 | ¿Las faltas justificadas afectan los reportes de asistencia de forma distinta? | Depende de justificantes (Fase 2); conviene prever el campo en el modelo de asistencia. | Fase 2 | Base de datos | \[PENDIENTE\] |
| D-15 | ¿Dirección podrá editar información o solo consultarla y autorizarla? | Afecta permisos de RF-14 (ver I-07). | 20 oct 2026 | Equipo | Resuelta: edita según la matriz (CC-02) |
| D-16 | ¿Administración podrá ver información académica o disciplinaria? | Rol fuera del alcance inicial; define el permiso “Limitado”. | Fase 4 | Equipo | \[PENDIENTE\] |
| D-17 | ¿Qué datos personales serán obligatorios para alumnos y tutores? | Define validaciones de RF-10 y RF-12. | 20 oct 2026 | Análisis y documentación | Resuelta: alumno — nombre completo, matrícula, fecha de nacimiento, CURP y grupo; tutor — nombre completo, teléfono, correo y parentesco (CC-02) |
| D-18 | ¿Qué reportes son indispensables para la primera versión? | Si se exige alguno, entra por control de cambios. | 20 oct 2026 | Equipo | Resuelta: ninguno; solo consultas con filtros (CC-02) |
| D-19 | ¿Cuánto tiempo se conservarán las evidencias y archivos adjuntos? | Política de almacenamiento de RF-19. No bloquea el desarrollo. | 3 nov 2026 | Equipo | Resuelta: durante el ciclo escolar; se archivan al cerrarlo (CC-02) |
| D-20 | ¿Se requiere respaldo automático diario? | Define RNF-06; mientras tanto, respaldo manual documentado. | 3 nov 2026 | Base de datos | Resuelta: respaldo manual documentado (CC-02) |
| D-21 | ¿Quién podrá consultar la bitácora completa? | Afecta RF-26 (ver I-06). | 20 oct 2026 | Equipo | Resuelta: Administrador y Dirección (CC-02) |
| D-22 *(añadida)* | Lenguaje, framework, base de datos y herramientas | Requerida por la materia para esta etapa; condiciona el repositorio y el código inicial. | Inicio del Sprint 1 (7 oct 2026) | Todo el equipo | Parcial: framework y reparto JavaScript/Python pospuestos (CC-03, I-14) |
| D-23 *(añadida)* | Tipos de archivo y tamaño máximo de evidencias | Define validaciones de RF-19. | 3 nov 2026 | Equipo | Tipos resueltos: JPG, PNG y PDF. Tamaño y almacenamiento pospuestos (CC-03, I-13) |

## 21. Inconsistencias o decisiones por confirmar

Se encontraron 12 contradicciones o vacíos entre los documentos del proyecto. No se resuelven en silencio: cada una indica cómo la trata este plan de forma provisional, sujeto a confirmación.

| ID | Inconsistencia | Documentos | Tratamiento provisional |
| --- | --- | --- | --- |
| I-01 | “Reporte de conducta” e “incidencia disciplinaria” aparecen como cosas distintas, pero solo existe la entidad Reporte de conducta. | 01, 02, 03 | Se tratan como la misma entidad con autor distinto (docente o prefectura) hasta confirmar. |
| I-02 | Fase 1 necesita asignar docentes a grupos, pero esa función está en el módulo académico (Fase 3). La regla dice “grupos o materias” y las materias son Fase 3. | 01, 03, 04 | Se incluye solo la asignación docente–grupo (RF-13); materias quedan fuera. |
| I-03 | La matriz permite a Administración crear y editar alumnos, pero ese rol está fuera de la Fase 1. | 02, 04 | En la primera versión crean alumnos Dirección y Administrador. |
| I-04 | La matriz dice que solo el Administrador gestiona usuarios; las decisiones pendientes preguntan si también Dirección. | 02, 05 | Resuelta: solo el Administrador crea usuarios (D-03). |
| I-05 | Requisitos y roles afirman “uno o más roles” por usuario; decisiones pendientes lo pregunta. | 01, 02, 05 | Resuelta: un usuario puede tener varios roles (D-02); el modelo usará una relación usuario–rol. |
| I-06 | La matriz da consulta de bitácora a Dirección (Sí) y Administración (Limitado); decisiones pendientes pregunta quién. | 02, 05 | Administrador y Dirección, hasta resolver D-21. |
| I-07 | La matriz permite a Dirección editar alumnos; decisiones pendientes pregunta si solo consulta. | 02, 05 | Se aplica la matriz hasta resolver D-15. |
| I-08 | Las reglas generales dicen que las notificaciones automáticas “deben generarse”; el roadmap las ubica en Fase 2. | 03, 04 | Se sigue el roadmap: fuera de la primera versión. |
| I-09 | El módulo 12 (Inscripciones y matrícula) no aparece en ninguna fase, aunque la Fase 1 necesita registrar alumnos y asignarlos a grupo. | 00, 01, 04 | Solo el registro del alumno y su asignación a grupo entran (RF-10, RF-11); reinscripciones y documentación quedan fuera. |
| I-10 | La matriz da al Alumno consulta de su asistencia, pero no está definido si tendrá cuenta en la primera versión. | 02, 05 | Resuelta: sin cuentas de alumno en la primera versión (D-01). |
| I-11 | Justificar faltas aparece en el módulo de padres y en la matriz, pero el roadmap lo ubica en Fase 2. | 01, 02, 04 | Se sigue el roadmap: fuera de la primera versión. |
| I-12 | Los valores “Limitado” y “si aplica” de la matriz no están definidos. | 02 | Se tratan como “No” (mínimo privilegio) hasta definirse. |

Clave de documentos: 00 resumen ejecutivo, 01 requisitos funcionales, 02 roles y permisos, 03 entidades y reglas, 04 roadmap, 05 decisiones pendientes.

**Conflictos técnicos detectados al definir tecnologías:**

- **I-13 — Evidencias dentro de Firestore vs. 5 MB.** Se eligió guardar las evidencias dentro de la base de datos con un máximo de 5 MB, pero un documento de Firestore admite como máximo 1 MiB. Opciones: bajar el límite a menos de 1 MiB, usar Cloud Storage for Firebase (requiere el plan Blaze con cuenta de facturación, aunque conserva una cuota sin costo) o guardar los archivos en el servidor del backend. Tratamiento: decisión futura (CC-03), antes del Sprint 3 (4 de noviembre), cuando se construye RF-19.
- **I-14 — Dos lenguajes sin reparto definido.** Se eligieron JavaScript y Python, pero no se ha definido qué parte del sistema usa cada uno ni el framework. Tratamiento: decisión futura (CC-03), antes del Sprint 1 (7 de octubre), porque la Etapa II exige código.

## 22. Evidencias de la Etapa I

La etapa se entrega con 11 evidencias: el plan y los primeros artefactos prácticos que pide la materia (repositorio, diagramas, prototipos, estructura de base de datos y, si existe, código).

| # | Evidencia | Qué demuestra | Formato | Nombre sugerido | Responsable |
| --- | --- | --- | --- | --- | --- |
| E-01 | Plan de Calidad (este documento) | Definición formal del proyecto y de sus criterios de calidad. | PDF | `E01_Plan_de_Calidad_v1.0.pdf` | Análisis y documentación |
| E-02 | Repositorio del proyecto | Que el repositorio existe (github.com/StephAmv/nexoEdu), con estructura inicial, README y commits de los tres integrantes. | Enlace + captura PNG | `E02_Repositorio.png` | Líder del proyecto |
| E-03 | Requisitos | RF y RNF con prioridad y criterio de aceptación. | PDF u hoja de cálculo | `E03_Requisitos_v1.0.xlsx` | Análisis y documentación |
| E-04 | Roles y permisos | Matriz de permisos aplicable a la primera versión. | PDF u hoja de cálculo | `E04_Matriz_Permisos_v1.0.xlsx` | Análisis y documentación |
| E-05 | Modelo inicial del sistema | Diagrama de casos de uso del alcance inicial y diagrama de arquitectura por módulos. | PNG o PDF | `E05_Casos_de_Uso.png`, `E05_Arquitectura.png` | Líder del proyecto |
| E-06 | Prototipos | Pantallas clave: login, asistencia por grupo, reporte de conducta, vista del padre/tutor. | PNG o enlace al prototipo | `E06_Prototipo_<pantalla>.png` | Diseño de interfaz |
| E-07 | Estructura inicial de base de datos | Modelo de datos (colecciones de Firestore) con Usuario, Rol, Alumno, Padre o tutor, Docente, Grupo, Grado, Ciclo escolar, Asistencia, Reporte de conducta, Evidencia y Bitácora. | PNG (draw.io) | `E07_Modelo_Datos.png` | Base de datos |
| E-08 | Código inicial | Proyecto base funcionando (por ejemplo, pantalla de login). **Solo si ya existe.** | Enlace al commit + captura | `E08_Codigo_Inicial.png` | Desarrollo |
| E-09 | Registro de métricas | Plantilla con M-01 a M-09 lista para el Sprint 1. | Hoja de cálculo | `E09_Registro_Metricas.xlsx` | Pruebas y calidad |
| E-10 | Registro de control de cambios | Registro con CC-00 (línea base). | Hoja de cálculo | `E10_Control_de_Cambios.xlsx` | Líder del proyecto |
| E-11 | Bitácora de participación | Actividades de cada integrante en la Etapa I (fecha, actividad, responsable, evidencia, tiempo, resultado). | Hoja de cálculo | `E11_Bitacora_Participacion.xlsx` | Cada integrante |

E-11 no la pide la Etapa I, pero la sección 8 de la materia la exige durante todo el proyecto; conviene iniciarla ahora.

## 23. Estructura de carpetas

Se adapta la estructura propuesta para incluir la bitácora de participación y para que cada carpeta corresponda a una evidencia (E-01 a E-11). La carpeta vive dentro de `04_Documentacion` de la entrega final que pide la materia, así no se reorganiza en noviembre.

```
PROYECTO_FINAL_NEXOEDU/
└── 04_Documentacion/
    └── ETAPA_1_GESTION_CALIDAD/
        ├── 01_PLAN_DE_CALIDAD/          E-01
        ├── 02_REQUISITOS/               E-03
        ├── 03_ROLES_Y_PERMISOS/         E-04
        ├── 04_DIAGRAMAS/                E-05
        ├── 05_PROTOTIPOS/               E-06
        ├── 06_BASE_DE_DATOS/            E-07
        ├── 07_REPOSITORIO/              E-02, E-08
        ├── 08_METRICAS/                 E-09
        ├── 09_CONTROL_DE_CAMBIOS/       E-10
        ├── 10_RIESGOS/                  Registro de riesgos (sección 19)
        ├── 11_BITACORA_PARTICIPACION/   E-11
        └── 12_EVIDENCIAS/               Capturas y material de apoyo
```

Los documentos se nombran con versión (`_v1.0`, `_v1.1`) para que el control de cambios sea visible en los propios archivos.

## 24. Trazabilidad

Cada requisito tiene un criterio de calidad, un caso de prueba (CP con el mismo número que el requisito) y una evidencia. La columna Resultado se llena en las etapas III y IV.

| Requisito | Criterio de calidad | Método de verificación | Evidencia | Resultado |
| --- | --- | --- | --- | --- |
| RF-01 Iniciar sesión | Seguridad | CP-01: credenciales válidas e inválidas | Bitácora de pruebas + capturas |  |
| RF-02 Sesión segura | Seguridad | CP-02: acceso a página protegida sin sesión | Bitácora de pruebas |  |
| RF-03 Menú según rol | Seguridad, Usabilidad | CP-03: un usuario por rol | Capturas del menú por rol |  |
| RF-04 Restringir acciones | Seguridad | CP-04: matriz rol × acción con acceso directo | Matriz de pruebas de permisos |  |
| RF-05 Restablecer contraseña | Seguridad | CP-05 | Bitácora de pruebas |  |
| RF-06 Gestionar usuarios | Funcionalidad, Integridad | CP-06: alta, edición y duplicado | Bitácora de pruebas |  |
| RF-07 Desactivar/reactivar | Seguridad, Trazabilidad | CP-07 | Bitácora de pruebas + registro en bitácora del sistema |  |
| RF-08 Asignar roles | Seguridad | CP-08 | Bitácora de pruebas |  |
| RF-09 Ciclo, grados y grupos | Integridad, Mantenibilidad | CP-09 + prueba de dos ciclos (RNF-03) | Bitácora de pruebas |  |
| RF-10 Registrar alumnos | Funcionalidad, Integridad | CP-10: alta y duplicado por matrícula | Bitácora de pruebas |  |
| RF-11 Alumno–grupo–ciclo | Integridad | CP-11 | Bitácora de pruebas |  |
| RF-12 Padres/tutores | Funcionalidad, Seguridad | CP-12: tutor con dos hijos; alumno con dos tutores | Bitácora de pruebas |  |
| RF-13 Docentes y grupos | Seguridad | CP-13 | Bitácora de pruebas |  |
| RF-14 Editar alumnos | Trazabilidad | CP-14 | Registro en bitácora del sistema |  |
| RF-15 Registrar asistencia | Funcionalidad, Integridad | CP-15: captura y duplicado por fecha | Bitácora de pruebas + capturas |  |
| RF-16 Modificar asistencia | Trazabilidad | CP-16 | Registro en bitácora del sistema |  |
| RF-17 Consultar asistencia | Funcionalidad, Rendimiento | CP-17 + medición RNF-09 | Bitácora de pruebas + mediciones |  |
| RF-18 Reporte de conducta | Funcionalidad, Seguridad | CP-18: docente fuera de su grupo | Bitácora de pruebas |  |
| RF-19 Evidencias | Funcionalidad, Seguridad | CP-19: subir y abrir; acceso por otro rol | Bitácora de pruebas |  |
| RF-20 Consultar reportes | Seguridad | CP-20: visibilidad por rol | Matriz de pruebas de permisos |  |
| RF-21 Incidencias | Funcionalidad | CP-21 | Bitácora de pruebas |  |
| RF-22 Tutor: datos del alumno | Seguridad | CP-22: acceso cruzado entre tutores | Capturas del acceso rechazado |  |
| RF-23 Tutor: asistencia | Funcionalidad, Rendimiento | CP-23 | Bitácora de pruebas |  |
| RF-24 Tutor: conducta | Seguridad, Usabilidad | CP-24 + recorrido guiado | Bitácora de pruebas |  |
| RF-25 Registrar bitácora | Trazabilidad | CP-25: una acción por tipo sensible | Capturas de la bitácora |  |
| RF-26 Consultar bitácora | Seguridad, Trazabilidad | CP-26 | Bitácora de pruebas |  |
| RNF-01 a RNF-10 | Según sección 10 | Método indicado en la sección 10 | Bitácora de pruebas y evidencias indicadas |  |

## 25. Criterios de aceptación de la primera versión

La primera versión se acepta solo si cumple las diez condiciones siguientes. Una interfaz sin funcionalidad no cuenta como avance.

1. El 100 % de los requisitos de prioridad Alta está aceptado con su caso de prueba aprobado (M-01).
2. Al menos el 80 % del total de requisitos comprometidos está aceptado, y los no aceptados están registrados como pospuestos en control de cambios.
3. El 100 % de la matriz de pruebas de permisos está ejecutado y aprobado (M-03).
4. No hay errores de prioridad alta abiertos (M-08).
5. Al menos el 90 % de los casos de prueba ejecutados está aprobado en la regresión final (M-02).
6. El flujo completo funciona de principio a fin con datos persistidos en la base de datos: el administrador crea usuarios y grupos → prefectura registra asistencia → un docente registra un reporte de conducta con evidencia → el padre/tutor consulta la asistencia y el reporte de su hijo → la bitácora muestra las acciones.
7. Las pantallas principales funcionan en computadora, tablet y celular (RNF-04), con capturas como evidencia.
8. Se ejecutó al menos un respaldo y una restauración de la base de datos (RNF-06).
9. Las operaciones medidas responden en menos de 3 segundos en el entorno de pruebas (RNF-09).
10. El repositorio contiene el código, el README con instrucciones de instalación y ejecución y credenciales de prueba, e historial de commits de los tres integrantes.

## 26. Checklist final de la Etapa I

Las filas 1 a 14 son los contenidos que la materia exige al Plan de Calidad; las 15 a 22, la evidencia práctica y de gestión.

| # | Elemento | Requerido | Evidencia | Responsable | Estado |
| --- | --- | --- | --- | --- | --- |
| 1 | Nombre del proyecto | Sí (materia) | Portada | Análisis y documentación | Completo (nexoEdu) |
| 2 | Descripción de la problemática | Sí (materia) | Sección 4 | Análisis y documentación | Borrador |
| 3 | Justificación | Sí (materia) | Sección 5 | Análisis y documentación | Borrador |
| 4 | Usuarios a quienes está dirigido | Sí (materia) | Sección 8 | Análisis y documentación | Borrador |
| 5 | Objetivo general | Sí (materia) | Sección 6 | Análisis y documentación | Borrador |
| 6 | Alcance inicial | Sí (materia) | Sección 7 | Líder del proyecto | Borrador |
| 7 | Requerimientos funcionales principales | Sí (materia) | Sección 9, E-03 | Análisis y documentación | Borrador |
| 8 | Requerimientos no funcionales | Sí (materia) | Sección 10, E-03 | Análisis y documentación | Borrador |
| 9 | Criterios de calidad | Sí (materia) | Sección 12 | Pruebas y calidad | Borrador |
| 10 | Metodología de trabajo justificada | Sí (materia) | Sección 13 | Líder del proyecto | Borrador |
| 11 | Integrantes y responsabilidades | Sí (materia) | Sección 14 | Líder del proyecto | Confirmado |
| 12 | Herramientas y tecnologías propuestas | Sí (materia) | Sección 15 | Todo el equipo | Parcial; framework pospuesto (CC-03) |
| 13 | Métricas o indicadores de calidad | Sí (materia) | Sección 16, E-09 | Pruebas y calidad | Borrador |
| 14 | Mecanismo para registrar cambios | Sí (materia) | Sección 18, E-10 | Líder del proyecto | Borrador |
| 15 | Repositorio creado | Sí (evidencia práctica) | E-02 | Líder del proyecto | Creado; falta README en la raíz |
| 16 | Diagramas | Sí, según corresponda | E-05 | Líder del proyecto | Pendiente |
| 17 | Prototipos o interfaces iniciales | Sí, según corresponda | E-06 | Diseño de interfaz | Pendiente |
| 18 | Estructura de base de datos | Sí, según corresponda | E-07 | Base de datos | Pendiente |
| 19 | Código inicial | Si existe | E-08 | Desarrollo | Pendiente |
| 20 | Registro de riesgos | Recomendado | Sección 19 | Líder del proyecto | Borrador |
| 21 | Bitácora de participación iniciada | Recomendado (sección 8 de la materia) | E-11 | Cada integrante | Pendiente |
| 22 | Autorización del proyecto por la docente | Sí, si el proyecto no está en la lista sugerida | Correo o registro de la autorización | Líder del proyecto | Obtenida |

## 27. Conclusión

Esta etapa deja una base controlada para el desarrollo: el equipo se compromete con la Fase 1 del roadmap (26 requisitos) y declara explícitamente que comunicación, académico, administración y reportes avanzados son trabajo futuro.

Cada requisito tiene criterio de aceptación, caso de prueba y evidencia, lo que permitirá demostrar en las siguientes etapas qué se cumplió y qué no. Las métricas son simples y medibles con herramientas al alcance del equipo, y el control de cambios protege la viabilidad frente al riesgo principal: que el alcance crezca sin control.

Las decisiones pendientes y las inconsistencias quedan visibles, con fecha para resolverse, en lugar de ocultarse. Con esta base, el equipo puede decir con claridad “esto sí lo vamos a hacer” y “esto todavía no”, y la arquitectura queda preparada para que las siguientes fases crezcan sobre ella sin rehacerla.

## 28. Información que necesito proporcionar

Para convertir este borrador en la versión final de entrega faltan estos datos:

- [x] Nombre del proyecto: nexoEdu.
- [x] Roles confirmados (sección 14).
- [x] Autorización de la docente obtenida. Conviene guardar el correo o mensaje como evidencia.
- [x] Escuela destinataria: preparatoria genérica, caso simulado.
- [x] Fecha de entrega: 5 de octubre de 2026.
- [x] Repositorio: github.com/StephAmv/nexoEdu.
- [x] Decisiones D-01 a D-06, D-11, D-15 y D-17 a D-21 resueltas (CC-01, CC-02).
- [x] Framework, reparto JavaScript/Python y almacenamiento de evidencias: pospuestos como decisiones futuras (CC-03).
- [ ] **README en la raíz del repositorio** con nombre, integrantes, tecnologías e instrucciones (hoy el repositorio solo tiene la carpeta docs).
- [ ] **Artefactos E-05 a E-07**: diagrama de casos de uso y de arquitectura, prototipos y modelo de datos. E-08 (código) solo si ya existe.
- [ ] **Commits de los tres integrantes** en el repositorio, para la evidencia E-02.
