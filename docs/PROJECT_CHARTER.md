# 📋 Project Charter — UPeU Events

**Versión:** 2.0 (mk2)
**Curso:** Ingeniería de Software II — Ciclo VII, Grupo 1
**Universidad:** Universidad Peruana Unión
**Profesor responsable:** Ing. Ruben Roque Sucari
**Fecha:** Marzo 2026

---

## 📑 Tabla de Contenidos

- [1. Información General](#1-información-general)
- [2. Caso de Negocio](#2-caso-de-negocio)
- [3. Objetivos](#3-objetivos)
- [4. Equipo del Proyecto](#4-equipo-del-proyecto)
- [5. Requerimientos Arquitecturales](#5-requerimientos-arquitecturales)
- [6. Historias de Usuario](#6-historias-de-usuario)
- [7. Evaluación de Calidad (ISO/IEC 25010)](#7-evaluación-de-calidad-isoiec-25010)
- [8. Ciclo de Vida del Software (NTP-ISO/IEC 12207)](#8-ciclo-de-vida-del-software-ntp-isoiec-12207)
- [9. Gestión del Proyecto](#9-gestión-del-proyecto)
- [10. Trabajo Colaborativo con GitHub](#10-trabajo-colaborativo-con-github)
- [11. Calidad del Software](#11-calidad-del-software)
- [12. Mejoras Implementadas](#12-mejoras-implementadas)
- [13. Conclusiones](#13-conclusiones)
- [14. Anexos](#14-anexos)
- [15. Registro de Versiones](#15-registro-de-versiones)

---

## 1. Información General

| Campo | Detalle |
| --- | --- |
| **Startup** | Shaka |
| **Producto** | UPeU Events |
| **Rubro** | Desarrollo de software, transformación digital |
| **Repositorio** | [github.com/Jhemder/AppEventsUPeU](https://github.com/Jhemder/AppEventsUPeU.git) |

**Descripción del startup:** Shaka es un equipo de estudiantes de Ingeniería de Sistemas que desarrolla soluciones de software como parte de su formación académica, aplicando análisis, diseño y desarrollo de sistemas para resolver problemas reales.

**Descripción del producto:** UPeU Events es un sistema de gestión de eventos orientado a mejorar el control de asistencia, el registro de calificaciones y la generación de reportes en eventos académicos. Permite registrar asistencia mediante códigos QR, gestionar evaluaciones de jurados y visualizar resultados en tiempo real, además de exportar reportes en PDF y Excel.

---

## 2. Caso de Negocio

En el contexto académico, la gestión de eventos (concursos, exposiciones, jornadas científicas) suele realizarse de forma manual o con herramientas poco eficientes, lo que genera errores en el registro de asistencia, demoras en la evaluación de participantes y dificultad para obtener resultados confiables.

**UPeU Events** automatiza estos procesos clave:

- ✅ Registro de asistencia mediante códigos QR
- ✅ Gestión de calificaciones por jurados
- ✅ Consulta de resultados en tiempo real
- ✅ Generación automática de reportes

### Funcionalidades principales
- Inicio de sesión de usuarios
- Control de asistencia mediante QR
- Registro de calificaciones
- Consulta de resultados
- Ranking de participantes
- Exportación de reportes (PDF y Excel)

### Modelamiento del proceso (BPMN)
- **AS-IS:** proceso actual, manual y propenso a errores.
- **TO-BE:** el administrador gestiona eventos, registra estudiantes, define criterios de evaluación y asigna jurados desde una plataforma única. El sistema valida la asistencia vía QR en tiempo real, los jurados califican según criterios definidos, y el sistema consolida resultados, rankings y reportes automáticamente.

> 📌 *Insertar diagramas BPMN AS-IS / TO-BE como imágenes en `/docs/img/`.*

---

## 3. Objetivos

### Objetivo general
Desarrollar un sistema de información que permita gestionar jornadas científicas mediante el registro automatizado de asistencia, la evaluación de ponentes, la generación de resultados en tiempo real y la elaboración de reportes digitales, optimizando la eficiencia y reduciendo errores en los procesos.

### Objetivos específicos
- Automatizar el registro de asistencia mediante códigos QR.
- Implementar un módulo de evaluación para jurados.
- Registrar y gestionar estudiantes dentro del sistema.
- Generar resultados y rankings automáticamente.
- Permitir la visualización de reportes en tiempo real.
- Exportar reportes en formatos PDF y Excel.
- Garantizar la seguridad mediante autenticación de usuarios.
- Facilitar la gestión de eventos, jurados y grupos.

---

## 4. Equipo del Proyecto

| Integrante | Código | Rol |
| --- | --- | --- |
| Howard Lemuel Coila Alberto | 202312709 | Líder de proyecto |
| Kevin Jherson Abarca Huayta | 202311896 | Desarrollador — QR, Firebase y asistencia |
| Rossel Teofilo Turpo Maza | 202312744 | Reportes, certificados y rúbricas |

### Perfiles del equipo

| Rol | Descripción |
| --- | --- |
| Líder de proyecto | Coordina el desarrollo y asegura el cumplimiento de objetivos. |
| Desarrollador | Desarrolla el sistema y programa las funcionalidades. |
| Analista | Analiza requerimientos y define funcionalidades. |
| Diseñador UX/UI | Diseña la interfaz para mejorar la experiencia del usuario. |

---

## 5. Requerimientos Arquitecturales

El sistema se desarrolla bajo una **arquitectura cliente-servidor**, con acceso desde dispositivos móviles y web.

| Aspecto | Descripción |
| --- | --- |
| **Escalabilidad** | Soporte para múltiples eventos y usuarios concurrentes |
| **Seguridad** | Control de acceso mediante autenticación de usuarios |
| **Disponibilidad** | Acceso en tiempo real a la información |
| **Interoperabilidad** | Exportación de datos en formatos PDF y Excel |
| **Mantenibilidad** | Código estructurado y modular |

---

## 6. Historias de Usuario

| ID | Historia de Usuario | Prioridad | Criterios de Aceptación |
| --- | --- | --- | --- |
| HU01 | Como administrador, quiero crear eventos para gestionar jornadas científicas. | Alta | Crear, editar y eliminar eventos |
| HU02 | Como administrador, quiero registrar estudiantes para gestionar su participación. | Alta | Registro correcto y listado |
| HU03 | Como asistente, quiero generar códigos QR para registrar asistencia. | Alta | Generación de QR por evento |
| HU04 | Como estudiante, quiero escanear QR para registrar mi asistencia. | Alta | Registro automático y validado |
| HU05 | Como sistema, quiero validar códigos QR para evitar duplicidad. | Alta | Validación única por usuario |
| HU06 | Como jurado, quiero evaluar grupos asignados para calificar ponentes. | Alta | Registro de evaluación por criterios |
| HU07 | Como sistema, quiero almacenar calificaciones para generar resultados. | Alta | Guardado correcto de datos |
| HU08 | Como administrador, quiero visualizar reportes para analizar resultados. | Media | Reportes por evento |
| HU09 | Como administrador, quiero publicar ganadores para mostrar resultados finales. | Media | Selección y visualización |
| HU10 | Como usuario, quiero iniciar sesión para acceder de forma segura. | Alta | Validación de credenciales |

---

## 7. Evaluación de Calidad (ISO/IEC 25010)

La evaluación se realizó con **SonarCloud**, analizando el código fuente del repositorio según el modelo de calidad ISO/IEC 25010.

| Característica | Métrica | Resultado | Objetivo |
| --- | --- | --- | --- |
| Mantenibilidad | Code Smells | 12 | ≤ 5 |
| Confiabilidad | Bugs | 0 | 0 |
| Seguridad | Vulnerabilidades | 1 | 0 |
| Seguridad | Severidad | Blocker | 0 |

### 7.1 Mantenibilidad
- **Code Smells:** 12
- **Maintainability Rating:** A

El sistema presenta una estructura de código adecuada, con oportunidades de mejora en buenas prácticas de desarrollo.

### 7.2 Confiabilidad
- **Bugs detectados:** 0
- **Reliability Rating:** A

No se presentan errores funcionales, lo que garantiza un comportamiento estable.

### 7.3 Seguridad
- **Vulnerabilidades:** 1
- **Severidad:** Blocker

Se identificó exposición de credenciales en el código fuente, representando un riesgo crítico.

#### Acción correctiva (ISO/IEC 12207)

**Antes:**
```properties
spring.datasource.username=postgres
spring.datasource.password=password
```

**Después (uso de variables de entorno):**
```properties
spring.datasource.username=${DB_USERNAME}
spring.datasource.password=${DB_PASSWORD}
```

---

## 8. Ciclo de Vida del Software (NTP-ISO/IEC 12207)

### Proceso principal
Se aplica el **proceso de desarrollo de software**: análisis de requisitos, diseño, implementación, pruebas e integración, orientado a una **aplicación móvil para la UPeU** destinada a la gestión de Jornadas Científicas (inscripción, difusión de cronograma y control de asistencia).

### Procesos de apoyo

**Verificación** — pruebas unitarias y funcionales sobre:
- Registro e inicio de sesión de usuarios
- Inscripción a jornadas científicas
- Visualización de cronogramas y ponencias
- Generación y lectura de códigos QR para asistencia
- Notificaciones y recordatorios del evento

**Validación** — pruebas con usuarios reales (estudiantes, docentes, organizadores) para confirmar usabilidad, rapidez y confiabilidad.

**Documentación:**
- Manual de usuario (participantes y organizadores)
- Manual técnico del sistema
- Evidencias de pruebas realizadas
- Guía de uso del módulo de asistencia por QR

### Proceso organizacional
Se aplica **mejora continua**: identificación de fallos, retroalimentación de usuarios y análisis de resultados para mejorar rendimiento, usabilidad y seguridad en futuros eventos.

### Métricas del proceso
- Número de defectos encontrados durante pruebas y uso real
- Tiempo promedio de inscripción de un participante en la app
- Tiempo promedio de registro de asistencia mediante QR
- Disponibilidad del sistema durante el evento
- Nivel de satisfacción del usuario (encuestas post-evento)
- Tiempo de registro de eventos
- Precisión en cálculos de resultados

---

## 9. Gestión del Proyecto

### 9.1 Metodología Scrum

El desarrollo se organizó en **Sprints** incrementales, facilitando la distribución de tareas, el seguimiento del avance y la colaboración del equipo.

| Sprint | Enfoque | Entregables |
| --- | --- | --- |
| Sprint 1 | Autenticación y Usuarios | Inicio de sesión, gestión de usuarios, control de acceso por roles |
| Sprint 2 | Gestión de Eventos | Creación/edición de eventos, registro de participantes |
| Sprint 3 | Control de Asistencia QR | Generación de QR, registro y validación de asistencia |
| Sprint 4 | Evaluación y Reportes | Rúbricas de evaluación, certificados, reportes PDF/Excel |

El **Product Backlog** contiene las historias de usuario que representan las funcionalidades requeridas por los distintos actores, priorizadas para cada Sprint.

### 9.2 Aplicación de CMMI

#### Technical Solution (TS)
- **Stack principal:** Flutter y Dart (Android, iOS, Web)
- **Backend as a Service:** Firebase
  - Firebase Authentication
  - Cloud Firestore
  - Firebase Storage
  - Firebase Hosting (si aplica)
- **Roles de la arquitectura:** Administrador, Administrador de Carrera, Jurados, Asistentes, Usuarios

**Evidencias TS:** historias de usuario, diseño de pantallas, implementación de funcionalidades, subtareas técnicas en Jira.

#### Verification (VER)

**Casos de prueba ejecutados:**
- Test Login
- Test Registro de Eventos
- Test Inscripción de Participantes
- Test QR
- Test Evaluación
- Test Certificados
- Test Reportes

**Resultados:**

| Funcionalidad | Resultado |
| --- | --- |
| Login | ✅ Correcto |
| Registro de Eventos | ✅ Correcto |
| Inscripciones | ✅ Correcto |
| QR | ✅ Correcto |
| Evaluaciones | ✅ Correcto |
| Certificados | ✅ Correcto |
| Reportes | ✅ Correcto |

#### Integrated Project Management (IP)

Gestión integrada mediante **Jira** y **GitHub** para asignación de tareas, control de versiones y seguimiento del avance.

| Integrante | Responsabilidades |
| --- | --- |
| Kevin Jherson | QR, Firebase y asistencia |
| Howard Lemuel | Gestión de eventos |
| Rossel Teofilo | Reportes, certificados y rúbricas |

> 📌 *Insertar capturas del tablero Scrum y de tareas asignadas en `/docs/img/`.*

---

## 10. Trabajo Colaborativo con GitHub

### 10.1 Gestión de ramas
Se implementó una estrategia basada en ramas para la incorporación controlada de cambios al proyecto principal.

### 10.2 Pull Requests
Se realizaron Pull Requests para integrar nuevas funcionalidades al repositorio principal.

### 10.3 Revisiones y aprobaciones
Se realizaron revisiones de código entre los integrantes antes de fusionar cambios a la rama principal.

**Repositorio:** [github.com/Jhemder/AppEventsUPeU](https://github.com/Jhemder/AppEventsUPeU.git)

---

## 11. Calidad del Software

### 11.1 SonarCloud
Se utilizó SonarCloud para el análisis estático del código fuente, identificando problemas de calidad, mantenibilidad y cobertura de pruebas.

**Métricas evaluadas:**
- Coverage
- Bugs
- Vulnerabilities
- Code Smells
- Security Hotspots

### 11.2 Cobertura de pruebas
Evaluada con **Flutter Test** y **LCOV**.

```bash
flutter test --coverage
```

---

## 12. Mejoras Implementadas

### 12.1 Eliminado lógico
Se implementó el mecanismo de eliminado lógico (*soft delete*) para preservar la integridad histórica de la información almacenada en Firestore, mediante un atributo de control que indica si un registro está activo o eliminado.

**Aplicado en:**
- Eventos
- Participantes
- Usuarios
- Evaluaciones

---

## 13. Conclusiones

- Se aplicó **Scrum** para la gestión del proyecto.
- Se implementaron prácticas **CMMI** en las áreas TS, VER e IP.
- Se utilizó **GitHub** para trabajo colaborativo.
- Se aplicaron herramientas de calidad como **SonarCloud** y **Snyk**.
- El sistema **UPeU Events** cumple los requisitos funcionales establecidos para la gestión de eventos académicos.

---

## 14. Anexos

### Anexo A — Evidencias de Jira
- Product Backlog del proyecto
- Historias de usuario registradas
- Sprint Backlog de cada iteración
- Asignación de tareas y subtareas
- Seguimiento del avance de los Sprints
- Tablero Scrum utilizado durante el desarrollo
- Evidencias de cierre de tareas y cumplimiento de objetivos

### Anexo B — Evidencias de GitHub
- Repositorio principal del proyecto
- Gestión de ramas de desarrollo
- Pull Requests generados por los integrantes
- Revisiones de código realizadas
- Aprobaciones de Pull Requests
- Historial de commits del proyecto

🔗 [github.com/Jhemder/AppEventsUPeU](https://github.com/Jhemder/AppEventsUPeU.git)

### Anexo C — Evidencias de SonarCloud
- Dashboard general del proyecto
- Métricas de calidad
- Reportes de mantenibilidad
- Reportes de seguridad
- Vulnerabilidades detectadas
- Acciones correctivas implementadas

### Anexo D — Evidencias de Cobertura de Pruebas
- Ejecución de pruebas unitarias
- Resultado del comando `flutter test`
- Generación de cobertura mediante LCOV
- Reporte visual de cobertura
- Archivos analizados para cobertura

```bash
flutter test --coverage
```

---

## 15. Registro de Versiones

| Fecha | Versión | Descripción | Autor |
| --- | --- | --- | --- |
| 02/04/2026 | 1.0 | Elaboración inicial: definición del sistema UPeU Events, alcance y actores. | Howard |
| 09/04/2026 | 2.0 | Diseño del sistema, funcionalidades y requerimientos del sistema de eventos. | Rossel |
| 16/04/2026 | 3.0 | Ajustes finales, mejoras en reportes y módulo de calificaciones. | Jherson |
| 30/06/2026 | **4.0 (mk2)** | Migración a formato Markdown para GitHub; reestructuración como Project Charter; consolidación de evidencias y métricas de calidad. | — |

---

*Documento generado a partir del informe final del curso Ingeniería de Software II — Universidad Peruana Unión, Grupo 1 (Shaka / UPeU Events).*
