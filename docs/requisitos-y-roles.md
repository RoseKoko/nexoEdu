# Requisitos y roles del sistema escolar

## 1. Objetivo del sistema

Construir una plataforma integral para la gestión escolar que centralice la información académica, disciplinaria, administrativa y de comunicación entre la escuela, docentes, prefectura, alumnos y padres o tutores.

El sistema debe servir como base operativa para registrar información diaria, dar seguimiento a alumnos, facilitar la comunicación con las familias, administrar procesos escolares y generar reportes útiles para la toma de decisiones.

## 2. Alcance inicial

El sistema contempla los siguientes módulos principales:

1. Módulo de docentes.
2. Módulo de alumnos.
3. Módulo de padres o tutores.
4. Módulo de prefectura.
5. Módulo de dirección.
6. Módulo de administración y contaduría.
7. Módulo de inventario de uniformes.
8. Módulo académico.
9. Módulo de calendario escolar.
10. Módulo de comunicación y notificaciones.
11. Módulo de inscripciones y matrícula.
12. Módulo de pagos y colegiaturas.
13. Módulo de reportes y dashboards.
14. Módulo de auditoría y bitácora.

## 3. Roles del sistema

### 3.1 Alumno

Usuario asociado a un expediente académico y escolar. Puede consultar información propia según las reglas definidas por la institución.

Responsabilidades y acceso esperado:

- Consultar horarios de clase.
- Consultar tareas y entregas asignadas.
- Consultar calificaciones propias si la escuela lo permite.
- Consultar avisos generales.
- Consultar calendario escolar.

### 3.2 Padre, madre o tutor

Usuario responsable de uno o más alumnos. Su función principal es dar seguimiento académico, disciplinario, administrativo y de asistencia.

Responsabilidades y acceso esperado:

- Consultar información de sus hijos o tutorados.
- Visualizar evidencias y reportes de conducta.
- Recibir notificaciones por incidencias, faltas, retardos o avisos escolares.
- Justificar faltas.
- Solicitar o autorizar permisos y salidas.
- Consultar calificaciones, boletas y estado académico.
- Consultar adeudos, pagos y colegiaturas.
- Comunicarse con docentes, prefectura o dirección según las reglas de la escuela.

### 3.3 Docente

Usuario responsable de impartir clases, registrar información académica y reportar situaciones relevantes sobre los alumnos.

Responsabilidades y acceso esperado:

- Consultar grupos y alumnos asignados.
- Registrar tareas y entregas.
- Capturar calificaciones.
- Subir evidencias académicas o conductuales.
- Registrar reportes de conducta.
- Consultar historial académico y conductual de sus alumnos asignados, según permisos.
- Enviar comunicados a alumnos, padres o tutores de sus grupos.

### 3.4 Prefectura

Usuario responsable del seguimiento disciplinario, asistencia, retardos, permisos y control operativo de alumnos dentro de la escuela.

Responsabilidades y acceso esperado:

- Registrar asistencias, faltas y retardos.
- Consultar reportes de conducta creados por docentes.
- Registrar incidencias disciplinarias.
- Validar o revisar justificantes de faltas.
- Registrar autorizaciones de salida o permisos.
- Notificar a padres o tutores sobre incidencias o ausencias.
- Generar reportes de asistencia y conducta.

### 3.5 Dirección

Usuario con visión global de la operación escolar y facultad para consultar reportes estratégicos.

Responsabilidades y acceso esperado:

- Consultar información general de alumnos, grupos, docentes y ciclos escolares.
- Consultar estadísticas de asistencia, desempeño académico y conducta.
- Consultar reportes administrativos y financieros.
- Publicar avisos generales.
- Supervisar incidencias relevantes.
- Autorizar procesos especiales, si aplica.
- Acceder a dashboards institucionales.

### 3.6 Administración y contaduría

Usuario responsable de procesos administrativos, pagos, colegiaturas, ventas e inventario relacionado con uniformes.

Responsabilidades y acceso esperado:

- Registrar pagos y colegiaturas.
- Consultar adeudos por alumno.
- Emitir comprobantes o recibos.
- Administrar ventas de uniformes.
- Consultar y actualizar inventario de uniformes.
- Generar reportes de ingresos, adeudos y ventas.

### 3.7 Administrador del sistema

Usuario técnico o institucional con permisos para configurar el sistema.

Responsabilidades y acceso esperado:

- Crear, editar y desactivar usuarios.
- Asignar roles y permisos.
- Configurar ciclos escolares, grados, grupos y materias.
- Administrar catálogos generales.
- Consultar bitácoras de auditoría.
- Configurar parámetros del sistema.

