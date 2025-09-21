# TC001-API - Get lista de usuarios

## 📋 Información General
- **ID:** TC001-API
- **Módulo:** User Management API
- **Prioridad:** Alta
- **Tipo:** API - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 19/09/2025

## 🎯 Objetivo
Verificar que el endpoint GET /api/users retorna correctamente la lista de usuarios con paginación y estructura de datos apropiada.

## 📡 Especificaciones del Endpoint
- **URL:** `https://reqres.in/api/users?page=2`
- **Método:** GET
- **Headers:** Ninguno requerido
- **Body:** N/A (método GET)
- **Documentación:** https://reqres.in/

## 🧪 Datos de Prueba
| Parámetro | Valor | Descripción |
|-----------|-------|-------------|
| page      | 2     | Página solicitada |
| per_page  | 6     | Usuarios por página (default) |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Crear nueva collection "ReqRes API Testing"
- Agregar nuevo request "Get Users Page 2"
- Método: GET
- URL: https://reqres.in/api/users?page=2

### Paso 2: Enviar Request
**Acción:** Hacer clic en "Send" en Postman

### Paso 3: Verificar Response Status
**Resultado Esperado:** Status Code 200 OK

### Paso 4: Validar Structure del Response
**Resultado Esperado:**
```json
{
  "page": 2,
  "per_page": 6,
  "total": 12,
  "total_pages": 2,
  "data": [
    {
      "id": number,
      "email": "string",
      "first_name": "string",
      "last_name": "string",
      "avatar": "string (URL)"
    }
  ],
  "support": {
    "url": "string",
    "text": "string"
  }
}
```

### Paso 5: Validar Contenido de Datos
**Resultado Esperado:**
- Array "data" contiene usuarios válidos
- Cada usuario tiene id, email, first_name, last_name, avatar
- Información de paginación coherente
- Campo "support" presente

## ✅ Criterios de Aceptación
- [ ] Status Code es 200
- [ ] Response time < 2 segundos
- [ ] Campo "page" = 2
- [ ] Campo "per_page" presente
- [ ] Array "data" no vacío
- [ ] Cada usuario tiene todos los campos requeridos
- [ ] Emails tienen formato válido
- [ ] URLs de avatares son accesibles
- [ ] Información de paginación es coherente

## 🐛 Posibles Defectos a Observar
- Status code incorrecto (500, 404, etc.)
- Response time excesivo
- Estructura JSON malformada
- Campos faltantes en objetos de usuario
- Información de paginación incorrecta
- Emails con formato inválido
- URLs de avatares rotas

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 19/09/2025
- **Herramienta:** Postman v10.x
- **Estado:** ✅ Pass
- **Response Time:** 380ms

## 📝 Observaciones
- Estructura JSON correcta, todos los campos presentes, paginación funciona apropiadamente

## 🔍 Evidencia de Prueba
- **Screenshot Request:** [postman_request_tc001.png]
- **Screenshot Response:** [postman_response_tc001.png]
- **JSON Response completo:** [response_tc001.json]

## 📈 Validaciones Realizadas
- ✅ Status Code: 200
- ✅ Response Time: 380ms < 2000ms
- ✅ Page: 2
- ✅ Data array length: 6
- ✅ All users have required fields
- ✅ Email format validation
- ✅ Avatar URLs accessible

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-API-001 (Consulta de usuarios con paginación)
- **Historia de usuario:** US-API-001 (Como cliente API quiero obtener lista de usuarios paginada)
- **Documentación:** https://reqres.in/
- **Casos relacionados:** 
  - TC002-API (Get single user)
  - TC003-API (Login endpoint)
  - Futuros casos de paginación

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 19/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 19/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 19/09/2025
**Revisado por:** [Karina Hanmse]