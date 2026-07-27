                                         Today 2:59 PM



                               ingresa a mi repo https://github.com/Diiegoal/CursoIA.git
                               hazle git clone e ingresa, verifica que hay como 7
                               modulos, el contenido de todos los modulos fueron
                               sacados de un curso, no son inventos, lee todo el
                               contenido de todos los modulos e investiga
                               exhaustivamente y busca en fuentes confiables sin
                               inventar datos sobre todo contenido de mi repo.

Worked for 9m 11s

Sí. Revisé el repositorio Diiegoal/CursoIA , reconstruí su estructura completa y contrasté
las afirmaciones técnicas y fechadas con documentación oficial, papers, organismos
regulatorios y fuentes primarias siempre que fue posible.

Hay una limitación que quiero dejar completamente clara: no pude ejecutar literalmente
git clone en el entorno local porque ese entorno no pudo resolver github.com . No
voy a decir que lo cloné cuando no ocurrió. Accedí al main actual mediante la integración
directa de GitHub y abrí los archivos del repositorio desde allí. No modifiqué nada.

1. Sí: tienes 7 módulos
El contenido actual se distribuye así:
Módulo                  Tema                                                  Archivos

1                       Los 3 pilares del uso efectivo de copilotos IA                     5


2                       Spec-Driven Development (SDD)                                      6


3                       Sistema operativo de copilotos IA                                  6


4                       Planificación efectiva con IA                                      7


5                       Documentación efectiva con IA                                      6


6                       Ética, regulación y privacidad                                     6


7                       Testing y calidad con IA — Parte 1                                 5


Total                                                                            41 archivos

Por tanto, tu recuerdo de que había “como 7 módulos” es correcto: son exactamente 7 en
el repositorio actual.




2. Conclusión general de la auditoría
Mi conclusión después de contrastar el material es esta:

   No veo evidencia de que el contenido del curso sea una colección de datos
   inventados.

Hay bastante investigación real detrás: METR, Anthropic, OpenAI, GitHub, LangChain,
C4, OpenSpec, GDPR, EU AI Act, Veracode, DORA, Faros AI, documentación oficial de
Claude Code, Cursor, etc.

Pero encontré un problema importante:

El curso mezcla tres cosas distintas como si tuvieran el mismo nivel de
certeza
 1. Hechos comprobables, por ejemplo el estudio de METR.
 2. Buenas prácticas y heurísticas, por ejemplo “compacta al 70% de contexto”.
 3. Opiniones/modelos mentales del autor, por ejemplo “el modelo ya no es el cuello
    de botella”.

Las tres pueden ser útiles, pero no deberían presentarse todas como si estuvieran
demostradas científicamente.

Además, varios datos son snapshots de abril de 2026. Hoy es 26 de julio de 2026, y
algunas cosas ya cambiaron.




3. Módulo 1 — Los 3 pilares
Veredicto: muy buena base, pero algunas conclusiones son más
fuertes que la evidencia
La idea central es:

   Herramienta + Contexto + Prompt

Como modelo mental pedagógico, es perfectamente razonable.

El problema aparece cuando el material pasa de:

     “estos tres factores son importantes”

a:

     “el modelo ya no es el cuello de botella”.

Eso último no es una conclusión científica establecida universalmente.

METR: correcto
Tu archivo afirma que en el estudio de julio de 2025 los desarrolladores experimentados
tardaron un 19% más usando herramientas de IA; además, esperaban ser 24% más
rápidos y percibieron haber sido 20% más rápidos. Eso coincide con METR.            Metr



También es correcto el update de febrero de 2026:

      desarrolladores originales: aproximadamente 18% más rápidos;
      intervalo de confianza: −38% a +9%;
      nuevos desarrolladores: alrededor de −4%, CI −15% a +9%.

Pero falta un matiz muy importante: METR dice expresamente que el segundo
resultado sufre problemas severos de selección y constituye evidencia muy débil.
No debería utilizarse como demostración firme de que “con siete meses de experiencia la
IA ya acelera 18%”.       Metr




El paper de mantenimiento también está correctamente citado
La afirmación de que ciertos core developers produjeron aproximadamente 19% menos
código original y revisaron alrededor de 6,5% más código ajeno está respaldada por el
trabajo citado.     ar…



Pero la frase:


     “La IA no reduce trabajo: lo transfiere del autor al revisor”

es una interpretación del autor, no algo demostrado de manera general para todos los
equipos.

De hecho, una meta-análisis publicado en 2026 que reunió 23 estudios encuentra, en
conjunto, un efecto moderadamente positivo de la IA sobre productividad, pero con
heterogeneidad muy grande según entorno, tarea y metodología.                ar…



Por eso yo reformularía la tesis como:


     “El modelo por sí solo no determina la productividad; el harness, el contexto, la tarea y

   la forma de uso son factores importantes.”

Eso sí está mucho mejor defendido.




Context engineering: sólido
La distinción entre:
    tener acceso al codebase;
    tenerlo realmente disponible en contexto;
    seleccionar;
    comprimir;
    aislar;
    persistir;

es técnicamente buena.

El material además aclara algo especialmente importante: los porcentajes 50% / 70% /
90% son heurísticas y no umbrales publicados oficialmente por los proveedores.

Eso está bien explicado.

Lost in the Middle también respalda el fenómeno de degradación dependiendo de
dónde se ubica la información dentro de contextos largos.    ACL Anthol…



Lo que evitaría es convertir:


   “puede perder 30+ puntos”

en una regla universal para Claude, GPT, Gemini y cualquier tarea actual.

Depende del modelo, benchmark, cantidad de distractores y tarea.




AGENTS.md: muy bien fundamentado
La explicación de AGENTS.md es esencialmente correcta.

OpenAI contribuyó AGENTS.md a la Agentic AI Foundation y reportó su presencia en más
de 60.000 proyectos open source. También existe adopción entre múltiples
herramientas y vendors.         OpenAI +1



Esta es una de las partes más sólidas del módulo.

Lo que ya envejeció en el módulo 1
La tabla de herramientas dice explícitamente que es un:

   “snapshot abril 2026”.

Por tanto, no es necesariamente un error que tenga modelos antiguos, pero no debe
leerse hoy como lista actual.

Por ejemplo, la documentación actual de Anthropic ya incluye modelos posteriores como
Claude Opus 4.8 y Sonnet 5, mientras el curso habla de Opus 4.7/Sonnet 4.6 como
frontera.      Claude Platfo… +1



Otro pequeño error concreto:

El material habla de la pausa de nuevos registros de Copilot Business desde el 20 de
abril de 2026. GitHub dice oficialmente:


   22 de abril de 2026.            GitHub D… +1




Y la afirmación de “GPT-5.4 = 1M tokens” necesita contexto: el millón de tokens fue
documentado como capacidad experimental en determinados contextos de Codex, no
simplemente como una característica universal que deba trasladarse sin matices.




4. Módulo 2 — Spec-Driven Development
Veredicto: uno de los módulos mejor sustentados
La filosofía fundamental:

   especificación → planificación → implementación → validación

es completamente coherente con el movimiento de Spec-Driven Development actual.

Pero SDD no es una norma internacional única ni existe una organización que haya
decretado “esta es la metodología SDD oficial”. Es mejor entenderlo como un enfoque
emergente con varias implementaciones.

Entre ellas:

    OpenSpec.
    GitHub Spec Kit.
    Kiro.
    otros workflows spec-first.

OpenSpec
El contenido del curso acerca de OpenSpec está bastante actualizado.

El flujo actual documentado incluye:


  /opsx:explore
  /opsx:propose
  /opsx:apply
  /opsx:archive


con explore opcional.         OpenSp… +1




OpenSpec también mantiene comandos más avanzados como:

     new
     continue
     ff
     verify
     sync
     bulk-archive
     onboard

por lo que la arquitectura explicada en el módulo sigue teniendo sentido.    GitHub



También es real la telemetría anónima documentada por OpenSpec; la documentación
especifica que no envía argumentos, paths, contenido del proyecto ni información
personal y permite opt-out.       GitHub +1




GitHub Spec Kit
No es una moda ficticia del curso: el proyecto sigue activo en 2026 y formaliza
precisamente el flujo:

   Specify → Plan → Tasks → Implement.         GitHub




Por tanto, la enseñanza central del módulo 2 está bien apoyada.




5. Módulo 3 — Sistema operativo de copilotos IA
Veredicto: técnicamente sólido
Las explicaciones sobre Claude Code:
     CLAUDE.md ;

    settings por scopes;
    skills;
    subagents;
    hooks;
    MCP;
    plugins;
    aislamiento de contexto;

corresponden a capacidades reales de Claude Code.       Claude +2



La explicación de plugins como paquetes que pueden combinar:

    skills;
    agents;
    hooks;
    servidores MCP;

también coincide con la documentación.     Clau…



Y la idea de que los subagentes permiten mantener contextos separados tiene
fundamento técnico real.    Claude +1




Cursor 3.2
Encontré también la afirmación del curso acerca de Cursor 3.2 del 24 de abril de 2026,
worktrees y multitarea/subagentes.

Es correcta según el changelog oficial.   Cur…



Lo que es heurístico
Consejos como:

   “nueva tarea → nueva sesión”

o evitar mantener una conversación de 80 turnos toda la tarde son muy buenos
operativamente, pero no son leyes científicas. Dependen del agente, sistema de
compaction, tamaño del contexto y naturaleza de las tareas.

Conviene enseñarlos como prácticas recomendadas.




6. Módulo 4 — Planificación efectiva con IA
Aquí encontré algunos de los problemas factuales más claros.

El 83% sí existe

El material afirma:

   “AI4Agile Practitioners Report 2026: 83%...”

Ese dato existe. La encuesta reporta aproximadamente 83% de adopción de IA entre los
participantes, aunque una gran parte todavía la utiliza en una proporción pequeña de su
trabajo.     Scrum.…




Rovo >5 millones: correcto
Atlassian comunicó en sus resultados de Q2 FY26 que Rovo había superado los 5
millones de usuarios activos mensuales.           Atlass…




Así que esa cifra tampoco fue inventada.




🔴 Faros AI: aquí sí hay que corregir
El archivo dice:

   Faros AI Engineering Report 2026
   PR sizes +150%
   bugs +9%
   22.000 developers.

El problema es que mezcla cifras de dos informes diferentes.

Informe Faros 2025
Reportó aproximadamente:
    +154% tamaño de PR;
    +91% tiempo de revisión;
    alrededor de +9% bugs por developer.           Fa…




Informe Faros 2026
Con datos de aproximadamente 22.000 developers reportó, entre otras cosas:
    +51% tamaño de PR;
    +28% bugs por PR;
    aproximadamente +54% bugs por developer;
    fuertes incrementos en tiempos de revisión, churn e incidentes.   Fa… +1


Por tanto:

   “Faros 2026 = +150% PR size y +9% bugs” es incorrecto.

Es probablemente una mezcla accidental del informe anterior.




🔴 DORA 2025 y el supuesto 42%
El curso afirma:

   “DORA 2025: el 42% de equipos admite manipular las métricas de velocity cuando se
   vinculan a performance reviews.”

Revisé el material oficial de DORA 2025 y no pude localizar esa cifra atribuida a
DORA.      Dora +1



Por tanto, no debería mantenerse con esa atribución sin proporcionar la fuente exacta.

La recomendación que viene después sí es buena:


   no usar story points/velocity como medida individual de productividad.

Pero eso no convierte automáticamente el 42% en un dato DORA.




🔴 Capgemini y “15% menos rework”
La afirmación:

   “generar criterios de aceptación con IA reduce el rework ~15%”

atribuida a Capgemini tampoco pude reproducirla en una fuente primaria de Capgemini.

No afirmaría que sea falsa, pero sí:

   no está suficientemente sustentada tal como aparece actualmente.

Debe incluir paper/informe/página exacta o eliminarse el porcentaje.




La idea general del módulo sí tiene respaldo
La investigación reciente sobre estimación y planificación asistida por LLM muestra
resultados prometedores, incluyendo trabajos de 2025-2026 sobre story points y sistemas
multiagente de estimación.     arXiv +1



Pero eso no demuestra que:

     “la implementación ya sea barata y la planificación sea ahora el cuello de botella
     universal”.

Eso sigue siendo una tesis razonable del autor, no una ley general de ingeniería de
software.




7. Módulo 5 — Documentación efectiva con IA
Veredicto: fundamentos muy buenos
La combinación de:
      ADRs;
      C4;
      Mermaid;
      Structurizr;
      OpenAPI;
      TSDoc/TypeDoc;
      docs-as-code;
      linters;
      link checking;

está muy bien encaminada.

C4
El modelo C4 efectivamente estructura arquitectura en niveles como:
 1. System Context.
 2. Container.
 3. Component.
 4. Code.

Y su propia documentación explica que Context + Container son suficientes para muchos
equipos.         C4 mo…



Structurizr es una herramienta/model-as-code creada específicamente alrededor del
enfoque C4.          Structu…



Mermaid también dispone de sintaxis para diagramas de arquitectura y soporte
relacionado con C4, aunque Mermaid no es “el modelo C4”: Mermaid es una
herramienta/sintaxis; C4 es el modelo conceptual.       Mermaid

Testing de documentación
Vale como prose linter es real y dispone de integración oficial con GitHub Actions.
   Vale Document…



TypeDoc también es una herramienta real para convertir información y comentarios de
proyectos TypeScript en documentación HTML/JSON.          Type…



Vale + markdownlint + lychee + TypeDoc es una arquitectura perfectamente razonable
para CI documental.

Pero hay cifras que deben etiquetarse como ejemplos
Por ejemplo:

   “la GitHub Action completa corre en menos de 2 minutos”.

Eso no puede ser una afirmación general.

Depende de:

    cantidad de archivos;
    runner;
    caché;
    red;
    cantidad de links;
    configuración.

Lo mismo ocurre con afirmaciones del tipo:

   “576 links en ~60 segundos”.

Eso puede ser un benchmark del proyecto del autor, pero no una propiedad de lychee.




🟡 llms.txt necesita un matiz importante
El curso lo presenta como:

   “el robots.txt para agentes IA”.

La analogía sirve pedagógicamente, pero técnicamente puede inducir a error.

llms.txt sigue siendo una propuesta/convenio emergente, no un estándar de Internet
ratificado comparable a robots.txt . La propia fuente original lo describe como una
propuesta.          llms-txt +1



Y a diferencia de robots.txt , no establece reglas de crawling obligatorias.

Yo lo explicaría como:


   “una convención emergente para ofrecer documentación optimizada a LLMs”.

Eso sería preciso.




8. Módulo 6 — Ética, regulación y privacidad
Este es el módulo que más urgentemente necesita actualización, porque la ley y las
políticas de proveedores han cambiado durante 2026.

GDPR: base correcta
El GDPR entró en aplicación en mayo de 2018 y los principios de:
    minimización;
    transparencia;
    privacy by design;
    bases legales;
    derechos de acceso/rectificación;
    tratamiento automatizado;

están correctamente tratados en términos generales.

Pero el DPIA está expresado demasiado ampliamente
El curso dice, esencialmente:

   cualquier IA que procese datos a gran escala o tome decisiones automatizadas debe
   hacer DPIA.

El artículo 35 no dice eso.

La condición general es que el tratamiento:


   sea probable que entrañe un alto riesgo para los derechos y libertades de las
   personas.

Después enumera situaciones particulares.     Eur-…



Así que debe cambiarse de “cualquier sistema” a “cuando el tratamiento probablemente
implique alto riesgo”.

9. 🔴 EU AI Act: la cronología del repo ya quedó
desactualizada
El archivo conserva esta cronología:
    agosto 2026 → sistemas de alto riesgo del Anexo III;
    agosto 2027 → aplicación restante.

Eso reflejaba la situación normativa anterior.

Pero el 7 de mayo de 2026 se alcanzó un acuerdo político respecto al AI Omnibus que
modifica el calendario. La Comisión Europea informa actualmente de fechas posteriores
para determinadas obligaciones de sistemas de alto riesgo:

    determinadas categorías del Anexo III: 2 de diciembre de 2027;
    IA integrada en productos regulados: 2 de agosto de 2028.       Digital Strat…



Al mismo tiempo, no significa que “el AI Act se haya aplazado entero”.

Las obligaciones de transparencia del artículo 50 siguen teniendo como fecha relevante 2
de agosto de 2026, y la Comisión publicó directrices sobre ellas el 20 de julio de 2026.
   Digital Strat… +1



Esa distinción debería corregirse en el curso.




10. GitHub Copilot y uso de datos: esencialmente
correcto, pero hay que actualizarlo
El módulo explica que desde abril de 2026 GitHub puede utilizar las interacciones de
usuarios individuales para entrenar modelos salvo opt-out.