## 4. Módulos funcionales

### 4.1 Módulo de autenticación y acceso

Permite el ingreso seguro al sistema mediante un login único basado en roles.

Requisitos funcionales:

- Iniciar sesión con usuario y contraseña.
- Asignar uno o más roles a cada usuario.
- Restringir el acceso a módulos y acciones según permisos.
- Permitir recuperación o restablecimiento de contraseña.
- Bloquear o desactivar usuarios cuando sea necesario.

Decisión inicial recomendada:

- Usar un login único para todos los tipos de usuarios.
- Controlar la experiencia mediante roles y permisos.
- Permitir que un padre o tutor pueda tener varios alumnos asociados.
- Definir si los alumnos tendrán cuenta propia desde la primera versión o si se habilitará en una fase posterior.

### 4.2 Módulo de docentes

Permite a los docentes gestionar actividades académicas y reportes relacionados con sus alumnos.

Requisitos funcionales:

- Consultar grupos y materias asignadas.
- Registrar tareas y entregas.
- Capturar calificaciones.
- Subir evidencias académicas.
- Subir evidencias de conducta.
- Registrar reportes de conducta.
- Consultar reportes previamente registrados.
- Enviar observaciones o mensajes a padres o tutores.

Regla importante:

- Las evidencias y reportes de conducta registrados por docentes deben poder ser visualizados por prefectura y por los padres o tutores del alumno correspondiente.

### 4.3 Módulo de alumnos

Centraliza el expediente del alumno y su información escolar.

Requisitos funcionales:

- Registrar datos generales del alumno.
- Asociar alumno con padre, madre o tutor.
- Asociar alumno con grado, grupo, ciclo escolar y matrícula.
- Consultar historial académico.
- Consultar historial de asistencia.
- Consultar historial de conducta.
- Consultar documentos entregados o pendientes.
- Consultar estado administrativo, como adeudos o pagos, según permisos.

### 4.4 Módulo de padres o tutores

Permite a las familias dar seguimiento a la información relevante de sus hijos o tutorados.

Requisitos funcionales:

- Consultar datos generales del alumno asociado.
- Visualizar asistencias, faltas y retardos.
- Visualizar evidencias y reportes de conducta.
- Visualizar calificaciones y boletas.
- Justificar faltas.
- Solicitar permisos o autorizaciones de salida.
- Recibir notificaciones.
- Consultar avisos generales.
- Consultar pagos, colegiaturas y adeudos.
- Comunicarse con docentes, prefectura o dirección.

### 4.5 Módulo de prefectura

Permite controlar asistencia, disciplina y permisos de alumnos.

Requisitos funcionales:

- Registrar asistencia diaria.
- Registrar faltas y retardos.
- Consultar y dar seguimiento a reportes de conducta.
- Registrar incidencias disciplinarias.
- Revisar justificantes de faltas.
- Registrar permisos y salidas autorizadas.
- Notificar a padres o tutores sobre incidencias, faltas o retardos.
- Generar reportes por alumno, grupo, fecha o periodo.

### 4.6 Módulo de dirección

Permite la supervisión general de la escuela.

Requisitos funcionales:

- Consultar dashboards institucionales.
- Consultar estadísticas de asistencia.
- Consultar estadísticas de conducta.
- Consultar desempeño académico por alumno, grupo, grado o periodo.
- Publicar avisos generales.
- Consultar reportes financieros resumidos.
- Consultar inventario bajo o movimientos relevantes.
- Dar seguimiento a casos importantes.

### 4.7 Módulo de administración y contaduría

Permite gestionar información financiera y administrativa de alumnos.

Requisitos funcionales:

- Registrar colegiaturas.
- Registrar pagos.
- Consultar adeudos.
- Generar recibos o comprobantes.
- Consultar historial de pagos por alumno.
- Generar reportes de ingresos y adeudos.
- Registrar conceptos de cobro.
- Administrar descuentos, becas o recargos, si aplica.

### 4.8 Módulo de inventario de uniformes

Permite controlar la existencia, venta y movimientos de uniformes escolares.

Requisitos funcionales:

- Registrar productos de uniforme.
- Registrar tallas, modelos, precios y existencias.
- Registrar entradas y salidas de inventario.
- Registrar ventas de uniformes.
- Asociar ventas a alumnos o padres/tutores cuando aplique.
- Generar alertas de bajo stock.
- Consultar historial de movimientos.
- Generar reportes de inventario y ventas.

### 4.9 Módulo académico

