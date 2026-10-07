## Tecnológico Nacional de México Instituto Tecnológico de Tijuana

SUBDIRECCIÓN ACADÉMICA

DEPARTAMENTO DE SISTEMAS Y COMPUTACIÓN

SEMESTRE: AGOSTO - DICIEMBRE 2026

INGENIERÍA EN SISTEMAS COMPUTACIONALES

GESTIÓN DE PROYECTOS DE SOFTWARE - SCG-1009

PROYECTO INTEGRADOR

nexoEDU

MEDRANO VARGAS STEPHANIE ARIANA - 23212013

PADILLA DYLAN ALEXIS - 23212038

PINEDA GÓMEZ RICARDO ALEJANDRO - 23212044

PROF. MARIA GUADALUPE RODRIGUEZ LOPEZ


## Índice


## Introducción

El proyecto parte de una visión amplia: una plataforma que centraliza la información académica, disciplinaria, administrativa y de comunicación de una escuela. Esa visión es demasiado grande para nueve semanas y tres integrantes. Por eso el plan separa con claridad lo que el equipo se compromete a entregar (la base operativa)

de lo que queda como evolución futura.

Este Plan de Calidad define qué parte del sistema escolar se desarrollará durante el periodo académico y con qué criterios se juzgará su calidad. Es la línea base contra

la que se medirán las siguientes etapas: planificación, presentación de avances, supervisión y entrega final.

El sistema es una plataforma de gestión escolar con un solo acceso mediante login y control de permisos por roles (RBAC). Su visión es centralizar la información académica, disciplinaria, administrativa y de comunicación entre escuela, docentes, prefectura, alumnos y padres o tutores.

Necesidad que atiende: facilitar el registro diario de información, el seguimiento de alumnos, la comunicación con las familias, la operación administrativa y la generación de reportes para la toma de decisiones.

Principales usuarios: alumno; padre, madre o tutor; docente; prefectura; dirección; administración y contaduría; administrador del sistema.

Principios base del producto:

- Un solo acceso al sistema mediante login con roles.

- Control de permisos basado en RBAC.

- Información organizada por ciclo escolar.

- Relación entre alumnos y uno o más padres/tutores.

- Bitácora para acciones sensibles.

- Desarrollo por fases para evitar construir todo al mismo tiempo.

Escuela destinataria: caso simulado de una preparatoria (nivel medio superior). El sistema no se desarrolla para una escuela específica; todos los datos de prueba serán ficticios.

## Descripción del proyecto


## Problemática

nexoEdu se plantea como un caso simulado: una preparatoria genérica, no una escuela específica. La problemática se deriva de la documentación del proyecto, a partir de lo que el sistema debe resolver. No se usan estadísticas ni datos externos.

Situación actual: la información de alumnos, asistencia, conducta y comunicación con las familias no está centralizada en un sistema único con control de acceso por rol.

Problemas identificados:

- El registro de asistencia, faltas y retardos no queda en un historial consultable por alumno, grupo o periodo.

- Los reportes de conducta y sus evidencias no llegan de forma directa a prefectura ni a los padres/tutores.

- Los padres/tutores no tienen un medio para consultar la asistencia y conducta de sus hijos.

- No existe un control formal de quién puede ver o modificar información sensible de alumnos y familias.

- No hay trazabilidad de quién creó o modificó un registro, lo que dificulta resolver aclaraciones o disputas.

Consecuencias: seguimiento tardío de ausencias e incidencias, información dispersa o duplicada, exposición de datos personales a personas no autorizadas y falta de evidencia ante reclamaciones.

Necesidad de una solución: un sistema que concentre el flujo escolar principal (alumnos, grupos, asistencia y conducta), restrinja el acceso según el rol y deje registro de las acciones sensibles.


## Justificación

Construir primero la base operativa resuelve el flujo escolar más frecuente y deja lista la estructura sobre la que crecerán las demás fases.

| Aspecto | Qué aporta la primera versión |
| --- | --- |
| Centralización de | Alumnos, padres/tutores, docentes, grados y grupos en una |
| información | sola base, organizada por ciclo escolar. |
| Seguimiento | de Historial de asistencia y de reportes de conducta consultable |
| alumnos | por alumno. |
| Control | de Prefectura registra asistencia diaria; docentes registran |
| asistencia | y reportes de conducta con evidencias. |
| conducta |   |
| Comunicación | Los padres/tutores consultan la asistencia y los reportes de |
| entre actores | conducta de sus hijos. Las notificaciones automáticas |
|   | quedan para la Fase 2. |
| Seguridad | y Login único con RBAC: cada rol ve y hace solo lo que le |
| permisos | permite la matriz de permisos. |
| Trazabilidad | Bitácora de quién creó, modificó o eliminó información |
|   | relevante, con fecha y hora. |
| Crecimiento futuro | Arquitectura modular y datos por ciclo escolar para agregar |
|   | comunicación, académico, administración y reportes sin |
|   | rehacer la base. |


