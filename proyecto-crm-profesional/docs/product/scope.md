# Alcance del producto — CRM Profesional

> **Estado:** alcance inicial aprobado para preparación
> **Fecha:** 2026-07-28
> **Fase:** Módulo 1 — Definición del producto
> **Producto:** CRM Profesional
> **Rama del proyecto:** `docs/module-1-product-discovery`
> **Implementación:** no iniciada
> **Documentos relacionados:** `vision.md`, `user-research-plan.md`
> **Próxima revisión obligatoria:** después de investigación con usuarios y antes de aprobar el piloto

---

## 1. Propósito

Este documento define qué pretende resolver la primera etapa de CRM Profesional, qué capacidades tendrá, qué quedará fuera y qué condiciones deben cumplirse para considerar completa cada versión.

No sustituye:

* la investigación con usuarios;
* una especificación OpenSpec;
* el diseño de interacción;
* la arquitectura;
* el modelo de datos;
* los contratos de API;
* el backlog;
* la Definition of Done técnica de cada cambio.

---

## 2. Política de ramas

`[DECISIÓN]`

El repositorio mantiene dos líneas independientes:

```text
main
└── material del curso
```

```text
docs/module-1-product-discovery
└── proyecto CRM Profesional
```

Reglas:

* los módulos del curso solo viven en `main`;
* el proyecto CRM no se fusionará hacia `main`;
* no se abrirán pull requests desde la rama del proyecto hacia `main`;
* no se recuperarán los módulos dentro de la rama del proyecto;
* no se fusionará ni rebasará la rama del proyecto sobre `main`;
* cualquier futura reorganización de ramas requerirá una decisión explícita y una copia de seguridad.

---

## 3. Convenciones de certeza

### `[DECISIÓN]`

Elección vigente del producto.

### `[HIPÓTESIS]`

Suposición pendiente de evidencia.

### `[POR VALIDAR]`

Pregunta que necesita investigación o experimentación.

### `[NO OBJETIVO]`

Elemento expresamente excluido.

### `[GATE]`

Condición obligatoria antes de avanzar de etapa.

---

## 4. Conceptos utilizados

### Visión

Explica por qué existe el producto y qué resultado pretende producir.

### Alcance

Define qué problema y qué capacidades se abordarán en una etapa.

### Especificación

Define posteriormente el comportamiento exacto y verificable.

### Backlog

Ordena el trabajo necesario para cumplir especificaciones.

### Development Preview

Primera aplicación integrada, restringida al equipo de desarrollo y a datos ficticios.

### Pilot Candidate

Versión endurecida y preparada para evaluación controlada.

### Piloto

Uso limitado por personas autorizadas en condiciones supervisadas.

### Producción

Operación sostenida con datos reales, seguridad, soporte y responsabilidades definidas.

---

## 5. Objetivo del producto

> Permitir que equipos pequeños mantengan una visión compartida de cada relación con clientes para conocer al cliente, entender qué ocurrió y saber qué debe suceder después.

Este objetivo permanece provisional hasta ser contrastado con usuarios reales.

---

## 6. Principio de alcance

La primera versión no intentará reproducir una suite CRM completa.

Construirá un recorrido pequeño de principio a fin:

```text
Cliente
  ↓
Contexto
  ↓
Interacción
  ↓
Seguimiento
  ↓
Acción completada
  ↓
Historial conservado
```

Una funcionalidad solo pertenecerá al alcance inicial cuando contribuya directamente a ese recorrido.

---

## 7. Usuarios provisionales

### Miembro operativo

Necesita consultar contexto, registrar lo ocurrido y dejar claro el siguiente paso.

### Propietario o coordinador

Necesita identificar relaciones y seguimientos que requieren atención.

### Administrador

No será todavía un rol separado en Development Preview.

### Cliente registrado

No utilizará directamente la aplicación inicial, pero sus datos se verán afectados por el sistema.

