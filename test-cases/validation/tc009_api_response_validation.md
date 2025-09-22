# TC009-API - Validación de estructura de response

## 📋 Información General
- **ID:** TC009-API
- **Módulo:** Posts Management API
- **Prioridad:** Media
- **Tipo:** API - Validación
- **Autor:** [Karina Hanmse]
- **Fecha:** 21/09/2025

## 🎯 Objetivo
Verificar que el endpoint GET /posts/1 retorna la estructura de datos correcta con todos los campos requeridos y tipos de datos apropiados.

## 📡 Especificaciones del Endpoint
- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Método:** GET
- **Headers:** Ninguno requerido
- **Body:** N/A (método GET)
- **Documentación:** https://jsonplaceholder.typicode.com/

## 🧪 Datos de Prueba
| Parámetro | Valor | Descripción |
|-----------|-------|-------------|
| Post ID   | 1     | ID específico para validar estructura |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Agregar nuevo request a collection
- Nombre: "Get Single Post - Structure Validation"
- Método: GET
- URL: https://jsonplaceholder.typicode.com/posts/1

### Paso 2: Enviar Request
**Acción:** Hacer clic en "Send" en Postman

### Paso 3: Verificar Response Status
**Resultado Esperado:** Status Code 200 (OK)

### Paso 4: Validar Estructura Completa del Response
**Resultado Esperado:**
```json
{
  "userId": number,
  "id": number,
  "title": "string",
  "body": "string"
}
```

### Paso 5: Validar Tipos de Datos
**Resultado Esperado:**
- userId: número entero
- id: número entero
- title: string no vacío
- body: string no vacío

### Paso 6: Validar Contenido de Campos
**Resultado Esperado:**
- userId mayor a 0
- id igual a 1 (según URL solicitada)
- title con contenido significativo
- body con contenido significativo

### Paso 7: Verificar Headers del Response
**Resultado Esperado:**
- Content-Type: application/json; charset=utf-8
- Headers estándar HTTP presentes

## ✅ Criterios de Aceptación
- [ ] Status Code es 200 (OK)
- [ ] Response time < 2 segundos
- [ ] Estructura JSON exacta como especificada
- [ ] Todos los campos requeridos presentes
- [ ] Tipos de datos correctos para cada campo
- [ ] Valores de campos son lógicos y válidos
- [ ] No hay campos adicionales inesperados
- [ ] Headers de response apropiados

## 🐛 Posibles Defectos a Observar
- Status code incorrecto
- Response time excesivo
- Campos faltantes en la estructura
- Tipos de datos incorrectos (string en lugar de number)
- Valores nulos o vacíos en campos requeridos
- Campos adicionales no documentados
- Content-Type incorrecto
- Estructura JSON malformada

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 22/09/2025
- **Herramienta:** Postman v10.x
- **Estado:** ✅ Pass
- **Response Time:** 322 ms

## 📝 Observaciones
- Todos los criterios de aceptación son correctos.

## 🔍 Evidencia de Prueba
- **Screenshot Request:** evidence/postman_request_tc009.png
- **Screenshot Response:** evidence/postman_response_tc009.png
- **JSON Response completo:** postman-collections/response_tc009.json

## 📈 Validaciones Realizadas
- ✅ Status Code: 200
- ✅ Response Time: 322 ms < 2000ms
- ✅ All required fields present: Si
- ✅ Data types correct: Si
- ✅ Field values valid: Si
- ✅ No extra fields: Si
- ✅ Headers correct: Si

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-GET-004 (Estructura consistente de response)
- **Requisito técnico:** REQ-TECH-001 (Validación de tipos de datos)
- **Historia de usuario:** US-GET-004 (Como cliente API quiero estructura de datos predecible)
- **Documentación:** https://jsonplaceholder.typicode.com/
- **Casos relacionados:** 
  - TC002-API (POST estructura de response)
  - TC003-API (PUT estructura de response)
  - TC008-API (GET con parámetros)

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 21/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 22/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 22/09/2025
**Revisado por:** [Karina Hanmse]