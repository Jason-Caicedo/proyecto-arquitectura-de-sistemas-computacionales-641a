# Requerimientos no funcionales

> Nota: Los siguientes requisitos son provisionales y podran ajustarse cuando se defina el sistema del proyecto.

| # | Atributo | Metrica | Umbral | Condicion de carga | Verificacion | Consecuencia si no se cumple |
|---|---|---|---|---|---|---|
| 1 | Rendimiento | p95 de latencia | menor a 400 ms | 200 usuarios concurrentes | Prueba de carga | La respuesta del sistema se considera demasiado lenta |
| 2 | Disponibilidad | Porcentaje de disponibilidad | mayor o igual a 99 % | Operacion durante un mes | Monitoreo del servicio | Los usuarios no podran utilizar el sistema durante las interrupciones |
| 3 | Seguridad | Intentos de acceso no autorizado registrados | 100 % de los intentos deben quedar registrados y auditados | Intentos de acceso durante la operacion | Revision de registros de seguridad | Se pierde trazabilidad sobre posibles accesos no autorizados |
| 4 | Usabilidad | Tiempo promedio para completar una operacion | menor a 2 minutos | Usuario realizando una operacion habitual | Prueba con usuarios | El usuario puede presentar dificultades para utilizar el sistema |

## Escenarios completos

### Escenario 1
- Fuente: Usuario del sistema
- Estimulo: Realiza una solicitud al sistema
- Artefacto: Aplicacion
- Entorno: Sistema en operacion
- Respuesta: El sistema procesa y responde a la solicitud
- Medida: p95 de latencia menor a 400 ms