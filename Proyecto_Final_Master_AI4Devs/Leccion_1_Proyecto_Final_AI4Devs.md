🧑🏻‍💻 Lección 1 - Todo lo que necesitás saber para arrancar tu Proyecto Final — 29 min
Antonio Perez
⏳ Tiempo estimado: 29 min

¿Para qué existe el Proyecto Final?
El Proyecto Final es uno de los cuatro criterios para obtener el certificado de AI4Devs. Es el más importante porque es donde llevas todo lo aprendido en el máster a la práctica real: desarrollar un producto de software end-to-end, apoyándote en IA en todas las fases del ciclo de vida, desde la idea hasta el despliegue.

El criterio de evaluación tiene tres ejes: la idea y arquitectura del producto, la calidad del código, y cómo usaste la IA a lo largo del proceso.

¿Qué tienes que construir?
Un MVP (Producto Mínimo Viable) de tema libre. El dominio es tuyo:

Puede ser algo de tu trabajo actual (una feature, un módulo nuevo, una automatización)

Puede ser un proyecto personal o una idea que tengas en mente

Puede hacerse en equipo si compartes esta edición con colegas de la misma empresa

El proyecto tiene que ser robusto: no es una pantalla de captura con un botón. Tiene que tener al menos un flujo end-to-end completo, con backend, frontend y base de datos, o su equivalente según tu perfil y stack.

¿Qué pasa si mi proyecto no tiene frontend? Sin problema. Si desarrollas un pipeline, un sistema de drivers, una herramienta CLI o algo sin interfaz visual, puedes documentarlo igualmente. Lo que pedimos es que se pueda verificar que funciona.

¿Qué pasa si mi proyecto es de hardware? También vale. Pedimos un video de 2-3 minutos mostrando el funcionamiento.

Alcance recomendado del MVP
Planifica entre 3 y 5 historias de usuario must-have (las imprescindibles) y 1-2 should-have (deseables pero opcionales). No intentes incluir todo lo que aprendiste en el máster de una sola vez. Elige lo que tenga sentido para tu proyecto.

Las 3 entregas
El proyecto se divide en tres entregas progresivas. Trabajas en la misma plantilla (fork del repositorio oficial) a lo largo de todo el proceso.

Entrega 1 — Documentación técnica
Qué incluye:

Ficha del proyecto: nombre, descripción, URL del repo o ZIP

Descripción general del producto: objetivo, características, funcionalidades

Arquitectura del sistema y modelo de datos

Historias de usuario y tickets de trabajo

Stack tecnológico elegido

Qué NO incluye todavía: código. Esta entrega es 100% documentación.

Entrega 2 — Código funcional
Qué incluye:

Scaffolds de tu arquitectura (front, back, base de datos ya conectados)

El flujo principal casi completo

Primeras funcionalidades operativas

No se espera que todo el proyecto esté terminado. Con IA, el salto de la entrega 1 a tener código funcional suele ser más rápido de lo que imaginas.

Entrega 3 — Entrega final
Qué incluye:

Unión de la entrega 1 y 2

Entre 3 y 5 funcionalidades del producto completas y funcionales

Suite de tests (unitarios, integración, al menos un test end-to-end del flujo principal)

Evidencia de despliegue: URL pública, screenshots o video del sistema funcionando

Archivo prompts.md completo (o equivalente de registro de uso de IA)

Esta es la única entrega que recibe feedback humano personalizado del equipo. Las entregas 1 y 2 tienen revisión automatizada.

Cómo entregar

https://vimeo.com/1202881478/646c8c4a11?fl=pl&fe=cm

El repositorio
Haz un fork del repositorio oficial del Proyecto Final de AI4Devs. Sobre ese fork trabajas todas las entregas.

Para cada entrega, trabajas en una rama con este formato:

Entrega 1: feature/entrega-1-TUS_INICIALES

Entrega 2: feature/entrega-2-TUS_INICIALES

Entrega final: final-project-TUS_INICIALES

Las iniciales son obligatorias. Sin ellas no podemos identificar tu entrega.

El formulario de entrega
Cada vez que terminas una entrega, completas el formulario de Typeform. Ese formulario nos genera una alerta en Slack y activa el flujo de revisión. Sin el formulario, la entrega no existe formalmente.

El formulario te pide: nombre completo, email, tipo de entrega (1, 2 o final), y la URL de tu pull request.

Si tu proyecto es privado o de empresa
No hay problema. Dos opciones:

Opción A: Pones el repo en privado y le das acceso solamente a tu TA (y al Líder de Programa, Jorge, si aplica). Entregas igual por el formulario con la URL del PR.

Opción B: Si no puedes compartir el código por confidencialidad, completas la plantilla (README + prompts) y grabas un video de 2-3 minutos mostrando el funcionamiento del producto. Eso es suficiente.

