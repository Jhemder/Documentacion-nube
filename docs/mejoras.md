## 12. Mejoras Implementadas

### 12.1 Eliminado lógico
Se implementó el mecanismo de eliminado lógico (*soft delete*) para preservar la integridad histórica de la información almacenada en Firestore, mediante un atributo de control que indica si un registro está activo o eliminado.

**Aplicado en:**
- Eventos
- Participantes
- Usuarios
- Evaluaciones

---