# TC004-API - Eliminar post existente

## 📋 Información General
- **ID:** TC004-API
- **Módulo:** Posts Management API
- **Prioridad:** Alta
- **Tipo:** API - Positivo
- **Autor:** [Karina Hanmse]
- **Fecha:** 20/09/2025

## 🎯 Objetivo
Verificar que el endpoint DELETE /posts/1 permite eliminar un post existente correctamente y retorna confirmación de eliminación.

## 📡 Especificaciones del Endpoint
- **URL:** `https://jsonplaceholder.typicode.com/posts/1`
- **Método:** DELETE
- **Headers:** Ninguno requerido específicamente
- **Body:** N/A (método DELETE)
- **Documentación:** https://jsonplaceholder.typicode.com/

## 🧪 Datos de Prueba
| Parámetro | Valor | Descripción |
|-----------|-------|-------------|
| Post ID   | 1     | ID del post a eliminar (en URL) |

## 🔄 Pasos de Ejecución

### Paso 1: Configurar Request en Postman
**Acción:** 
- Agregar nuevo request a collection
- Nombre: "Delete Post"
- Método: DELETE
- URL: https://jsonplaceholder.typicode.com/posts/1

### Paso 2: Verificar configuración
**Acción:** 
- Confirmar que no se requieren headers especiales
- Body debe estar vacío (método DELETE)
- URL contiene el ID del recurso a eliminar

### Paso 3: Enviar Request
**Acción:** Hacer clic en "Send" en Postman

### Paso 4: Verificar Response Status
**Resultado Esperado:** Status Code 200 (OK)

### Paso 5: Validar Response Body
**Resultado Esperado:**
- Response body vacío {} o
- Mensaje de confirmación de eliminación
- No debe contener datos del post eliminado

### Paso 6: Validar Headers del Response
**Resultado Esperado:**
- Content-Type apropiado
- Headers estándar de respuesta HTTP

## ✅ Criterios de Aceptación
- [ ] Status Code es 200 (OK)
- [ ] Response time < 2 segundos
- [ ] Response body confirma eliminación (vacío o mensaje)
- [ ] No se retornan datos del post eliminado
- [ ] Headers de response son apropiados
- [ ] No hay errores en el proceso

## 🐛 Posibles Defectos a Observar
- Status code incorrecto (404, 400, 500)
- Response time excesivo
- Response contiene datos del post (no debería)
- Error al procesar eliminación
- Headers de response incorrectos
- Mensaje de error cuando debería ser exitoso

## 📊 Resultado de Ejecución
- **Ejecutado por:** [Karina Hanmse]
- **Fecha:** 20/09/2025
- **Herramienta:** Postman v10.x
- **Estado:** ✅ Pass
- **Response Time:** 545 ms

## 📝 Observaciones
- Status Code: 200 OK
- Response body: {} (objeto vacío confirma eliminación exitosa)
- Eliminación procesada correctamente según estándares REST
- No se retornaron datos del post eliminado (comportamiento esperado)

## 🔍 Evidencia de Prueba
- **Screenshot Request:** [postman_request_tc004.png]
- **Screenshot Response:** [postman_response_tc004.png]
- **Response body completo:** [response_tc004.json]

## 📈 Validaciones Realizadas
- ✅ Status Code: 200
- ✅ Response Time: 545 ms < 2000ms
- ✅ Deletion confirmed: Yes
- ✅ Response body appropriate: Yes
- ✅ Headers correct: Yes
- ✅ No errors occurred: Yes

## 🔗 Trazabilidad y Referencias
- **Requisito funcional:** REQ-POST-003 (Eliminación de posts)
- **Historia de usuario:** US-POST-003 (Como usuario quiero eliminar posts vía API)
- **Documentación:** https://jsonplaceholder.typicode.com/
- **Casos relacionados:** 
  - TC001-API (Get lista de usuarios)
  - TC002-API (Crear nuevo post)
  - TC003-API (Actualizar post existente)
  - TC005-API (Casos negativos)

## 📋 Historial de Cambios
| Versión | Fecha | Cambio Realizado | Responsable |
|---------|--------|------------------|-------------|
| 1.0 | 20/09/2025 | Creación inicial del caso | Karina Hanmse |
| 1.1 | 20/09/2025 | Ejecución del caso | Karina Hanmse |

---
**Última actualización:** 20/09/2025
**Revisado por:** [Karina Hanmse]