## Objetivos

Desarrollar, la primera versión funcional de la plataforma de gestión escolar (base operativa), que permita registrar alumnos, padres/tutores, docentes, grados y grupos, controlar la asistencia y los reportes de conducta con evidencias, y ofrecer consulta a padres/tutores, con acceso por roles y bitácora de acciones sensibles,

verificando su cumplimiento mediante los criterios y métricas de este plan.

## Objetivo general

## Objetivos específicos

- 1. Implementar un login único con control de acceso por roles conforme a la matriz de permisos del proyecto.

- 2. Permitir al administrador del sistema gestionar usuarios, roles, ciclos escolares, grados y grupos.

- 3. Registrar alumnos, padres/tutores y docentes, con sus asociaciones a grupos y entre alumno y tutor.

- 4. Permitir a la prefectura registrar asistencias, faltas y retardos diarios por grupo.

- 5. Permitir a docentes y prefectura registrar reportes de conducta con evidencias adjuntas.

- 6. Permitir a los padres/tutores consultar asistencia, reportes de conducta y evidencias solo de sus hijos.

- 7. Registrar en bitácora las acciones sensibles del alcance inicial.

- 8. Verificar la primera versión con casos de prueba documentados, incluidas pruebas de permisos por rol.

- 9. Mantener control de cambios, métricas y evidencias durante todo el proyecto.


## Alcance del proyecto

A largo plazo, el sistema contempla 15 módulos: autenticación y acceso, docentes, alumnos, padres o tutores, prefectura, dirección, administración y contaduría, inventario de uniformes, académico, calendario escolar, comunicación y notificaciones, inscripciones y matrícula, pagos y colegiaturas, reportes y dashboards, y auditoría y bitácora.

## Visión completa de sistema

## Alcance de la primera versión

| Área |   | Qué incluye |
| --- | --- | --- |
| Autenticación | y | Login con usuario y contraseña, cierre de sesión, menú |
| roles |   | según rol, restricción de módulos y acciones. |
| Gestión | de | Crear, editar, desactivar y reactivar usuarios; asignar roles. |
| usuarios |   |   |
| Estructura escolar |   | Ciclo escolar, grados y grupos. |
| mínima |   |   |
| Comunidad escolar Alumnos, padres/tutores (relación muchos a muchos) y |   |   |
|   |   | docentes asignados a grupos. |
| Prefectura |   | Registro y consulta de asistencias, faltas y retardos. |
| Conducta |   | Reportes de conducta con evidencias, registrados por |
|   |   | docentes y prefectura. |
| Padres/tutores |   | Consulta de datos, asistencia, reportes de conducta y |
|   |   | evidencias de sus hijos. |
| Bitácora básica |   | Registro y consulta de acciones sensibles del alcance inicial. |


## Usuarios y actores

La visión general contempla siete roles; la primera versión involucra directamente a cinco. Alumno y Administración y contaduría quedan fuera de esta versión.

| Rol |   | Función en la visión general |
| --- | --- | --- |
| Administrador | del | Configura usuarios, roles, ciclos, grados, grupos, |
| sistema |   | catálogos y consulta la bitácora. |
| Prefectura |   | Asistencia, disciplina, permisos y control operativo de |
|   |   | alumnos. |
| Docente |   | Imparte clases, registra información académica y reporta |
|   |   | situaciones de sus alumnos. |
| Padre, madre o tutor Da seguimiento académico, disciplinario, administrativo y |   |   |
|   |   | de asistencia. |
| Dirección |   | Visión global de consulta y supervisión; reportes |
|   |   | estratégicos. |
| Alumno |   | Consulta su información académica y escolar. |
| Administración | y | Pagos, colegiaturas, ventas e inventario de uniformes. |
| contaduría |   |   |


## Requerimientos funcionales del alcance inicial

