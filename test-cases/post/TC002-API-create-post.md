# TC002-API - Crear nuevo post

## 📋 Información General
- **ID:** TC002-API
- **Módulo:** Posts Management API
- **Prioridad:** Alta
- **Tipo:** API - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 19/09/2025

## 🎯 Objetivo
Verificar que el endpoint POST /posts permite crear un nuevo post correctamente y retorna la estructura de datos esperada con ID asignado.

## 📡 Especificaciones del Endpoint
- **URL:** `https://jsonplaceholder.typicode.com/posts`
- **Método:** POST
- **Content-Type:** application/json
- **Documentación:** https://jsonplaceholder.typicode.com/

## 🧪 Datos de Prueba
```json
{
  "title": "Mi primer post",
  "body": "Contenido de prueba para API testing",
  "userId": 1
}
```

| Campo | Valor | Descripción |
|-------|-------|-------------|
| title | Mi primer post | Título del post a crear |
| body | Contenido de prueba para API testing | Contenido del post |
| userId | 1 | ID del usuario que crea el post |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Agregar nuevo request a collection
- Nombre: "Create Post"
- Método: POST
- URL: https://jsonplaceholder.typicode.com/posts

### Paso 2: Configurar Headers
**Acción:** 
- Headers tab
- Key: Content-Type
- Value: application/json

### Paso 3: Configurar Body
**Acción:**
- Body tab
- Seleccionar "raw"
- Seleccionar "JSON" del dropdown
- Ingresar datos de prueba

### Paso 4: Enviar Request
**Acción:** Hacer clic en "Send" en Postman

### Paso 5: Verificar Response Status
**Resultado Esperado:** Status Code 201 (Created)

### Paso 6: Validar Structure del Response
**Resultado Esperado:**
```json
{
  "id": number,
  "title": "Mi primer post",
  "body": "Contenido de prueba para API testing",
  "userId": 1
}
```

### Paso 7: Validar Datos Creados
**Resultado Esperado:**
- Campo "id" presente y es número
- Campos "title", "body", "userId" coinciden con datos enviados
- Estructura JSON correcta

## ✅ Criterios de Aceptación
- [ ] Status Code es 201 (Created)
- [ ] Response time < 2 segundos
- [ ] Response contiene campo "id" generado automáticamente
- [ ] Datos enviados se reflejan correctamente en response
- [ ] Content-Type del response es application/json
- [ ] ID generado es numérico y mayor a 0

## 🐛 Posibles Defectos a Observar
- Status code incorrecto (400, 500, etc.)
- Response time excesivo
- Campo "id" ausente o no numérico
- Datos del request no se reflejan en response
- Estructura JSON malformada
- Content-Type incorrecto en response

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 19/09/2025
- **Herramienta:** Postman v10.x
- **Estado:** ✅ Pass
- **Response Time:** 339ms

## 📝 Observaciones
- Creación de post correcta
- JSON creado correctamente

## 🔍 Evidencia de Prueba
- **Screenshot Request Headers:** [postman_headers_tc002.png]
- **Screenshot Request Body:** [postman_body_tc002.png]
- **Screenshot Response:** [postman_response_tc002.png]
- **JSON Response completo:** [response_tc002.json]

## 📈 Validaciones Realizadas
- ✅ Status Code: 201
- ✅ Response Time: 339ms < 2000ms
- ✅ ID generated: Sí
- ✅ Data consistency: Válido
- ✅ Content-Type: application/json
- ✅ Response structure correct

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-POST-001 (Creación de posts)
- **Historia de usuario:** US-POST-001 (Como usuario quiero crear posts a través de API)
- **Documentación:** https://jsonplaceholder.typicode.com/
- **Casos relacionados:** 
  - TC001-API (Get lista de usuarios)
  - TC003-API (Get posts existentes)
  - Futuros casos CRUD de posts

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 19/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 19/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 19/09/2025
**Revisado por:** [Karina Hanmse]