Todos estos perfiles siguen sujetos a investigación.

---

## 8. Resultado mínimo de usuario

La primera versión deberá permitir responder:

1. ¿Existe este cliente?
2. ¿Qué información básica conocemos?
3. ¿Qué ocurrió recientemente?
4. ¿Quién registró lo ocurrido?
5. ¿Hay una acción pendiente?
6. ¿Quién es responsable?
7. ¿Cuándo debe realizarse?
8. ¿Ya fue completada?
9. ¿Se conserva el historial?

---

## 9. Recorrido funcional central

### Escenario central

1. Una persona busca un cliente.
2. Si no existe, registra un perfil básico.
3. Abre el detalle del cliente.
4. consulta el contexto disponible;
5. registra una interacción;
6. crea un seguimiento;
7. otro integrante consulta sus pendientes;
8. abre el seguimiento;
9. revisa el contexto del cliente;
10. completa o cancela la acción;
11. el sistema conserva el historial.

El recorrido deberá funcionar de extremo a extremo.

---

## 10. Development Preview

### 10.1. Objetivo

Comprobar que el producto puede ejecutar el recorrido central mediante una aplicación full stack integrada.

### 10.2. Audiencia

Exclusivamente:

* desarrolladores;
* revisores técnicos;
* evaluadores internos;
* participantes de demostraciones controladas sin datos reales.

### 10.3. Datos

Solo:

* ficticios;
* sintéticos;
* generados para pruebas;
* anonimizados de manera irreversible cuando exista autorización.

Está prohibido utilizar:

* clientes reales;
* conversaciones reales;
* correos personales;
* teléfonos reales;
* documentos de identidad;
* información sensible;
* credenciales reutilizadas.

### 10.4. Identidades

Development Preview podrá utilizar integrantes demostrativos preconfigurados para representar autoría y asignaciones.

Estas identidades:

* no equivalen a autenticación;
* no deben utilizarse para control de acceso;
* no permiten datos reales;
* deberán reemplazarse antes del piloto.

---

## 11. Capacidades Must Have

Una capacidad Must Have es indispensable para completar el recorrido central.

### M-01 — Registrar clientes

El sistema permitirá crear un registro de cliente con la información mínima necesaria para distinguirlo.

Los campos definitivos se especificarán posteriormente.

### M-02 — Listar clientes activos

El usuario podrá consultar clientes no archivados.

### M-03 — Consultar detalle

El usuario podrá abrir un cliente y comprender:

* su identidad;
* su estado;
* su información disponible;
* su actividad;
* sus seguimientos.

### M-04 — Actualizar información

El usuario podrá corregir o actualizar información del cliente.

### M-05 — Archivar

El usuario podrá retirar un cliente del flujo activo sin destruir su historial.

### M-06 — Restaurar

Un cliente archivado podrá volver al estado activo.

### M-07 — Buscar

El usuario podrá buscar clientes mediante información identificadora.

El comportamiento exacto de búsqueda se definirá en OpenSpec.

### M-08 — Registrar interacción

El usuario podrá registrar que ocurrió una interacción con el cliente.

La interacción deberá conservar, como mínimo conceptual:

* cliente relacionado;
* momento;
* resumen;
* tipo o contexto;
* autor demostrativo;
* fecha de creación.

### M-09 — Consultar historial

Las interacciones deberán mostrarse de forma cronológica y comprensible.

### M-10 — Crear seguimiento

El usuario podrá crear una acción posterior relacionada con un cliente.

### M-11 — Asignar seguimiento

El seguimiento podrá asociarse con un integrante demostrativo.

### M-12 — Establecer vencimiento

El seguimiento permitirá indicar cuándo debe completarse.

### M-13 — Cambiar estado del seguimiento

Los estados mínimos serán conceptualmente:

* pendiente;
* completado;
* cancelado.

La representación técnica se definirá posteriormente.