Esto sí es verdadero.

GitHub anunció el 25 de marzo de 2026 que, desde el 24 de abril de 2026, datos como:

    inputs;
    outputs;
    fragmentos de código;
    contexto asociado;

de Copilot Free, Pro y Pro+ serían utilizados para entrenar/mejorar modelos salvo opt-out.
   The GitHub B… +1



La documentación actual ya incluye además Copilot Max entre los planes individuales a
los que puede aplicarse esa política. Business y Enterprise no se utilizan para entrenar

modelos de GitHub.      GitHub D… +1



Por tanto la idea del curso es correcta, pero la tabla necesita mantenimiento.




11. Seguridad: el 45% de Veracode existe, pero está
redactado demasiado universalmente
Tu módulo dice:

   “el 45% del código generado por IA tiene vulnerabilidades”.

Veracode sí publicó una evaluación de más de 100 modelos donde aproximadamente
45% de las muestras fallaron las pruebas de seguridad e introdujeron
vulnerabilidades OWASP Top 10.         Verac…




Por tanto el número no es inventado.

Pero debe escribirse:


   “En la evaluación de Veracode, el 45% de las muestras…”

y no:

   “El 45% de todo código generado por IA…”

Son afirmaciones científicamente diferentes.

Otros estudios encuentran tasas distintas según lenguaje, modelo, tarea y metodología.
   ar…



Lo mismo ocurre con slopsquatting: el riesgo es real, pero el porcentaje de paquetes
alucinados cambia radicalmente entre familias y generaciones de modelos; una
evaluación de 2026 obtuvo alrededor de 4,62–6,10% en su cohorte de modelos frontier.
   ar…



No conviene enseñar un porcentaje único como constante.




12.     🔴 El acuerdo de Anthropic ya no está “pendiente”
El módulo 6 fue escrito cuando algunos litigios seguían evolucionando.

En concreto, el acuerdo de USD 1.500 millones de Anthropic que aparece tratado como
pendiente/inminente ya cambió de estado:

   el juez concedió la aprobación final el 20 de julio de 2026.

Hay tanto documentación judicial como cobertura de Reuters sobre la aprobación.
   Justia Dockets… +1



Eso ocurrió hace seis días respecto a hoy, 26 de julio de 2026.

Por tanto es un ejemplo claro de contenido que era razonable cuando se preparó el
curso y simplemente quedó desactualizado.

Para Doe v. GitHub, en cambio, localicé los argumentos orales del 11 de febrero de 2026,
pero no una opinión publicada posterior del Noveno Circuito hasta la fecha de esta
revisión.       Chat GPT Is E… +1




13. LLM locales
La tesis de que los LLM locales se han vuelto mucho más prácticos es correcta.

Por ejemplo, NVIDIA ofrece actualmente DGX Spark con:

    128 GB de memoria unificada;
    precio actual oficial alrededor de USD 4.699;
    capacidad anunciada por NVIDIA para inferencia de modelos de hasta 200B
    parámetros bajo sus condiciones.      NVIDIA Market… +1



AMD también dispone de plataformas Ryzen AI Max+ con hasta 128 GB de memoria
unificada y 256 GB/s de ancho de banda.       AMD +1



Lo que no está demostrado
El curso afirma que un modelo local puede cubrir:

   “70–80% de las tareas diarias”

y el cloud queda para el restante 20–30%.

Eso no debería presentarse como dato.

Es una estimación/experiencia del autor.

La investigación sobre inferencia local muestra que la viabilidad depende muchísimo de:

    modelo;
    cuantización;
    memoria;

    runtime;
    contexto;
    task;
    throughput esperado.       ar…


Yo conservaría la idea, pero la etiquetaría:

   “regla práctica del autor, no benchmark universal”.




14. Módulo 7 — Testing y TDD
Veredicto: buena base de ingeniería
Red → Green → Refactor, Fake It, tests unitarios, integración, E2E, mutation testing,
Testcontainers, Playwright, property-based testing, etc. son conceptos reales y bien
asentados.

fast-check , por ejemplo, es efectivamente una biblioteca de property-based testing que
genera múltiples entradas y aplica shrinking para reducir contraejemplos.     Fast Ch… +1



Playwright MCP también está bien explicado: puede trabajar mediante snapshots
estructurados de accesibilidad en lugar de depender obligatoriamente de screenshots o
visión.     Playwright +1



Y GitHub Copilot Coding Agent alcanzó GA en septiembre de 2025 y trabaja en un
entorno aislado para producir PRs, así que esa parte también está respaldada.
   The GitHub B…




🟡 “TDD elimina la validación circular” es demasiado absoluto
El curso dice:

   “Esto elimina el problema de la validación circular”.

Yo cambiaría elimina por reduce.

Porque si el propio agente genera un test equivocado a partir de una interpretación
equivocada de la spec, tener el test primero no garantiza automáticamente que la
interpretación sea correcta.

De hecho, investigación de 2026 en desarrollo asistido por agentes muestra que el simple
prompting TDD no evita por sí mismo regresiones y que la calidad del
contexto/arquitectura sigue siendo determinante.     ar…

TDD sigue siendo una excelente barrera, pero no una prueba matemática de corrección.




15.    🔴 Qodo está desactualizado
El archivo afirma:

   “Qodo … Tier gratuito con 250 créditos/mes.”

El cambio de nombre CodiumAI → Qodo en 2024 sí ocurrió.        Qodo




Pero el pricing actual de Qodo ya no ofrece ese tier gratuito permanente de 250
créditos/mes. La oferta actual contempla una prueba gratuita temporal y planes de pago.
   Qodo



Este dato hay que actualizarlo.




16. Cursor /test : no pude verificarlo
El módulo dice:

   “Cursor — comando /test ”.

Busqué documentación/changelog actual de Cursor y no pude confirmar /test como
comando oficial vigente.

Eso no demuestra que jamás haya existido en alguna versión o integración, pero para un
curso de 2026 no lo enseñaría como hecho sin:

      URL oficial;
      versión;
      fecha.

Esta entrada necesita verificación o eliminación.




17. Problemas puramente editoriales que encontré
Estos no significan que la materia esté equivocada.

1. Lección 1 del módulo 1 duplicada
En:

Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/1. El modelo mental de
los 3 pilares.md


el contenido comienza una vez y luego vuelve a arrancar desde el encabezado alrededor
de la línea 98.

Hay que eliminar una de las dos versiones.

2. Módulo 6 también contiene una introducción GDPR duplicada
El archivo comienza con una introducción y después vuelve a empezar:

    ## Introducción a GDPR


alrededor de la línea 41.

Además aparece el typo:

    datosen


en lugar de datos en .

3. Quedó un artefacto interno de ChatGPT
En el módulo 2 aparece literalmente:


  :contentReference[oaicite:0]{index=0}


después de la recomendación de YouTube.

Eso no pertenece al curso y debe borrarse.

4. Nombre de archivo con typo
Tienes:


  1. ntroducción a TDD.md


Debería ser:


  1. Introducción a TDD.md




18. Las correcciones prioritarias que yo haría
No reescribiría el curso. Conservaría la gran mayoría. Pero sí corregiría, en este orden:

Prioridad           Problema                    Acción

🔴1                  EU AI Act                   Actualizar calendario 2026–2028


🔴2                  Faros 2026                  Cambiar +150%/+9% por cifras del informe
                                                correcto


🔴3                  DORA “42%”                  Eliminar o aportar fuente exacta


🔴4                  Capgemini “15%”             Eliminar porcentaje o proporcionar fuente
                                                primaria


🔴5                  Anthropic settlement        Cambiar “pendiente” → aprobado el 20-jul-
                                                2026


🔴6                  Qodo 250 créditos gratis    Actualizar pricing


🟠7                  Veracode 45%                Atribuirlo al experimento, no universalizar


🟠8                  GDPR DPIA                   Cambiar “cualquier sistema” por criterio de
                                                alto riesgo


🟠9                  llms.txt                    Llamarlo propuesta/convenio emergente


🟠 10                TDD “elimina”               Cambiar por “reduce”


🟡 11                Cursor /test                Verificar versión/fuente o eliminar


🟡 12                Copilot                     Corregir 20 → 22 abril y actualizar planes


🟡 13                Modelos/precios             Mantener etiqueta “snapshot abril 2026”


🟡 14                Archivos                    Eliminar duplicados, marcador oaicite y
                                                typo




Mi veredicto final
No descartaría este curso. Todo lo contrario.

Los pilares conceptuales son bastante buenos:

Módulo 1: herramienta + contexto + prompt → sólido como modelo mental.
Módulo 2: SDD/OpenSpec → muy bien alineado con el ecosistema actual.

Módulo 3: Claude Code, skills, hooks, MCP, subagents → fuerte y práctico.
Módulo 4: planificación IA → buena tesis, pero es el módulo con varias estadísticas que
necesitan corrección.
Módulo 5: docs-as-code, ADR, C4, CI → muy sólido.
Módulo 6: seguridad/privacidad → concepto sólido, pero necesita actualización urgente
por los cambios legales de 2026.
Módulo 7: TDD/testing + IA → buena ingeniería; necesita moderar algunas afirmaciones y
actualizar Qodo/Cursor.

La diferencia fundamental que incorporaría al material es etiquetar cada afirmación como
una de estas cuatro categorías:


   [HECHO VERIFICADO] respaldado directamente por fuente.
   [EVIDENCIA LIMITADA] paper/estudio real, pero no generalizable.
   [HEURÍSTICA] buena práctica basada en experiencia.
   [SNAPSHOT] precio, versión, modelo o estado legal válido en una fecha concreta.

Con ese cambio y las correcciones anteriores, el repositorio pasaría de ser simplemente
“material de un curso” a convertirse en una base de conocimiento mucho más rigurosa
y auditable, donde puedes aprender sin confundir una opinión razonable con un hecho
demostrado.                                        



                               Quiero que hagamos un proyecto empezando por Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA paso a paso, detalladamente, me guiaras en el proyecto de forma masticada como si guiaras a un niño, sin omitir informacion, poniendo en practica todo el contenido sin omitir nada, me diras la cantidad de pasos totales y al terminar cada paso me preguntaras si deseo continuar con el siguiente paso, cada paso usara su maxima ventana de contexto, el proyecto sera real, profesional, full stack, podria ser un crm pero basico, poco a poco lo mejoraremos, creadolo con Claude Code, quiero que ingreses la informacion maxima recomendable en cada md, ya sea CLAUDE/AGENTS.md, tambien al finalizar todos los pasos del Modulo 1, te paso despues el modulo 2 de sdd con openspec para que haga match con lo que se hizo con el modulo 1, vamos por partes, esta es la primera parte, tambien quiciera dividir el proyecto full stack, cada uno con su propio md y que cada uno tenga su maxima informacion sin superar sus limites, investiga exhaustivamente y busca en fuentes confiables sin inventar datos como hacer este modulo 1, con datos mas recientes hasta julio 2026, si me entiendes?.


Worked for 2m 19s

Sí. Y vamos a hacerlo como un proyecto de verdad, no como una colección de ejercicios
aislados.

Voy a tomar todo el Módulo 1 como metodología de trabajo: no solo vamos a programar
un CRM, sino que iremos construyendo conscientemente el harness, el contexto y los
prompts alrededor de Claude Code, tal como plantea el curso. Tu propio material define
esos tres pilares como Herramienta, Contexto y Prompt y sostiene que deben combinarse,
no estudiarse aisladamente.

Además, voy a corregir durante el proyecto cualquier recomendación del curso que haya
envejecido. Por ejemplo, la documentación actual de Anthropic ya recomienda
explícitamente que un CLAUDE.md apunte a menos de 200 líneas; llenarlo simplemente
“hasta el máximo” puede consumir contexto y reducir la adherencia. Por eso buscaremos
máxima información útil, no máximo volumen de texto.       Claude +1




Proyecto

Nombre de trabajo:


   crm-profesional


Será un monorepo full stack profesional, inicialmente pequeño.

Tecnología base que propongo al 26 de julio de 2026:

Capa                                  Tecnología

Backend                               Java 25 + Spring Boot 4.1


Build backend                         Maven + Maven Wrapper


Frontend                              React 19.2 + TypeScript


Tooling frontend                      Vite 8.1


Runtime frontend                      Node.js 24 LTS


Base de datos                         PostgreSQL 18


Infraestructura local                 Docker Compose


IA de desarrollo                      Claude Code


Control de versiones                  Git


Arquitectura repo                     Monorepo


API                                   REST/JSON


Migraciones                           Flyway


Validación                            Backend + frontend


Testing inicial                       Básico; profundizaremos cuando lleguemos al módulo
                                      de testing



La elección es deliberadamente estable. Spring Boot 4.1 soporta Java 17–26; Java 25 es
una versión con soporte prolongado ofrecido por los principales vendors; Node 24 está
actualmente en LTS mientras Node 26 sigue siendo Current, y el propio proyecto Node
recomienda usar versiones LTS para producción. React tiene actualmente la línea 19.2 y
Vite mantiene 8.1 como línea estable con parches regulares. PostgreSQL 18 es la versión
mayor estable actual; 19 sigue en beta.     Home +5

Y usaremos siempre:


      Bash

  ./mvnw


o en Windows:


      PowerShell

  mvnw.cmd


en vez de depender del Maven global de la máquina. El Maven Wrapper existe
precisamente para que todos construyan el proyecto con la distribución definida por el
propio proyecto.    Apache Ma… +1




Los 18 pasos del Módulo 1
No voy a saltarme ninguno.

Bloque A — Fundamentos
Paso 1. Definir exactamente qué vamos a construir y preparar el laboratorio.
Paso 2. Crear el repositorio y la estructura inicial del monorepo.
Paso 3. Entender y configurar el Pilar 1: Claude Code como herramienta y harness.

Bloque B — Harness de Claude Code
Paso 4. Configurar permisos, Plan Mode y política segura de ejecución.
Paso 5. Crear .claude/settings.json , separar settings.local.json y configurar el
proyecto correctamente.
Paso 6. Diseñar los hooks deterministas y distinguir “instrucción” de “regla ejecutable”.

Bloque C — Context Engineering
Paso 7. Diseñar la arquitectura completa de contexto del monorepo.
Paso 8. Crear AGENTS.md y CLAUDE.md de la raíz.
Paso 9. Crear backend/AGENTS.md y backend/CLAUDE.md .
Paso 10. Crear frontend/AGENTS.md y frontend/CLAUDE.md .
Paso 11. Crear reglas con alcance por rutas en .claude/rules/ .
Paso 12. Crear subagentes, aislamiento de contexto y estrategia de
memoria/compactación.

Bloque D — Prompt Engineering

Paso 13. Construir nuestro estándar profesional de prompts para Claude Code.

Bloque E — Proyecto real
Paso 14. Crear el backend real con Spring Boot + PostgreSQL.
Paso 15. Crear el frontend real con React + TypeScript + Vite.
Paso 16. Integrar PostgreSQL, Docker Compose, backend y frontend.
Paso 17. Construir nuestra primera funcionalidad CRM completa usando Explore → Plan
→ Execute.

Bloque F — Integración de los tres pilares
Paso 18. Auditoría final del Módulo 1: herramienta + contexto + prompt, limpieza del
repositorio y preparación exacta para introducir OpenSpec en el Módulo 2.

Al terminar el paso 18 tendremos algo que funciona, no solamente una plantilla.

Y en ese momento no improvisaremos el módulo 2: introduciremos OpenSpec sobre esta
misma base.




PASO 1 DE 18
Definir qué construiremos y preparar el laboratorio
En este primer paso todavía no vamos a pedirle a Claude que escriba código.

Eso es intencional.

Es exactamente la primera enseñanza que quiero que interiorices.

1.1. El error que queremos evitar
Una persona abre Claude Code y escribe:


  Hazme un CRM profesional con Spring Boot y React.


Claude puede generar cientos o miles de líneas.

Pero todavía no sabemos:

    qué significa CRM;
    qué funcionalidades necesitamos;
    qué tecnología exacta utilizaremos;
    qué debe quedar fuera;
    dónde irá el backend;

    dónde irá el frontend;
    cuáles son nuestros comandos;
    cuál es nuestra arquitectura;
    qué puede modificar Claude;
    qué no puede modificar;
    cómo verificaremos que terminó;
    qué contexto debe cargar;
    qué contexto debe permanecer fuera;
    qué reglas son generales;
    qué reglas pertenecen solo al backend;
    cuáles pertenecen al frontend.

Por eso generación rápida de código ≠ ingeniería.

Ese es precisamente el razonamiento detrás del Módulo 1.




1.2. Nuestro modelo mental
Piensa en Claude como un empleado nuevo extraordinariamente rápido.

