# Plan de Pruebas - Login

## 1. Identificación
- Proyecto: qa-manual-login
- Aplicación bajo prueba: formulario de login "Acceso Estudiantes" de ITCA (www.itca.com.ar)
- Responsable: Sandra Ibarra, QA Manual Tester
- Versión del documento: 1.0

## 2. Objetivo
Verificar que el inicio de sesión funcione correctamente con datos válidos e inválidos, que los mensajes de error sean claros y que solo los usuarios autenticados accedan al sistema.

## 3. Alcance
**Dentro del alcance**
- Ingreso con credenciales válidas e inválidas.
- Validación de campos obligatorios.
- Mensajes de error.
- Acceso al sistema tras el login y cierre de sesión.

**Fuera del alcance**
- Registro de usuarios y recuperación de contraseña.
- Pruebas de rendimiento y carga.
- Pruebas de seguridad intrusivas sobre el sitio real. El caso TC-LOGIN-012 (inyección SQL) se documenta pero no se ejecuta sin autorización de la institución.

## 4. Estrategia de pruebas
| Tipo | Descripción |
| --- | --- |
| Funcional | Verifica el flujo principal de ingreso |
| Negativa | Datos incorrectos o inexistentes |
| Validación | Campos vacíos, espacios, mayúsculas y minúsculas |
| Seguridad básica | Contraseña enmascarada |
| Regresión | Repetición de casos tras la corrección de un defecto |

Técnicas: partición de equivalencias y análisis de valores límite sobre los campos usuario y contraseña. Ejecución manual con registro de evidencias.

## 5. Entorno de pruebas
- Navegador: [indicar navegador y versión usados]
- Sistema operativo: [indicar]
- Datos de prueba: ver hoja "Casos de prueba" del Excel.

## 6. Criterios
**Entrada:** acceso al sitio disponible, casos de prueba diseñados y datos de prueba definidos.

**Salida:** todos los casos ejecutados, defectos registrados con su severidad y resumen de resultados completo.

## 7. Gestión de defectos
Cada defecto se registra en la hoja "Reporte de bugs" (o con la plantilla de `04-Reporte-de-Bugs/`) con título, pasos para reproducir, resultado esperado, resultado obtenido, severidad, prioridad y evidencia.

| Severidad | Criterio |
| --- | --- |
| Crítica | Impide el acceso o compromete la seguridad |
| Alta | Falla una función principal sin alternativa |
| Media | Falla una función con alternativa |
| Baja | Problema estético o de texto |

## 8. Riesgos
- Disponibilidad del sitio durante la ejecución.
- Ausencia de un usuario válido para los casos de acceso exitoso.
- Cambios en el sitio que alteren el resultado de las pruebas.

## 9. Entregables
- Plan de pruebas (este documento).
- Casos de prueba y resumen de ejecución (Excel).
- Reportes de bugs.
- Evidencias de ejecución (capturas).
