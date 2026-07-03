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