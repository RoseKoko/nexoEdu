# nexoEdu

Plataforma web de gestión escolar para una preparatoria. Centraliza la información de alumnos, padres o tutores, docentes, asistencia y conducta, con acceso por roles y bitácora de acciones sensibles.

Proyecto integrador de la materia **Gestión de Proyectos de Software**, Instituto Tecnológico de Tijuana (TecNM).
Docente: Mtra. María Guadalupe Rodríguez López · Periodo: 23 de septiembre al 25 de noviembre de 2026.

> **Estado actual:** Etapa I — Gestión de calidad. El repositorio contiene la documentación del proyecto; el código se integrará a partir del Sprint 1.

---

## Integrantes

| Integrante | Rol |
| --- | --- |
| Stephanie Ariana Medrano Vargas | Líder del proyecto, desarrollo, diseño de interfaz |
| Dylan Alexis Padilla | Análisis y documentación, base de datos |
| Ricardo Alejandro Pineda Gómez | Pruebas y calidad, desarrollo |

---

## Alcance de la primera versión

La primera versión corresponde a la **Fase 1 — Base operativa** del roadmap:

- Inicio de sesión único con control de acceso por roles (RBAC).
- Gestión de usuarios y roles (un usuario puede tener varios roles).
- Ciclo escolar, grados y grupos.
- Registro de alumnos, padres/tutores y docentes.
- Registro y consulta de asistencias, faltas y retardos (prefectura).
- Reportes de conducta con evidencias (docentes y prefectura).
- Consulta de asistencia y conducta para padres/tutores.
- Bitácora de acciones sensibles.

**Fuera del alcance de esta versión:** cuentas de alumno, notificaciones, justificantes, permisos de salida, calendario, calificaciones, pagos, inventario de uniformes y dashboards. Están contemplados como fases futuras del sistema.

---

## Tecnologías

| Categoría | Tecnología |
| --- | --- |
| Lenguajes | JavaScript y Python (reparto entre frontend y backend por definir) |
| Framework | Por definir |
| Frontend | Plantillas del framework (HTML, CSS y JavaScript) |
| Base de datos | Firebase (Cloud Firestore) |
| Almacenamiento de evidencias | Por definir |
| Control de versiones | Git y GitHub |
| Gestión del proyecto | GitHub Projects |
| Diagramas y prototipos | draw.io |

Plataforma: aplicación web responsiva (computadora, tablet y celular).

---

## Estructura del repositorio

```
nexoEdu/
├── docs/                         Documentación del proyecto
│   ├── requisitos-y-roles.md     Punto de entrada a la documentación
│   ├── 00-resumen-ejecutivo.md
│   ├── 01-requisitos-funcionales.md
│   ├── 02-roles-y-permisos.md
│   ├── 03-entidades-y-reglas.md
│   ├── 04-roadmap.md
│   └── 05-decisiones-pendientes.md
└── README.md
```

Las carpetas de código fuente, base de datos, pruebas y evidencias se agregarán conforme avance el proyecto.

---

## Requisitos previos

Por definir cuando se elija el framework. Se espera incluir:

- Versión de Node.js y/o Python requerida.
- Proyecto de Firebase configurado.
- Navegador web actualizado.

## Instalación

Por definir.

```bash
git clone https://github.com/StephAmv/nexoEdu.git
cd nexoEdu
# Pasos de instalación de dependencias: por definir
```

## Ejecución

Por definir.

## Credenciales de prueba

Todos los datos del sistema son ficticios. Las credenciales se publicarán aquí cuando el sistema esté funcionando.

| Rol | Usuario | Contraseña |
| --- | --- | --- |
| Administrador del sistema | Por definir | Por definir |
| Dirección | Por definir | Por definir |
| Prefectura | Por definir | Por definir |
| Docente | Por definir | Por definir |
| Padre/tutor | Por definir | Por definir |

---

## Forma de trabajo

- **Metodología:** Scrum adaptado a tres integrantes, con sprints de dos semanas.
- **Seguimiento:** tablero en GitHub Projects.
- **Revisión de código:** todo cambio se integra mediante pull request revisado por un integrante distinto al autor.
- **Errores:** se registran en la bitácora de pruebas y su corrección hace referencia al ID del error en el commit.
- **Control de cambios:** ningún cambio de alcance se implementa sin registro y decisión del equipo.