### M-14 — Consultar pendientes

El usuario podrá consultar seguimientos:

* vencidos;
* para hoy;
* próximos.

### M-15 — Navegar del seguimiento al cliente

El usuario podrá recuperar el contexto del cliente desde su seguimiento.

### M-16 — Conservar historial

Completar, cancelar o archivar no deberá borrar el contexto histórico.

### M-17 — Persistencia

La información deberá mantenerse después de reiniciar la aplicación y almacenarse en la base de datos definida para el proyecto.

### M-18 — Validación

El sistema deberá impedir entradas estructuralmente inválidas y explicar el problema.

### M-19 — Manejo de inexistencia

El sistema deberá responder claramente cuando el registro solicitado no existe.

### M-20 — Estados de interfaz

La interfaz deberá representar:

* carga;
* éxito;
* ausencia de resultados;
* error recuperable;
* error no recuperable.

---

## 12. Capacidades Should Have

Son importantes, pero pueden introducirse después del primer recorrido integrado.

### S-01 — Ordenar clientes

### S-02 — Paginar listas

### S-03 — Filtrar por estado activo o archivado

### S-04 — Filtrar seguimientos por responsable

### S-05 — Filtrar por estado temporal

### S-06 — Mostrar actividad reciente

### S-07 — Confirmar operaciones de archivo

### S-08 — Estados vacíos con orientación

### S-09 — Advertir posibles duplicados

### S-10 — Conservar criterios de búsqueda durante la navegación

### S-11 — Mostrar información incompleta

### S-12 — Mostrar fecha y autor de los cambios relevantes

---

## 13. Capacidades Could Have

Se considerarán solamente si no comprometen los Must Have.

### C-01 — Etiquetas

### C-02 — Filtros guardados

### C-03 — Acciones rápidas

### C-04 — Búsqueda tolerante a pequeñas variaciones

### C-05 — Vista compacta

### C-06 — Conteos básicos

### C-07 — Atajos desde la vista de trabajo

### C-08 — Restauración rápida

### C-09 — Preferencias visuales locales

### C-10 — Datos demostrativos preconfigurados

---

## 14. Won’t Have for Now

### Gestión comercial avanzada

* leads independientes;
* oportunidades;
* deals;
* pipeline;
* forecast;
* scoring;
* metas comerciales;
* territorios;
* cotizaciones.

### Marketing

* campañas;
* formularios públicos;
* newsletters;
* segmentación avanzada;
* automatización de marketing;
* redes sociales.

### Comunicaciones integradas

* correo;
* WhatsApp;
* SMS;
* telefonía;
* videollamadas;
* chat en vivo.

### Operación avanzada

* workflows configurables;
* reglas de automatización;
* aprobaciones;
* escalamiento;
* calendarios externos;
* notificaciones externas.

### Datos y personalización

* campos personalizados;
* módulos personalizados;
* importaciones masivas;
* exportaciones masivas;
* deduplicación automática;
* enriquecimiento de datos;
* archivos adjuntos.

### Plataforma comercial

* multitenancy;
* suscripciones;
* facturación;
* pagos;
* marketplace;
* administración de planes;
* personalización por organización.

### Inteligencia artificial

* generación de mensajes;
* resúmenes automáticos;
* clasificación;
* scoring;
* predicciones;
* agentes autónomos;
* recomendaciones;
* análisis de sentimiento.

### Infraestructura innecesaria

* microservicios;
* Kafka;
* Redis;
* Kubernetes;
* service mesh;
* arquitectura multirregión.

---

## 15. Reglas de negocio provisionales

### RB-01

Un cliente archivado no aparece en la lista activa por defecto.

### RB-02

Archivar un cliente no elimina sus interacciones ni seguimientos.

### RB-03

Un cliente archivado puede restaurarse.

### RB-04

Una interacción siempre pertenece a un cliente.

### RB-05

Un seguimiento siempre pertenece a un cliente.