Tenemos tres problemas diferentes.

Herramienta
Es lo que Claude puede hacer.

Claude Code puede acceder al proyecto, utilizar el terminal, observar Git, leer CLAUDE.md ,
usar memoria, skills, subagentes, MCP y otras extensiones configuradas.      Clau…



Esto es:


  HERRAMIENTA
           ↓
  Claude Code
           ↓
  Read
  Edit
  Bash
  Grep
  Git
  subagents
  hooks
  skills
  MCP

  permissions




Contexto
Es lo que Claude sabe en este momento.

Por ejemplo:


  Estamos construyendo un CRM.
  Backend = Spring Boot.
  Frontend = React.
  DB = PostgreSQL.


  La lógica de negocio no debe estar
  en los controllers.


  El frontend nunca habla directamente
  con PostgreSQL.


  Antes de terminar ejecuta los tests.


Esto pertenece principalmente al contexto persistente.




Prompt
Es:

      qué queremos que haga ahora.

Por ejemplo:


  Implementa la creación de clientes.


Pero un prompt profesional será mucho más preciso:


  OBJETIVO


  Implementar la creación de clientes.


  CRITERIOS DE ÉXITO


  - POST /api/customers devuelve 201.
  - Valida nombre y email.
  - Persiste el cliente en PostgreSQL.
  - Los tests correspondientes pasan.

  RESTRICCIONES


  - No cambies otras funcionalidades.
  - No añadas dependencias nuevas.
  - Respeta la arquitectura existente.


  VERIFICACIÓN


  Ejecuta los tests afectados antes
  de considerar finalizada la tarea.

Anthropic sigue recomendando definir primero criterios de éxito verificables antes de
intentar optimizar prompts.   Claude Platfo… +1



Eso será muy importante más adelante.




1.3. Qué CRM vamos a construir
La primera versión será deliberadamente sencilla.

No vamos a intentar fabricar Salesforce.

Nuestro producto será:


   CRM Profesional: aplicación web para gestionar clientes comerciales de una
   pequeña empresa.

Inicialmente tendremos una única capacidad de negocio suficientemente completa para
recorrer todo el stack:

Gestión de clientes
Cada cliente podrá tener inicialmente:


  id
  name
  email
  phone
  company
  status
  notes
  createdAt
  updatedAt


No debes preocuparte todavía por cómo se representan en Java.

No estamos diseñando aún la entidad.

Simplemente estamos definiendo el producto.




1.4. Funcionalidades de nuestra primera versión
Al finalizar el Módulo 1 tendremos al menos:


  Dashboard
     │
     └── resumen básico de clientes


  Clientes
     │
     ├── listar
     ├── buscar
     ├── filtrar
     ├── crear
     ├── consultar detalle
     ├── editar
     └── archivar


La interfaz será real.

El backend será real.

Los datos estarán en PostgreSQL.

No vamos a utilizar arrays ficticios del frontend como almacenamiento definitivo.




1.5. Cosas que conscientemente NO construiremos
todavía
Esto es extremadamente importante.

Un proyecto profesional también define sus non-goals.

Todavía NO haremos:


  ❌ autenticación completa
  ❌ autorización por roles
  ❌ leads avanzados
  ❌ pipeline de oportunidades
  ❌ tareas comerciales
  ❌ calendario
  ❌ integración con correo
  ❌ WhatsApp

  ❌ facturación
  ❌ reportes complejos
  ❌ archivos adjuntos
  ❌ microservicios
  ❌ Kafka
  ❌ Redis
  ❌ Kubernetes
  ❌ cloud
  ❌ OpenSpec
  ❌ MCP personalizado
  ❌ agentes IA dentro del producto
No significa que estas funcionalidades sean malas.

Significa:


   todavía no las necesitamos.

Esto evita algo muy común cuando se programa con agentes:

sobreingeniería generada por IA.



1.6. ¿Por qué no vamos a empezar con microservicios?
Nuestro CRM es pequeño.

Por tanto:


  backend único
  +
  frontend único
  +
  PostgreSQL


es suficiente.

Tendremos:


  ┌────────────────────┐
  │          React      │
  │     Frontend        │
  └─────────┬──────────┘
              │ HTTP/JSON
              ▼
  ┌────────────────────┐
  │    Spring Boot      │
  │      Backend        │

  └─────────┬──────────┘
                 │ SQL/JPA
                 ▼
  ┌────────────────────┐
  │      PostgreSQL          │
  └────────────────────┘

Eso ya permite trabajar profesionalmente sobre:
      arquitectura;
      API;
      persistencia;
      migraciones;
      validaciones;
      testing;
      manejo de errores;
      seguridad posteriormente;
      frontend;
      integración.

No necesitamos añadir complejidad artificial.




1.7. Por qué será un monorepo
Tendremos:


  crm-profesional/
  │
  ├── backend/
  │
  ├── frontend/
  │
  ├── docs/
  │
  ├── .claude/
  │
  ├── AGENTS.md
  │
  ├── CLAUDE.md
  │
  ├── compose.yml
  │
  ├── README.md
  │
  └── .gitignore


Esto es muy importante para nuestro estudio de context engineering.

Porque tendremos:


  Contexto global
               │
               ├── contexto backend
               │
               └── contexto frontend


Es decir:


  crm-profesional/
  │
  ├── AGENTS.md
  ├── CLAUDE.md
  │
  ├── backend/
  │   ├── AGENTS.md
  │   ├── CLAUDE.md
  │   └── ...
  │
  └── frontend/
      ├── AGENTS.md
      ├── CLAUDE.md
      └── ...


Y aquí entra uno de los conceptos más importantes del módulo.




1.8. ¿Por qué tendremos AGENTS.md Y CLAUDE.md?
Porque no son exactamente lo mismo.

AGENTS.md es actualmente un formato abierto y multi-vendor. OpenAI lo aportó a la
Agentic AI Foundation de Linux Foundation en diciembre de 2025; OpenAI reportaba más
de 60.000 proyectos OSS adoptándolo.      OpenAI +1



Pero Claude Code actualmente dice explícitamente:


   Claude Code lee CLAUDE.md , no AGENTS.md directamente.

Anthropic recomienda, cuando ya tienes AGENTS.md , hacer que CLAUDE.md lo importe.
   Clau…



Por tanto utilizaremos:


  AGENTS.md
           │

       │ Fuente portable
       │ de instrucciones
       ▼
  CLAUDE.md
       │
       │ @AGENTS.md
       ▼
  Claude Code


Por ejemplo:


     Markdown

  @AGENTS.md


  ## Claude Code


  - Usa Plan Mode para cambios complejos.
  - No implementes cambios fuera del alcance solicitado.


Esto nos proporciona:

Portabilidad
AGENTS.md puede servir a otros agentes.


Especialización
CLAUDE.md contiene únicamente cosas particulares de Claude Code.




1.9. Algo MUY importante: no duplicaremos
información
NO quiero esto:


  AGENTS.md
    contiene 150 líneas


  CLAUDE.md
    copia las mismas 150 líneas


Porque tendremos dos fuentes que pueden divergir.

Haremos:


  AGENTS.md
           ↓

   información portable


  CLAUDE.md
         ↓
   @AGENTS.md
   +
   instrucciones Claude-específicas

Una fuente de verdad.




1.10. Tampoco vamos a importar backend y frontend
completos desde la raíz
Este detalle es importantísimo.

Podríamos hacer:


       Markdown

  @AGENTS.md
  @backend/AGENTS.md
  @frontend/AGENTS.md


dentro del CLAUDE.md raíz.

Parece conveniente.

Pero sería una mala decisión.

¿Por qué?

Porque los imports de CLAUDE.md también consumen contexto. Separarlos en
diferentes archivos no reduce tokens si todos son importados al inicio. Anthropic lo señala
expresamente.      Claude +1



Entonces aprovecharemos la carga jerárquica.

Claude Code carga las instrucciones raíz inicialmente y descubre las instrucciones de
subdirectorios cuando comienza a leer archivos de esos directorios.     Claude +1



Así:


  Trabajando en cualquier parte:


  root/CLAUDE.md
  root/AGENTS.md

               ↓


  Claude entra a backend/


               ↓


  backend/CLAUDE.md
  backend/AGENTS.md


               ↓


  Claude entra a frontend/


               ↓


  frontend/CLAUDE.md
  frontend/AGENTS.md

Eso es aislamiento de contexto.

Y es exactamente lo que queremos practicar.




1.11. Cuánto contenido meteremos en cada MD
Aquí corrijo deliberadamente la idea de “meter el máximo posible”.

El objetivo será:


   máxima densidad útil.

No:

   máximo número de tokens.

Anthropic recomienda actualmente mantener CLAUDE.md por debajo aproximadamente de
200 líneas; los archivos largos consumen contexto y pueden reducir el seguimiento
individual de las reglas.    Clau…



Nuestra política será aproximadamente:


  root/AGENTS.md
  ≈ 120–170 líneas


  root/CLAUDE.md
  ≈ 20–60 líneas

  backend/AGENTS.md
  ≈ 130–180 líneas


  backend/CLAUDE.md
  ≈ 20–50 líneas



  frontend/AGENTS.md
  ≈ 130–180 líneas


  frontend/CLAUDE.md
  ≈ 20–50 líneas

Estos rangos son nuestra heurística de diseño, no límites oficiales de AGENTS.md.

La información más extensa vivirá en:


  docs/


o en reglas cargadas selectivamente.




1.12. ¿Qué meteremos en AGENTS.md?
Información que un desarrollador nuevo necesitaría conocer siempre.

Por ejemplo:


  Project overview


  Architecture


  Repository layout


  Technology stack


  Important commands


  General coding conventions


  Git workflow


  Error-handling expectations


  Testing expectations


  Security invariants


  Dependency policy

  Definition of done


  Important gotchas




1.13. ¿Qué NO meteremos ahí?
No vamos a convertirlo en Wikipedia.

No meteremos:


  ❌ tutorial completo de Java
  ❌ tutorial completo de React
  ❌ documentación de Spring
  ❌ documentación de PostgreSQL
  ❌ 300 ejemplos
  ❌ conversaciones anteriores
  ❌ logs
  ❌ decisiones temporales
  ❌ instrucciones de una sola tarea
  ❌ documentación copiada de Internet
Porque eso contaminaría el contexto.




1.14. ¿Dónde irá la información específica?
Tendremos varias capas.


                       ┌──────────────────┐
                       │   AGENTS.md       │
                       │ contexto estable │
                       └────────┬─────────┘
                               │
                               ▼
                       ┌──────────────────┐
                       │   CLAUDE.md       │
                       │ Claude-specific   │
                       └────────┬─────────┘
                               │
                ┌──────────────┼──────────────┐
                ▼              ▼               ▼
         .claude/rules      skills         subagents
         por rutas          workflows      contexto aislado


Anthropic recomienda precisamente mover procedimientos largos o información relevante
solo para determinadas partes del codebase fuera del CLAUDE.md ; las reglas con paths

pueden cargarse únicamente cuando Claude trabaja con los archivos correspondientes.
   Clau…




1.15. Por qué esto importa
Imagina que Claude está haciendo:


  frontend/src/pages/CustomersPage.tsx


No necesita mantener permanentemente en contexto reglas como:


  Spring @Transactional
  Hibernate mappings
  Flyway migrations
  Maven dependency rules
  JPA repositories


Y cuando trabaja en:


  backend/src/main/java/...


no necesita recordar constantemente:


  React hooks
  component composition
  ARIA roles
  TanStack Query conventions
  CSS architecture


El contexto debe ser:


  pequeño
  +
  relevante
  +
  preciso


No:


  todo lo que sabemos


La investigación de Chroma sigue mostrando que la confiabilidad de los modelos puede
deteriorarse conforme crece el input incluso antes de alcanzar el límite físico del contexto.
   Chro…

Por eso:


   una ventana enorme es capacidad disponible, no una invitación a llenarla.




1.16. Nuestra estrategia de sesiones
Tampoco tendremos una sola sesión de Claude Code durante semanas.

Usaremos:


  Tarea A
     ↓
  sesión A


  Tarea B distinta
     ↓
  sesión B


Cuando una subtarea produzca mucha exploración:


  Main Agent
         │
         ├── Subagent Explore Backend
         │
         ├── Subagent Explore Frontend
         │
         └── devuelve conclusiones


Claude Code recomienda delegar investigación a subagentes precisamente porque las
lecturas extensas del codebase llenan el contexto del agente principal; el subagente
trabaja con su propia ventana y devuelve un resumen.     Clau…



Más adelante lo haremos de verdad.




1.17. No usaremos porcentajes mágicos de 50/70/90
como reglas duras
Tu curso menciona heurísticas sobre:


  50%
  70%
  90%

del contexto.

Las conservaremos como intuición, no como ley científica.

Nuestra regla profesional será más sencilla:


     ¿La conversación sigue centrada
     en UNA tarea coherente?


                         │
           ┌───────┴─────────┐
           │                      │
         sí                      no
           │                      │
     continuar               sesión nueva


Y:


     ¿la exploración produce demasiado ruido?
                  │
                 sí
                  │
            subagente


Y:


     ¿el contexto acumulado está perjudicando
     la claridad?
                  │
                 sí
                  │
            compactar
            o reiniciar


Anthropic hoy recomienda la compactación para conversaciones y workflows agénticos
largos justamente porque mantener demasiado historial puede reducir el foco.
     Claude Platfo… +1




1.18. Estrategia de permisos
Al principio NO vamos a utilizar:


         Bash

     --dangerously-skip-permissions

Ni:


  bypassPermissions


Trabajaremos con:


  plan


y después:


  acceptEdits


cuando entendamos exactamente lo que Claude va a hacer.

Plan Mode permite que Claude:

      lea;
      explore;
      investigue;
      proponga un plan;

pero no modifique el código fuente hasta que aprobemos el plan.   Claude +1




Eso es perfecto para aprender.




1.19. Cómo sabremos que el Módulo 1 realmente fue
aprendido
No bastará con que el CRM funcione.

Al finalizar deberás ser capaz de explicar:

Herramienta

  ¿Qué diferencia existe entre modelo
  y harness?


  ¿Por qué Claude Code no es simplemente
  "Claude en una terminal"?


  ¿Qué hacen permissions?


  ¿Qué hace Plan Mode?


  ¿Qué diferencia hay entre instrucción

  y hook?


  ¿Qué hace un subagent?



Contexto

  ¿Qué carga el root CLAUDE.md?


  ¿Por qué backend tiene otro?


  ¿Por qué frontend tiene otro?


  ¿Qué contiene AGENTS.md?


  ¿Qué contiene CLAUDE.md?


  ¿Qué contiene CLAUDE.local.md?


  ¿Por qué settings.local.json
  no se versiona?


  ¿Qué información debe vivir en rules?


  ¿Qué debe convertirse en skill?


  ¿Cuándo crear una sesión nueva?


  ¿Cuándo utilizar subagentes?



Prompt

  ¿Qué es un objetivo?


  ¿Qué son criterios de éxito?


  ¿Qué son restricciones?


  ¿Qué recursos debe consultar Claude?


  ¿Qué es una definición de terminado?


  ¿Por qué no debemos microgestionar
  cada paso del razonamiento?


Y deberás poder mirar una tarea y decidir:


  ¿Tengo un problema de...


  herramienta?

  contexto?


  prompt?


Ese es el verdadero resultado del Módulo 1.




1.20. Ahora vamos a revisar tu laboratorio
Todavía no generes el proyecto.

Abre Git Bash o la terminal desde la que utilizas normalmente Claude Code.

Ejecuta exactamente:


      Bash

  printf '\n=== Git ===\n'
  git --version


  printf '\n=== Claude Code ===\n'
  claude --version
  claude doctor


  printf '\n=== Java ===\n'
  java -version


  printf '\n=== Node.js ===\n'
  node --version


  printf '\n=== npm ===\n'
  npm --version


  printf '\n=== Docker ===\n'
  docker --version


  printf '\n=== Docker Compose ===\n'
  docker compose version


No instales nada todavía si alguno falla.

Quiero primero observar la realidad de tu máquina.




¿Por qué NO compruebo Maven?
Porque nuestra aplicación traerá:

  mvnw
  mvnw.cmd


El proyecto controlará su propia versión de Maven mediante Maven Wrapper.
   Apache Ma…



Eso elimina una dependencia global innecesaria.




1.21. Lo que esperamos encontrar
Idealmente:

Git

  git version ...



Claude
Una instalación válida y:


  No installation issues found


o equivalente.

Java
Necesitamos finalmente:


  25.x


No vamos a cambiar nada todavía si tienes 21 u otra versión.

Primero revisamos.

