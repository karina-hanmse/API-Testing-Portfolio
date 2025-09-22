# TC008-API - GET con parámetros de query

## 📋 Información General
- **ID:** TC008-API
- **Módulo:** Posts Management API
- **Prioridad:** Media
- **Tipo:** API - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 21/09/2025

## 🎯 Objetivo
Verificar que el endpoint GET /posts maneja correctamente parámetros de query para filtrar resultados según userId específico.

## 📡 Especificaciones del Endpoint
- **URL:** `https://jsonplaceholder.typicode.com/posts?userId=1`
- **Método:** GET
- **Headers:** Ninguno requerido
- **Body:** N/A (método GET)
- **Documentación:** https://jsonplaceholder.typicode.com/

## 🧪 Datos de Prueba
| Parámetro | Valor | Descripción |
|-----------|-------|-------------|
| userId    | 1     | ID de usuario para filtrar posts |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Agregar nuevo request a collection
- Nombre: "Get Posts by User ID"
- Método: GET
- URL: https://jsonplaceholder.typicode.com/posts?userId=1

### Paso 2: Enviar Request
**Acción:** Hacer clic en "Send" en Postman

### Paso 3: Verificar Response Status
**Resultado Esperado:** Status Code 200 (OK)

### Paso 4: Validar Structure del Response
**Resultado Esperado:**
```json
[
  {
    "userId": 1,
    "id": number,
    "title": "string",
    "body": "string"
  }
]
```

### Paso 5: Validar Filtrado de Datos
**Resultado Esperado:**
- Todos los posts retornados tienen userId = 1
- Array no está vacío
- Estructura de cada post es correcta
- Solo posts del usuario especificado

### Paso 6: Verificar cantidad de resultados
**Resultado Esperado:**
- Se retornan múltiples posts (no solo uno)
- Cantidad razonable de resultados
- Filtrado funcionando correctamente

## ✅ Criterios de Aceptación
- [ ] Status Code es 200 (OK)
- [ ] Response time < 2 segundos
- [ ] Response es array de posts
- [ ] Todos los posts tienen userId = 1
- [ ] Estructura de cada post es correcta
- [ ] Array contiene múltiples elementos
- [ ] Filtrado por userId funciona correctamente

## 🐛 Posibles Defectos a Observar
- Status code incorrecto
- Response time excesivo
- Posts con userId diferente a 1
- Array vacío cuando debería tener resultados
- Estructura de posts incorrecta
- Parámetro de query ignorado
- Error en lugar de resultados filtrados

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 22/09/2025
- **Herramienta:** Postman v10.x
- **Estado:** ✅ Pass
- **Response Time:** 196 ms

## 📝 Observaciones
- Todos los post tienen userId=1.
- Estructura del array acorde a lo especificado.
- Contiene multiples elementos pertenecientes al userId = 1.

## 🔍 Evidencia de Prueba
- **Screenshot Request:** evidence/postman_request_tc008.png
- **Screenshot Response:** evidence/postman_response_tc008.png
- **JSON Response completo:** [response_tc008.json]

## 📈 Validaciones Realizadas
- ✅ Status Code: 200
- ✅ Response Time: 196 ms < 2000ms
- ✅ Array of posts returned: Sí
- ✅ All posts userId = 1: Sí
- ✅ Multiple results: Sí
- ✅ Query filtering working: Sí

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-GET-003 (Filtrado por parámetros de query)
- **Historia de usuario:** US-GET-003 (Como usuario quiero filtrar posts por usuario específico)
- **Documentación:** https://jsonplaceholder.typicode.com/
- **Casos relacionados:** 
  - TC001-API (Get usuarios con paginación)
  - TC006-API (GET recurso inexistente)
  - TC009-API (Validación de estructura)

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 21/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 22/09/2025 | Ejecución  del caso | Karina Hanmse |

---
**Última actualización:** 22/09/2025
**Revisado por:** [Karina Hanmse]