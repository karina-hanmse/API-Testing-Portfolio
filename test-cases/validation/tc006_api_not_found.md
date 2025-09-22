# TC006-API - GET recurso inexistente

## 📋 Información General
- **ID:** TC006-API
- **Módulo:** Posts Management API
- **Prioridad:** Media
- **Tipo:** API - Negativo
- **Autor:** [Karina Hanmse]
- **Fecha:** 21/09/2025

## 🎯 Objetivo
Verificar que el endpoint GET /posts/999 maneja correctamente la solicitud de un recurso inexistente y retorna error 404 apropiado.

## 📡 Especificaciones del Endpoint
- **URL:** `https://jsonplaceholder.typicode.com/posts/999`
- **Método:** GET
- **Headers:** Ninguno requerido
- **Body:** N/A (método GET)
- **Documentación:** https://jsonplaceholder.typicode.com/

## 🧪 Datos de Prueba
| Parámetro | Valor | Descripción |
|-----------|-------|-------------|
| Post ID   | 999   | ID inexistente (fuera del rango válido 1-100) |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Agregar nuevo request a collection
- Nombre: "Get Post - Not Found"
- Método: GET
- URL: https://jsonplaceholder.typicode.com/posts/999

### Paso 2: Enviar Request
**Acción:** Hacer clic en "Send" en Postman (sin headers adicionales)

### Paso 3: Verificar Response Status
**Resultado Esperado:** Status Code 404 (Not Found)

### Paso 4: Validar Response Body
**Resultado Esperado:**
- Response body vacío {} o
- Mensaje de error indicando recurso no encontrado
- No debe contener datos de ningún post

### Paso 5: Validar Headers del Response
**Resultado Esperado:**
- Content-Type apropiado
- Headers estándar de error HTTP

## ✅ Criterios de Aceptación
- [ ] Status Code es 404 (Not Found)
- [ ] Response time < 2 segundos
- [ ] Response body apropiado para error 404
- [ ] No se retornan datos de posts existentes
- [ ] Headers de response son consistentes
- [ ] Comportamiento predecible para recursos inexistentes

## 🐛 Posibles Defectos a Observar
- Status code incorrecto (200, 500, etc.)
- Response time excesivo
- Response contiene datos de otro post
- Error 500 en lugar de 404
- Mensaje de error confuso
- Comportamiento inconsistente

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 21/09/2025
- **Herramienta:** Postman v10.x
- **Estado:** ✅ Pass
- **Response Time:** 556 ms

## 📝 Observaciones
- Status code correcto 404 NOT FOUND
- Resultado esperado body vació {}

## 🔍 Evidencia de Prueba
- **Screenshot Request:** evidence/postman_request_tc006.png
- **Screenshot Response:** evidence/postman_response_tc006.png
- **Error response completo:** postman-collections/response_tc006.json

## 📈 Validaciones Realizadas
- ✅ Status Code: 404
- ✅ Response Time: 556ms < 2000ms
- ✅ Error response appropriate: SI
- ✅ No data leaked:SI
- ✅ Headers consistent: SI

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-GET-002 (Manejo de recursos inexistentes)
- **Historia de usuario:** US-GET-002 (Como sistema debo retornar error claro cuando recurso no existe)
- **Documentación:** https://jsonplaceholder.typicode.com/
- **Casos relacionados:** 
  - TC001-API (Get usuarios existentes)
  - TC005-API (POST con datos inválidos)
  - TC007-API (Request sin Content-Type)

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 21/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 21/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 21/09/2025
**Revisado por:** Karina Hanmse