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