| ID | Requisito | Descripción | Priorida | Criterio de aceptación |
| --- | --- | --- | --- | --- |
|   |   |   | d |   |
| RF-01 Iniciar sesión |   | Todo usuario ingresa con | Alta | Con credenciales válidas se |
|   |   | usuario y contraseña por un |   | accede; con inválidas se |
|   |   | login único. |   | rechaza el acceso con |
|   |   |   |   | mensaje y no se crea |
|   |   |   |   | sesión. |
| RF-02 Mantener sesión |   | El usuario puede cerrar | Alta | Tras cerrar sesión, ninguna |
|   | segura | sesión; las | páginas | página protegida es |
|   |   | protegidas exigen sesión |   | accesible sin volver a |
|   |   | activa. |   | autenticarse. |
| RF-03 Menú según rol El |   | sistema muestra | Alta | Cada rol ve solo los |
|   |   | opciones diferentes según |   | módulos que la matriz le |
|   |   | el rol del usuario. |   | permite (verificado con un |
|   |   |   |   | usuario de prueba por rol). |
| RF-04 Restringir |   | Las acciones no permitidas | Alta | 100 % de los intentos de |
|   | acciones según | se bloquean aunque se |   | acción no permitida en la |
|   | permisos | intente | acceder | matriz de pruebas de |
|   |   | directamente (URL | o | permisos son rechazados. |
|   |   | petición). |   |   |
| RF-05 Restablecer |   | El administrador restablece | Baja | El usuario accede con la |
|   | contraseña | la contraseña de un |   | nueva contraseña y la |
|   |   | usuario. |   | anterior deja de funcionar. |
| RF-06 Gestionar |   | El administrador crea y | Alta | Un usuario creado puede |
|   | usuarios | edita usuarios. |   | iniciar sesión; no se permite |
|   |   |   |   | un nombre de usuario |
|   |   |   |   | duplicado. |
| RF-07 Desactivar |   | y El administrador bloquea, | Media Un usuario desactivado no |   |
|   | reactivar | desactiva o | reactiva | puede iniciar sesión; al |
|   | usuarios | usuarios. |   | reactivarlo, sí. La acción |
|   |   |   |   | queda en bitácora. |
| RF-08 Asignar roles |   | El administrador asigna | Alta | Al cambiar el rol, cambian el |
|   |   | rol(es) a cada usuario. Un |   | menú y los permisos en el |
|   |   | usuario puede tener varios |   | siguiente inicio de sesión. |
|   |   | roles. |   |   |
| RF-09 Configurar ciclo |   | Administrador (y dirección | Alta | Todo grupo pertenece a un |
|   | escolar, grados y | para grupos) configuran la |   | grado y a un ciclo escolar; |
|   | grupos | estructura escolar. |   | no se permiten grupos |
|   |   |   |   | duplicados en el mismo |
|   |   |   |   | grado y ciclo. |


| RF-10 Registrar | Registro de datos generales | Alta | El alumno se guarda con los |
| --- | --- | --- | --- |
| alumnos | y matrícula del alumno |   | datos obligatorios [POR |
|   | (dirección, administrador). |   | DEFINIR, D-17]; el sistema |
|   |   |   | impide duplicados por |
|   |   |   | matrícula. |
| RF-11 Asociar alumno a | Cada alumno queda inscrito | Alta | El alumno aparece en la |
| grado, grupo y | en un grupo de un ciclo |   | lista de su grupo y ciclo, y |
| ciclo | escolar. |   | en ningún otro grupo del |
|   |   |   | mismo ciclo. |
| RF-12 Registrar | Un tutor puede tener varios | Alta | Un tutor con dos hijos ve a |
| padres/tutores y | alumnos y un alumno varios |   | ambos; un alumno con dos |
| asociarlos | tutores. |   | tutores es visible para los |
|   |   |   | dos. |
| RF-13 Registrar | Alta de docentes y su | Alta | El docente ve únicamente |
| docentes | y asignación a uno o más |   | los grupos asignados. |
| asignarlos | a grupos. |   |   |
| grupos |   |   |   |
| RF-14 Editar alumnos | Edición por dirección y | Media | La edición se guarda y |
|   | administrador; prefectura |   | queda en bitácora con el |
|   | “limitado”. |   | valor anterior y el nuevo. |
| RF-15 Registrar | Prefectura marca | Alta | Se guarda un solo registro |
| asistencia diaria | asistencia, falta o retardo |   | por alumno y fecha; un |
|   | por alumno, por grupo y |   | segundo intento se rechaza |
|   | fecha. |   | o se trata como edición. |
| RF-16 Modificar | Corrección de un registro | Media El cambio se guarda y la |   |
| asistencia | de asistencia ya capturado. |   | bitácora conserva quién, |
|   |   |   | cuándo y qué cambió. |
| RF-17 Consultar | Por alumno, grupo y fecha | Media | Los filtros devuelven |
| asistencia | o periodo (prefectura, |   | exactamente los registros |
|   | dirección; docente solo sus |   | capturados en los datos de |
|   | grupos). |   | prueba. |
| RF-18 Registrar reporte | Docente (sus grupos), | Alta | Un docente solo puede |
| de conducta | prefectura y dirección |   | elegir alumnos de sus |
|   | registran reportes sobre un |   | grupos; el reporte queda |
|   | alumno. |   | asociado al alumno, autor y |
|   |   |   | fecha. |
| RF-19 Adjuntar | Se suben archivos como | Alta | El archivo se guarda y |
| evidencias | evidencia de un reporte de |   | puede abrirse desde el |
|   | conducta. |   | reporte. Tipos y tamaño |
|   |   |   | máximo [POR DEFINIR]. |
| RF-20 Consultar | Prefectura y dirección ven | Alta | Cada rol ve exactamente los |
| reportes | y todos; docente, los de sus |   | reportes que le |
| evidencias | grupos. |   | corresponden en los datos |
|   |   |   | de prueba. |