### RB-06

Un seguimiento pendiente tiene una responsabilidad visible.

### RB-07

Completar un seguimiento conserva su información.

### RB-08

Cancelar un seguimiento conserva su información y estado.

### RB-09

No habrá eliminación destructiva disponible desde la interfaz inicial.

### RB-10

Development Preview utiliza únicamente identidades y datos ficticios.

### RB-11

Ninguna identidad demostrativa representa seguridad o autorización.

### RB-12

Antes del piloto, toda acción que consulte o modifique datos requerirá control de acceso.

Estas reglas deberán convertirse posteriormente en escenarios verificables.

---

## 16. Límites de información

La primera versión podrá trabajar conceptualmente con:

### Perfil de cliente

* identidad;
* información de contacto;
* organización o contexto comercial opcional;
* estado;
* notas generales limitadas;
* fechas relevantes.

### Interacción

* cliente;
* tipo;
* momento;
* resumen;
* autor;
* metadatos.

### Seguimiento

* cliente;
* descripción;
* responsable;
* fecha límite;
* estado;
* fecha de finalización;
* metadatos.

Esta sección no define todavía tablas, nombres de campos ni tipos de datos.

---

## 17. Calidad mínima

### Comprensibilidad

El usuario debe poder identificar:

* qué está viendo;
* qué acción puede realizar;
* si la acción funcionó;
* cómo recuperarse de un error.

### Accesibilidad

El recorrido principal deberá ser utilizable mediante teclado y no depender exclusivamente del color.

### Integridad

La aplicación no deberá perder datos por una navegación normal o reinicio controlado.

### Validación

Frontend y backend deberán validar en sus respectivas fronteras.

El backend será la autoridad final.

### Seguridad de la etapa

Development Preview no podrá exponerse como servicio público con datos reales.

### Trazabilidad

Los registros deberán conservar metadatos suficientes para comprender cuándo fueron creados y actualizados.

### Mantenibilidad

El código deberá respetar la arquitectura definida posteriormente y contar con verificaciones automatizadas acordes con cada etapa.

### Observabilidad mínima

La aplicación deberá permitir detectar:

* si backend está disponible;
* si la base de datos está disponible;
* si una operación falla;
* qué clase de error ocurrió sin exponer secretos.

---

## 18. Matriz de trazabilidad

| Necesidad provisional      | Capacidad                   |
| -------------------------- | --------------------------- |
| Encontrar al cliente       | listado, búsqueda y detalle |
| Comprender el contexto     | perfil e historial          |
| Registrar lo ocurrido      | interacciones               |
| Saber qué sigue            | seguimientos                |
| Conocer responsabilidad    | asignación                  |
| Evitar olvidos             | vista de pendientes         |
| Mantener continuidad       | historial compartido        |
| Evitar pérdida destructiva | archivo y restauración      |

---

## 19. Condiciones de aceptación de Development Preview

`[GATE]`

La Development Preview estará completa cuando:

1. el recorrido central funcione de extremo a extremo;
2. frontend, backend y base de datos estén integrados;
3. los datos persistan;
4. sea posible crear y encontrar un cliente;
5. sea posible registrar y consultar una interacción;
6. sea posible crear, consultar y completar un seguimiento;
7. sea posible archivar y restaurar;
8. los estados de error principales sean comprensibles;
9. las validaciones principales estén presentes;
10. existan pruebas automatizadas para el recorrido crítico;
11. no se utilicen datos reales;
12. no se presente como producción;
13. el código pueda levantarse mediante comandos documentados;
14. no haya secretos versionados;
15. la documentación coincida con el comportamiento.

---

## 20. Condiciones adicionales del Pilot Candidate

`[GATE]`

Antes de ser Pilot Candidate deberá incluir:

