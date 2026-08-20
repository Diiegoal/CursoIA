📚Ejemplo: Proyectos Finales Reales — 12 min
Antonio Perez
Aquí tienes 2 proyectos reales entregados por alumnos. Úsalos como referencia de estructura y calidad, no como molde para copiar.

¿Qué deberías mirar?
1. La estructura del repositorio
Entra a cualquiera de los dos repos y busca:

README.md - cómo se documenta un proyecto. Lee cómo está organizado, qué secciones tiene, cómo conecta la idea con la arquitectura.

prompts.md - cómo se documentó el uso de IA. Busca ejemplos de prompts, cómo se organizaron por fase, qué información incluyen.

/docs o /architecture - planos, diagramas C4, decisiones de diseño.

/.github/workflows (si existe) - cómo se hizo CI/CD.

2. El código
Backend: busca la estructura de carpetas. ¿Cómo organizó el código? ¿Qué patrones usó?

Frontend: mira si hay componentes reutilizables, cómo se gestiona el estado, qué librería de UI.

Tests: ¿tiene tests unitarios? ¿Tests E2E? ¿Cuántos?

3. Despliegue y evidencia
README: sección "Cómo ejecutar localmente" — ¿está clara? ¿Puedo correr el proyecto en mi máquina?

URL o video: ¿hay evidencia del proyecto funcionando? Si tiene URL pública, intenta usarlo.

4. Decisiones de diseño
Lee el archivo de arquitectura (si existe)

Busca comentarios en el código que expliquen decisiones no obvias

Pregúntate: ¿por qué eligió este stack? ¿Por qué esta estructura?

Los 2 ejemplos
👉 Repositorio Ejemplo 1 https://github.com/LIDR-academy/AI4Devs-finalproject-Example1
Foco: Sistema completo de reservas para campings/hospederías con frontend React + backend PHP funcional desde el minuto 0.

Stack: PHP 8.1+ (Slim Framework) + React 18 + TypeScript + Vite | Testing: PHPUnit >85% coverage + Vitest >78% coverage

Lo que hace bien:

Mock-First Development. Diseñado para funcionar inmediatamente sin base de datos real. Usa datos JSON que simula 6 meses de disponibilidad con precios dinámicos. Perfecto para demostración rápida.

Documentación técnica numbered y completa. 7 documentos estructurados (0-ficha → 1-descripción → 2-arquitectura → 3-datos → 4-API → 5-historias → 6-tickets). Es un modelo de cómo documentar un proyecto profesional.

Repository Pattern. Arquitectura abstraída que permite cambiar JSON por base de datos SIN tocar lógica de negocio. Muestra decisiones de arquitectura reales.

Testing integrado desde el inicio. Unit + Integration + E2E con coverage reports. No es un afterthought, es parte del core.

Úsalo para aprender:

Cómo estructurar documentación (los 7 documentos numbered son exactamente lo que pide la plantilla)

Repository Pattern en PHP/React (abstracción de datos para migración fácil)

Mock-first development (funciona sin dependencias externas)

Integración de testing en ambos lados (backend + frontend) con cobertura medible

👉 Repositorio Ejemplo 2 https://github.com/LIDR-academy/AI4Devs-finalproject-Example2
Foco: Chatbot RAG avanzado con Gemini que actúa como representante virtual 24/7 para portfolio profesional, capturando leads de forma natural durante conversaciones.

Stack: Python 3.11+ (FastAPI) + React 18 + TypeScript + Gemini 2.5 Flash + HuggingFace embeddings (multilingüe) + pgvector + GCP (Cloud Run + Cloud SQL) | Testing: Pytest + Coverage >80%

Lo que hace bien:

Arquitectura RAG Avanzada. Implementación production-ready con HuggingFace embeddings locales (multilingüe), pgvector para búsqueda semántica, y Gemini 2.5 Flash. RAG pipeline reduce tokens enviados al LLM en 40-60%. Está muy bien documentado el flujo completo.

Optimización Inteligente de Costos. Sistema que mantiene costos en $6-17/mes usando capas gratuitas de GCP. Cache inteligente con >70% hit rate. Monitoreo de costos en tiempo real. Demuestra cómo ser eficiente con LLMs en producción.

GDPR Compliance + Lead Capture. Sistema completo de consentimientos GDPR, captura de leads no invasiva durante conversación, multi-idioma (español/inglés), flujos naturales con validación de IA vs humano. Lead scoring automático.

Infrastructure Profesional. Setup completo de GCP (Cloud Run serverless, Cloud SQL con pgvector, Artifact Registry, CI/CD automático con Cloud Build, Secret Manager). Deployment production-ready.

Úsalo para aprender:

RAG en producción: Cómo implementar Retrieval Augmented Generation real con HuggingFace + pgvector + LLM en una arquitectura escalable

Optimización de costos con IA: Técnicas concretas para reducir 60-80% costos vs. implementación estándar (RAG + cache + token optimization)

GDPR compliance: Implementación real de GDPR en sistema con IA, gestión de consentimientos, data privacy, 7 años de retención para legal

Full-stack Python/React: FastAPI backend con RAG + React frontend integrado, ambos en producción con GCP

Lead generation IA-nativa: Cómo capturar leads de forma natural usando conversación inteligente sin ser invasivo

Cómo usar estos ejemplos
No copies estructura. Cada proyecto es diferente. Tu contexto es único.

Sí copia decisiones. Si ves algo que tiene sentido para tu caso (organización de tests, patrón de carpetas, cómo se documenta), tómalo.

Compara. Nota qué hace diferente cada ejemplo. ¿Cuál te gusta más? ¿Por qué?

Aprende de errores. Si ves algo que podría mejorar, anótalo. Cuando entregues, evítalo.

Preguntas que deberías poder responder después de mirar:
¿Cómo estructuraría YO mi proyecto de forma diferente?

¿Qué patrones de esos 2 ejemplos quiero usar?

¿Dónde voy a poner documentación en mi repo?

¿Cómo voy a organizar mis tests?

Si no puedes responder ninguna, vuelve a mirar.

Nota
Estos son proyectos de entregas anteriores. El nivel de detalle, calidad de código y completitud varían. Eso es normal. No hay un "proyecto perfecto". Hay proyectos que resuelven bien el problema de una forma, y otros que lo resuelven de otra.

La tuya será diferente. Y eso está bien 🤖