# Visión del producto — CRM Profesional

> **Estado:** borrador provisional sujeto a validación
> **Fecha inicial:** 2026-07-28
> **Fase:** Módulo 1 — Preparación del proyecto
> **Producto:** CRM Profesional
> **Nombre del directorio:** `proyecto-crm-profesional`
> **Implementación:** todavía no iniciada
> **Próxima revisión:** después de la primera ronda de investigación con usuarios

---

## 1. Propósito de este documento

Este documento define por qué debería existir CRM Profesional, a quién pretende ayudar, qué problema provisional intenta resolver y qué resultados debería producir.

No define todavía:

* el stack tecnológico;
* la arquitectura de software;
* las entidades de persistencia;
* los contratos de API;
* las pantallas;
* los campos definitivos;
* el backlog;
* los criterios de aceptación de funcionalidades;
* la implementación.

Las decisiones técnicas se tomarán después de comprender suficientemente el producto.

---

## 2. Convenciones de certeza

Para impedir que una hipótesis se convierta accidentalmente en un requisito, este documento utiliza cuatro etiquetas.

### `[DECISIÓN]`

Elección consciente del proyecto que se considera vigente hasta que una nueva decisión la sustituya.

### `[HIPÓTESIS]`

Suposición razonable que todavía no cuenta con evidencia suficiente de usuarios reales.

### `[POR VALIDAR]`

Pregunta o incertidumbre que requiere investigación, observación, datos o una prueba.

### `[NO OBJETIVO]`

Elemento que conscientemente queda fuera de esta fase o de la primera versión.

Ninguna afirmación etiquetada como hipótesis debe presentarse después como un hecho confirmado.

---

## 3. Contexto del producto

`[DECISIÓN]`

CRM Profesional será una aplicación web destinada inicialmente a equipos pequeños que prestan servicios y necesitan coordinar relaciones con clientes.

`[HIPÓTESIS]`

Algunos de estos equipos pueden gestionar información mediante una combinación de:

* memoria individual;
* conversaciones privadas;
* teléfonos personales;
* mensajería;
* hojas de cálculo;
* documentos;
* notas;
* herramientas sin una fuente compartida de verdad.

Esta hipótesis no implica que todas las organizaciones trabajen de esa manera.

`[POR VALIDAR]`

Debemos identificar:

* qué herramientas utilizan realmente;
* dónde se produce la fragmentación;
* qué información se pierde;
* con qué frecuencia ocurre;
* qué impacto tiene;
* quién experimenta el problema;
* qué soluciones utilizan actualmente;
* por qué esas soluciones no son suficientes.

---

## 4. Visión

> CRM Profesional permitirá que equipos pequeños de servicios mantengan una visión compartida, sencilla y confiable de cada relación con clientes, para encontrar contexto, registrar lo ocurrido y comprender qué debe suceder después.

La visión se resume en:

> **Conocer al cliente. Entender qué ocurrió. Saber qué sigue.**

---

## 5. Declaración de posicionamiento

Para equipos pequeños que prestan servicios y necesitan conservar continuidad en sus relaciones con clientes, CRM Profesional será una aplicación web sencilla que organizará el contexto esencial de cada relación.

A diferencia de plataformas empresariales extensas, la primera versión priorizará:

* baja complejidad;
* claridad;
* adopción progresiva;
* información mínima útil;
* trazabilidad comprensible;
* facilidad de aprendizaje;
* responsabilidades visibles;
* protección de datos desde el diseño.

Esta declaración es una dirección de producto, no una comparación comercial demostrada.

---

## 6. Organización objetivo provisional

`[HIPÓTESIS]`

La organización objetivo inicial tiene algunas de estas características:

* presta servicios;
* tiene un equipo pequeño;
* aproximadamente entre 2 y 20 integrantes;
* mantiene relaciones recurrentes con clientes;
* necesita compartir contexto entre varias personas;
* no dispone de un equipo especializado para administrar un CRM complejo;
* requiere una solución que pueda aprenderse progresivamente;
* utiliza español como idioma principal;
* opera inicialmente en Colombia.

El rango de integrantes es una decisión operativa provisional, no una clasificación jurídica de empresa.

`[POR VALIDAR]`

* ¿El problema aparece también en negocios de una sola persona?
* ¿A partir de cuántos integrantes se vuelve crítica la coordinación?
* ¿Existen diferencias importantes entre equipos de 2, 5, 10 y 20 personas?
* ¿El problema depende más del tamaño, del volumen de clientes o del tipo de servicio?
* ¿Debemos empezar por una industria específica?

