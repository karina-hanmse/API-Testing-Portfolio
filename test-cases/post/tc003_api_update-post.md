# TC003-API - Actualizar post existente

## 📋 Información General
- **ID:** TC003-API
- **Módulo:** Posts Management API
- **Prioridad:** Alta
- **Tipo:** API - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 20/09/2025

## 🎯 Objetivo
Verificar que el endpoint PUT /posts/1 permite actualizar un post existente correctamente y retorna los datos modificados.

## 📡 Especificaciones del Endpoint
- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Método:** PUT
- **Content-Type:** application/json
- **Documentación:** https://jsonplaceholder.typicode.com/

## 🧪 Datos de Prueba
```json
{
  "id": 1,
  "title": "Post actualizado via API testing",
  "body": "Contenido modificado para validar operación PUT",
  "userId": 1
}
```

| Campo   | Valor | Descripción |
|-------  |-------|-------------|
| id      | 1     | ID del post a actualizar |
| title   | Post actualizado via API testing | Nuevo título |
| body    | Contenido modificado para validar operación PUT | Nuevo contenido |
| userId  |   1   | ID del usuario propietario |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Agregar nuevo request a collection
- Nombre: "Update Post"
- Método: PUT
- URL: https://jsonplaceholder.typicode.com/posts/1

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
- Ingresar datos de prueba actualizados

### Paso 4: Enviar Request
**Acción:** Hacer clic en "Send" en Postman

### Paso 5: Verificar Response Status
**Resultado Esperado:** Status Code 200 (OK)

### Paso 6: Validar Structure del Response
**Resultado Esperado:**
```json
{
  "id": 1,
  "title": "Post actualizado via API testing",
  "body": "Contenido modificado para validar operación PUT",
  "userId": 1
}
```

### Paso 7: Validar Actualización de Datos
**Resultado Esperado:**
- Todos los campos enviados se reflejan en el response
- ID permanece como 1 (no cambia)
- Título y contenido muestran valores actualizados
- UserId se mantiene correctamente

## ✅ Criterios de Aceptación
- [ ] Status Code es 200 (OK)
- [ ] Response time < 2 segundos
- [ ] ID permanece inalterado (1)
- [ ] Campos title y body reflejan nuevos valores
- [ ] UserId se mantiene correcto
- [ ] Content-Type del response es application/json
- [ ] Estructura JSON correcta

## 🐛 Posibles Defectos a Observar
- Status code incorrecto (404, 400, 500)
- Response time excesivo
- ID del post cambiado incorrectamente
- Datos enviados no se reflejan en response
- Campos faltantes en response
- Estructura JSON malformada
- Content-Type incorrecto

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 20/09/2025
- **Herramienta:** Postman v10.x
- **Estado:** ✅ Pass
- **Response Time:** 327 ms

## 📝 Observaciones
- Status Code es  200
- Los datos se procesaron sin modificación
- La estructura JSON es correcta
- El ID se mantuvo como 1

## 🔍 Evidencia de Prueba
- **Screenshot Request Headers:** [postman_headers_tc003.png]
- **Screenshot Request Body:** [postman_body_tc003.png]
- **Screenshot Response:** [postman_response_tc003.png]
- **JSON Response completo:** [response_tc003.json]

## 📈 Validaciones Realizadas
- ✅ Status Code: 200
- ✅ Response Time: 327ms < 2000ms
- ✅ ID preserved: Yes
- ✅ Data updated correctly: Yes
- ✅ Content-Type: application/json
- ✅ Response structure correct: Yes

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-POST-002 (Actualización de posts)
- **Historia de usuario:** US-POST-002 (Como usuario quiero actualizar posts existentes vía API)
- **Documentación:** https://jsonplaceholder.typicode.com/
- **Casos relacionados:** 
  - TC001-API (Get lista de usuarios)
  - TC002-API (Crear nuevo post)
  - TC004-API (Eliminar post)
  - Futuros casos CRUD de posts

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 20/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 20/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 20/09/2025
**Revisado por:** [Karina Hanmse]