Node
Nuestra referencia será:


  v24.x


porque actualmente Node 24 es LTS; Node 26 todavía es Current y está previsto que entre
en LTS en octubre de 2026.       Node… +1



Docker

Necesitamos tanto:


  docker


como:


  docker compose


Spring Boot también soporta integración de desarrollo con Docker Compose, aunque
decidiremos conscientemente en un paso posterior si dejamos el ciclo de vida a Spring o
lo gestionamos desde el monorepo.     Home




1.22. No hagas todavía estas cosas
No ejecutes:


     Bash

  spring init


No ejecutes:


     Bash

  npm create vite


No crees:


  CLAUDE.md
  AGENTS.md


No ejecutes:


     Bash

  openspec init


No escribas todavía:


  "Claude, créame un CRM"


Y sobre todo:

  NO hagas todavía git init


Quiero que el repositorio nazca conscientemente en el Paso 2, con la estructura que
vamos a diseñar.




Estado después del Paso 1
Todavía tenemos:


  Código escrito:              0
  Contexto contaminado:        0
  Decisiones improvisadas:     0


Pero ya tenemos:


  ✓ producto definido
  ✓ alcance inicial definido
  ✓ non-goals
  ✓ arquitectura de alto nivel
  ✓ stack provisional
  ✓ estrategia monorepo
  ✓ estrategia de contexto
  ✓ estrategia AGENTS/CLAUDE
  ✓ estrategia de sesiones
  ✓ criterio para subagentes
  ✓ política inicial de permisos
  ✓ definición de éxito del Módulo 1
  ✓ camino preparado para OpenSpec posteriormente


Y eso es ingeniería.

Para cerrar el Paso 1, ejecuta el bloque de diagnóstico anterior y pégame su salida
completa, sin corregir nada aunque aparezca un error.

¿Deseas continuar con el Paso 2 de 18: crear correctamente el repositorio y la
estructura base del monorepo?




                               Absolutamente todo funciono, continuemoscon el Paso 2
                               de 18: crear correctamente el repositorio y la estructura
                               base del monorepo, investiga exhaustivamente y busca en

                             fuentes confiables sin inventar datos para hacer este paso
                             2.

Worked for 1m 18s

Perfecto. Como el Paso 1 quedó limpio, entramos al Paso 2 de 18.

Paso 2 de 18 — Crear correctamente el repositorio y la
estructura base del monorepo
Este paso tiene un objetivo muy concreto:

   Crear una base Git limpia, reproducible y profesional antes de que Claude Code
   empiece a tomar decisiones sobre nuestro código.

Todavía no vamos a crear Spring Boot, React, PostgreSQL, Docker Compose,
CLAUDE.md , AGENTS.md , .claude/settings.json ni OpenSpec.


Eso es deliberado.

Al terminar este paso tendremos:


  crm-profesional/
  ├── .git/
  ├── backend/
  │   └── .gitkeep
  ├── frontend/
  │   └── .gitkeep
  ├── docs/
  │   └── .gitkeep
  ├── .editorconfig
  ├── .gitattributes
  ├── .gitignore
  └── README.md


Y Git estará:


  rama: main
  working tree: limpio
  primer commit: creado
  remote GitHub: conectado




2.1. Primero: ¿qué estamos construyendo realmente?
No estamos creando tres proyectos independientes:

  backend-repo
  frontend-repo
  docs-repo


Vamos a crear un solo repositorio Git:


  crm-profesional


que contendrá:


  crm-profesional/
  │
  ├── backend/
  ├── frontend/
  └── ...


Esto es un monorepo en el sentido básico:

   varios componentes relacionados de un producto viven bajo un único repositorio y un
   único historial Git.

Nuestro frontend y backend tendrán sus propias reglas y contextos posteriormente, pero
compartirán:
      historial;
      issues;
      pull requests;
      documentación de proyecto;
      infraestructura;
      decisiones arquitectónicas;
      contexto global;
      automatizaciones futuras.

Para este CRM pequeño es una elección muy conveniente porque no tenemos todavía
una razón real para introducir coordinación entre repositorios.




2.2. ¿Por qué no dejamos que Claude cree todo ahora?
Podríamos entrar a Claude Code y decir:


  Crea la estructura inicial de mi CRM.


Pero todavía sería una mala práctica.

Claude tendría que adivinar:

       nombre;
       estructura;
       política Git;
       .gitignore ;
       line endings;
       qué archivos locales versionar;
       cuáles ignorar;
       cómo dividir frontend/backend;
       qué documentación crear.

En este paso vamos a crear nosotros la frontera del sistema.

Después Claude trabajará dentro de ella.

Esta distinción es importante:


  NOSOTROS
         ↓
  definimos el terreno


  CLAUDE
         ↓
  trabaja dentro del terreno


Ese es el comienzo del harness engineering.




2.3. Escoge dónde vivirá físicamente el proyecto
No pongas el proyecto dentro de:


  Downloads/
  Desktop/
  OneDrive/


si puedes evitarlo.

Especialmente evitaría una carpeta sincronizada automáticamente como OneDrive porque
puede introducir cambios de archivos, locks o sincronizaciones que no forman parte de
Git.

Una ubicación limpia podría ser, por ejemplo:

     C:/dev/


o:


     C:/projects/


En Git Bash esas rutas se ven aproximadamente así:


        Bash

     /c/dev


o:


        Bash

     /c/projects


Usaré:


     C:\dev\crm-profesional


como ejemplo.

No significa que obligatoriamente debas usar C:\dev .




2.4. Crear la carpeta raíz
En Git Bash:


        Bash

     cd /c


     mkdir -p dev
     cd dev


     mkdir crm-profesional
     cd crm-profesional


Comprueba:


        Bash

  pwd


Deberías obtener algo parecido a:


  /c/dev/crm-profesional


Ahora:


        Bash

  ls -la


La carpeta debería estar prácticamente vacía.




2.5. Antes de git init : comprueba que no estés
dentro de otro repositorio
Esto es importantísimo.

Ejecuta:


        Bash

  git rev-parse --show-toplevel


En una carpeta nueva esperamos un error parecido a:


  fatal: not a git repository



¿Por qué queremos ese error?
Porque demuestra que:


  crm-profesional


no quedó accidentalmente dentro de otro repositorio Git.

Ejemplo malo:


  mi-repo-existente/
  ├── .git/
  │
  └── crm-profesional/

Aquí crm-profesional sería simplemente una carpeta del repositorio superior.

Nosotros queremos:


     crm-profesional/
     ├── .git/
     ├── backend/
     └── frontend/


Es decir:

      crm-profesional debe ser la raíz Git.




2.6. Inicializar Git directamente con main
Ejecuta:


        Bash

     git init -b main


Git soporta -b para indicar explícitamente el nombre de la rama inicial; GitHub también
documenta este procedimiento para proyectos locales que luego se publicarán.
     GitHub D…



Ahora:


        Bash

     git branch --show-current


Debe mostrar:


     main


Y:


        Bash

     git rev-parse --show-toplevel


debe devolver:


     /c/dev/crm-profesional

Perfecto.




2.7. ¿Qué acaba de aparecer?
Ejecuta:


       Bash

  ls -la


Ahora encontrarás:


  .git/


Visualmente:


  crm-profesional/
  └── .git/


Ese directorio es crucial.

No es simplemente “una carpeta escondida”.

Contiene la base de datos local de Git:

      referencias;
      objetos;
      configuración;
      índice;
      historial;
      información sobre ramas;
      remotes posteriormente.

Por eso:


  .git/


convierte esta carpeta normal:


  crm-profesional/


en:

  repositorio Git


Nunca debemos editar manualmente .git/ para operaciones normales.




2.8. Verificar identidad de Git antes del primer commit
Ejecuta:


      Bash

  git config --get user.name
  git config --get user.email


Las dos deberían devolver algo.

Por ejemplo:


  Diego Aguirre
  correo@ejemplo.com


No voy a inventar cuál debe ser tu correo.

Debe ser el que tú quieras asociar con los commits.

Si cualquiera queda vacío, configúralo antes del commit.

Puedes hacerlo solamente para este repositorio:


      Bash

  git config user.name "TU NOMBRE"
  git config user.email "TU CORREO"


Me gusta más local al repositorio durante aprendizaje que modificar configuraciones
globales sin necesidad.

Comprueba:


      Bash

  git config --local --list




2.9. Crear las tres áreas fundamentales

Ahora:


      Bash

  mkdir backend
  mkdir frontend
  mkdir docs


Comprueba:


      Bash

  find . -maxdepth 2 -type d | sort


Deberías observar:


  .
  ./.git
  ./backend
  ./docs
  ./frontend


Esto representa:


  crm-profesional
           │
           ├──────── backend
           │
           ├──────── frontend
           │
           └──────── docs




2.10. Pero existe un detalle: Git no versionará esas
carpetas vacías
Git fundamentalmente versiona archivos.

Si hacemos ahora:


      Bash

  git status


Git no te va a presentar:

  backend/
  frontend/
  docs/


como estructura versionable si están completamente vacías.

Por eso necesitamos temporalmente un archivo dentro de cada una.

Usaremos la convención:


  .gitkeep


Ejecuta:


      Bash

  touch backend/.gitkeep
  touch frontend/.gitkeep
  touch docs/.gitkeep


Ahora:


      Bash

  find . -maxdepth 2 -type f | sort


deberías tener:


  ./backend/.gitkeep
  ./docs/.gitkeep
  ./frontend/.gitkeep



Atención
.gitkeep no es una característica especial de Git.


Para Git es simplemente un archivo vacío con un nombre extraño.

Lo utilizamos para conseguir:


  directorio vacío
         ↓
  contiene .gitkeep
         ↓
  Git puede registrar algo

Cuando Spring Boot ocupe backend/ , eliminaremos:


  backend/.gitkeep


Y cuando React ocupe frontend/ , haremos lo mismo.




2.11. Ahora vamos a crear el .gitignore
Este archivo sí es crítico.

GitHub recomienda colocar un .gitignore en la raíz y versionarlo, porque las reglas
compartidas deben acompañar a todos los clones del repositorio.   GitHub D… +1



Piensa en él así:


  .gitignore
       ↓
  "estos archivos pueden existir
  en mi computadora,
  pero NO pertenecen al repositorio"


Ejemplos:


  node_modules/
  target/
  .env
  settings.local.json
  .idea/




2.12. Diferencia importantísima: “ignorado” no significa
“secreto borrado”
Supongamos que tienes:


  .env


con:


  DATABASE_PASSWORD=supersecreto


y primero haces:

      Bash

  git add .env
  git commit


y después añades .env a .gitignore .

El secreto ya entró al historial.

.gitignore no viaja al pasado.


La propia documentación de Git explica que los archivos que ya están trackeados no
dejan de estarlo simplemente porque posteriormente aparezcan en .gitignore .        Git




GitHub también advierte explícitamente que no debes hacer add , commit o push de
contraseñas, API keys u otra información sensible.    GitHub D…



Por eso establecemos .gitignore antes de introducir código real.




2.13. Nuestro .gitignore
Ejecuta exactamente desde la raíz:


      Bash

  cat > .gitignore <<'EOF'
  # =============================================================================
  # crm-profesional
  # Shared Git ignore rules
  # =============================================================================


  # -----------------------------------------------------------------------------
  # Secrets and local environment
  # -----------------------------------------------------------------------------
  .env
  .env.*
  !.env.example
  !.env.*.example


  secrets/
  *.pem
  *.key


  # -----------------------------------------------------------------------------
  # Claude Code - local/private project state
  # -----------------------------------------------------------------------------
  .claude/settings.local.json

CLAUDE.local.md


# -----------------------------------------------------------------------------
# Java / Maven
# -----------------------------------------------------------------------------
**/target/
*.class


pom.xml.tag
pom.xml.releaseBackup
pom.xml.versionsBackup
release.properties


hs_err_pid*
replay_pid*


# -----------------------------------------------------------------------------
# Node.js / frontend
# -----------------------------------------------------------------------------
**/node_modules/
**/dist/
**/coverage/
**/.vite/


npm-debug.log*
yarn-debug.log*
yarn-error.log*
pnpm-debug.log*


# -----------------------------------------------------------------------------
# IDEs
# -----------------------------------------------------------------------------
.idea/
*.iml
*.iws
*.ipr


.vscode/


# -----------------------------------------------------------------------------
# Operating-system files
# -----------------------------------------------------------------------------
.DS_Store
Thumbs.db
Desktop.ini


# -----------------------------------------------------------------------------
# Temporary files
# -----------------------------------------------------------------------------
*.tmp
*.temp
*.swp

  *.swo
  *~
  EOF

No escribimos esta lista aleatoriamente.

GitHub mantiene plantillas oficiales de .gitignore para Java, Node y distintos IDEs; por
ejemplo, su plantilla de Java excluye clases compiladas y logs de crash, mientras la de
Node cubre directorios de dependencias, cobertura y logs.     GitHub +1



Nuestro archivo está adaptado al stack que realmente tendremos, en lugar de copiar
cientos de reglas que no utilizaremos.




2.14. Vamos a comprender cada bloque del .gitignore
Secrets

        gitignore

  .env
  .env.*
  !.env.example
  !.env.*.example


Primero decimos:


  ignora .env
  ignora .env.development
  ignora .env.local
  ignora etc.


Después:


  !.env.example


significa:

   excepción: sí permitimos versionar .env.example .

Git documenta precisamente ! como la negación de un patrón anterior.       Git




Más adelante tendremos algo semejante a:


  .env.example

con:


  DATABASE_HOST=localhost
  DATABASE_PORT=5432
  DATABASE_NAME=crm
  DATABASE_USERNAME=crm
  DATABASE_PASSWORD=CHANGE_ME


Pero nunca:


  .env


con una contraseña real.

Todavía no lo crearemos porque esas variables no están definidas.




2.15. Claude Code local
Tenemos:


       gitignore

  .claude/settings.local.json
  CLAUDE.local.md


Esto está puesto desde ahora para que posteriormente no cometamos un error.

Anthropic distingue explícitamente:


  .claude/settings.json


como configuración de proyecto compartible/versionable,

de:


  .claude/settings.local.json


como configuración personal/local que no se debe versionar. Claude Code incluso
configura Git para ignorar settings.local.json cuando lo crea.      Claude +1




Y lo mismo ocurre con:


  CLAUDE.local.md

Anthropic lo define para preferencias personales específicas del proyecto y recomienda
añadirlo al .gitignore .     Claude +1




Por eso en nuestro futuro tendremos:


  VERSIONADO
  ────────────────────────
  CLAUDE.md
  AGENTS.md
  .claude/settings.json



  NO VERSIONADO
  ────────────────────────
  CLAUDE.local.md
  .claude/settings.local.json


Exactamente la distinción sobre la que ya habíamos hablado.




2.16. Java

      gitignore

  **/target/
  *.class


Cuando Maven compile:


  backend/
  ├── src/
  ├── pom.xml
  └── target/


target/ será output generado.


No es código fuente.

Podemos reconstruirlo ejecutando Maven.

Por tanto:


  SOURCE
  src/
  pom.xml
  mvnw
  .mvn/

             ↓
           Git ✓



  OUTPUT
  target/
             ↓
           Git ✗




2.17. Frontend
Tenemos:


      gitignore

  **/node_modules/
  **/dist/
  **/coverage/
  **/.vite/



node_modules
Se reconstruye desde el manifest y lockfile.

Por eso:


  package.json             ✓ Git
  package-lock.json        ✓ Git
  node_modules/            ✗ Git


El lockfile sí se versionará.

Esto es importante.

Nunca agregaremos:


      gitignore

  package-lock.json


El lockfile forma parte de la reproducibilidad de dependencias.




dist

Vite genera por defecto el build de producción dentro de dist , salvo que se configure
otra salida.       vitejs +1



Por eso:


  frontend/src/                ✓
  frontend/dist/               ✗




coverage
Es salida derivada de tests.

La podemos regenerar.

No necesitamos versionarla.




2.18. ¿Por qué usamos **/target/ y no solamente
target/ ?
Porque estamos construyendo un monorepo.

Con:


       gitignore

  **/target/


si en un futuro aparece:


  backend/target/
  tools/example/target/


los dos quedan cubiertos.

Lo mismo:


       gitignore

  **/node_modules/


permite:

  frontend/node_modules/
  tools/node_modules/


sin crear nuevas reglas.




2.19. Probar el .gitignore antes de confiar en él
Esto es algo que quiero que aprendas a hacer profesionalmente.

No digas:


   “creo que está ignorado”.

Pregúntale a Git.

Ejecuta:


      Bash

  git check-ignore -v .claude/settings.local.json