---

## 7. Problema central provisional

> Los equipos pequeños pueden perder continuidad en la relación con sus clientes cuando la información relevante está fragmentada, desactualizada o depende de la memoria y las herramientas privadas de cada integrante.

Esta es una hipótesis de problema y debe validarse antes de convertirse en una especificación definitiva.

---

## 8. Posibles manifestaciones del problema

`[HIPÓTESIS]`

El problema podría manifestarse mediante:

* dificultad para encontrar el registro correcto;
* información duplicada;
* datos de contacto desactualizados;
* desconocimiento de la última interacción;
* falta de claridad sobre el siguiente paso;
* seguimientos olvidados;
* notas sin contexto;
* clientes obligados a repetir información;
* dos personas contactando al mismo cliente sin coordinación;
* dependencia excesiva de un integrante;
* pérdida de continuidad durante ausencias;
* falta de visibilidad para el responsable del negocio;
* dificultad para distinguir relaciones activas de relaciones cerradas;
* eliminación accidental de información;
* ausencia de responsabilidad clara.

Cada punto debe comprobarse mediante investigación.

---

## 9. Resultado que buscamos

`[DECISIÓN]`

El producto deberá ayudar a que un integrante autorizado pueda responder, de manera suficientemente rápida y confiable:

1. ¿Quién es este cliente?
2. ¿Qué información relevante conocemos?
3. ¿Qué ocurrió recientemente?
4. ¿Quién fue responsable de la interacción?
5. ¿Existe algo pendiente?
6. ¿Qué debería suceder después?

La primera versión no necesita responder todas las preguntas comerciales posibles.

Debe resolver bien las preguntas fundamentales.

---

## 10. Usuarios provisionales

### 10.1. Usuario principal diario — Miembro operativo

Persona que atiende, contacta, visita, asesora o presta seguimiento a clientes.

#### Necesidades provisionales

* encontrar el cliente correcto;
* comprender el contexto relevante;
* registrar información sin interrumpir excesivamente su trabajo;
* dejar constancia de lo ocurrido;
* identificar si existe una acción posterior;
* evitar transcribir repetidamente los mismos datos;
* distinguir información vigente de información antigua.

#### Riesgos de adopción

* demasiados campos obligatorios;
* navegación confusa;
* duplicación de trabajo;
* vocabulario ajeno al negocio;
* lentitud;
* ausencia de utilidad inmediata;
* registro posterior que termina olvidándose;
* temor a que la herramienta se use únicamente para vigilar al trabajador.

---

### 10.2. Usuario principal de coordinación — Propietario o coordinador

Persona responsable de la continuidad del servicio y de que las relaciones no dependan de un único integrante.

#### Necesidades provisionales

* comprender qué relaciones requieren atención;
* detectar información incompleta;
* conocer responsabilidades;
* identificar acciones pendientes;
* conservar continuidad durante ausencias;
* evitar pérdida de conocimiento cuando una persona deja el equipo;
* confiar en la calidad básica de los registros;
* obtener visibilidad sin exigir procesos innecesariamente pesados.

#### Riesgos de adopción

* utilizar el CRM únicamente como mecanismo de control;
* solicitar demasiada información;
* confundir cantidad de registros con valor;
* crear estados o procesos que el equipo no comprende;
* intentar reproducir todas las particularidades del negocio desde el primer día.

---

### 10.3. Usuario secundario — Administrador

Persona responsable de la configuración y mantenimiento operativo del sistema.

`[POR VALIDAR]`

Todavía no sabemos si:

* será una función separada;
* la realizará el propietario;
* la realizará una persona técnica;
* será necesaria en la primera versión.

Sus posibles responsabilidades futuras incluyen:

* gestionar integrantes;
* configurar permisos;
* mantener parámetros;
* ayudar a corregir problemas de datos;
* supervisar importaciones;
* apoyar el ciclo de vida de la información.

---

### 10.4. Persona indirectamente afectada — Cliente registrado

El cliente puede no utilizar directamente la aplicación, pero su información será almacenada y tratada por ella.

Sus intereses incluyen:

* exactitud;
* privacidad;
* confidencialidad;
* uso legítimo;
* acceso restringido;
* actualización;
* corrección;
* supresión cuando corresponda;
* ausencia de recolección excesiva.

La organización usuaria del CRM será responsable de determinar la finalidad y legitimidad del tratamiento realizado en su operación.

