# Estrategia de versiones y validación — CRM Profesional

> **Estado:** estrategia inicial
> **Fecha:** 2026-07-28
> **Fase:** Módulo 1 — Definición del producto
> **Rama actual:** `docs/module-1-product-discovery`
> **Producción autorizada:** no
> **Uso de datos reales autorizado:** no

---

## 1. Propósito

Este documento define cómo CRM Profesional avanzará desde documentación hasta una aplicación de producción sin confundir progreso técnico con validación de producto.

La estrategia busca:

* aprender antes de ampliar;
* mantener versiones pequeñas;
* evitar datos reales prematuros;
* establecer gates verificables;
* permitir retroceder;
* separar demostración, piloto y producción;
* conservar trazabilidad entre evidencia, alcance, especificaciones y código.

---

## 2. Política de ramas

### `main`

Contiene exclusivamente el material del curso.

### `docs/module-1-product-discovery`

Contiene el proyecto CRM Profesional en su fase actual.

### Reglas obligatorias

* no fusionar la rama del CRM hacia `main`;
* no abrir pull requests del CRM hacia `main`;
* no fusionar `main` dentro de la rama del CRM;
* no recuperar los módulos en la rama del CRM;
* verificar la rama antes de cada commit;
* crear copias remotas frecuentes;
* revisar cualquier operación destructiva.

Antes de iniciar implementación se evaluará si la rama debe renombrarse a una línea permanente como `project/crm-profesional`.

Ese cambio no se realizará durante este paso.

---

## 3. Principio de liberación

> Cada etapa debe responder una pregunta distinta.

No se avanza porque “ya escribimos suficiente código”.

Se avanza cuando existe evidencia para responder la pregunta de la etapa.

---

## 4. Etapa 0 — Descubrimiento

### Pregunta

¿Comprendemos suficientemente el problema y sus usuarios?

### Artefactos

* visión;
* plan de investigación;
* alcance;
* estrategia de versiones;
* hipótesis;
* preguntas abiertas.

### Datos

No se recopilan datos operativos dentro del producto.

### Gate de salida

* problema claramente formulado;
* usuarios provisionales identificados;
* hipótesis registradas;
* recorrido central definido;
* no objetivos acordados;
* plan para conseguir evidencia.

### Estado

En progreso.

---

## 5. Etapa 1 — Definición con OpenSpec

### Pregunta

¿Podemos describir el comportamiento deseado de manera inequívoca y verificable?

### Actividades

* crear especificaciones;
* definir escenarios;
* definir criterios de aceptación;
* identificar edge cases;
* establecer restricciones;
* revisar dependencias;
* dividir el trabajo.

### Salidas

* especificaciones aprobadas;
* plan de implementación;
* tareas verificables;
* trazabilidad con `scope.md`.

### Gate de salida

* cada Must Have necesario para el primer recorrido tiene especificación;
* los escenarios incluyen errores y estados vacíos;
* no existen contradicciones conocidas;
* las decisiones abiertas críticas están resueltas;
* existe criterio para comprobar cada comportamiento.

---

## 6. Etapa 2 — Development Preview

### Pregunta

¿Puede el sistema completar el recorrido central mediante el stack real?

### Audiencia

* equipo de desarrollo;
* revisores;
* demostraciones internas.

### Capacidades

* clientes;
* búsqueda;
* interacciones;
* seguimientos;
* vista de trabajo;
* archivo y restauración;
* persistencia;
* validación;
* manejo de errores.

### Datos

Solo ficticios o sintéticos.

### Entorno

* local;
* contenedor aislado;
* entorno de demostración restringido.

### Prohibiciones

* datos reales;
* acceso público;
* promesas de producción;
* tratamiento de información sensible;
* integraciones externas reales.

### Gate de salida

* recorrido crítico completado;
* pruebas principales verdes;
* persistencia verificada;
* instrucciones reproducibles;
* secretos ausentes;
* errores principales manejados;
* revisión técnica realizada.

---

## 7. Etapa 3 — Evaluación con prototipo o Preview

### Pregunta

¿Las personas comprenden el modelo del producto y pueden completar las tareas?

### Métodos

* pruebas moderadas;
* observación;
* entrevistas de seguimiento;
* análisis de errores;
* medición de tareas;
* revisión de terminología.

### Datos

Casos de prueba ficticios.

### Tareas mínimas

1. encontrar un cliente;
2. interpretar su contexto;
3. registrar una interacción;
4. crear un seguimiento;
5. encontrarlo posteriormente;
6. completarlo;
7. archivar y restaurar.

### Gate de salida

* problemas críticos identificados;
* terminología revisada;
* necesidades actualizadas;
* alcance corregido;
* decisiones documentadas.