| RF-21 Registrar | Prefectura | registra Media | La | incidencia | queda |
| --- | --- | --- | --- | --- | --- |
| incidencias | incidencias | y da | asociada al alumno y es |   |   |
| disciplinarias | seguimiento a reportes. |   | consultable por prefectura, |   |   |
|   | Relación con “reporte de |   | dirección y sus tutores. |   |   |
|   | conducta” por confirmar. |   |   |   |   |
| RF-22 Padre/tutor | Datos generales de sus | Alta | Solo ve alumnos asociados; |   |   |
| consulta datos | hijos o tutorados. |   | intentar abrir otro alumno |   |   |
| del alumno |   |   | (por ejemplo, cambiando el |   |   |
|   |   |   | ID en la URL) es rechazado. |   |   |
| RF-23 Padre/tutor | Asistencias, | faltas y Alta | Los |   | datos mostrados |
| consulta | retardos de sus hijos. |   | coinciden con lo capturado |   |   |
| asistencia |   |   | por prefectura. |   |   |
| RF-24 Padre/tutor | Reportes de conducta y | Alta | Ve los reportes y abre las |   |   |
| consulta | evidencias de sus hijos. |   | evidencias de sus hijos; no |   |   |
| conducta |   |   | ve los de otros alumnos. |   |   |
| RF-25 Registrar | Quién creó, modificó o | Alta | Cada acción sensible de la |   |   |
| bitácora | eliminó usuarios, | roles, | lista genera exactamente un |   |   |
|   | alumnos, asistencias y |   | registro con usuario, acción, |   |   |
|   | reportes de conducta, con |   | entidad y fecha/hora. |   |   |
|   | fecha y hora. |   |   |   |   |
| RF-26 Consultar | Administrador y dirección | Media | Los filtros devuelven los |   |   |
| bitácora | consultan la bitácora con |   | registros esperados; ningún |   |   |
|   | filtros básicos (usuario, |   | otro rol puede abrir |   | la |
|   | fecha). |   | bitácora. |   |   |


## Requisitos no funcionales

| ID | Requisito Descripción | Método de verificación |
| --- | --- | --- |
| RNF-01 Seguridad | Toda función valida el rol del | Matriz de pruebas rol × acción ejecutada |
|   | basada en usuario en el servidor, no | con un usuario por rol, incluyendo accesos |
|   | roles y solo ocultando botones. | directos por URL. |
|   | permisos |   |
| RNF-02 Registro | Las acciones sensibles del | Ejecutar cada acción sensible y comprobar |
|   | de alcance inicial quedan en | su registro en la bitácora. |
|   | auditoría bitácora. |   |
| RNF-03 Diseño | Grupos, inscripciones | y Crear dos ciclos con datos de prueba y |
|   | para asistencias se asocian a un | verificar que las consultas de uno no |
|   | múltiples ciclo escolar. | muestran datos del otro. |
|   | ciclos |   |
|   | escolares |   |
| RNF-04 Interfaz | Uso en computadora, tablet y | Revisar las pantallas principales en tres |
|   | responsiv celular. | anchos de pantalla (herramientas del |
|   | a | navegador) con una lista de verificación y |
|   |   | capturas. |
| RNF-05 Protección | Datos de alumnos y familias | Pruebas de acceso cruzado (tutor A intenta |
|   | de datos solo visibles para roles | ver alumno de tutor B) y revisión de la tabla |
|   | personale autorizados; | contraseñas de usuarios en la base de datos. |
|   | s almacenadas cifradas con |   |
|   | hash. |   |
| RNF-06 Respaldos | Procedimiento documentado | Ejecutar al menos un respaldo y una |
|   | de para respaldar y restaurar la | restauración completa antes de la entrega |
|   | informació base de datos. Será manual: | final; conservar evidencia. |
|   | n exportación de | las |
|   | colecciones de Firestore a |   |
|   | archivos. |   |
| RNF-07 Validacion | Se evitan alumnos, usuarios | Casos de prueba que intentan crear cada |
|   | es contra y registros de asistencia | duplicado y esperan rechazo. |
|   | duplicidad duplicados. |   |
| RNF-08 Arquitectu | El código se organiza por | Revisión de la estructura del repositorio |
|   | ra módulos para agregar fases | contra el diseño de arquitectura en cada |
|   | modular posteriores. | cierre de iteración. |
| RNF-09 Tiempo de | Las operaciones principales | Medición con las herramientas de red del |
|   | respuesta responden en menos de 3 | navegador sobre RF-01, RF-15, RF-20 y |
|   | segundos en el entorno de | RF-23. |
|   | pruebas con los datos de |   |
|   | prueba del equipo. |   |
| RNF-10 Control de | Todo el código y la | Historial de commits con participación de |
|   | versiones documentación se versionan | los tres integrantes. |
|   | en el repositorio del proyecto. |   |