---

## 11. Jobs to Be Done provisionales

### JTBD-01 — Recuperar contexto

> Cuando un cliente vuelve a comunicarse, necesito recuperar rápidamente el contexto relevante de la relación para responder sin obligarlo a repetir toda su historia.

### JTBD-02 — Registrar una interacción

> Cuando termino una interacción con un cliente, necesito dejar un registro comprensible de lo ocurrido para que yo u otra persona podamos continuar posteriormente.

### JTBD-03 — Conservar el siguiente paso

> Cuando una conversación genera una acción posterior, necesito que quede claro qué debe hacerse y quién es responsable para reducir el riesgo de olvido.

### JTBD-04 — Coordinar al equipo

> Cuando varias personas pueden atender al mismo cliente, necesito una visión compartida para evitar trabajo duplicado o contradictorio.

### JTBD-05 — Mantener continuidad

> Cuando un integrante está ausente o deja el equipo, necesito conservar el conocimiento relevante de las relaciones que gestionaba para que la atención pueda continuar.

### JTBD-06 — Supervisar sin reconstruir manualmente

> Cuando coordino el negocio, necesito identificar relaciones y seguimientos que requieren atención para actuar antes de que se pierda una oportunidad o se deteriore el servicio.

Todos estos trabajos están pendientes de validación.

---

## 12. Recorrido actual provisional

`[HIPÓTESIS]`

Un recorrido posible antes del CRM es:

1. El cliente se comunica por algún canal.
2. Un integrante recibe el contacto.
3. Busca información en una o más herramientas.
4. Pregunta a otra persona por contexto faltante.
5. Atiende la solicitud.
6. Registra parte de la información o no la registra.
7. Guarda un recordatorio en una herramienta personal.
8. Otra persona desconoce el acuerdo.
9. El seguimiento depende de que alguien lo recuerde.

No afirmamos que este recorrido represente a todos los usuarios.

Debe compararse con experiencias reales.

---

## 13. Experiencia futura deseada

`[DECISIÓN]`

La experiencia deseada deberá permitir que una persona autorizada:

1. identifique al cliente;
2. encuentre el contexto esencial;
3. comprenda qué ocurrió;
4. registre una nueva interacción;
5. indique si existe una continuación;
6. deje información útil para otra persona;
7. complete el proceso con una carga razonable.

La tecnología específica para conseguirlo se definirá después.

---

## 14. Propuesta de valor

CRM Profesional busca ofrecer:

### Claridad

La información relevante debe poder comprenderse sin capacitación extensa.

### Continuidad

El conocimiento sobre un cliente no debe depender exclusivamente de una persona.

### Coordinación

El equipo debe poder comprender responsabilidades y antecedentes.

### Simplicidad

El esfuerzo de registrar información debe ser proporcional al valor obtenido.

### Confianza

Los usuarios deben poder identificar qué información existe, quién la registró y cuándo cambió.

### Crecimiento progresivo

El producto debe permitir añadir capacidades sin exigir complejidad empresarial desde el inicio.

---

## 15. Principios del producto

### 15.1. Resolver el problema antes de ampliar el catálogo

No añadiremos una funcionalidad únicamente porque otros CRM la tengan.

### 15.2. Una fuente compartida de verdad

La información principal no debe depender de archivos o cuentas personales desconectadas.

### 15.3. Información mínima útil

Recopilaremos únicamente datos que tengan una finalidad clara.

### 15.4. Registrar debe producir valor inmediato

El usuario debe percibir por qué vale la pena registrar la información.

### 15.5. La historia debe ser comprensible

Un registro sin fecha, responsable o contexto puede generar más confusión que utilidad.

### 15.6. Lo importante debe ser encontrable

La cantidad de información no debe impedir localizar el contexto relevante.

### 15.7. La privacidad es una propiedad del diseño

No se añadirá al final como una página legal desconectada del sistema.

### 15.8. Accesibilidad desde el inicio

La interfaz futura deberá diseñarse para ser perceptible, operable, comprensible y robusta.

### 15.9. Automatizar después de comprender

No automatizaremos procesos que todavía no entendemos.

### 15.10. IA después de contar con datos y controles confiables

La inteligencia artificial no forma parte de la primera versión.

Su incorporación futura requerirá:

* propósito claro;
* datos adecuados;
* evaluación;
* supervisión;
* privacidad;
* seguridad;
* trazabilidad.

---

## 16. Resultados de usuario