Permite administrar la estructura académica y el avance escolar de los alumnos.

Requisitos funcionales:

- Configurar grados, grupos y materias.
- Definir plan de estudios por grado.
- Asignar docentes a materias y grupos.
- Registrar tareas y entregas.
- Registrar calificaciones.
- Generar boletas.
- Consultar kardex o historial académico.
- Consultar desempeño por alumno, grupo, materia o periodo.

### 4.10 Módulo de calendario escolar

Permite organizar fechas importantes y eventos escolares.

Requisitos funcionales:

- Registrar horarios de clases.
- Registrar eventos escolares.
- Registrar exámenes.
- Registrar juntas de padres.
- Registrar días festivos o suspensión de clases.
- Mostrar calendario por rol.
- Enviar recordatorios o notificaciones de eventos relevantes.

### 4.11 Módulo de comunicación y notificaciones

Permite centralizar avisos, mensajes y alertas automáticas.

Requisitos funcionales:

- Publicar avisos generales desde dirección.
- Enviar mensajes dirigidos por grupo, alumno o rol.
- Notificar a padres o tutores cuando se registre una falta, retardo o incidencia.
- Notificar cuando se suba una evidencia de conducta.
- Notificar fechas importantes del calendario escolar.
- Registrar historial de notificaciones enviadas.

Canales sugeridos:

- Notificación dentro del sistema.
- Correo electrónico.
- Notificación push, si se desarrolla aplicación móvil o PWA.

### 4.12 Módulo de inscripciones y matrícula

Permite gestionar altas, reinscripciones y documentación escolar.

Requisitos funcionales:

- Registrar nuevos alumnos.
- Registrar documentación requerida.
- Controlar documentos entregados y pendientes.
- Asignar ciclo escolar, grado y grupo.
- Gestionar reinscripciones.
- Consultar historial de matrícula.

### 4.13 Módulo de pagos y colegiaturas

Permite controlar obligaciones económicas de alumnos y familias.

Requisitos funcionales:

- Definir conceptos de pago.
- Generar colegiaturas por ciclo o periodo.
- Registrar pagos realizados.
- Consultar adeudos.
- Registrar descuentos, becas o recargos.
- Emitir recibos.
- Generar reportes financieros.

### 4.14 Módulo de reportes y dashboards

Permite generar información para dirección, administración, prefectura y docentes.

Requisitos funcionales:

- Reporte de asistencia por alumno, grupo, grado o periodo.
- Reporte de incidencias por alumno, grupo, tipo o periodo.
- Reporte de calificaciones y desempeño académico.
- Reporte de adeudos y pagos.
- Reporte de ventas de uniformes.
- Reporte de inventario bajo en stock.
- Dashboard general para dirección.
- Exportación a PDF o Excel, si aplica.

### 4.15 Módulo de auditoría y bitácora

Permite registrar acciones importantes realizadas dentro del sistema.

Requisitos funcionales:

- Registrar quién creó, modificó o eliminó información relevante.
- Registrar fecha y hora de cada acción.
- Registrar cambios en asistencias, calificaciones, pagos, incidencias y permisos.
- Permitir consulta de bitácora por administradores autorizados.
- Mantener evidencia ante aclaraciones o disputas.

## 5. Matriz inicial de permisos

| Módulo / Acción | Alumno | Padre/Tutor | Docente | Prefectura | Dirección | Administración | Administrador |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Consultar datos propios del alumno | Sí | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | Limitado | Sí |
| Crear alumnos | No | No | No | No | Sí | Sí | Sí |
| Editar alumnos | No | No | No | Limitado | Sí | Sí | Sí |
| Registrar asistencia | No | No | No | Sí | Sí | No | Sí |
| Consultar asistencia | Sí, propia | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Justificar faltas | No | Solicita | No | Revisa/valida | Sí | No | Sí |
| Registrar reportes de conducta | No | No | Sí | Sí | Sí | No | Sí |
| Consultar reportes de conducta | Sí, propios si aplica | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Subir evidencias de conducta | No | No | Sí | Sí | Sí | No | Sí |
| Consultar evidencias de conducta | Sí, propias si aplica | Sí, de sus hijos | Sí, de sus grupos | Sí | Sí | No | Sí |
| Registrar calificaciones | No | No | Sí | No | Sí | No | Sí |
| Consultar calificaciones | Sí, propias | Sí, de sus hijos | Sí, de sus grupos | No | Sí | No | Sí |
| Gestionar materias y grupos | No | No | No | No | Sí | No | Sí |
| Publicar avisos generales | No | No | No | No | Sí | No | Sí |
| Enviar mensajes | Limitado | Sí | Sí | Sí | Sí | Limitado | Sí |
| Registrar pagos | No | No | No | No | Sí | Sí | Sí |
| Consultar adeudos | Limitado | Sí, de sus hijos | No | No | Sí | Sí | Sí |
| Gestionar inventario de uniformes | No | No | No | No | Sí | Sí | Sí |
| Consultar reportes institucionales | No | No | Limitado | Limitado | Sí | Según área | Sí |
| Consultar bitácora | No | No | No | No | Sí | Limitado | Sí |
| Administrar usuarios y roles | No | No | No | No | No | No | Sí |