Esta etapa puede provocar volver a OpenSpec antes de continuar.

---

## 8. Etapa 4 — Pilot Candidate

### Pregunta

¿El sistema está suficientemente protegido y operable para una prueba limitada?

### Capacidades obligatorias adicionales

* autenticación;
* autorización;
* usuarios;
* aislamiento de datos;
* configuración segura;
* HTTPS;
* respaldos;
* restauración;
* monitoreo;
* logs;
* manejo de secretos;
* procedimiento de soporte;
* revisión de privacidad;
* accesibilidad revisada.

### Datos

Preferiblemente ficticios durante la preparación.

Los datos reales solo podrán introducirse después de aprobar el gate del piloto.

### Gate de salida

* revisión de seguridad aprobada;
* pruebas automatizadas aprobadas;
* procedimiento de respaldo probado;
* procedimiento de restauración probado;
* acceso no autorizado verificado;
* errores no exponen secretos;
* responsables operativos identificados;
* participantes y consentimiento definidos;
* canal de soporte preparado.

---

## 9. Etapa 5 — Piloto controlado

### Pregunta

¿El producto aporta valor en condiciones reales y controladas?

### Audiencia

Un grupo pequeño y expresamente autorizado.

### Condiciones

* alcance limitado;
* duración definida;
* soporte directo;
* monitoreo activo;
* mecanismo de reporte;
* capacidad de detener el piloto;
* política de datos comunicada;
* participantes informados.

### Métricas de aprendizaje

* tareas completadas;
* tiempo para encontrar contexto;
* seguimientos identificados;
* registros abandonados;
* errores;
* necesidad de soporte;
* confianza percibida;
* razones para no utilizar el sistema.

### Regla

Una métrica de actividad no demuestra valor por sí sola.

### Gate de salida

* evidencia de utilidad;
* riesgos aceptables;
* errores críticos resueltos;
* privacidad y soporte sostenibles;
* decisión explícita de continuar, cambiar o detener.

---

## 10. Etapa 6 — Producción inicial

### Pregunta

¿Podemos operar el producto de forma confiable y responsable?

### Requisitos

* organización responsable;
* soporte;
* monitoreo;
* copias de seguridad;
* recuperación;
* seguridad;
* actualización;
* documentación;
* gestión de incidentes;
* gestión de vulnerabilidades;
* política de retención;
* derechos sobre datos;
* accesibilidad;
* despliegue repetible;
* rollback probado.

### Gate de salida

La producción no se declara automáticamente.

Requiere una decisión formal basada en evidencia técnica, operativa, legal y de producto.

---

## 11. Priorización

Se utilizará MoSCoW para el alcance de cada etapa.

### Must Have

Sin la capacidad, el objetivo de la etapa no puede cumplirse.

### Should Have

La ausencia reduce significativamente el valor, pero existe una alternativa temporal.

### Could Have

Aporta valor, pero no compromete el objetivo si se aplaza.

### Won’t Have for Now

No se incluirá en la etapa.

### Regla de descope

Cuando el tiempo o la complejidad crezcan:

1. retirar Could Have;
2. aplazar Should Have que tengan alternativa;
3. conservar Must Have;
4. reducir la amplitud del escenario;
5. nunca degradar seguridad necesaria para la etapa.

---

## 12. Unidad de entrega

La unidad preferida será una capacidad vertical verificable.

Ejemplo:

```text
Crear seguimiento
├── comportamiento definido
├── interfaz
├── API
├── persistencia
├── validación
├── errores
├── pruebas
└── documentación
```

No se considerará completa una capacidad cuando solo exista en una capa.

---

## 13. Definition of Done general

Una capacidad estará terminada cuando:

* cumple la especificación vigente;
* incluye comportamiento de éxito;
* incluye errores relevantes;
* incluye validación;
* cuenta con pruebas adecuadas;
* no rompe pruebas existentes;
* no contiene secretos;
* no introduce dependencias sin justificar;
* mantiene accesibilidad del flujo;
* actualiza documentación cuando corresponde;
* fue revisada;
* puede demostrarse;
* no deja trabajo crítico oculto.

La Definition of Done específica se perfeccionará cuando el stack sea elegido.

---

## 14. Criterios de parada

El proyecto deberá detener o replantear una etapa cuando:

* la investigación contradiga el problema central;
* los usuarios no perciban valor;
* el registro introduzca más carga que beneficio;
* el producto requiera datos cuyo tratamiento no pueda justificarse;
* el alcance dependa de capacidades excluidas;
* los riesgos de seguridad no puedan controlarse;
* el equipo no pueda operar el sistema;
* una solución existente resuelva mejor el problema;
* la complejidad exceda el aprendizaje esperado.