Incluso aunque el archivo no exista, podemos probar patrones con:


      Bash

  git check-ignore -v --no-index .claude/settings.local.json


Debe indicar una regla de .gitignore .

Ahora:


      Bash

  git check-ignore -v --no-index frontend/node_modules
  git check-ignore -v --no-index backend/target
  git check-ignore -v --no-index .env


Los tres deberían encontrar una regla.




2.20. Prueba también que .env.example NO esté
ignorado
Ejecuta:

       Bash

  git check-ignore -v --no-index .env.example


Aquí puede aparecer la regla de excepción dependiendo del comportamiento/salida del
comando, pero lo que importa de verdad es la prueba definitiva:


       Bash

  touch .env.example
  git status --short
  rm .env.example


Deberías verlo temporalmente como archivo no trackeado.

Eso significa:


  .env            → ignorado
  .env.example    → versionable


Exactamente lo que queremos.




2.21. Crear .gitattributes
Ahora solucionaremos un problema invisible pero muy real.

Tú estás trabajando con Windows/Git Bash y Claude Code puede interactuar con
herramientas Unix-like.

Windows tradicionalmente usa:


  CRLF
  \r\n


Unix/Linux usa:


  LF
  \n


Sin una política del repositorio puedes terminar con diffs como:


  100 líneas eliminadas
  100 líneas añadidas

aunque visualmente el código sea idéntico.

Git permite controlar la normalización mediante .gitattributes . La documentación
oficial establece que text=auto puede normalizar texto a LF en el repositorio y que
eol=lf / eol=crlf permite controlar casos específicos.     Git




Creemos:


        Bash

  cat > .gitattributes <<'EOF'
  # =============================================================================
  # Normalize text files across operating systems
  # =============================================================================


  * text=auto eol=lf


  # Windows command scripts
  *.bat text eol=crlf
  *.cmd text eol=crlf


  # Unix shell scripts must stay LF
  *.sh text eol=lf
  mvnw text eol=lf


  # Maven Wrapper Windows launcher
  mvnw.cmd text eol=crlf


  # Binary files: never perform text normalization
  *.png binary
  *.jpg binary
  *.jpeg binary
  *.gif binary
  *.ico binary
  *.pdf binary
  *.jar binary
  *.woff binary
  *.woff2 binary
  *.ttf binary
  EOF




2.22. ¿Qué significa la primera línea importante?

        gitattributes

  * text=auto eol=lf

Simplificando:

   Para archivos que Git detecte como texto, normalízalos y utiliza LF.

La propia documentación de Git recomienda text=auto cuando quieres normalización
consistente en proyectos multiplataforma.    Git




2.23. ¿Entonces por qué .cmd usa CRLF?
Porque:


  mvnw.cmd


será un script nativo de Windows.

Queremos expresamente:


       gitattributes

  *.cmd text eol=crlf


Mientras:


  mvnw


será el script Unix:


       gitattributes

  mvnw text eol=lf


Así un mismo repositorio funciona limpiamente en:


  Windows
  Linux
  macOS
  CI
  Claude Code




2.24. ¿Qué significa binary ?
Por ejemplo:

        gitattributes

  *.png binary


le dice a Git que no trate un PNG como texto.

No queremos que intente modificar finales de línea dentro de datos binarios.




2.25. Crear .editorconfig
.gitattributes gobierna cómo Git trata archivos.


.editorconfig gobierna cómo los editores compatibles deberían guardarlos.


Son complementarios:


  Editor / IDE
         │
         │ .editorconfig
         ▼
  archivo de trabajo
         │
         │ .gitattributes
         ▼
  Git


EditorConfig estandariza propiedades como:
    charset;
    line ending;
    indentación;
    whitespace final;
    newline final.

Su especificación define explícitamente root , end_of_line , charset ,
trim_trailing_whitespace e insert_final_newline .          EditorConfig +1




Creemos:


        Bash

  cat > .editorconfig <<'EOF'
  root = true


  # Default rules for text files
  [*]

  charset = utf-8
  end_of_line = lf
  insert_final_newline = true
  trim_trailing_whitespace = true
  indent_style = space
  indent_size = 2


  # Java and XML use 4 spaces
  [*.{java,xml}]
  indent_style = space
  indent_size = 4


  # Shell scripts use 2 spaces
  [*.sh]
  indent_style = space
  indent_size = 2


  # Markdown may intentionally use trailing spaces for hard line breaks
  [*.md]
  trim_trailing_whitespace = false


  # Makefiles require tabs
  [Makefile]
  indent_style = tab
  EOF




2.26. ¿Por qué Java usa 4 pero frontend 2?
Nuestra regla base dice:


        INI

  indent_size = 2


Por tanto archivos como:


  .ts
  .tsx
  .json
  .yaml
  .css
  .html


heredan 2 espacios.

Pero después especificamos:

      INI

  [*.{java,xml}]
  indent_size = 4


Eso sobrescribe la regla para Java/XML.

Resultado:


  Java         → 4 espacios
  TypeScript   → 2 espacios
  JSON         → 2 espacios
  YAML         → 2 espacios


Esta decisión será posteriormente incluida también en nuestro contexto del proyecto.




2.27. ¿Por qué root = true ?
Porque EditorConfig puede buscar archivos .editorconfig en directorios superiores.

root = true significa:


   esta es la raíz de configuración; deja de buscar más arriba.

Eso está definido expresamente por la especificación.      EditorCon…



Así evitamos que alguna configuración accidental de:


  C:\dev\.editorconfig


cambie silenciosamente nuestro proyecto.




2.28. Crear un README mínimo, no una novela
GitHub recomienda que los repositorios tengan README porque facilita comprender y
navegar el proyecto.     GitHub D…



Pero no vamos a escribir todavía una arquitectura ficticia que aún no existe.

Crearemos únicamente información verdadera:


      Bash

  cat > README.md <<'EOF'
  # crm-profesional


  CRM full stack en construcción para practicar desarrollo de software profesional asistido


  ## Estado actual


  Proyecto en fase inicial.


  El repositorio se está construyendo progresivamente, empezando por la configuración del e


  ## Estructura prevista


  ```text
  crm-profesional/
  ├── backend/       # API y lógica de negocio
  ├── frontend/      # Aplicación web
  └── docs/          # Documentación del proyecto



Producto inicial
La primera versión permitirá gestionar clientes de una pequeña empresa.

El alcance se ampliará progresivamente durante el desarrollo.
EOF



  Observa algo importante:


  No dice:


  ```text
  Spring Boot 4.1 funcionando
  PostgreSQL configurado
  React funcionando
  Docker configurado


porque todavía no es verdad.

Una regla que seguiremos durante todo el proyecto será:


   La documentación describe el sistema que existe, no el sistema que nos gustaría que
   existiera.




2.29. Revisar cómo quedó todo antes de hacer git add
Ejecuta:

       Bash

  find . \
      -path './.git' -prune -o \
      -maxdepth 2 -print | sort


Deberías observar aproximadamente:


  .
  ./.editorconfig
  ./.gitattributes
  ./.gitignore
  ./README.md
  ./backend
  ./backend/.gitkeep
  ./docs
  ./docs/.gitkeep
  ./frontend
  ./frontend/.gitkeep


Nuestro repositorio lógico:


  crm-profesional/
  │
  ├── backend/
  │    └── .gitkeep
  │
  ├── frontend/
  │    └── .gitkeep
  │
  ├── docs/
  │    └── .gitkeep
  │
  ├── .editorconfig
  ├── .gitattributes
  ├── .gitignore
  └── README.md




2.30. Lo que deliberadamente NO existe todavía
Compruébalo mentalmente:


  CLAUDE.md                        ✗
  AGENTS.md                        ✗
  CLAUDE.local.md                  ✗


  .claude/settings.json            ✗

  .claude/settings.local.json      ✗
  .claude/rules/                   ✗
  .claude/agents/                  ✗


  backend/pom.xml                  ✗
  backend/mvnw                     ✗
  backend/src/                     ✗


  frontend/package.json            ✗
  frontend/src/                    ✗


  compose.yml                      ✗


  openspec/                        ✗


Esto no significa que nos faltó hacer el trabajo.

Significa que respetamos el diseño de los 18 pasos.




2.31. Examinar Git antes de añadir nada
Ejecuta:


      Bash

  git status


Git debería mostrar aproximadamente:


  On branch main


  No commits yet


  Untracked files:
    .editorconfig
    .gitattributes
    .gitignore
    README.md
    backend/
    docs/
    frontend/


Aquí aparecen como:


  Untracked


Eso significa:

   Git sabe que existen, pero todavía no forman parte de su historial.




2.32. Ahora utiliza la salida “porcelain”
Ejecuta:


      Bash

  git status --porcelain


Esta salida será importante durante todo nuestro proyecto.

Ahora sí debería mostrar cosas.

Algo semejante:


  ?? .editorconfig
  ?? .gitattributes
  ?? .gitignore
  ?? README.md
  ?? backend/
  ?? docs/
  ?? frontend/


?? significa:


  archivo no trackeado


Recuerda la pregunta que ya habías tenido anteriormente:

   “La guía dice que git status --porcelain no debe mostrar nada. ¿Qué pasa si sí
   muestra?”

La respuesta ahora la puedes comprender perfectamente:

Antes del commit
Que muestre archivos es correcto:


  ?? README.md


porque tenemos cambios pendientes.

Después del commit

Queremos:


  [ninguna salida]


porque significará:


  working tree clean


No existe contradicción.

El significado depende del momento en el flujo.




2.33. Primero revisamos, después hacemos git add
Nunca quiero enseñarte este hábito:


      Bash

  git add .
  git commit


sin mirar.

El hábito profesional será:


  1. crear/modificar
  2. git status
  3. revisar
  4. git diff
  5. stage
  6. revisar stage
  7. commit


En este primer commit no existe todavía diff tradicional para archivos untracked, pero
revisaremos contenidos.

Ejecuta:


      Bash

  cat .gitignore


Después:

      Bash

  cat .gitattributes


Después:


      Bash

  cat .editorconfig


Después:


      Bash

  cat README.md


Mira que no haya:


  passwords
  tokens
  correos sensibles
  rutas privadas
  basura accidental




2.34. Agregar los archivos al staging area
Ahora sí:


      Bash

  git add .


Después:


      Bash

  git status


Ya deberían estar en:


  Changes to be committed


No han sido commit todavía.

Piensa:

  Working directory
           │
           │ git add
           ▼
  Staging area
           │
           │ git commit
           ▼
  Repository history




2.35. Inspeccionar exactamente qué entraría en el
commit
Ejecuta:


      Bash

  git diff --cached --stat


Después:


      Bash

  git diff --cached


Ahora sí podrás revisar el contenido staged.

Ésta es una costumbre que posteriormente obligaremos también a Claude Code a
respetar.

Queremos evitar que un agente haga:


  tarea solicitada
  +
  7 archivos no relacionados
  +
  configuración extra
  +
  secreto accidental


y que nosotros simplemente hagamos commit.




2.36. Comprueba qué archivos están realmente staged

Ejecuta:


        Bash

  git diff --cached --name-only


Debería haber únicamente:


  .editorconfig
  .gitattributes
  .gitignore
  README.md
  backend/.gitkeep
  docs/.gitkeep
  frontend/.gitkeep


Siete archivos.

Nada más.




2.37. Primer commit
Ahora:


        Bash

  git commit -m "chore: initialize monorepo structure"


¿Por qué:


  chore:


y no:


  feat:


Porque todavía no hemos añadido funcionalidad del producto.

No existe todavía:


  crear cliente
  listar cliente
  dashboard


Sólo infraestructura inicial del repositorio.

Por tanto chore expresa mejor la intención.

No vamos a convertir Conventional Commits en dogma todavía; simplemente
comenzamos con mensajes descriptivos.




2.38. Comprobar el commit
Ejecuta:


        Bash

  git log --oneline --decorate -n 5


Deberías tener algo semejante a:


  abc1234 (HEAD -> main) chore: initialize monorepo structure


Ahora entiende:


  HEAD
    │
    ▼
  main
    │
    ▼
  abc1234


HEAD está apuntando a nuestra rama actual:


  main


y main está apuntando al commit inicial.




2.39. Ahora viene la prueba importante
Ejecuta:


        Bash

  git status --porcelain



Resultado correcto:

absolutamente nada.

No:


  On branch main
  nothing to commit


Nada.

Una línea vacía.

Esto:


        Bash

  git status --porcelain




significa:

   No existen cambios tracked/untracked pendientes que Git deba reportar.

Ése es nuestro primer checkpoint limpio.




2.40. Probemos de verdad el .gitignore
Vamos a crear basura deliberadamente.

Ejecuta:


        Bash

  mkdir -p frontend/node_modules/test-package
  touch frontend/node_modules/test-package/example.js


  mkdir -p backend/target
  touch backend/target/example.class


  touch .env


Ahora:


        Bash

  git status --porcelain

¿Qué queremos?


     NADA


Porque:


     frontend/node_modules/         ignorado
     backend/target/                ignorado
     .env                           ignorado


Ahora puedes comprobar cada uno:


        Bash

     git check-ignore -v frontend/node_modules/test-package/example.js
     git check-ignore -v backend/target/example.class
     git check-ignore -v .env


Aquí Git te mostrará qué regla exacta hizo match.

Esto es muchísimo mejor que asumir.




2.41. Eliminar nuestra basura de prueba
Ahora:


        Bash

     rm -rf frontend/node_modules
     rm -rf backend/target
     rm -f .env


Y:


        Bash

     git status --porcelain


Otra vez:


     sin salida

2.42. Ahora publicar el proyecto en GitHub
Como queremos un proyecto real, no quiero dejarlo simplemente en tu disco.

Mi recomendación para esta fase:


   crear inicialmente el repositorio como Private.

¿Por qué?

No porque vaya a contener secretos — los secretos nunca deberían versionarse
incluso en repositorios privados.

Sino porque mientras estamos aprendiendo vamos a:

    reorganizar;
    crear reglas;
    hacer experimentos con Claude;
    cambiar arquitectura;
    introducir posteriormente OpenSpec.

Cuando quieras convertirlo en portafolio puedes evaluar hacerlo público.




2.43. Crear el repositorio remoto
En GitHub entra a:


  New repository


Configura:


  Owner:
  Diiegoal


  Repository name:
  crm-profesional


  Visibility:
  Private


Y MUY IMPORTANTE:

NO marques:

  Add a README file
  Add .gitignore
  Choose a license


Debe crearse completamente vacío.

GitHub recomienda justamente no inicializar el remoto con README/licencia/gitignore
cuando vas a empujar un repositorio local existente, porque de lo contrario introduces un
historial remoto independiente y puedes generar conflictos innecesarios.    GitHub D… +1




2.44. ¿Por qué no queremos que GitHub cree otro
README?
Nosotros ya tenemos:


  LOCAL
  commit A
  └── README.md


Si GitHub crea otro inicial:


  REMOTE
  commit B
  └── README.md


terminas teniendo:


  historia local ≠ historia remota


y tienes que reconciliarlas.

Queremos:


  REMOTE VACÍO
           ↑
           │ push
           │
  LOCAL
  commit A


Resultado:


  LOCAL = REMOTE

Mucho más limpio.




2.45. Añadir origin
Cuando GitHub cree el repositorio vacío te mostrará su URL.

Si utilizas HTTPS, será aproximadamente:


  https://github.com/Diiegoal/crm-profesional.git


Comprueba primero:


      Bash

  git remote -v


En este momento no debería haber origin .

Ahora:


      Bash

  git remote add origin https://github.com/Diiegoal/crm-profesional.git


Después:


      Bash

  git remote -v


Debes ver:


  origin   https://github.com/Diiegoal/crm-profesional.git (fetch)
  origin   https://github.com/Diiegoal/crm-profesional.git (push)


GitHub documenta exactamente este patrón:


      Bash

  git remote add origin REMOTE-URL
  git remote -v


para conectar un repositorio local existente.   GitHub D…

2.46. ¿Qué significa origin ?
origin no es una palabra mágica obligatoria.


Es simplemente el nombre convencional que damos a un remote.

Podríamos llamarlo:


  github
  remoto
  servidor
  pepito


pero casi todo el ecosistema utiliza:


  origin


Así:


  LOCAL
  crm-profesional
           │
           │ origin
           ▼
  GitHub
  Diiegoal/crm-profesional




2.47. Primer push
Ahora:


       Bash

  git push -u origin main


GitHub documenta git push -u origin main precisamente para publicar una rama local
main y establecer su upstream.          GitHub D…




La primera vez te puede solicitar autenticación dependiendo de cómo tengas configurado
Git Credential Manager.




2.48. ¿Qué hace -u ?

Es abreviatura de:


     --set-upstream