## Control de acceso y seguridad

La seguridad se trata como criterio de calidad central: un error de permisos en este sistema expone datos de menores y familias. Se aplican cinco reglas.

- 1. Control de acceso basado en roles (RBAC). Cada usuario tiene rol(es) y cada rol determina módulos y acciones permitidas, conforme a la matriz de permisos del proyecto.

- 2. Restricción de módulos. El menú muestra solo los módulos del rol (RF-03).

- 3. Restricción de acciones. El servidor valida cada acción; ocultar un botón no cuenta como control (RF-04, RNF-01).

- 4. Mínimo privilegio por relación. El docente solo accede a alumnos de sus grupos; el padre/tutor solo a sus hijos o tutorados. Estas reglas vienen de la matriz y de las reglas generales.

- 5. Registro de acciones importantes. Altas, cambios y bajas sobre usuarios, roles, alumnos, asistencia y conducta quedan en bitácora (RF-25).

## Matriz de permisos aplicable a la primera versión

| Acción | Alumno | Padre/Tutor | Docente | Prefectura | Dirección | Administración | Administrador |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Consultar datos del | Sí | Sí, de sus | Sí, de sus | Sí | Sí | Limitado | Sí |
| alumno |   | hijos | grupos |   |   |   |   |
| Crear alumnos | No | No | No | No | Sí | Sí | Sí |
| Editar alumnos | No | No | No | Limitado | Sí | Sí | Sí |
| Registrar asistencia | No | No | No | Sí | Sí | No | Sí |
| Consultar asistencia | Sí, propia Sí, de sus |   | Sí, de sus | Sí | Sí | No | Sí |
|   |   | hijos | grupos |   |   |   |   |
| Registrar reportes | No | No | Sí | Sí | Sí | No | Sí |
| de conducta |   |   |   |   |   |   |   |
| Consultar reportes | Sí, propios | Sí, de sus | Sí, de sus | Sí | Sí | No | Sí |
| de conducta | si aplica | hijos | grupos |   |   |   |   |
| Subir evidencias de | No | No | Sí | Sí | Sí | No | Sí |
| conducta |   |   |   |   |   |   |   |
| Consultar evidencias | Sí, propias | Sí, de sus | Sí, de sus | Sí | Sí | No | Sí |
| de conducta | si aplica | hijos | grupos |   |   |   |   |
| Gestionar materias | No | No | No | No | Sí | No | Sí |
| y grupos |   |   |   |   |   |   |   |
| Consultar bitácora No |   | No | No | No | Sí | Limitado | Sí |
| Administrar usuarios | No | No | No | No | No | No | Sí |
| y roles |   |   |   |   |   |   |   |


## Criterio de calidad

La primera versión se considera de calidad solo si cumple los siete criterios siguientes, cada uno con evidencia.

| Criterio | Qué significa | Cómo se verificará | Evidencia generada |
| --- | --- | --- | --- |
| Funcionalidad | El sistema cumple los | Un caso de prueba por | Bitácora de pruebas; |
|   | requisitos del alcance | requisito con resultado | matriz de trazabilidad |
|   | inicial. | esperado y obtenido. | actualizada. |
| Seguridad | Cada usuario | solo Matriz de pruebas rol × | Registro de pruebas |
|   | accede a lo que su rol | acción y pruebas de acceso | de permisos con |
|   | permite. | cruzado. | capturas de accesos |
|   |   |   | rechazados. |
| Usabilidad | Las funciones | Recorrido guiado: | un Lista de tareas con |
|   | principales | se integrante que no desarrolló | resultado (completada |
|   | completan sin ayuda. | la función completa las | / con dificultad) y |
|   |   | tareas clave (login, pasar | observaciones. |
|   |   | lista, registrar reporte, |   |
|   |   | consulta del tutor) sin |   |
|   |   | instrucciones. |   |
| Integridad | de No hay | registros Casos de prueba de | Resultados de |
| datos | duplicados | ni duplicidad y de campos | pruebas y capturas de |
|   | inconsistentes. | obligatorios (RNF-07). | los mensajes de |
|   |   |   | validación. |
| Trazabilidad | Las acciones sensibles | Verificar que cada acción de | Capturas de la |
|   | se pueden identificar. | RF-25 genera su registro. | bitácora con los |
|   |   |   | registros generados |
|   |   |   | en las pruebas. |
| Rendimiento | Respuesta ágil en las | Medición de RNF-09 | Tabla de mediciones |
|   | operaciones | (menos de 3 s) con | con fecha y capturas. |
|   | principales. | herramientas | del |
|   |   | navegador. |   |
| Mantenibilidad | Las siguientes fases se | Revisión de código por un | Revisiones registradas |
|   | pueden agregar sin | integrante distinto al autor; | en el repositorio (pull |
|   | rehacer la base. | estructura por módulos | requests o |
|   |   | (RNF-08). | comentarios) y |
|   |   |   | diagrama de |
|   |   |   | arquitectura. |