Detenerse o cambiar no se considera fracaso.

Se considera una decisión basada en evidencia.

---

## 15. Criterios de rollback

Toda liberación posterior a Development Preview deberá contar con:

* versión anterior identificable;
* artefacto reproducible;
* migraciones reversibles o procedimiento documentado;
* respaldo previo;
* validación posterior;
* responsable de decidir el rollback;
* comunicación del incidente.

Las migraciones destructivas requerirán precauciones adicionales.

---

## 16. Datos por ambiente

### Desarrollo local

* datos sintéticos;
* secretos locales ignorados;
* base reemplazable.

### Integración y pruebas

* datos generados;
* entorno aislado;
* limpieza automatizada.

### Demostración

* datos ficticios;
* acceso restringido;
* reinicio posible.

### Piloto

* datos autorizados;
* acceso controlado;
* respaldo;
* monitoreo;
* retención definida.

### Producción

* datos reales;
* controles completos;
* responsabilidades contractuales y legales;
* auditoría operativa.

---

## 17. Validación por etapa

### Descubrimiento

Validar problema y usuarios.

### OpenSpec

Validar claridad y consistencia.

### Development Preview

Validar integración técnica.

### Evaluación de uso

Validar comprensión y usabilidad.

### Pilot Candidate

Validar seguridad y operación.

### Piloto

Validar valor real.

### Producción

Validar sostenibilidad.

---

## 18. Métricas iniciales

No se fijarán objetivos numéricos definitivos sin una línea base.

Se observarán:

### Resultado de usuario

* éxito al encontrar clientes;
* éxito al comprender contexto;
* éxito al registrar interacciones;
* éxito al crear y completar seguimientos.

### Esfuerzo

* pasos;
* tiempo;
* errores;
* solicitudes de ayuda;
* abandonos.

### Calidad

* fallos;
* datos inválidos;
* duplicados;
* recuperaciones;
* incidencias.

### Adopción futura

* usuarios activos;
* interacciones registradas;
* seguimientos gestionados;
* recurrencia;
* razones de abandono.

---

## 19. Evidencia necesaria para cambiar el alcance

Una propuesta deberá incluir:

```text
Problema:
Usuario afectado:
Evidencia:
Resultado esperado:
Etapa:
Prioridad:
Esfuerzo aproximado:
Riesgos:
Criterio de éxito:
Elemento que podría salir:
```

Las peticiones de funcionalidades se registrarán, pero no entrarán automáticamente.

---

## 20. Registro de decisiones

Las decisiones importantes deberán conservar:

* fecha;
* contexto;
* opciones;
* elección;
* razón;
* consecuencias;
* evidencia;
* estado.

Los ADR técnicos se introducirán cuando corresponda.

Las decisiones de producto permanecerán en la documentación de producto.

---

## 21. Estrategia de demostración

Cada demostración deberá mostrar un recorrido, no una colección de pantallas.

Demostración mínima:

1. abrir la vista de trabajo;
2. localizar un cliente;
3. consultar su historial;
4. registrar una interacción;
5. crear un seguimiento;
6. encontrar el seguimiento;
7. completarlo;
8. comprobar que permanece en el historial.

---

## 22. Estrategia de feedback

Cada sesión deberá distinguir:

* observación;
* declaración;
* interpretación;
* decisión.

No se preguntará únicamente:

```text
¿Te gusta?
```

Se observará:

* qué intenta hacer;
* dónde duda;
* qué espera;
* qué interpreta;
* qué omite;
* qué error comete;
* qué resultado obtiene.

---

## 23. Estrategia de documentación

Cada etapa deberá mantener:

* alcance vigente;
* especificaciones vigentes;
* decisiones;
* instrucciones de ejecución;
* restricciones;
* riesgos;
* notas de versión;
* cambios incompatibles;
* pendientes conocidos.

La documentación debe describir el sistema real, no la intención antigua.

---

## 24. Preparación para OpenSpec

El Módulo 2 deberá transformar este alcance en especificaciones para:

* clientes;
* búsqueda;
* archivo y restauración;
* interacciones;
* seguimientos;
* vista de trabajo;
* validaciones;
* errores;
* persistencia.

Cada especificación deberá enlazar:

```text
Necesidad
→ capacidad
→ escenarios
→ implementación
→ pruebas
```

---

## 25. Estado

* Descubrimiento: en progreso.
* Alcance inicial: definido.
* Estrategia de versiones: definida.
* OpenSpec: pendiente.
* Development Preview: pendiente.
* Pilot Candidate: pendiente.
* Piloto: no autorizado.
* Producción: no autorizada.
* Datos reales: no autorizados.