Relacionamos:


     local main


con:


     origin/main


Después de ese primer push podrás normalmente ejecutar simplemente:


        Bash

     git push


en vez de:


        Bash

     git push origin main


Y:


        Bash

     git pull


sabrá de dónde traer.




2.49. Verificar la relación local-remota
Ejecuta:


        Bash

     git branch -vv


Deberías observar algo parecido:


     * main abc1234 [origin/main] chore: initialize monorepo structure

Esto nos dice:


     main
     │
     └──── upstream → origin/main


Ahora:


         Bash

     git remote -v


Y:


         Bash

     git status


Esperamos aproximadamente:


     On branch main
     Your branch is up to date with 'origin/main'.


     nothing to commit, working tree clean




2.50. Verificación final fuerte
Quiero que hagas estas comprobaciones una por una.

A. Rama

         Bash

     git branch --show-current


Debe ser:


     main




B. Root Git

      Bash

  git rev-parse --show-toplevel


Debe terminar en:


  crm-profesional




C. Estado

      Bash

  git status --porcelain


Debe devolver:


  NADA




D. Commit

      Bash

  git log --oneline -1


Debe terminar con:


  chore: initialize monorepo structure




E. Remote

      Bash

  git remote -v


Debe mostrar:


  origin


para fetch y push.

F. Upstream

     Bash

  git branch -vv


Debe contener:


  [origin/main]




G. Estructura

     Bash

  find . \
    -path './.git' -prune -o \
    -maxdepth 2 -print | sort


Debe contener solamente nuestra estructura prevista.




2.51. Ahora una prueba especial de seguridad para
Claude
Aunque todavía no hemos creado .claude/settings.json , quiero dejar preparado el
concepto.

Actualmente Anthropic permite impedir incluso que Claude lea ciertos archivos sensibles
mediante permissions.deny , por ejemplo .env o credenciales.       Clau…




Por tanto más adelante tendremos dos barreras diferentes:


  BARRERA 1
  .gitignore
        ↓
  Git no versiona .env



  BARRERA 2
  Claude permissions.deny
        ↓
  Claude tampoco lee .env

Esto es muy importante.

Porque:


  .gitignore


NO significa:

   Claude no puede leerlo.

Sólo significa:

   Git no debería versionarlo.

Más adelante configuraremos:


          JSON

  {
      "permissions": {
          "deny": [
              "Read(./.env)",
              "Read(./.env.*)"
          ]
      }
  }


Pero no lo crees todavía.

Eso pertenece al harness que construiremos de manera consciente en los siguientes
pasos.




2.52. Otra distinción que debes memorizar
Tenemos tres categorías diferentes:

1. Compartido por todo el equipo
Ejemplo futuro:


  .claude/settings.json


Versionado:


  ✓

2. Personal de un desarrollador para este repo
Ejemplo:


  .claude/settings.local.json
  CLAUDE.local.md


Versionado:


  ✗


Anthropic establece precisamente esa separación entre scopes Project y Local .
   Clau…




3. Secreto
Ejemplo:


  .env
  API_KEY
  password


Versionado:


  NUNCA


Y además, en lo posible:


  Claude Read:
  DENY


No confundas:


  local


con:


  secret


Un archivo puede ser local sin contener secretos.

2.53. ¿Por qué no creamos todavía backend/AGENTS.md
y frontend/AGENTS.md ?
Porque ahora mismo no existe:


  Spring Boot
  React
  estructura real
  comandos reales
  dependencias reales


Si escribiéramos ya 170 líneas sobre backend tendríamos que inventar contexto.

Por ejemplo podríamos poner:


  Ejecuta ./mvnw test


pero todavía:


  ./mvnw


no existe.

Quiero que nuestros archivos de contexto tengan una propiedad fundamental:


   Ground truth.

Es decir:


  CLAUDE.md
  AGENTS.md


deben describir el repositorio real, no una fantasía arquitectónica.

Por eso construiremos el harness y posteriormente lo iremos completando
conscientemente.




2.54. ¿Y por qué sí creamos .gitignore ahora?
Porque éste establece una restricción antes de que aparezcan los archivos
peligrosos/generados.

Hay dos tipos de conocimiento:

  DESCRIPTIVO
  "backend usa Spring Boot"


Todavía sería falso.

Pero:


  NORMATIVO
  ".env no se versiona"


ya podemos decidirlo desde el comienzo.

Por eso uno sí entra ahora y el otro no.




2.55. Nuestro primer checkpoint profesional
Al terminar debemos tener exactamente esta situación:


                              GitHub
                                │
                                │ origin/main
                                │
                                ▼
  ┌──────────────────────────────────────────┐
  │               crm-profesional               │
  │                                             │
  │   main                                      │
  │     │                                       │
  │     └── chore: initialize monorepo...       │
  │                                             │
  │   backend/                                  │
  │   frontend/                                 │
  │   docs/                                     │
  │                                             │
  │   .gitignore                                │
  │   .gitattributes                            │
  │   .editorconfig                             │
  │   README.md                                 │
  │                                             │
  └──────────────────────────────────────────┘


  git status --porcelain
              │
              ▼
            [vacío]

2.56. Qué hemos aprendido realmente en este paso
No quiero que recuerdes solamente comandos.

git init -b main
Aprendiste:

   Aquí nace el historial del producto.




.gitignore
Aprendiste:

   Qué archivos pueden existir localmente pero no pertenecen al historial compartido.

Git recomienda que las reglas que deben compartir todos los colaboradores estén en el
.gitignore versionado del repositorio.      Git




.gitattributes
Aprendiste:

   El repositorio, no la computadora individual, establece la política de line endings.

Git proporciona exactamente este mecanismo.        Git




.editorconfig
Aprendiste:

   El formato básico de los archivos también forma parte del contrato del proyecto.




git status --porcelain
Aprendiste:


  con salida
      ↓
  hay algo que revisar


  vacío

      ↓


No significa que “siempre tiene que estar vacío”.

Debe estar vacío en nuestros checkpoints limpios.




origin/main
Aprendiste:


  main


es tu rama local.


  origin/main


es la referencia local del estado remoto.


  origin


es el remote.




2.57. Algo todavía más importante: acabamos de
empezar el harness sin usar Claude
Nuestro harness ya contiene decisiones:


  repo boundary
         ↓
  crm-profesional


  source-control boundary
         ↓
  .gitignore


  text normalization
         ↓
  .gitattributes


  editor formatting baseline
         ↓
  .editorconfig


  component boundaries
         ↓

  backend/
  frontend/
  docs/


  remote collaboration
       ↓
  GitHub


Por eso:

   Harness no significa solamente .claude/ .

El entorno completo alrededor del agente condiciona cómo trabaja.

Claude Code heredará este terreno.




2.58. Lo que NO debes hacer antes del Paso 3
Una vez tengas el estado limpio, detente.

Todavía no:


     Bash

  claude


para empezar a pedir implementación.

No ejecutes:


     Bash

  claude /init


No crees:


  CLAUDE.md
  AGENTS.md


No crees:


  .claude/settings.json


No generes Spring.

No generes React.

No crees compose.yml .

No instales OpenSpec.

No añadas dependencias.

El próximo paso es precisamente donde vamos a estudiar por primera vez:

Pilar 1 — La Herramienta
y transformar una instalación genérica de Claude Code en el harness consciente de
crm-profesional .




Checklist final del Paso 2
Antes de decirme que continuemos, verifica mentalmente:


  [ ] crm-profesional es la raíz Git
  [ ] rama = main
  [ ] backend/ existe
  [ ] frontend/ existe
  [ ] docs/ existe
  [ ] .gitignore existe
  [ ] .gitattributes existe
  [ ] .editorconfig existe
  [ ] README.md existe
  [ ] no existe código de aplicación todavía
  [ ] no existe CLAUDE.md todavía
  [ ] no existe AGENTS.md todavía
  [ ] no existe OpenSpec todavía
  [ ] primer commit creado
  [ ] origin configurado
  [ ] main tiene upstream origin/main
  [ ] push a GitHub completado
  [ ] git status --porcelain no imprime absolutamente nada


Cuando todos estén cumplidos, el Paso 2 está terminado.

El Paso 3 de 18 será especialmente importante: Pilar 1 — entender Claude Code como
herramienta + harness, inspeccionar cómo está funcionando realmente en nuestro
repositorio y configurar la estrategia correcta antes de darle permisos para construir
nada.

¿Deseas continuar con el Paso 3 de 18?

                                              Today 6:10 PM


                                    Absolutamente todo funciono, continuemos con el Paso 3:
                                    Entender y configurar el Pilar 1: Claude Code como
                                    herramienta y harness, investiga exhaustivamente y busca
                                    en fuentes confiables sin inventar datos para hacer este
                                    paso 3.

Worked for 1m 37s

Perfecto. Llegamos al Paso 3 de 18.

Este paso es especialmente importante porque aquí dejamos de ver Claude Code como
“un chat que escribe código” y empezamos a entenderlo como lo que Anthropic describe
actualmente: un harness agéntico alrededor del modelo. El modelo razona; Claude
Code proporciona herramientas, acceso al proyecto, Git, terminal, gestión de contexto,
permisos, sesiones y extensiones.

PASO 3 D            Clau…       Code como herramienta + harness
Objetivo
Al finalizar este paso quiero que puedas mirar esto:


  Claude Code


y mentalmente verlo así:


  ┌──────────────────────────────────────────────────────┐
  │                         CLAUDE CODE                           │
  │                                                           │
  │                         ┌───────────┐                     │
  │                         │   MODELO    │                       │
  │                         │   Claude    │                   │
  │                         └─────┬─────┘                     │
  │                                │                          │
  │              razonamiento / decisiones                    │
  │                                │                          │
  │             ┌────────────▼────────────┐                   │
  │             │               HARNESS          │            │
  │             │                                │            │
  │             │ Tools                          │            │
  │             │ Permissions                    │            │
  │             │ Context management             │            │
  │             │ Git state                      │            │
  │             │ Terminal                       │            │
  │             │ Sessions                       │            │
  │             │ Checkpoints                    │            │

  │             │ Skills                  │              │
  │             │ Hooks                   │              │
  │             │ Subagents               │              │
  │             │ MCP                     │              │
  │             └────────────┬────────────┘              │
  │                           │                          │
  └──────────────────────────┼───────────────────────────┘
                              │
                              ▼
                      crm-profesional/


No vamos a configurar todavía todas esas piezas.

En este paso:


  ENTENDEMOS
  +
  INSPECCIONAMOS
  +
  PROBAMOS


En los siguientes:


  Paso 4 → permisos y seguridad
  Paso 5 → settings
  Paso 6 → hooks


Así no mezclamos conceptos.




3.1. Primero conectemos esto con el Módulo 1
El material del curso clasifica Claude Code dentro de los agentes de terminal/CLI y
explica que su unidad de trabajo puede ser una tarea completa: puede leer archivos,
ejecutar comandos, editar múltiples archivos y comprobar resultados. Para un trabajo que
cruza capas y necesita ejecutar builds/tests, esta categoría resulta especialmente
apropiada.

Nuestro CRM tendrá eventualmente:


  React
      ↓
  API REST
      ↓
  Spring Boot
      ↓
  PostgreSQL

Una feature como:

   “crear clientes”

podría afectar:


  backend/domain
  backend/repository
  backend/service
  backend/controller
  backend/tests


  frontend/types
  frontend/api
  frontend/components
  frontend/pages
  frontend/tests


  migraciones


Eso explica por qué Claude Code tiene sentido para este proyecto.

No porque sea “el modelo más inteligente”.

Sino porque su harness coincide con nuestro tipo de trabajo.

Este punto es fundamental.




3.2. Modelo y herramienta NO son lo mismo
Supongamos hipotéticamente:


  Claude Sonnet


El modelo por sí mismo puede razonar sobre código.

Pero no necesariamente puede:


  abrir tu repositorio
  buscar un archivo
  ejecutar Maven
  mirar git diff
  modificar Customer.java
  ejecutar tests
  leer el error

Necesita un sistema alrededor.

Eso es Claude Code.

Anthropic describe actualmente el ciclo agéntico así:


  Gather context
           ↓
  Take action
           ↓
  Verify results
           ↓
  aprende del resultado
           ↓
  repite


y afirma expresamente que Claude Code proporciona el harness que convierte al modelo
en un coding agent mediante herramientas, gestión de contexto y entorno de ejecución.
   Clau…



En castellano sencillo:

   El modelo es el cerebro. Claude Code es el cuerpo, las manos, los ojos y el lugar
   de trabajo.




3.3. Aplicado a nuestro CRM
Cuando en unos pasos digamos:


  Implementa creación de clientes.


el modelo puede pensar:


  Necesito conocer la arquitectura.
  Necesito encontrar ejemplos existentes.
  Necesito revisar la entidad.
  Necesito revisar el repository.
  Necesito revisar el controller.
  Necesito hacer cambios.
  Necesito ejecutar tests.


Pero Claude Code es quien le proporciona los mecanismos:

  Glob
      ↓
  encontrar archivos


  Grep
      ↓
  buscar texto


  Read
      ↓
  leer contenido


  Edit / Write
      ↓
  modificar contenido


  Bash
      ↓
  ./mvnw test


  Git
      ↓
  mediante Bash


  Agent
      ↓
  delegar exploración


  WebSearch / WebFetch
      ↓
  documentación externa


Las tools son lo que transforma:


  "sé qué hacer"


en:


  "puedo hacerlo"


Anthropic clasifica actualmente las capacidades fundamentales en operaciones de
archivos, búsqueda, ejecución, web y code intelligence.   Clau…




3.4. Pero hay una tercera pieza
No es solamente:

  modelo + tools


También necesitamos:


  CONTROL


Porque darle a un modelo:


  Bash
  Edit
  Write
  Web
  Git


sin controles sería peligroso.

Por eso tenemos:


  modelo
  +
  tools
  +
  permissions


Y posteriormente:


  hooks
  sandbox
  settings
  restricciones


Ahí empieza realmente el harness profesional.




3.5. Nuestro harness actualmente es extremadamente
pequeño
Después del Paso 2 tenemos algo parecido a:


  HARNESS ACTUAL
  │
  ├── Git
  │     ├── main
  │     ├── origin
  │     └── repositorio limpio

  │
  ├── Filesystem
  │      ├── backend/
  │      ├── frontend/
  │      └── docs/
  │
  ├── Repository policy
  │      ├── .gitignore
  │      ├── .gitattributes
  │      └── .editorconfig
  │
  └── Claude Code
         └── instalación global

Todavía falta:


  CLAUDE.md
  AGENTS.md
  .claude/settings.json
  .claude/rules/
  .claude/agents/
  hooks
  skills
  MCP


Perfecto.

Eso significa que podemos observar Claude Code casi desnudo antes de empezar a
personalizarlo.

Esa comparación será muy útil.




3.6. Asegurarnos primero de ejecutar Claude desde la
raíz correcta
Abre Git Bash.

Entra:


         Bash

  cd /c/dev/crm-profesional


Adaptando la ruta si escogiste otra.

Comprueba:

        Bash

  pwd


Después:


        Bash

  git rev-parse --show-toplevel


Ambas rutas deberían terminar en:


  crm-profesional


Finalmente:


        Bash

  git status --porcelain


Debe devolver:


  [nada]


Ése será nuestro punto cero.




3.7. Comprueba nuevamente la versión
Ejecuta:


        Bash

  claude --version


Pero ahora hay un matiz importante respecto a cuando comenzamos.

La documentación actual de Claude Code ya contempla modelos posteriores a los que
aparecían en el snapshot de abril del curso. Por ejemplo, la documentación actual lista
Sonnet 5, Opus 5 y Fable 5 en determinados proveedores/configuraciones; la
disponibilidad exacta depende del proveedor, cuenta y versión de Claude Code.
Anthropic indica además que Opus 5 requiere Claude Code 2.1.219 o posterior.
   Claude +1



Por tanto, ejecuta:

        Bash

     claude update


Después:


        Bash

     claude --version


Y:


        Bash

     claude doctor


No necesitamos forzar una versión determinada.

La regla será:

     La versión que tu canal oficial de actualización te entregue es nuestra fuente de
     verdad.

claude doctor también comprueba actualmente si existe una versión más nueva en tu
canal configurado.      Clau…




3.8. No confundas dos comandos llamados doctor
Esto merece quedar completamente claro.

Desde Git Bash, fuera de Claude:


        Bash

     claude doctor


hace diagnósticos de instalación en modo de terminal.

La documentación lo describe como diagnóstico de solo lectura.    Clau…



Dentro de una sesión Claude tenemos:


     /doctor

