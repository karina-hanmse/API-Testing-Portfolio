# TC007-API - Request sin Content-Type requerido

## 📋 Información General
- **ID:** TC007-API
- **Módulo:** Posts Management API
- **Prioridad:** Media
- **Tipo:** API - Negativo
- **Autor:** [Karina Hanmse]
- **Fecha:** 21/09/2025

## 🎯 Objetivo
Verificar que el endpoint POST /posts maneja correctamente requests sin el header Content-Type requerido y retorna error apropiado.

## 📡 Especificaciones del Endpoint
- **URL:** `https://jsonplaceholder.typicode.com/posts`
- **Método:** POST
- **Content-Type:** OMITIDO (para provocar error)
- **Documentación:** https://jsonplaceholder.typicode.com/

## 🧪 Datos de Prueba
```json
{
  "title": "Post sin Content-Type header",
  "body": "Contenido para probar validación de headers",
  "userId": 1
}
```

| Configuración | Valor | Descripción |
|---------------|-------|-------------|
| Headers | Sin Content-Type | Header omitido intencionalmente |
| Body | JSON válido | Datos correctos pero sin header apropiado |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Agregar nuevo request a collection
- Nombre: "Create Post - No Content-Type"
- Método: POST
- URL: https://jsonplaceholder.typicode.com/posts

### Paso 2: Omitir Header Content-Type
**Acción:** 
- Headers tab
- NO agregar Content-Type (dejarlo vacío)
- Confirmar que no hay headers de contenido

### Paso 3: Configurar Body con datos válidos
**Acción:**
- Body tab
- Seleccionar "raw"
- Seleccionar "JSON" del dropdown
- Ingresar datos de prueba válidos

### Paso 4: Enviar Request
**Acción:** Hacer clic en "Send" en Postman

### Paso 5: Verificar Response Status
**Resultado Esperado:** Status Code 400 (Bad Request) o 415 (Unsupported Media Type)

### Paso 6: Validar Response de Error
**Resultado Esperado:**
- Mensaje de error relacionado con Content-Type
- Indicación de header faltante o incorrecto
- No se debe crear el post

## ✅ Criterios de Aceptación
- [ ] Status Code es 400 o 415
- [ ] Response contiene mensaje de error sobre Content-Type
- [ ] No se crea recurso sin header apropiado
- [ ] Error es claro y descriptivo
- [ ] Response time < 2 segundos

## 🐛 Posibles Defectos a Observar
- Sistema acepta request sin Content-Type (status 201)
- Mensaje de error confuso
- Status code incorrecto (500)
- Se crea recurso sin validar headers
- Response time excesivo
- Error genérico sin mencionar Content-Type

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** [21/09/2025]
- **Herramienta:** Postman v10.x
- **Estado:** ⏳ Pendiente
- **Response Time:** [X ms]

## 📝 Observaciones
[Completar después de la ejecución]

## 🔍 Evidencia de Prueba
- **Screenshot Request Headers:** [postman_headers_tc007.png]
- **Screenshot Request Body:** [postman_body_tc007.png]
- **Screenshot Response:** [postman_response_tc007.png]
- **Error response completo:** [response_tc007.json]

## 📈 Validaciones Realizadas
- [ ] Status Code: 400/415
- [ ] Response Time: [X ms] < 2000ms
- [ ] Content-Type error mentioned: [Yes/No]
- [ ] No resource created: [Yes/No]
- [ ] Error message clear: [Yes/No]

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-POST-005 (Validación de headers requeridos)
- **Requisito seguridad:** REQ-SEC-003 (Validación de Content-Type)
- **Historia de usuario:** US-POST-005 (Como sistema debo validar headers HTTP requeridos)
- **Documentación:** https://jsonplaceholder.typicode.com/
- **Casos relacionados:** 
  - TC002-API (POST con headers correctos)
  - TC005-API (POST con datos inválidos)
  - TC006-API (GET recurso inexistente)

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 21/09/2025 | Creación inicial del caso | Karina Hanmse |

---
**Última actualización:** 21/09/2025
**Revisado por:** [Karina Hanmse]