Lo que sí es obligatorio en cualquier caso: completar el archivo README con toda la documentación del proyecto y el archivo prompts.md (o equivalente).

El archivo de registro de IA
Antes esto se llamaba prompts.md y pedíamos los prompts clave. Hoy evolucionó a algo más completo: documentar tu flujo de trabajo con IA.

Incluye:

Qué herramientas usaste (Claude, Cursor, ChatGPT, etc.)

Qué modelos usaste y para qué (por ejemplo: Opus para especificaciones, Sonnet para codeo)

Si usaste skills, subagentes, rules o comandos personalizados

Los prompts o workflows más importantes del proyecto

Qué ajustes humanos tuviste que hacer sobre el output de la IA

Esto es lo que nos permite ver cómo desarrollaste las habilidades del máster. Es uno de los tres ejes de evaluación de la entrega final.

▶ Ejemplo real: así se ve un flujo de trabajo con IA en un proyecto

https://vimeo.com/1198090811/27eacb7375?fl=pl&fe=cm


En este clip puedes ver cómo documentar y estructurar el flujo completo de agentes para un proyecto mobile. No tienes que replicar exactamente esto, es para que entiendas el nivel de detalle que buscamos en el registro de IA.

Preguntas frecuentes
¿El proyecto es individual o grupal?
Normalmente es individual, pero se puede hacer en grupo. Si son varias personas de la misma empresa o de esta edición que quieren colaborar, sin problema.

¿Qué tecnología tengo que usar?
La que quieras. JavaScript, Python, Java, PHP, Elixir, lo que te sirva. No hay restricción de stack.

¿Tengo que implementar todo lo que se enseña en el máster?
No. Usa lo que tenga sentido para tu proyecto. Si no llegas a implementar CI/CD o testing avanzado, no es un problema. El foco es que el producto funcione y que se vea cómo usaste la IA.

¿Puedo empezar con un proyecto que ya tengo o es mejor arrancar de cero?
Ambas opciones son válidas. Si ya tienes un proyecto en marcha, puedes tomarlo como base y agregarle funcionalidades nuevas aplicando lo aprendido. Si comienzas de cero, la ventaja es que la IA puede estructurarlo todo desde el principio con mejor arquitectura.

¿Qué pasa si mi proyecto es una migración de código legacy?
Es más complejo y la IA puede traer errores del código viejo. Recomendamos comenzar de cero cuando sea posible, pero si la migración es lo que tiene valor real para ti, puedes hacerlo. Consúltalo con tu TA antes de arrancar.

¿Cuántas horas tengo que dedicarle?
La estimación oficial es 30 horas. En la práctica, la mayoría de los alumnos dedica más, especialmente los que terminan usando el proyecto en su trabajo real. Hay alumnos que terminaron dedicando 90 o 120 horas y salieron con un producto que siguieron desarrollando. La IA acelera mucho el proceso, pero un buen proyecto toma tiempo.

¿Qué pasa si no llego a la fecha de entrega final?
Existe una prórroga de hasta 2 semanas a partir de la fecha límite. Para pedirla, escríbele a tu TA con anticipación. La prórroga se evalúa caso por caso.

¿Podemos tener una sesión de consultas?
Puedes compartir tus dudas con el TA, e iremos liberando lecciones que te ayudarán para desbloquear problemas de diseño e implementación y para pulir detalles antes de la entrega final.

Si tengo una duda técnica ahora, ¿a quién le escribo?
Primero al grupo del cohort en WhatsApp: puede que alguien más tenga la misma duda y se resuelve entre todos. Si es algo específico de tu proyecto, escríbele directamente a tu TA. Para dudas técnicas que requieren un mentor especializado, tu TA te conecta con la persona indicada.

Inspiración: ejemplos de proyectos anteriores
Algunos proyectos reales entregados por alumnos:

Chatbot en Telegram para reportar basura con geolocalización y foto → evolucionó en sistema para pedir comida por WhatsApp

Sistema de control de salud de animales bovinos con hardware (chip) y backend

Dashboard de orquestación de agentes que ejecuta tickets y abre pull requests automáticos

Aplicación de fitness personalizada con IA

Sistema de gestión de almacén con módulos de inventario y despliegue en SAP

CMS educativo tipo Moodle con interfaz drag & drop para profesores

Puedes ver ejemplos completos de entregas anteriores (documentación técnica, entrega 2 y entrega final) en el repositorio oficial de AI4Devs Final Project, en la sección de Pull Requests.

¿Tienes dudas después de leer esto?
👇Déjanos tus preguntas al pie de esta lección y las respondemos.

Antes de escribir, revisa si tu duda ya aparece en la sección de preguntas frecuentes. Si es algo muy específico de tu proyecto o de tu perfil profesional (data, hardware, proyectos de empresa), escríbela igual: esos casos los manejamos de forma personalizada con tu TA o con un mentor especializado.