La versión interna puede hacer una auditoría más amplia del setup y proponer
correcciones; actualmente incluso puede detectar problemas de configuración/contexto y
después pedir confirmación antes de efectuar cambios.    Clau…



Así que conceptualmente:


  claude doctor
       ↓
  diagnóstico CLI


  /doctor
       ↓
  workflow dentro de Claude Code


Por ahora basta con el primero.




3.9. Ahora vamos a arrancar Claude de forma
deliberadamente segura
NO ejecutes simplemente:


     Bash

  claude


En este laboratorio quiero empezar explícitamente en Plan Mode.

Ejecuta:


     Bash

  claude --permission-mode plan


Claude Code acepta --permission-mode plan como forma oficial de iniciar directamente
en ese modo.        Clau…



Ahora has creado una sesión dentro de:


  crm-profesional/




3.10. Qué significa realmente Plan Mode

No significa:

   Claude queda completamente congelado.

Significa principalmente:


  puede explorar
  puede leer
  puede investigar
  puede ejecutar determinadas operaciones de lectura
  NO debe editar el código fuente


La documentación actual describe plan como un modo pensado para explorar antes de
modificar; puede leer y utilizar operaciones de exploración, mientras evita editar el source.
   Claude +1



Ésta es una distinción importante.

Plan Mode no significa:


  Claude no hace nada.


Significa:


  Claude puede pensar con evidencia real
  sin empezar a cambiar el proyecto.




3.11. Piensa en Plan Mode como un arquitecto
caminando por una casa
Imagina que contratas a alguien para reformar tu casa.

Mal procedimiento:


  entra
  ↓
  toma un martillo
  ↓
  derriba una pared
  ↓
  después investiga qué había detrás


Plan Mode es:

  entra
  ↓
  observa
  ↓
  mide
  ↓
  revisa planos
  ↓
  identifica instalaciones
  ↓
  propone un plan
  ↓
  tú revisas
  ↓
  DESPUÉS empieza la obra


Eso será nuestro patrón para cambios importantes.




3.12. Primer comando dentro de Claude: /status
Dentro de Claude escribe:


  /status


Actualmente /status muestra entre otras cosas:
      versión;
      modelo;
      cuenta;
      conectividad.   Clau…


Observa la información.

No cambies nada.

Quiero que empieces a acostumbrarte a:

   inspeccionar antes de configurar.




3.13. Aquí conoceremos el modelo REAL que tienes
El curso habla de modelos concretos porque estaba escrito en otro momento.

Nosotros no vamos a fijar nuestro aprendizaje a:

     Opus 4.7


o:


     Sonnet 4.6


como si fueran eternos.

La documentación actual utiliza aliases como:


     default
     best
     fable
     sonnet
     opus
     haiku
     opusplan


y esos aliases pueden resolver a versiones diferentes según proveedor y momento.
Anthropic recomienda precisamente aliases cuando quieres seguir la versión
recomendada y nombres completos cuando necesitas fijar una versión concreta.       Clau…



Eso nos enseña una idea profunda del Pilar 1:

     Nuestro harness no debería depender innecesariamente del número de versión
     de un modelo.




3.14. Abre ahora /model
Ejecuta:


     /model


No selecciones nada todavía.

Simplemente mira.

La lista que aparezca en tu instalación y tu cuenta es más fiable para nosotros que
cualquier tabla que yo escriba aquí.

La documentación confirma que /model abre el selector y que el conjunto concreto
puede variar según disponibilidad/configuración.   Claude +1

Presiona:


  Esc


para salir del selector sin necesidad de cambiar nada.




3.15. Qué modelo utilizaremos por defecto
Por ahora:


  default


o el modelo que ya haya seleccionado tu cuenta.

No necesitamos optimizar esto todavía.

La razón es pedagógica.

Queremos demostrar:


  BUEN HARNESS
  +
  BUEN CONTEXTO
  +
  BUEN PROMPT


antes de caer en:


  "el resultado fue malo,
  voy a cambiar de modelo"


Ese es exactamente uno de los hábitos que el módulo intenta desmontar.

Más adelante podremos comparar deliberadamente modelos.




3.16. ¿Y qué es opusplan ?
La documentación actual contiene un alias interesante:


  opusplan


que utiliza opus en planificación y sonnet durante ejecución.   Clau…

Conceptualmente:


  PLAN
   ↓
  modelo de razonamiento más fuerte


  IMPLEMENTACIÓN
   ↓
  modelo más eficiente


Es una manifestación directa de:

   el harness puede enrutar modelos según la fase del trabajo.

No vamos a activarlo todavía.

Solo quiero que entiendas por qué es importante.

Ya no estamos hablando simplemente de:


  ¿Qué modelo uso?


Sino de:


  ¿Qué modelo usa mi harness
  para qué fase
  y bajo qué condiciones?




3.17. Ahora inspeccionemos el contexto base
Ejecuta:


  /context all


Claude Code muestra actualmente con /context qué está ocupando la ventana y puede
indicar consumo relacionado con herramientas, memoria y otros componentes.   Clau…



Esto es importantísimo.

Porque todavía NO tenemos:


  CLAUDE.md
  AGENTS.md
  skills del proyecto

  rules del proyecto
  MCP del proyecto
Por tanto estás viendo aproximadamente nuestro:

   baseline de contexto.

Guárdalo mentalmente.

Más adelante repetiremos:


  /context all


y verás cómo cada pieza del harness tiene un costo.




3.18. El contexto NO contiene únicamente nuestra
conversación
La documentación actual explica que la ventana puede contener:


  conversation history
  file contents
  command outputs
  CLAUDE.md
  auto memory
  loaded skills
  system instructions


y otros elementos del trabajo de la sesión.   Clau…



Así:


  1.000.000 tokens disponibles


no significa:


  1.000.000 tokens para mi prompt.


Parte de ese presupuesto está ocupado por:


  sistema
  herramientas
  historial
  archivos leídos
  resultados de Bash
  memorias

  skills
  etc.

Esto será crucial cuando lleguemos al Pilar 2.




3.19. Ahora pregunta qué tools tienes realmente
La propia documentación recomienda, para conocer el toolset real de una sesión:


  What tools do you have access to?


porque depende de proveedor, plataforma y configuración.      Clau…



Nosotros lo haremos en español y con una restricción importante.

Pega:


  Sin modificar ningún archivo ni ejecutar acciones con efectos secundarios, explícam


  Agrúpalas por función:


  - lectura y búsqueda de archivos;
  - modificación de archivos;
  - ejecución de comandos;
  - web;
  - Git o terminal;
  - planificación;
  - subagentes u orquestación;
  - extensiones externas.


  No utilices herramientas para responder salvo que sea estrictamente necesario. Solo


Aquí no estamos programando.

Estamos haciendo:


  introspección del harness




3.20. Las tools importantes que debes reconocer
Tu lista concreta puede cambiar.

Pero Claude Code documenta actualmente herramientas fundamentales como:

  Read
  Glob
  Grep
  Edit
  Write
  Bash
  Agent
  AskUserQuestion
  EnterPlanMode
  ExitPlanMode
  WebSearch
  WebFetch


además de otras dependiendo de versión/proveedor/configuración.   Clau…



No quiero que memorices cincuenta nombres.

Quiero que comprendas familias.




3.21. Familia 1: descubrir

  Glob
  Grep
  Read


Piensa:


  Glob
   ↓
  ¿qué archivos existen?


  Grep
   ↓
  ¿dónde aparece este concepto?


  Read
   ↓
  ¿qué contiene exactamente este archivo?