## 6. Reglas generales del sistema

- Toda información debe estar asociada a un ciclo escolar.
- Un alumno puede tener uno o más padres o tutores asociados.
- Un padre o tutor puede tener uno o más alumnos asociados.
- Un docente solo debe gestionar alumnos de sus grupos o materias asignadas.
- Prefectura debe poder consultar reportes de conducta y asistencia de todos los alumnos bajo su responsabilidad operativa.
- Dirección debe tener visibilidad global, principalmente de consulta y supervisión.
- Administración debe tener acceso a información financiera y de inventario, pero no necesariamente a información disciplinaria detallada.
- Toda modificación importante debe quedar registrada en la bitácora.
- Las notificaciones automáticas deben generarse ante eventos relevantes como faltas, retardos, incidencias, evidencias de conducta y avisos generales.

## 7. Entidades principales sugeridas

Estas entidades sirven como base para el futuro diseño de base de datos:

- Usuario.
- Rol.
- Permiso.
- Alumno.
- Padre o tutor.
- Docente.
- Grupo.
- Grado.
- Materia.
- Ciclo escolar.
- Inscripción o matrícula.
- Asistencia.
- Justificante.
- Reporte de conducta.
- Evidencia.
- Calificación.
- Tarea.
- Entrega.
- Boleta.
- Calendario escolar.
- Evento escolar.
- Aviso.
- Notificación.
- Pago.
- Concepto de pago.
- Adeudo.
- Producto de uniforme.
- Movimiento de inventario.
- Venta de uniforme.
- Bitácora.

## 8. Prioridad recomendada para desarrollo

### Fase 1: Base operativa

- Autenticación y roles.
- Gestión de usuarios.
- Gestión de alumnos, padres/tutores, docentes, grados y grupos.
- Módulo de prefectura para asistencia.
- Módulo de docentes para reportes de conducta y evidencias.
- Visualización para padres/tutores.
- Bitácora básica.

### Fase 2: Comunicación y seguimiento

- Notificaciones automáticas.
- Justificación de faltas.
- Permisos y autorizaciones de salida.
- Avisos generales.
- Calendario escolar.

### Fase 3: Académico

- Materias y planes de estudio.
- Tareas y entregas.
- Calificaciones.
- Boletas.
- Kardex o historial académico.

### Fase 4: Administración

- Pagos y colegiaturas.
- Adeudos.
- Recibos.
- Inventario de uniformes.
- Ventas de uniformes.

### Fase 5: Reportes avanzados

- Dashboards para dirección.
- Reportes estadísticos.
- Exportaciones.
- Indicadores académicos, disciplinarios, administrativos e inventario.

## 9. Requisitos no funcionales iniciales

- Seguridad basada en roles y permisos.
- Registro de auditoría para acciones sensibles.
- Diseño preparado para múltiples ciclos escolares.
- Interfaz responsiva para uso en computadora, tablet o celular.
- Protección de datos personales de alumnos y familias.
- Respaldos de información.
- Validaciones para evitar duplicidad de alumnos, usuarios, pagos o registros críticos.
- Posibilidad de exportar reportes en formatos comunes.
- Arquitectura modular para agregar funciones por etapas.

## 10. Decisiones pendientes

Antes de iniciar el desarrollo técnico conviene confirmar:

- Si los alumnos tendrán cuenta propia desde la primera versión.
- Si se requiere aplicación móvil o solo plataforma web responsiva.
- Qué canales de notificación se usarán al inicio.
- Si los pagos se registrarán manualmente o se integrarán con pasarela de pago.
- Si los comprobantes tendrán validez fiscal o serán solo recibos internos.
- Qué información disciplinaria podrá ver directamente el alumno.
- Qué personal puede validar justificantes y permisos.
- Si dirección podrá editar información o solo consultarla y autorizarla.
- Qué reportes son indispensables para la primera versión.
