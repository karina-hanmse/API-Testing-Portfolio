# TC005-API - POST con datos inválidos

## 📋 Información General
- **ID:** TC005-API
- **Módulo:** Posts Management API
- **Prioridad:** Alta
- **Tipo:** API - Negativo
- **Autor:** Karina Hanmse
- **Fecha:** 21/09/2025

## 🎯 Objetivo
Verificar que el endpoint POST /posts maneja correctamente datos inválidos o malformados y retorna errores apropiados.

## 📡 Especificaciones del Endpoint
- **URL:** `https://jsonplaceholder.typicode.com/posts`
- **Método:** POST
- **Content-Type:** application/json
- **Documentación:** https://jsonplaceholder.typicode.com/

## 🧪 Datos de Prueba (Inválidos)
```json
{
  "title": "",
  "body": "",
  "userId": "invalid_user_id"
}
```

| Campo | Valor | Descripción |
|-------|-------|-------------|
| title | ""    | Campo vacío (inválido) |
| body  | ""    | Campo vacío (inválido) |
| userId | "invalid_user_id" | String en lugar de number |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Agregar nuevo request a collection
- Nombre: "Create Post - Invalid Data"
- Método: POST
- URL: https://jsonplaceholder.typicode.com/posts

### Paso 2: Configurar Headers
**Acción:** 
- Headers tab
- Key: Content-Type
- Value: application/json

### Paso 3: Configurar Body con datos inválidos
**Acción:**
- Body tab
- Seleccionar "raw"
- Seleccionar "JSON" del dropdown
- Ingresar datos de prueba inválidos

### Paso 4: Enviar Request
**Acción:** Hacer clic en "Send" en Postman

### Paso 5: Verificar Response Status
**Resultado Esperado:** Status Code 400 (Bad Request) o similar error

### Paso 6: Validar Response de Error
**Resultado Esperado:**
- Mensaje de error descriptivo
- Indicación de qué campos son inválidos
- No se debe crear el post

## ✅ Criterios de Aceptación
- [ ] Status Code es 4xx (400, 422, etc.)
- [ ] Response contiene mensaje de error
- [ ] Error indica problemas específicos con los datos
- [ ] No se crea recurso con datos inválidos
- [ ] Response time < 2 segundos

## 🐛 Posibles Defectos a Observar
- Sistema acepta datos inválidos (status 201)
- Mensaje de error confuso o ausente
- Status code incorrecto (500 en lugar de 400)
- Se crea recurso con datos inválidos
- Response time excesivo
- Error genérico sin detalles específicos

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 21/09/2025
- **Herramienta:** Postman v10.x
- **Estado:** ❌ Fail
- **Response Time:** [X ms]

## 📝 Observaciones
- El sistema acepta datos inválidos (Status 201)
- Se crea recurso con datos inválidos

## 🔍 Evidencia de Prueba
- **Screenshot Request:** evidence/postman_request_tc005.png
- **Screenshot Response:** evidence/postman_response_tc005.png
- **Error response completo:** postman-collections/response_tc005.json

## 📈 Validaciones Realizadas
- ❌ Status Code: 4xx
- ✅ Response Time: 352ms < 2000ms
- ❌ Error message present: NO
- ❌ Validation errors specific: NO
- ❌ No resource created: SI

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-POST-004 (Validación de datos de entrada)
- **Requisito seguridad:** REQ-SEC-002 (Rechazo de datos inválidos)
- **Historia de usuario:** US-POST-004 (Como sistema debo rechazar datos inválidos)
- **Documentación:** https://jsonplaceholder.typicode.com/
- **Casos relacionados:** 
  - TC002-API (Crear post con datos válidos)
  - TC006-API (GET recurso inexistente)
  - TC007-API (Request sin Content-Type)

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 21/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 21/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 21/09/2025
**Revisado por:** Karina Hanmse