# API Testing Portfolio - Manual Testing Suite

## Descripción del Proyecto

Este repositorio contiene una suite completa de casos de prueba manuales para APIs REST desarrollada para demostrar habilidades de QA Testing en servicios backend. Se utilizó JSONPlaceholder como API de prueba para ejecutar testing funcional exhaustivo de diferentes operaciones y escenarios.

## Objetivos Cumplidos

- **Demostrar metodología estructurada** de API testing manual
- **Documentar casos de prueba** para diferentes métodos HTTP
- **Validar operaciones CRUD** completas (Create, Read, Update, Delete)
- **Probar casos negativos** y manejo de errores
- **Generar evidencia completa** de ejecución con Postman
- **Aplicar diferentes técnicas** de testing de APIs REST

## Estructura del Proyecto

```
API-Testing-Portfolio/
├── test-cases/
│   ├── users/              # Casos de gestión de usuarios
│   ├── posts/              # Operaciones CRUD de posts
│   └── validation/         # Casos negativos y validaciones
├── postman-collections/    # Collections de Postman exportadas
├── evidence/              # Screenshots y responses
│   └── screenshots/
└── README.md             # Documentación principal
```

## Suite de Casos de Prueba

### Cobertura Funcional
- **9 casos de prueba ejecutados**
- **3 áreas funcionales cubiertas**
- **Métodos HTTP:** GET, POST, PUT, DELETE
- **Tipos de testing:** Positivo, Negativo, Validación

### Distribución por Área

| Área | Casos | Descripción |
|------|-------|-------------|
| Users | 1 | Consulta de usuarios con paginación |
| Posts | 3 | Operaciones CRUD completas |
| Validation | 5 | Casos negativos y validaciones |

## Casos de Prueba Detallados

### Operaciones CRUD Básicas
- **TC001-API:** GET /users - Lista usuarios con paginación
- **TC002-API:** POST /posts - Crear nuevo post
- **TC003-API:** PUT /posts/1 - Actualizar post existente
- **TC004-API:** DELETE /posts/1 - Eliminar post

### Casos Negativos y Validación
- **TC005-API:** POST con datos inválidos (400 Bad Request)
- **TC006-API:** GET recurso inexistente (404 Not Found)
- **TC007-API:** POST sin Content-Type requerido
- **TC008-API:** GET con parámetros de query
- **TC009-API:** Validación de estructura de response

## Métodos HTTP Probados

| Método | Casos | Propósito |
|--------|-------|-----------|
| GET    | 3     | Consulta de recursos |
| POST   | 3     | Creación de recursos |
| PUT    | 1     | Actualización completa |
| DELETE | 1     | Eliminación de recursos |

## Status Codes Validados

- **200 OK** - Operaciones exitosas
- **201 Created** - Recursos creados
- **400 Bad Request** - Datos inválidos
- **404 Not Found** - Recursos inexistentes
- **415 Unsupported Media Type** - Headers incorrectos

## Metodología Aplicada

### Técnicas de Testing
- **Testing Funcional:** Verificación de operaciones CRUD
- **Testing Negativo:** Validación de manejo de errores
- **Validación de Datos:** Estructura y tipos de response
- **Testing de Headers:** Content-Type y validaciones HTTP

### Documentación Estructurada
- Especificaciones de endpoints claras
- Datos de prueba definidos
- Pasos de ejecución detallados
- Criterios de aceptación específicos
- Evidencia completa con Postman

### Validaciones Implementadas
- Status codes apropiados
- Estructura JSON correcta
- Tipos de datos validados
- Manejo de errores consistente
- Response times aceptables

## Herramientas Utilizadas

- **API de Prueba:** JSONPlaceholder (https://jsonplaceholder.typicode.com/)
- **Cliente API:** Postman v10.x
- **Documentación:** Markdown
- **Control de versiones:** Git/GitHub
- **Evidencia:** Screenshots de requests/responses
- **SO:** Windows 11 Home

## Habilidades Demostradas

### Technical Skills
- Testing manual de APIs REST
- Validación de métodos HTTP (GET, POST, PUT, DELETE)
- Análisis de status codes y responses
- Validación de estructura JSON
- Manejo de headers HTTP
- Testing de casos positivos y negativos

### Methodological Skills
- Diseño de casos de prueba API
- Documentación técnica estructurada
- Validación de requisitos funcionales
- Análisis de casos límite
- Reporte de defectos técnicos

## Métricas del Proyecto

- **Tiempo total:** 2 semanas
- **Casos ejecutados:** 9
- **Métodos HTTP cubiertos:** 4 (GET, POST, PUT, DELETE)
- **Status codes validados:** 5
- **APIs probadas:** JSONPlaceholder
- **Evidencia generada:** 20+ screenshots, 9+ JSON responses

## Casos de Prueba Destacados

### TC002-API - Crear Post
- **Método:** POST con datos válidos
- **Validación:** Status 201, estructura response, datos reflejados
- **Resultado:** Operación CREATE exitosa

### TC005-API - Datos Inválidos
- **Método:** POST con datos incorrectos
- **Validación:** Status 4xx, mensaje de error apropiado
- **Resultado:** Validación de entrada funcionando

### TC006-API - Recurso Inexistente
- **Método:** GET a ID inexistente
- **Validación:** Status 404, manejo de error
- **Resultado:** Error handling apropiado

## Próximos Pasos

### Expansión del Testing
- Casos de autenticación con tokens
- Testing de performance y carga
- Validaciones de seguridad
- Testing automatizado con scripts

### Mejoras Identificadas
- Implementación de data-driven testing
- Casos de prueba para diferentes códigos de error
- Testing de límites de payload
- Validaciones de rate limiting

## Comparación con Testing de UI

Este portfolio complementa las habilidades demostradas en testing de UI al cubrir:
- **Backend vs Frontend:** APIs vs interfaces de usuario
- **Datos vs Visual:** JSON/estructura vs elementos visuales
- **HTTP vs Navegador:** Protocolos vs interacciones de usuario
- **Automatizable:** APIs más fáciles de automatizar que UI

## Contacto

**Karina Hanmse**
- LinkedIn: www.linkedin.com/in/karinahanmse
- GitHub: [\karina-hanmse GitHub\](https://github.com/karina-hanmse/API-Testing-Portfolio)
- Email:karinahanmse@gmail.com

---

*Este portfolio demuestra competencias sólidas en testing manual de APIs REST y capacidad para validar servicios backend. Desarrollado como complemento al portfolio de testing de UI para mostrar habilidades integrales de QA Testing.*