Queremos observar mejoras en:

* capacidad de encontrar información;
* comprensión del contexto;
* continuidad entre integrantes;
* claridad del siguiente paso;
* confianza en los registros;
* reducción de reconstrucción manual;
* menor necesidad de preguntar repetidamente por antecedentes;
* facilidad para registrar una interacción.

No se establecen todavía metas numéricas porque no existe una línea base.

---

## 17. Resultados de negocio

El producto podría contribuir a:

* disminuir seguimientos olvidados;
* reducir duplicación de esfuerzos;
* conservar conocimiento organizacional;
* mejorar coordinación;
* aumentar consistencia en la atención;
* facilitar crecimiento del equipo;
* reducir dependencia de herramientas personales.

Estos resultados son hipótesis de valor, no beneficios garantizados.

---

## 18. Métricas que deberemos estudiar

### Métricas de comportamiento

* tiempo necesario para localizar un cliente;
* tiempo necesario para comprender su contexto;
* tiempo necesario para registrar una interacción;
* porcentaje de tareas de prueba completadas;
* frecuencia de registros duplicados;
* frecuencia de búsquedas sin resultado;
* proporción de relaciones con información pendiente comprensible;
* cantidad de correcciones de datos.

### Métricas de adopción

* usuarios activos dentro del equipo;
* frecuencia de uso;
* porcentaje de interacciones registradas;
* abandono durante el registro;
* uso por rol;
* retorno después de la primera sesión.

### Métricas cualitativas

* confianza percibida en la información;
* claridad del lenguaje;
* facilidad de aprendizaje;
* percepción de utilidad;
* frustraciones;
* razones para no registrar;
* preocupaciones de privacidad;
* percepción de vigilancia.

### Regla

Ninguna métrica de actividad se considerará éxito por sí sola.

Más registros no significan automáticamente mejores relaciones.

---

## 19. Principios de datos personales

El sistema deberá diseñarse para permitir que la organización usuaria cumpla sus responsabilidades legales.

Principios iniciales:

* finalidad definida;
* minimización;
* exactitud;
* actualización;
* acceso restringido;
* seguridad;
* confidencialidad;
* trazabilidad;
* retención limitada;
* capacidad de corrección;
* capacidad de eliminación o anonimización cuando corresponda;
* separación entre datos reales y ambientes de desarrollo.

`[NO OBJETIVO]`

La primera versión no almacenará deliberadamente:

* datos médicos;
* biometría;
* información crediticia;
* orientación sexual;
* creencias religiosas;
* afiliación política;
* datos de menores;
* contraseñas de servicios externos;
* números completos de tarjetas;
* secretos de autenticación;
* documentos adjuntos sensibles.

Cualquier necesidad futura de datos sensibles requerirá análisis separado.

---

## 20. Accesibilidad e inclusión

La dirección del producto será:

* interfaz en español claro;
* vocabulario comprensible;
* uso posible mediante teclado;
* etiquetas visibles;
* mensajes de error útiles;
* estructura semántica;
* contraste adecuado;
* objetivos táctiles razonables;
* diseño adaptable;
* prevención de pérdida de información;
* ausencia de dependencia exclusiva del color;
* pruebas con personas que tengan diferentes capacidades y niveles de experiencia digital.

La conformidad formal solo podrá afirmarse después de implementación, auditoría y pruebas.

---

## 21. Dispositivos y contexto de uso

`[POR VALIDAR]`

Debemos investigar:

* si el uso principal será en computador;
* si se necesita uso frecuente desde teléfono;
* calidad habitual de conexión;
* navegadores utilizados;
* necesidad de trabajar durante visitas;
* interrupciones frecuentes;
* espacios compartidos;
* uso de dispositivos personales;
* disponibilidad de teclado;
* necesidades de impresión;
* necesidad de funcionamiento con conectividad inestable.

No asumiremos que una aplicación responsive resuelve automáticamente la experiencia móvil.

---

## 22. Suposiciones iniciales

1. Existe un problema de fragmentación de información.
2. Más de una persona necesita consultar contexto.
3. Los usuarios aceptarán registrar interacciones si el proceso es sencillo.
4. El siguiente paso es más importante que almacenar notas ilimitadas.
5. La continuidad tiene valor para el propietario.
6. Un producto básico puede ser útil sin automatización avanzada.
7. Los usuarios pueden aprender un flujo pequeño.
8. El español será suficiente para la primera versión.
9. Una aplicación web será accesible para el segmento inicial.
10. El beneficio percibido compensará el esfuerzo de mantener datos actualizados.