## Metodología de trabajo

El equipo usará Scrum adaptado a un equipo de tres integrantes, con iteraciones de dos semanas alineadas a las etapas de la materia.

## Justificación:

- La materia exige avances funcionales desde la Etapa II; las iteraciones cortas producen un incremento demostrable al final de cada sprint.

- El backlog priorizado (Alta, Media, Baja) permite posponer requisitos de forma ordenada cuando falta tiempo, que es el principal riesgo del proyecto.

- Las revisiones al cierre de cada sprint coinciden con los puntos de control de la materia y generan evidencia de seguimiento.

- Se descartan ceremonias que no aportan a un equipo de tres (por ejemplo, un Scrum Master dedicado): el líder del proyecto asume esa función.

## Aplicación

| Sprint | Fechas | Objetivo del sprint |
| --- | --- | --- |
| Sprint 0 23 sep – 6 oct Plan de calidad, repositorio, modelo de datos inicial, |   |   |
|   |   | prototipos. |
| Sprint 1 7 – 20 oct |   | Autenticación, roles, usuarios, ciclo/grados/grupos, |
|   |   | bitácora base. |
| Sprint 2 21 oct – 3 nov Alumnos, tutores, docentes y asistencia. |   |   |
| Sprint 3 4 – 17 nov |   | Conducta, evidencias, vista de padres/tutores y consulta |
|   |   | de bitácora. |
| Cierre | 18 – 24 nov | Pruebas de regresión, correcciones, manual de usuario |
|   |   | y entrega. |


## Organización del equipo

| Integrante Rol |   |   | Responsabilidades | Evidencias |
| --- | --- | --- | --- | --- |
|   |   |   |   | generadas |
| Stephanie | Líder | del | Coordinar sprints y tablero; | Registro de cambios, |
| Ariana | proyecto; |   | controlar cambios y decisiones; | actas de revisión de |
| Medrano | desarrollo; |   | diseñar prototipos y pantallas; | sprint, prototipos, |
| Vargas | diseño | de | desarrollar autenticación, roles, | commits. |
|   | interfaz |   | vista de padres/tutores y bitácora. |   |
| Dylan | Responsable |   | Mantener requisitos y matriz de | Plan de calidad, |
| Alexis | de análisis y |   | trazabilidad; redactar los | requisitos, matriz de |
| Padilla | documentació |   | documentos de cada etapa y el | permisos, modelo |
|   | n; responsable |   | manual de usuario; diseñar el | entidad–relación, |
|   | de base de |   | modelo de datos; crear scripts, | scripts de BD, |
|   | datos |   | datos de prueba ficticios y | manual de usuario, |
|   |   |   | procedimiento de respaldo. | commits. |
| Ricardo | Responsable |   | Diseñar casos de prueba; ejecutar | Casos de prueba, |
| Alejandro | de pruebas y |   | la matriz de permisos; llevar la | bitácora de pruebas, |
| Pineda | calidad; |   | bitácora de pruebas y las | registro de métricas, |
| Gómez | desarrollo |   | métricas; desarrollar alumnos, | commits. |
|   |   |   | tutores, docentes, asistencia y |   |
|   |   |   | conducta. |   |


## Tecnologías y herramientas

| Categoría |   | Tecnología | Propósito |
| --- | --- | --- | --- |
| Lenguaje | de | JavaScript y Python | Desarrollo del sistema. |
| programación |   |   |   |
| Framework |   | Por definir, el frontend usará las | Estructura de la |
|   |   | plantillas del framework (HTML, CSS | aplicación web |
|   |   | y JavaScript) | responsiva. |
| Base de datos |   | Firebase | Almacenamiento de |
|   |   |   | usuarios, alumnos, |
|   |   |   | asistencia, conducta y |
|   |   |   | bitácora. |
| Almacenamient |   | Pendiente se eligió guardarlas dentro | Archivos adjuntos a |
| o de evidencias |   | de la base de datos para la primera | reportes de conducta. |
|   |   | versión, pero hay límites de espacio |   |
|   |   | en Firebase |   |
| Control | de | Git | Historial de cambios y |
| versiones |   |   | evidencia de |
|   |   |   | participación. |
| Repositorio |   | GitHub | Alojamiento del código y |
| remoto |   |   | la documentación. |
| Diseño | y | draw.io | Prototipos de interfaz y |
| prototipos |   |   | diagramas. |
| Pruebas |   | Pendiente | Registro de casos de |
|   |   |   | prueba; pruebas |
|   |   |   | automatizadas si el |
|   |   |   | equipo las adopta. |
| Documentación Google Docs |   |   | Plan de calidad, reportes |
|   |   |   | y manual de usuario. |