* autenticación;
* autorización;
* administración básica de usuarios;
* aislamiento del espacio de trabajo;
* HTTPS;
* configuración segura;
* secretos externos al repositorio;
* revisión de privacidad;
* política de respaldo;
* estrategia de recuperación;
* registro operativo;
* monitoreo;
* gestión de errores;
* pruebas de seguridad;
* accesibilidad revisada;
* términos de uso del piloto;
* canal de soporte;
* procedimiento para corregir y eliminar datos.

---

## 21. Hipótesis principales

### H-SCOPE-01

El recorrido cliente → interacción → seguimiento resuelve una parte valiosa del problema.

### H-SCOPE-02

Un historial sencillo puede producir valor sin pipeline de ventas.

### H-SCOPE-03

La vista de pendientes será más útil inicialmente que un dashboard analítico.

### H-SCOPE-04

El archivo reversible es suficiente sin eliminación destructiva inicial.

### H-SCOPE-05

Un conjunto reducido de datos puede sostener la coordinación.

### H-SCOPE-06

Los usuarios aceptarán registrar interacciones si el proceso es corto.

### H-SCOPE-07

La asignación visible reduce dependencia de memoria personal.

Estas hipótesis deben relacionarse con investigación futura.

---

## 22. Riesgos

### R-01 — Construir sin evidencia

Mitigación: conservar etiquetas de hipótesis y actualizar el alcance después de investigar.

### R-02 — Convertir el CRM en agenda de contactos

Mitigación: exigir interacción, seguimiento e historial.

### R-03 — Sobrecargar el registro

Mitigación: minimizar campos obligatorios y probar el flujo.

### R-04 — Añadir funciones por comparación comercial

Mitigación: toda capacidad debe vincularse con una necesidad.

### R-05 — Tratar Development Preview como producción

Mitigación: prohibir datos reales y documentar gates.

### R-06 — Confundir identidades demostrativas con seguridad

Mitigación: reemplazarlas antes del piloto.

### R-07 — Crecimiento descontrolado

Mitigación: aplicar MoSCoW y retirar Could Have primero.

### R-08 — Eliminar accidentalmente el curso

Mitigación: no fusionar la rama del proyecto hacia `main`.

---

## 23. Control de cambios

Una nueva capacidad solo podrá entrar cuando incluya:

1. problema o necesidad relacionada;
2. evidencia disponible;
3. resultado esperado;
4. etapa propuesta;
5. prioridad;
6. impacto sobre alcance;
7. riesgos;
8. coste aproximado;
9. criterio de verificación;
10. elementos que deberán salir si el alcance crece.

Añadir una capacidad sin retirar o replanificar otra se considera crecimiento de alcance.

---

## 24. Preguntas abiertas

* ¿El concepto principal debe ser cliente, contacto o relación?
* ¿Deben distinguirse personas y organizaciones?
* ¿Puede una organización tener varios contactos?
* ¿Qué tipos de interacción reconocen los usuarios?
* ¿Qué datos identifican suficientemente a un cliente?
* ¿Qué información es obligatoria?
* ¿Qué significa archivar para cada negocio?
* ¿Quién puede restaurar?
* ¿Deben poder corregirse interacciones?
* ¿Se necesita una razón de cancelación?
* ¿Qué ventana temporal define “próximo”?
* ¿Qué dispositivos son prioritarios?
* ¿Qué datos consideran sensibles?
* ¿Qué permisos necesita cada rol?

Estas preguntas no deben resolverse por intuición cuando puedan investigarse.

---

## 25. Estado

* Visión: definida provisionalmente.
* Usuarios: provisionales.
* Investigación ejecutada: pendiente.
* Recorrido central: definido.
* Development Preview: delimitada.
* Pilot Candidate: delimitado.
* Must Have: definidos.
* Should Have: definidos.
* Could Have: definidos.
* Won’t Have: definidos.
* Arquitectura: pendiente.
* Stack: pendiente.
* OpenSpec: pendiente.
* Implementación: no iniciada.