Por ejemplo posteriormente:


  Glob
  **/*Customer*


podría localizar archivos relacionados con clientes.

Después:


  Grep
  CustomerRepository


podría localizar referencias.

Después:


  Read
  CustomerService.java


obtiene el contenido necesario.




3.22. Una sorpresa importante: .gitignore no es una
barrera para todas las tools
Esto conecta directamente con lo que aprendimos en el Paso 2.

Actualmente:

     Grep normalmente omite archivos ignorados por Git;

     Glob , por defecto, puede encontrar también archivos gitignored.   Clau…



Por tanto:


  .gitignore


NO equivale a:


  Claude no puede ver este archivo.


Eso confirma algo que adelantamos en el Paso 2.

Más adelante construiremos:


  permissions.deny


para secretos.

Ésa será una barrera del harness.

3.23. Familia 2: actuar
Tenemos principalmente:


     Edit
     Write
     Bash



Edit
Cambia partes concretas de archivos.

Write
Crea o reemplaza un archivo completo.

Bash
Ejecuta comandos del sistema.

Por ejemplo:


        Bash

     ./mvnw test


o:


        Bash

     npm run build


o:


        Bash

     git diff


Eso hace que Bash sea extremadamente poderoso.

Porque Claude no necesita una tool separada:


     GitTool


para usar Git.

Puede utilizar:

  Bash
        ↓
  git status
  git diff
  git log
  ...




3.24. Y Bash también explica buena parte del riesgo
Bash puede ejecutar:


        Bash

  git status


que es benigno.

Pero también potencialmente comandos con efectos importantes.

Por eso nunca debemos pensar:


  Claude tiene Bash
  =
  Claude puede hacer cualquier cosa automáticamente.


El harness intercala permisos.

En modo normal, Claude Code utiliza un sistema por niveles:

      operaciones de lectura dentro del working directory generalmente no requieren
      aprobación;
      Bash normalmente requiere aprobación salvo determinadas operaciones de lectura
      reconocidas;
      modificación de archivos requiere aprobación dependiendo del modo.      Clau…


Eso será el centro del Paso 4.




3.25. Una diferencia crucial: instrucción vs enforcement
Supongamos que en un futuro escribimos:


        Markdown

  # CLAUDE.md


  Nunca leas .env.


Eso es:


  INSTRUCCIÓN


El modelo intenta obedecerla.

Pero no es una barrera mecánica.

En cambio:


          JSON

  {
      "permissions": {
          "deny": [
              "Read(./.env)"
          ]
      }
  }


es:


  ENFORCEMENT


Claude Code aplica esa regla fuera del razonamiento del modelo.

La documentación dice explícitamente que las permission rules son aplicadas por Claude
Code, no por el modelo; una instrucción del prompt o de CLAUDE.md no modifica lo que
el harness permite.            Clau…



Éste es uno de los conceptos más importantes del Pilar 1.




3.26. Memorízalo de esta manera

  "Por favor no hagas X"
               ↓
  instrucción al modelo



  "Hacer X está bloqueado"

            ↓

Otro ejemplo:


  CLAUDE.md:
  "Ejecuta tests antes de terminar"


es una instrucción.

Pero un hook que ejecuta un validador automáticamente es comportamiento determinista.

Eso lo veremos en Paso 6.




3.27. Ahora inspeccionemos permissions, SIN
cambiarlos
Ejecuta:


  /permissions


La interfaz actual permite inspeccionar:


  allow
  ask
  deny
  working directories
  scope de cada regla


y también desde qué archivo de settings viene una regla.   Claude +1



Por ahora:


   NO añadas reglas.

Simplemente mira.

Podrías encontrar:


  User
  Project
  Local
  Managed


dependiendo de tu configuración.

Eso nos interesa porque en los pasos siguientes veremos por qué una regla puede ser:


     mía


o:


     del proyecto


o:


     impuesta por una organización




3.28. Si /permissions está casi vacío, está perfecto
No necesitamos veinte reglas el primer día.

Un harness profesional no significa:


     más configuración
     =
     mejor configuración


Nuestro objetivo será:


     mínima configuración
     que haga explícitas
     las restricciones importantes


Eso es muy diferente.




3.29. Los modos actuales de Claude Code
El material del curso hablaba principalmente de modos como Plan.

La versión actual de Claude Code dispone de varios permission modes:

Modo                                   Idea

Manual / default                       máximo control interactivo


acceptEdits                            acepta edits y filesystem común

Modo                                 Idea

plan                                 exploración antes de implementar


auto                                 decisiones automáticas con controles de seguridad


dontAsk                              solo herramientas previamente autorizadas


bypassPermissions                    omite la mayoría de prompts



La documentación actual los distingue explícitamente.    Claude +1



No necesitas utilizarlos todos.




3.30. Nuestra política inicial
Durante aprendizaje:


  PLAN
       ↓
  investigar
  planificar



  MANUAL
       ↓
  primeras ejecuciones sensibles



  ACCEPT EDITS
       ↓
  más adelante cuando confiemos
  en el alcance



  AUTO
       ↓
  solo cuando tengamos suficientes
  guardrails y experiencia


Y por ahora:


  bypassPermissions
           ↓
  NO

Anthropic recomienda bypassPermissions para entornos aislados como containers/VMs,
no como modo normal para trabajar directamente sobre una estación de desarrollo.
   Clau…




3.31. Practica cambiar de modo SIN ejecutar nada
Estás todavía en Plan Mode.

Presiona:


  Shift + Tab


Observa el cambio del indicador.

Vuelve a presionarlo.

Claude Code utiliza actualmente Shift+Tab para recorrer los permission modes
disponibles en el CLI.   Claude +1



No envíes ninguna tarea mientras practicas.

Simplemente observa:


  Plan
  Manual
  Accept Edits
  Auto
  ...


según lo que tu instalación presente.

Finalmente vuelve a Plan.

Este pequeño ejercicio es importante porque cuando Claude esté trabajando algún día no
quiero que estés pensando:


   “¿Cómo hago para detenerlo antes de que toque archivos?”

Debes reconocer el modo visualmente.




3.32. Plan Mode no sustituye a Git
Supón que Claude más adelante edita mal cinco archivos.

Tenemos dos mecanismos diferentes:


     Claude checkpoint


y:


     Git


Claude Code crea checkpoints antes de modificar archivos y permite rebobinar
determinadas modificaciones locales; la documentación advierte que esto no cubre
acciones externas como bases de datos, APIs o deployments.           Clau…



Git, en cambio, es nuestro registro del proyecto.

Por eso:


     CHECKPOINT
     =
     comodidad de sesión


     GIT
     =
     control de versiones del proyecto


No sustituiremos uno por otro.




3.33. Ahora vamos a observar el ciclo agéntico en
nuestro repositorio real
Seguimos en:


     PLAN


Pega exactamente este prompt:


     Analiza el repositorio actual crm-profesional únicamente para comprender su estado.


     No crees, modifiques, muevas ni elimines archivos.


     No hagas commits ni cambies configuración.


     Quiero que determines:


     - cuál es la raíz del repositorio;

  - cuál es la rama actual;
  - qué estructura existe;
  - qué archivos de configuración existen;
  - qué componentes están todavía vacíos;
  - qué políticas básicas puede deducir de .gitignore, .gitattributes y .editorconfig
  - qué cosas importantes del proyecto todavía NO se pueden saber porque aún no exist


  Distingue claramente entre hechos observados y conclusiones inferidas.


  Al final, confirma explícitamente que no modificaste ningún archivo.

Éste será el primer trabajo real que Claude Code hace sobre crm-profesional .

Pero todavía no está implementando nada.




3.34. Mira cómo trabaja, no solo su respuesta final
Presta atención a las tools.

Idealmente verás algo semejante a:


  Glob
  Read
  Bash


o combinaciones equivalentes.

Quizá primero:


  git status


Después:


  Read(.gitignore)


Después:


  Read(.gitattributes)


Después:


  Read(.editorconfig)


Y finalmente sintetizará.

Eso es:

  Gather context


No:


  adivinar desde el prompt




3.35. Esto nos permite diferenciar tres situaciones
Situación A
Claude afirma:

   “El backend utiliza Spring Boot.”

Incorrecto.

Todavía no existe Spring.

Sería una alucinación o inferencia indebida.




Situación B
Claude afirma:

   “ backend/ existe pero actualmente solo contiene .gitkeep .”

Eso es:


  hecho observado




Situación C
Claude dice:

   “La estructura sugiere que se pretende separar frontend y backend.”

Eso es:


  inferencia razonable


pero no debería presentarla como hecho arquitectónico ya implementado.

Esta disciplina de:


  observado
  vs
  inferido


será importantísima en todo el proyecto.




3.36. Ahora comprobamos que Plan Mode hizo lo que
prometía
No confíes únicamente en que Claude diga:

   “No modifiqué nada.”

Verifícalo.

Dentro de Claude puedes escribir directamente:


  ! git status --porcelain


El prefijo ! activa el shell mode: ejecuta el comando directamente, añade el resultado al
contexto y no necesita que Claude interprete primero el comando.     Clau…



Debe aparecer:


  [nada]




3.37. Acabas de conocer otra pieza del harness: Shell
Mode
Hay dos caminos distintos.

Camino A
Tú escribes:


  Revisa el estado de Git.


Claude decide:

  necesito Bash


y ejecuta:


      Bash

  git status



Camino B
Tú escribes:


  ! git status


Y estás ordenando directamente:


  ejecuta esto en el shell


Claude Code añade la salida al contexto después.     Clau…



Esto es útil para operaciones que tú ya sabes exactamente que quieres ejecutar.




3.38. Cuándo usar uno u otro
Utiliza:


  ! git status


cuando:

   sabes exactamente qué comando necesitas.

Utiliza:


  Comprueba si el repositorio está limpio.


cuando:

   quieres delegar a Claude la decisión de cómo comprobarlo.

La primera forma es:


  command-driven

La segunda:


  outcome-driven


Más adelante preferiremos el segundo estilo para tareas de ingeniería complejas.




3.39. Observemos ahora cuánto contexto consumió la
exploración
Ejecuta nuevamente:


  /context all


Compara mentalmente con el primer resultado.

Ahora tenemos más información:


  conversación
  +
  prompt
  +
  archivos leídos
  +
  outputs de tools


Ésta es una demostración real del Pilar 2 dentro del Pilar 1:

   Las tools no son gratuitas en términos de contexto.

Una tool puede darte información útil, pero su resultado entra en el ciclo y ocupa
presupuesto de contexto. Claude Code administra este contexto y compacta
automáticamente cuando es necesario.        Clau…




3.40. ¿Por qué no le decimos “lee todo el repo”?
Nuestro repositorio actual es diminuto.

No pasaría nada.

Pero queremos desarrollar un hábito que escale.

Dentro de unos meses podría existir:

  10.000 archivos
  100.000 líneas
  500.000 líneas


El patrón sano será:


  objetivo
      ↓
  búsqueda dirigida
      ↓
  lecturas relevantes
      ↓
  acción


No:


  mete todo
      ↓
  espera que el modelo encuentre
  la información correcta




3.41. El modelo decide qué tools utilizar, no
deberíamos microgestionarlo normalmente
La documentación oficial recomienda describir el resultado deseado y permitir que Claude
decida qué archivos/commands necesita, especialmente para trabajo complejo.      Clau…



Por eso más adelante preferiremos:


  Identifica por qué falla la creación de clientes
  y corrígelo.


sobre algo parecido a:


  1. ejecuta grep
  2. abre archivo A
  3. lee línea 25
  4. abre archivo B
  5. modifica método C


excepto cuando tengamos una razón concreta para imponer esos pasos.

3.42. “Delegar, no dictar”
Ésta es una idea muy importante.

Tú decides:


  QUÉ


Claude puede decidir:


  CÓMO EXPLORAR


Pero tú conservas control sobre:


  CRITERIOS
  RESTRICCIONES
  PERMISOS
  VERIFICACIÓN


Así:


  Humano
   ├── objetivo
   ├── restricciones
   ├── arquitectura
   ├── decisiones de negocio
   └── criterios de éxito


  Claude
   ├── búsqueda
   ├── navegación
   ├── edición
   ├── ejecución
   └── iteración


Esto será una relación muchísimo más profesional que utilizar Claude como
autocompletado glorificado.




3.43. Herramienta ≠ contexto ≠ prompt
Vamos a aplicar nuestro diagnóstico de tres pilares.

Supongamos que dentro de unos días escribes:


  Crea clientes.

y Claude genera algo malo.

Tenemos que preguntar:

¿Problema de herramienta?

  ¿Claude puede leer el repo?
  ¿puede ejecutar tests?
  ¿tiene Bash?
  ¿está en el modo adecuado?



¿Problema de contexto?

  ¿conoce nuestra arquitectura?
  ¿conoce las convenciones?
  ¿leyó archivos relevantes?
  ¿CLAUDE.md está actualizado?



¿Problema de prompt?

  ¿Qué significa "crear clientes"?
  ¿Cuáles son los criterios?
  ¿Qué restricciones existen?


No saltamos directamente a:


  Necesito otro modelo.


Ése es precisamente el modelo mental que queremos desarrollar.




3.44. Hagamos un ejemplo infantil
Imagina un chef.

Modelo

  cerebro del chef



Tool

  cuchillo
  horno

  sartén


Contexto

  receta
  ingredientes disponibles
  alergias del cliente
  inventario



Prompt

  prepara una pizza margarita



Permissions

  puede usar el horno,
  pero no puede entrar
  al almacén restringido



Hook

  antes de servir,
  un termómetro comprueba
  automáticamente la temperatura


No arreglas una mala cocina únicamente contratando un chef con un cerebro un poco
mejor.




3.45. Nuestro equivalente

  MODELO
  Claude


  TOOLS
  Read/Edit/Bash/Grep/...


  CONTEXTO
  repo + instrucciones + archivos


  PROMPT
  tarea actual


  PERMISSIONS
  qué puede ejecutar

  HOOKS
  qué validamos automáticamente


  GIT
  checkpoint profesional


  TESTS
  oráculo de comportamiento


  OPENSPEC
  más adelante:
  contrato formal del cambio


Ahora empieza a verse por qué todos nuestros módulos harán match.




3.46. ¿Qué NO configuraremos en este paso?
Todavía no crees:


  .claude/settings.json


Eso llegará en el Paso 5.

Todavía no crees:


  CLAUDE.md
  AGENTS.md


Eso llegará cuando diseñemos el Pilar 2.

Todavía no crees:


  hooks


Paso 6.

Todavía no crees:


  subagents personalizados


Paso 12.

Todavía no configures:

  MCP


sin necesidad real.

Y absolutamente todavía no:


  OpenSpec


Eso será Módulo 2.




3.47. ¿Por qué no vamos a ejecutar /init todavía?
Actualmente /init puede generar un CLAUDE.md inicial.     Clau…




Pero no quiero que Claude nos genere automáticamente el contexto antes de que tú
entiendas:


  qué debe entrar
  qué debe quedar fuera
  qué debe ser global
  qué debe ser backend
  qué debe ser frontend
  qué debe ser rule
  qué debe ser skill


En nuestro proyecto:


  CLAUDE.md


será una decisión de ingeniería.

No el resultado ciego de:


  /init


Podremos usar /init posteriormente como comparación o auditoría, no
necesariamente como fuente de verdad.




3.48. Otro detalle importante de /doctor
La documentación actual ha evolucionado muchísimo.

/doctor puede incluso detectar CLAUDE.md con información derivable del codebase y
sugerir mover conocimiento a mecanismos cargados bajo demanda.         Clau…



Eso refuerza la decisión que tomamos en el Paso 1:


   no queremos CLAUDE.md gigantes.

El producto mismo puede contener información.

No necesitamos duplicarla toda en contexto persistente.




3.49. Qué información pertenece al harness
Aquí quiero establecer una taxonomía que utilizaremos durante el resto del proyecto.

Capa 1 — entorno

  Windows
  Git Bash
  Java
  Node
  Docker
  Git



Capa 2 — repositorio

  .git
  .gitignore
  .gitattributes
  .editorconfig



Capa 3 — Claude Code base

  modelo
  tools
  sessions
  context
  checkpoints
  permission mode



Capa 4 — configuración del proyecto
Más adelante:

  .claude/settings.json
  permissions



Capa 5 — automatización

  hooks



Capa 6 — conocimiento

  AGENTS.md
  CLAUDE.md
  rules



Capa 7 — workflows

  skills
  subagents



Capa 8 — integraciones externas

  MCP


Nuestro harness crecerá progresivamente.




3.50. Un principio que quiero que conserves
Cada vez que añadamos algo al harness preguntaremos:

   ¿Qué problema concreto resuelve?

No añadiremos un MCP porque esté de moda.

No añadiremos 20 subagentes porque Claude los soporte.

No añadiremos 500 líneas de reglas.

No añadiremos 30 hooks.

No añadiremos plugins innecesarios.

La arquitectura correcta inicialmente será:

     mínima
     +
     explícita
     +
     auditable
     +
     ampliable




3.51. Las sesiones también pertenecen al harness
Claude Code guarda las conversaciones localmente y permite reanudarlas; una sesión
nueva arranca con una ventana de contexto fresca.    Clau…



Esto significa que:


     Nueva sesión


no equivale a:


     perdí el proyecto.


El proyecto permanece en:


     Git
     archivos
     CLAUDE.md futuro
     AGENTS.md futuro


La conversación no debería ser nuestra base de datos arquitectónica.




3.52. La conversación es memoria de trabajo
Piensa:


     Sesión Claude
     =
     RAM


y:


     repositorio + documentación
     =

     disco

No quieres que información crítica exista exclusivamente en:


     "algo que hablamos hace 78 turnos"


Porque puede compactarse, perder prioridad o quedar asociada a otra sesión.

Lo persistente debe estar donde corresponde.

Eso será Pilar 2.




3.53. Claude Code ya compacta automáticamente
Cuando el contexto se aproxima al límite, Claude Code puede eliminar outputs antiguos y
posteriormente resumir la conversación. También permite:


     /compact


y:


     /context


para gestionar el proceso conscientemente.     Claude +1



No estableceremos todavía una regla rígida:


     compactar exactamente al 70%


porque Anthropic no define ese porcentaje universal como ley.

Nuestra regla será:


     contexto útil > contexto abundante




3.54. Hay otra herramienta útil que conocerás ahora:
/btw
Las versiones actuales ofrecen:


     /btw

para hacer una pregunta lateral utilizando el contexto actual sin añadir esa
pregunta/respuesta al historial principal. No dispone de tools propias y funciona como una
consulta efímera.     Clau…



Por ejemplo:


  /btw ¿qué rama de Git detectaste?


puede ser útil durante una tarea grande sin contaminar la conversación principal.

No es obligatorio utilizarlo.

Pero es otro ejemplo excelente de harness engineering aplicado a gestión del
contexto.




3.55. Hagamos una prueba con /btw
Como Claude ya exploró nuestro repo, escribe:


  /btw ¿qué archivos de configuración encontraste en la raíz?


Observa que responde desde lo que ya sabe.

No debería realizar nuevas búsquedas.

Eso demuestra:


  mismo contexto
  +
  pregunta lateral
  +
  sin ensuciar historial principal


Las preguntas /btw no tienen tool access; solo utilizan lo que ya está en contexto.
   Clau…




3.56. Interrumpir también es parte del harness
Cuando Claude haga algo que no deseas:


  Esc


lo detiene.

Anthropic documenta que puedes interrumpir la ejecución y redirigirla durante el ciclo
agéntico.    Clau…



No tienes que observar impotente hasta que termine.

Ésta es una diferencia psicológica importante.

Claude Code es:


  agente supervisado


no:


  programador autónomo dueño del repo




3.57. Al terminar nuestro laboratorio, no queremos
cambios
Ejecuta nuevamente:


  ! git status --porcelain


Debe estar vacío.

Ahora sal:


  /exit


Volverás a Git Bash.

Ejecuta otra vez:


      Bash

  git status --porcelain


Resultado esperado:


  [nada]

3.58. ¿Entonces el Paso 3 no produce commit?
Correcto.

Y eso es totalmente profesional.

No todo paso de ingeniería necesita producir código.

El producto del Paso 3 es:


  conocimiento validado
  +
  harness observado
  +
  baseline establecido


Todavía tenemos:


  git log


con nuestro único commit de estructura.

No hagas un commit vacío únicamente para “tener un commit del paso 3”.

Git debe representar cambios del repositorio, no nuestro número de lección.




3.59. Estado exacto del proyecto
Después del Paso 3:


  crm-profesional/
  │
  ├── backend/
  │   └── .gitkeep
  │
  ├── frontend/
  │   └── .gitkeep
  │
  ├── docs/
  │   └── .gitkeep
  │
  ├── .editorconfig
  ├── .gitattributes
  ├── .gitignore
  └── README.md


Todavía NO:

  CLAUDE.md
  AGENTS.md
  .claude/
  Spring
  React
  Docker Compose
  OpenSpec


Perfecto.




3.60. Lo que ya sabemos ahora sobre nuestra
herramienta
Antes:


  Claude Code
  =
  programa al que escribo prompts


Ahora:


  Claude Code
  =
  harness agéntico


que combina:


  MODEL
  +
  TOOLS
  +
  ENVIRONMENT
  +
  CONTEXT MANAGEMENT
  +
  PERMISSIONS
  +
  SESSIONS
  +
  CHECKPOINTS
  +
  EXTENSIONS


La documentación oficial actual utiliza precisamente esta distinción entre modelo que
razona y harness que proporciona tools, contexto y entorno de ejecución.    Clau…

3.61. Lo más importante que debes poder explicar
Pregunta 1
¿Claude y Claude Code son lo mismo?

No.


  Claude
  =
  modelo


  Claude Code
  =
  harness agéntico
  alrededor del modelo




Pregunta 2
¿Qué hacen las tools?

Transforman decisiones del modelo en acciones reales.


  Read
  Edit
  Bash
  Grep
  ...




Pregunta 3
¿Qué hacen permissions?

Deciden qué acciones puede ejecutar Claude Code y bajo qué condiciones.

No dependen únicamente de que el modelo quiera obedecer.




Pregunta 4
¿Qué hace Plan Mode?

Permite explorar y diseñar antes de modificar el source.




Pregunta 5
¿Por qué .gitignore no basta para secretos?

Porque es una política Git.

No constituye por sí sola una barrera universal de lectura para Claude.

De hecho, herramientas como Glob pueden encontrar archivos ignorados por Git.
   Clau…




Pregunta 6
¿Por qué usamos Git si Claude tiene checkpoints?

Porque:


  checkpoints = seguridad de sesión


  Git = historia profesional del proyecto




Pregunta 7
¿Qué hacemos cuando Claude produce malos resultados?

No cambiamos inmediatamente de modelo.

Preguntamos:


  ¿herramienta?
  ¿contexto?
  ¿prompt?




3.62. Nuestro primer mapa oficial de diagnóstico
Quiero que memorices este árbol:

            CLAUDE HIZO ALGO MAL
                     │
                     ▼
        ┌───────────────────────┐
        │ ¿PUDO hacer la tarea? │
        └──────────┬────────────┘
                     │
            NO ────┴──── SÍ
            │                │
            ▼                ▼
       HERRAMIENTA       ¿TENÍA la
       / HARNESS         información?
                             │
                         NO ──┴── SÍ
                         │            │
                         ▼            ▼
                     CONTEXTO        ¿ENTENDIÓ
                                 claramente
                                 el objetivo?
                                          │
                                 NO ──┴── SÍ
                                 │             │
                                 ▼             ▼
                             PROMPT           investigar
                                              otro factor


Éste será uno de nuestros marcos fundamentales.




3.63. Checklist práctico del Paso 3
Antes de cerrar este paso verifica:


  [ ] Estoy dentro de crm-profesional


  [ ] git status --porcelain estaba vacío


  [ ] comprobé/actualicé Claude Code mediante canal oficial


  [ ] claude doctor no reporta un problema que bloquee trabajo local


  [ ] inicié:
      claude --permission-mode plan


  [ ] ejecuté /status


  [ ] inspeccioné /model


  [ ] dejé el modelo actual/default por ahora

  [ ] ejecuté /context all antes de explorar


  [ ] pregunté qué tools tiene Claude disponibles


  [ ] abrí /permissions sin cambiar reglas


  [ ] recorrí los modos con Shift+Tab


  [ ] regresé a Plan Mode


  [ ] Claude inspeccionó el repositorio sin modificarlo


  [ ] distinguí hechos observados de inferencias


  [ ] probé shell mode con:
      ! git status --porcelain


  [ ] ejecuté nuevamente /context all


  [ ] probé /btw


  [ ] salí con /exit


  [ ] git status --porcelain sigue completamente vacío

Si todos se cumplen:

Paso 3 completado.


Qué viene ahora
Tenemos:


  Paso 1
  Producto y metodología
           ✓


  Paso 2
  Repositorio y monorepo
           ✓


  Paso 3
  Comprender Claude Code
  como modelo + harness
           ✓


Ahora estamos preparados para una parte muchísimo más delicada.

Paso 4 de 18 — Permisos, Plan Mode y política segura
de ejecución
Ahí ya no nos limitaremos a observar /permissions .

Vamos a diseñar conscientemente qué debe ocurrir con operaciones como:


  Read
  Edit
  Write


  git status
  git diff
  git log


  ./mvnw test
  npm test


  rm
  git reset
  git checkout
  git clean


  .env
  secrets
  SSH keys
  credenciales


  comandos de red


Y aprenderemos la diferencia entre:


  allow
  ask
  deny


además de decidir qué jamás debería quedar aprobado automáticamente.

Será la primera configuración real de seguridad de nuestro harness, antes de
permitirle construir una sola línea del CRM.

¿Deseas continuar con el Paso 4 de 18: configurar permisos, Plan Mode y una
política segura de ejecución para crm-profesional ?