## Métricas e Indicadores de calidad

| ID | Métrica | Fórmula | Meta | Frecuencia | Responsable | Evidencia |   |
| --- | --- | --- | --- | --- | --- | --- | --- |
| M-01 | Requisitos | RF aceptados | 100 % de | Cierre de | Pruebas | y Matriz | de |
|   | cumplidos | / RF | RF Alta; ≥ | sprint | calidad |   | trazabilidad |
|   |   | comprometido | 80 % del |   |   |   |   |
|   |   | s × 100 | total |   |   |   |   |
| M-02 | Pruebas | Casos | ≥ 90 % | Cierre de | Pruebas | y | Bitácora de |
|   | satisfactorias | aprobados / | antes de la | sprint | calidad | pruebas |   |
|   |   | casos | entrega |   |   |   |   |
|   |   | ejecutados × | final |   |   |   |   |
|   |   | 100 |   |   |   |   |   |
| M-03 | Cobertura de | Combinacione | 100 %, | Cierre de | Pruebas | y Matriz | de |
|   | pruebas de | s rol × acción | todas | sprint | calidad |   | pruebas de |
|   | permisos | probadas / | aprobadas |   |   | permisos |   |
|   |   | combinacione |   |   |   |   |   |
|   |   | s definidas × |   |   |   |   |   |
|   |   | 100 |   |   |   |   |   |
| M-04 | Errores | Conteo por | Seguimient | Semanal Pruebas |   | y | Bitácora de |
|   | detectados | prioridad (alta, | o; sin meta |   | calidad | pruebas |   |
|   |   | media, baja) | numérica |   |   |   |   |
| M-05 | Errores | Errores | 100 % de | Semanal | Líder | del | Bitácora de |
|   | corregidos | cerrados / | prioridad |   | proyecto | pruebas; |   |
|   |   | errores | alta; ≥ 80 % |   |   |   | commits de |
|   |   | detectados × | del total al |   |   |   | corrección |
|   |   | 100 | cierre |   |   |   |   |
| M-06 | Cumplimient | Tareas | ≥ 80 % por | Cierre de | Líder | del | Tablero de |
|   | o de | terminadas / | sprint | sprint | proyecto | gestión |   |
|   | actividades | tareas |   |   |   |   |   |
|   |   | planificadas |   |   |   |   |   |
|   |   | del sprint × |   |   |   |   |   |
|   |   | 100 |   |   |   |   |   |
| M-07 | Cambios | Conteo de | 100 % de | Cierre de | Líder | del | Registro de |
|   | solicitados y | solicitudes; | cambios | sprint | proyecto | cambios |   |
|   | aprobados | aprobados / | con registro |   |   |   |   |
|   |   | solicitados | y decisión |   |   |   |   |
| M-08 | Incidencias | Conteo de | 0 | Semanal Pruebas |   | y Tablero | o |
|   | abiertas y | abiertas vs. | incidencias |   | calidad |   | bitácora de |
|   | cerradas | cerradas | de prioridad |   |   | pruebas |   |
|   |   |   | alta abiertas |   |   |   |   |
|   |   |   | en la |   |   |   |   |
|   |   |   | entrega |   |   |   |   |
|   |   |   | final |   |   |   |   |
| M-09 | Participación | Horas y | Cada | Cierre de | Análisis | y | Bitácora de |
|   | del equipo | actividades | integrante | sprint | documentació |   | participación |
|   |   | por integrante | con |   | n |   | ; historial de |
|   |   | / total del | actividades |   |   | commits |   |
|   |   | equipo | registradas |   |   |   |   |
|   |   |   | en todos los |   |   |   |   |
|   |   |   | sprints |   |   |   |   |


## Plan de aseguramiento y control de calidad.

| Actividad | Momento | Responsable Qué se revisa |
| --- | --- | --- |
| Revisión de | Planeación de | Todo el equipo Que cada requisito sea claro, |
| requisitos | cada sprint | esté dentro del alcance y tenga |
|   |   | criterio de aceptación. |
| Revisión de | Antes | de Autor + un Modelo de datos, relaciones |
| diseño | programar | revisor (alumno–tutor, docente–grupo) y |
|   | cada módulo | asociación con ciclo escolar. |
| Revisión de | Antes | de Integrante Legibilidad, estructura por |
| código | integrar cada | distinto al módulos, validación de permisos |
|   | cambio | autor en el servidor. |
| Pruebas | Al terminar | Pruebas y Caso de prueba del requisito |
| funcionales | cada requisito | calidad con resultado esperado y |
|   |   | obtenido. |
| Validación | Cierre de cada | Pruebas y Matriz rol × acción y accesos |
| de permisos | sprint | calidad cruzados. |
| Validación | Al terminar | Pruebas y Campos obligatorios, formatos y |
| de datos | cada formulario | calidad duplicados. |
| Pruebas de | Cierre (18–24 | Todo el equipo Todos los casos de prueba de |
| regresión | nov) | nuevo sobre la versión final. |