Todas estas suposiciones deben poder cuestionarse.

---

## 23. Preguntas abiertas prioritarias

1. ¿Cuál es el problema más frecuente relacionado con información de clientes?
2. ¿Qué ocurrió la última vez que faltó contexto?
3. ¿Qué herramienta se utiliza hoy como fuente principal?
4. ¿Qué información se consulta con mayor frecuencia?
5. ¿Qué información casi nunca se utiliza?
6. ¿Quién registra información?
7. ¿Cuándo se registra?
8. ¿Por qué no se registra?
9. ¿Cómo se recuerdan seguimientos?
10. ¿Quién puede modificar datos?
11. ¿Qué errores de datos son más comunes?
12. ¿Qué información consideran sensible?
13. ¿Qué ocurre cuando una persona está ausente?
14. ¿Qué dispositivo se utiliza?
15. ¿Cuál sería una mejora suficientemente valiosa para cambiar de método?
16. ¿Qué haría que abandonaran el CRM?
17. ¿Necesitan gestionar personas, empresas o ambas?
18. ¿Una relación puede tener varios contactos?
19. ¿Qué significa que un cliente esté activo?
20. ¿Qué significa archivar una relación?
21. ¿Qué datos necesitan conservar legal u operativamente?
22. ¿Qué datos deberían eliminarse?
23. ¿Cómo distinguen un cliente de un prospecto?
24. ¿Qué grado de configuración necesitan realmente?
25. ¿Qué proceso no debemos intentar digitalizar todavía?

---

## 24. No objetivos de esta fase

En esta fase no se decidirán:

* campos definitivos;
* modelo de datos;
* módulos;
* estados;
* roles de autorización finales;
* autenticación;
* integraciones;
* importaciones;
* reportes;
* dashboard;
* pipeline comercial;
* tareas;
* calendario;
* mensajería;
* facturación;
* automatización;
* inteligencia artificial;
* diseño visual;
* arquitectura;
* proveedor cloud;
* modelo de precios.

Estas decisiones dependerán de los siguientes pasos y de la evidencia obtenida.

---

## 25. Criterios para mantener una necesidad

Una necesidad podrá considerarse suficientemente respaldada cuando:

* corresponda a un resultado del usuario, no solo a una funcionalidad solicitada;
* aparezca en experiencias reales;
* tenga consecuencias comprensibles;
* pueda distinguirse del método actual utilizado para resolverla;
* sea relevante para el segmento objetivo;
* no contradiga restricciones legales o éticas;
* pueda ser evaluada posteriormente.

Una petición aislada no se convertirá automáticamente en requisito.

---

## 26. Criterios para rechazar una funcionalidad

Una funcionalidad podrá rechazarse o aplazarse cuando:

* no contribuya a la visión;
* no responda a una necesidad validada;
* añada más complejidad que valor;
* requiera datos sin finalidad clara;
* duplique una capacidad existente;
* impida una arquitectura incremental;
* aumente riesgos de privacidad injustificadamente;
* dependa de procesos todavía desconocidos;
* pertenezca a una etapa futura.

---

## 27. Relación con los próximos pasos

### Paso 3

Definirá alcance, primera versión, funcionalidades y no objetivos basándose en esta visión.

### Paso 4

Elegirá arquitectura y base tecnológica según las necesidades del producto.

### Paso 5

Diseñará la estructura del monorepo.

### Módulo 2

OpenSpec transformará las necesidades priorizadas en especificaciones verificables antes de implementar.

---

## 28. Política de actualización

Este documento no es inmutable.

Debe actualizarse cuando:

* la investigación contradiga una hipótesis;
* cambie el segmento;
* se descubra un usuario diferente;
* aparezca un riesgo relevante;
* una decisión de producto sea reemplazada;
* el producto entre en una fase nueva.

Cada cambio importante debe:

1. explicar qué cambió;
2. indicar por qué;
3. señalar la evidencia;
4. revisar consecuencias sobre alcance y especificaciones.

---

## 29. Estado actual

* Visión provisional: definida.
* Segmento provisional: definido.
* Usuarios provisionales: definidos.
* Problema: formulado como hipótesis.
* Investigación con usuarios: pendiente.
* Alcance funcional: pendiente.
* Stack: pendiente.
* Arquitectura: pendiente.
* Implementación: no iniciada.
* OpenSpec: todavía no introducido.