## Control de cambios

Procedimiento:

- 1. Cualquier integrante (o la docente) propone el cambio y se registra.

- 2. El líder analiza el impacto en tiempo, complejidad, recursos, requisitos, calidad y alcance.

- 3. El equipo decide: aprobar, rechazar o posponer (al backlog de trabajo futuro).

- 4. Si se aprueba, se actualizan los documentos afectados (requisitos, trazabilidad, plan) con nueva versión.

- 5. Se implementa y se verifica como cualquier requisito; luego se cierra.

## Reglas para proteger la viabilidad:

- Un cambio que agregue funciones de las fases 2 a 5 se pospone por defecto.

- Un cambio que ponga en riesgo un requisito de prioridad Alta se rechaza o se compensa retirando un requisito de prioridad Media o Baja.

- Después del 17 de noviembre solo se aceptan correcciones de errores, no funciones nuevas.

- Resolver una decisión pendiente (sección 20) también se registra como cambio.


## Riesgos relacionados con la calidad

| ID | Riesgo | Probab | Impa | Nivel Mitigación | Responsabl |
| --- | --- | --- | --- | --- | --- |
|   |   | ilidad | cto |   | e |
| R-01 Crecimiento excesivo del |   | Alta Alto Alto Línea base CC-00; reglas de |   |   | Líder del |
|   | alcance |   |   | control de cambios; posponer | proyecto |
|   |   |   |   | por defecto. |   |
| R-02 Falta de tiempo para |   | Alta Alto Alto Prioridades Alta/Media/Baja; |   |   | Líder del |
|   | completar el alcance |   |   | entregar primero los RF Alta | proyecto |
| R-03 Decisiones pendientes |   | Medi | Alto Alto Fecha límite por decisión ; |   | Líder del |
|   | sin resolver bloquean el | a |   | valor por defecto de mínimo | proyecto |
|   | desarrollo |   |   | privilegio mientras tanto. |   |
| R-04 Errores de permisos que |   | Medi | Alto Alto Validación en servidor; matriz |   | Pruebas |
|   | exponen datos a roles no | a |   | de pruebas de permisos al | y calidad |
|   | autorizados |   |   | 100 %. |   |
| R-05 Manejo incorrecto de |   | Medi | Alto Alto Contraseñas con hash; solo |   | Base de |
|   | datos | sensibles a |   | datos de prueba ficticios; | datos |
|   | (contraseñas, datos de |   |   | evidencias accesibles solo |   |
|   | alumnos, evidencias) |   |   | por rol. |   |
| R-06 Requisitos |   | ambiguos Alta Medi |   | Alto Registro de inconsistencias ; | Análisis y |
|   | (“Limitado”, “si aplica”, |   | o | criterio de aceptación por | documen |
|   | reporte vs. incidencia) |   |   | requisito. | tación |
| R-07 Falta de pruebas por |   | Medi | Alto Alto Definición de terminado |   | Pruebas |
|   | dejarlas al final | a |   | exige caso de prueba | y calidad |
|   |   |   |   | aprobado. |   |
| R-08 Problemas |   | de Medi | Medi | Med Modelo de datos revisado | Base de |
|   | integración | entre a | o | io antes de | programar; datos |
|   | módulos (roles, alumnos, |   |   | integración continua en la |   |
|   | asistencia, conducta) |   |   | rama principal. |   |
| R-09 Dependencia excesiva |   | Medi | Alto Alto Revisión cruzada de código y |   | Líder del |
|   | de una persona | a |   | de base de datos; cada | proyecto |
|   |   |   |   | integrante documenta su |   |
|   |   |   |   | parte; bitácora | de |
|   |   |   |   | participación. |   |
| R-10 Cambios tardíos que |   | Medi | Alto Alto Congelamiento de funciones |   | Líder del |
|   | desestabilizan la versión | a |   | después del | 17 de proyecto |
|   | final |   |   | noviembre. |   |
| R-11 Tecnologías |   | elegidas Medi | Medi | Med Decidir antes del 6 de | Todo el |
|   | tarde o poco conocidas | a | o | io octubre (D-22), priorizando lo | equipo |
|   | por el equipo |   |   | que el equipo ya domina. |   |
