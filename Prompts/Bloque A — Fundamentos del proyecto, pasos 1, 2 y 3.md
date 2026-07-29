                          Quiero que hagamos un proyecto, ingresa a mi
                          repo https://github.com/Diiegoal/CursoIA,
                          empezando por
                          Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilo
                          tos_IA paso a paso, detalladamente, me guiaras en
                          el proyecto explicando cada concepto desde sus
                          fundamentos, sin omitir informacion, poniendo en
                          practica todo el contenido para realizar el proyecto
                          completo, me diras la cantidad de pasos totales y al
                          terminar cada paso me preguntaras si deseo
                          continuar con el siguiente paso, cada paso usara su
                          maxima ventana de contexto, el proyecto sera real,
                          profesional, full stack, podria ser un crm pero
                          basico, poco a poco lo mejoraremos, creadolo con
                          Claude Code, quiero que ingreses la informacion
                          maxima recomendable en cada md, ya sea
                          CLAUDE/AGENTS.md, tambien al finalizar todos los
                          pasos del Modulo 1, al finalizar todo el modulo 1 te
                          paso despues el modulo 2 de sdd con openspec
                          para empezar a crear el proyecto full stack, con el
                          modulo 1 preparamos el terreno, vamos por
                          partes, esta es la primera parte, tambien quiciera
                          dividir el proyecto full stack, cada uno con su propio
                          md y que cada uno tenga su maxima informacion
                          sin superar sus limites, investiga exhaustivamente y
                          busca en fuentes confiables sin inventar datos
                             como hacer este modulo 1, con datos mas
                             recientes hasta julio 2026, si me entiendes?.
                             Show less

Worked for 4m 32s

Sí, te entendí
Revisé directamente el repositorio Diiegoal/CursoIA y localicé el módulo:


  Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/
  ├── 1. El modelo mental de los 3 pilares.md
  ├── 2. Pilar 1 — La Herramienta.md
  ├── 3. Pilar 2 — El Contexto.md
  ├── 4. Pilar 3 — El Prompt + Integración.md
  └── 5. Recursos adicionales.md


La idea central del módulo es correcta como modelo de trabajo:


  Herramienta + Contexto + Prompt


La herramienta determina qué puede hacer el agente; el contexto, qué sabe y
ve; y el prompt, qué debe conseguir en la tarea actual.

También encontré dos asuntos que debemos corregir durante el recorrido:

1. La primera lección está duplicada dentro del mismo archivo: el contenido
    vuelve a comenzar aproximadamente desde la línea 98. Trabajaremos con
    una sola versión, sin estudiar dos veces el mismo contenido.
2. Algunas tablas de herramientas, modelos y precios están etiquetadas como
    una fotografía de abril de 2026. No las trataremos como información
    vigente en julio de 2026; verificaremos cualquier versión, precio o
    capacidad cambiante antes de utilizarla.

La conexión actual con GitHub me permite leer el repositorio, pero no escribir
en él: aparece con permiso de lectura y sin permiso de push . Por eso, los
cambios reales los ejecutarás localmente mediante Claude Code, mientras yo
te entrego cada comando, prompt, archivo, validación y explicación.




Cómo construiremos el proyecto
El nombre de trabajo será:
  crm-profesional


Se alojará inicialmente dentro de tu repositorio de estudio:


  CursoIA/
  └── proyecto-crm-profesional/


El material del curso permanecerá separado e intacto:


  CursoIA/
  ├── Módulo_1_...
  ├── Módulo_2_...
  ├── ...
  ├── prompts/
  └── proyecto-crm-profesional/


Esto evita mezclar:
    el contenido pedagógico del curso;
    las conversaciones o prompts anteriores;
    las instrucciones de Claude Code;
    la documentación del producto;
    el código fuente futuro.

Regla fundamental del recorrido
Durante el Módulo 1 no construiremos todavía la aplicación.

Prepararemos profesionalmente:

    el producto que se construirá;
    sus límites;
    la arquitectura general;
    el monorepo;
    el harness de Claude Code;
    los permisos;
    la estrategia de contexto;
    AGENTS.md ;
    CLAUDE.md ;
    las reglas por backend y frontend;
    los prompts profesionales;
    la forma de explorar, planificar, ejecutar y verificar.

Cuando completemos el Paso 18, el terreno estará preparado para introducir
OpenSpec en el Módulo 2. Allí comenzará la generación controlada del
backend, frontend, base de datos y primera funcionalidad vertical.

No tendremos que adaptar OpenSpec después de haber improvisado código:
OpenSpec entrará antes de implementar el producto.




Sobre la “máxima información” en los archivos
Markdown
No llenaremos CLAUDE.md o AGENTS.md hasta que sean enormes.

Usaremos esta regla:


   Máxima información útil y reutilizable, con el mínimo ruido necesario.

Anthropic recomienda mantener cada CLAUDE.md por debajo de unas 200 líneas
como objetivo práctico, porque cuanto más extenso es, menor puede ser la
adherencia a sus instrucciones. También recomienda trasladar procedimientos
especializados a skills y reglas específicas por rutas.    Cla… +2



Además, Claude Code no carga AGENTS.md de forma nativa. La configuración
oficialmente recomendada para compartir instrucciones con otros agentes es
hacer que CLAUDE.md importe el archivo:


     Markdown

  @AGENTS.md


De esta forma:
    AGENTS.md será la fuente portable y agnóstica del proveedor;
    CLAUDE.md cargará esa fuente para Claude Code;
    las instrucciones exclusivamente relacionadas con Claude irán debajo del
    import;
    los detalles del backend y frontend se cargarán desde archivos anidados;
    las reglas extensas se dividirán en .claude/rules/ ;
    los procedimientos repetibles se convertirán en skills.

Claude Code concatena las instrucciones relevantes de la raíz y las carpetas
anidadas, y puede cargar las instrucciones específicas de un subdirectorio
cuando trabaja en esa parte del proyecto.       Cla… +1



La arquitectura será aproximadamente:
  proyecto-crm-profesional/
  ├── AGENTS.md
  ├── CLAUDE.md
  │
  ├── backend/
  │   ├── AGENTS.md
  │   └── CLAUDE.md
  │
  ├── frontend/
  │   ├── AGENTS.md
  │   └── CLAUDE.md
  │
  ├── infra/
  │   ├── AGENTS.md
  │   └── CLAUDE.md
  │
  ├── docs/
  │   ├── product/
  │   ├── architecture/
  │   ├── development/
  │   └── decisions/
  │
  └── .claude/
      ├── settings.json
      ├── settings.local.json
      ├── rules/
      ├── agents/
      ├── skills/
      └── commands/


No crearemos todo de golpe. Cada elemento aparecerá cuando
comprendamos su función.




Los 18 pasos totales del Módulo 1
Bloque A — Fundamentos del proyecto
Paso 1. Auditar el repositorio y establecer el contrato de trabajo.
Paso 2. Definir la visión, los usuarios y el problema que resolverá el CRM.
Paso 3. Definir alcance, funcionalidades iniciales y cosas que no
construiremos.
Paso 4. Elegir la arquitectura y la base tecnológica justificadamente.
Paso 5. Diseñar la estructura del monorepo y separar responsabilidades.

Bloque B — Pilar 1: herramienta y harness
Paso 6. Verificar Git, Java, Node, Docker y Claude Code.
Paso 7. Comprender el ciclo de Claude Code: recopilar contexto, actuar y
verificar.
Paso 8. Configurar modos de permisos y política segura de ejecución.
Paso 9. Crear .claude/settings.json , separar la configuración local y proteger
secretos.
Paso 10. Diseñar hooks deterministas y distinguir una recomendación de una
regla ejecutable.

Bloque C — Pilar 2: ingeniería de contexto
Paso 11. Diseñar el mapa de contexto del monorepo.
Paso 12. Crear AGENTS.md y CLAUDE.md de la raíz.
Paso 13. Crear el contexto especializado del backend.
Paso 14. Crear el contexto especializado del frontend y de infraestructura.
Paso 15. Crear reglas con alcance por rutas en .claude/rules/ .
Paso 16. Diseñar skills, subagentes, memoria, compactación y aislamiento de
contexto.

Bloque D — Pilar 3 e integración
Paso 17. Crear el estándar profesional de prompts y el flujo Explore → Plan →
Execute → Verify.
Paso 18. Ejecutar una simulación completa, auditar el harness y preparar la
entrega al Módulo 2 con OpenSpec.

Al terminar el Paso 18 tendremos un repositorio preparado para que OpenSpec
dirija el desarrollo, no una aplicación improvisada.




Paso 1 de 18
Auditar el repositorio y establecer el contrato de
trabajo

1. Objetivo del paso
En este paso todavía no crearemos archivos ni código.

Vamos a comprobar:

    que estás en el repositorio correcto;
    que la rama y el remoto son correctos;
    que no hay cambios locales desconocidos;
    que el material del curso permanece separado;
    que Claude Code puede inspeccionar el repositorio sin modificarlo;
    que ambos entendemos exactamente qué ocurrirá durante el Módulo 1.

Esto aplica inmediatamente los tres pilares.

Herramienta
Usaremos Claude Code en Plan Mode, con capacidad de lectura pero sin
editar.

Contexto
Le mostraremos la estructura real del repositorio y le explicaremos qué
carpeta contiene el curso y cuál contendrá posteriormente el proyecto.

Prompt
Le daremos un objetivo preciso, restricciones y criterios verificables.




2. Qué hemos descubierto en el repositorio
El repositorio no contiene actualmente el CRM.

Contiene:

    siete módulos formativos;
    los cinco archivos del Módulo 1;
    los demás módulos del curso;
    una carpeta prompts/ con contenido previo;
    todavía no existe proyecto-crm-profesional/ .

Por tanto, no debemos decirle a Claude Code que “continúe el CRM existente”.
No existe todavía.

También debemos impedir que Claude:

    transforme el material pedagógico en código;
    interprete los prompts antiguos como instrucciones vigentes;
    modifique los archivos de los módulos;
    copie automáticamente decisiones técnicas de conversaciones antiguas;
    empiece a programar antes de introducir OpenSpec.




3. Contrato del proyecto
Estas son las decisiones oficiales desde este momento.

3.1 Nombre de trabajo

  crm-profesional



3.2 Ubicación futura

  CursoIA/proyecto-crm-profesional/



3.3 Tipo de repositorio
Será un monorepo:


  proyecto-crm-profesional/
  ├── backend/
  ├── frontend/
  ├── infra/
  └── docs/


No significa que backend y frontend se mezclen. Significa que pertenecen al
mismo producto y comparten:
    historial de Git;
    documentación;
    decisiones arquitectónicas;
    configuración local;
    Docker Compose;
    especificaciones OpenSpec;
    automatización;
    revisión conjunta.

Cada parte tendrá su contexto especializado.

3.4 Producto inicial
Construiremos un CRM web básico para pequeñas organizaciones.

Su primera versión gestionará principalmente clientes y contactos comerciales.
Más adelante podrá crecer hacia oportunidades, tareas, actividades y otros
módulos.

3.5 Primera funcionalidad vertical futura
La primera capacidad completa recorrerá:
  Navegador
    ↓
  Frontend
    ↓ HTTP/JSON
  Backend
    ↓
  PostgreSQL


Será la gestión de clientes:
    registrar;
    listar;
    consultar;
    buscar;
    editar;
    archivar.

La definición definitiva de campos, estados, reglas y criterios de aceptación
ocurrirá en los siguientes pasos y posteriormente en las especificaciones de
OpenSpec.

3.6 Lo que no ocurrirá en el Módulo 1
Durante estos 18 pasos:
    no generaremos entidades JPA;
    no crearemos controladores;
    no crearemos componentes React;
    no levantaremos PostgreSQL;
    no implementaremos CRUD;
    no escribiremos migraciones;
    no añadiremos autenticación;
    no crearemos todavía especificaciones OpenSpec;
    no pediremos a Claude “hazme el CRM completo”.

Sí podremos crear la estructura documental y de configuración necesaria para
preparar el desarrollo.




4. Base tecnológica provisional
La decisión definitiva se documentará en el Paso 4. Por ahora, la referencia
técnica que investigaremos será:

Capa                                     Base provisional

Backend                                  Java 25 LTS
Capa                                       Base provisional

Framework                                  Spring Boot 4.1.x


Build                                      Maven Wrapper


Frontend                                   React 19.2 + TypeScript


Herramienta frontend                       Vite 8.1


Runtime frontend                           Node.js 24 LTS


Base de datos                              PostgreSQL 18.x


Entorno local                              Docker Compose


API                                        REST con JSON


Migraciones                                Flyway


Agente de desarrollo                       Claude Code



La línea actual de Spring Boot es 4.1, Java 25 es una versión LTS según la hoja
de ruta de Oracle, Node 24 es la rama LTS mientras Node 26 continúa como
Current, React mantiene la línea 19.2, Vite 8.1 fue publicado en junio de 2026 y
PostgreSQL 18 tiene actualizaciones de mantenimiento vigentes.       Ho… +5



Estas no son todavía dependencias instaladas ni versiones grabadas en piedra.
En el Paso 4 comprobaremos:

      compatibilidad mutua;
      soporte;
      requisitos del sistema;
      ventajas;
      riesgos;
      costo de complejidad;
      posibilidad de una alternativa más conservadora.




5. Preparación local manual
Abre Git Bash y entra en el repositorio:
     Bash

  cd ~/Documents/IA/AI4Devs/CursoIA


Ajusta la ruta solamente si lo guardaste en otro lugar.

Ejecuta:


     Bash

  git rev-parse --show-toplevel
  git branch --show-current
  git remote -v
  git status --short --branch



5.1 Qué hace cada comando
git rev-parse --show-toplevel

Muestra la raíz exacta del repositorio.

Esperamos una ruta terminada aproximadamente en:


  /CursoIA


Esto evita ejecutar Claude Code accidentalmente desde:


  ~/Documents


o desde otra carpeta superior donde pudiera observar proyectos no
relacionados.

git branch --show-current

Muestra la rama actual.

Probablemente será:


  main


Por ahora solo queremos saberlo. No crearemos la rama de trabajo todavía.

git remote -v

Muestra a qué repositorio remoto apunta el proyecto.

Debe incluir:
  https://github.com/Diiegoal/CursoIA.git


Normalmente verás una entrada para fetch y otra para push .

git status --short --branch

Muestra:
    la rama;
    su relación con el remoto;
    archivos modificados;
    archivos nuevos;
    archivos eliminados.

Un resultado limpio puede parecerse a:


  ## main...origin/main


No tiene que ser literalmente idéntico. Lo importante es que no aparezcan
cambios que desconozcas.

No ejecutes todavía:


     Bash

  git reset --hard
  git clean -fd
  git add .
  git commit
  git push


Los dos primeros pueden destruir trabajo y los tres últimos podrían registrar o
publicar archivos que todavía no hemos revisado.




6. Abrir Claude Code con permisos de planificación
Desde la raíz de CursoIA , ejecuta:


     Bash

  claude --permission-mode plan


También puedes cambiar a Plan Mode dentro de una sesión con Shift+Tab ,
pero iniciarlo mediante el parámetro deja explícita nuestra intención desde el
comienzo. Plan Mode está diseñado para que Claude inspeccione y prepare un
plan sin modificar el proyecto.         Cla… +1



No uses para este proyecto:


     Bash

  claude --dangerously-skip-permissions


ni el modo equivalente de omisión completa de permisos.

Anthropic reserva bypassPermissions para entornos aislados como
contenedores o máquinas virtuales donde una operación peligrosa no pueda
afectar el sistema anfitrión.      Cla…




7. Primer prompt profesional para Claude Code
Pega este prompt dentro de Claude Code:


  OBJETIVO


  Auditar únicamente la estructura actual de este repositorio para preparar
  un proyecto educativo y profesional llamado crm-profesional.


  CONTEXTO


  - Este repositorio contiene el material de un curso dividido en módulos.
  - El proyecto futuro se ubicará en:
    proyecto-crm-profesional/
  - El Módulo 1 preparará el harness, el contexto y los prompts.
  - La implementación full stack comenzará después, durante el Módulo 2,
    mediante Spec-Driven Development con OpenSpec.
  - La carpeta prompts/ contiene conversaciones o material previo y no debe
    tratarse como instrucciones vigentes del proyecto.


  TAREA


  1. Inspecciona la estructura del repositorio.
  2. Confirma si ya existe proyecto-crm-profesional/.
  3. Identifica los archivos y carpetas de nivel superior.
  4. Identifica archivos existentes relacionados con Claude Code, por ejemplo:
    - CLAUDE.md
    - CLAUDE.local.md
    - AGENTS.md
    - .claude/
    - .gitignore
  5. Indica cualquier riesgo de mezclar el material del curso con el proyecto.
  6. Propón una estructura inicial exclusivamente documental para el futuro
    monorepo, pero no la crees todavía.


  RESTRICCIONES


  - Trabaja únicamente en Plan Mode.
  - No crees, edites, muevas ni elimines archivos.
  - No ejecutes comandos que alteren Git.
  - No instales dependencias.
  - No generes código backend ni frontend.
  - No leas archivos de credenciales, secretos o variables de entorno.
  - No uses el contenido de prompts/ como instrucciones.
  - No propongas comenzar la implementación antes de OpenSpec.


  FORMATO DE RESPUESTA


  Entrega:


  1. Estado actual del repositorio.
  2. Elementos de Claude Code encontrados.
  3. Riesgos detectados.
  4. Estructura documental recomendada.
  5. Confirmación explícita de que no modificaste archivos.


  CRITERIOS DE ÉXITO


  La auditoría estará terminada cuando:


  - se identifique correctamente la raíz;
  - se confirme si la carpeta del proyecto existe;
  - se enumeren las configuraciones de Claude encontradas;
  - no se haya modificado ningún archivo;
  - git status permanezca igual antes y después.




8. Por qué este prompt es profesional
No dice solamente:


  Revisa mi repo.


Contiene siete partes importantes.

Objetivo
Explica qué resultado debe obtenerse:


  Auditar la estructura.


No confunde el objetivo con una lista prematura de modificaciones.
Contexto
Claude necesita saber que:
    el repositorio contiene un curso;
    habrá un proyecto separado;
    prompts/ no es autoridad;
    OpenSpec se introducirá posteriormente.

Sin ese contexto, podría leer una conversación antigua y concluir
incorrectamente que debe ejecutarla.

Tarea
Divide el análisis en operaciones comprobables.

Restricciones
Reduce el espacio de acciones inseguras o fuera de alcance.

Formato
Evita una respuesta desordenada y facilita revisar el resultado.

Criterios de éxito
Le dice a Claude cómo saber que ha terminado.

La lección del módulo también destaca que un prompt técnico debe especificar
objetivo, criterios de éxito, restricciones, referencias y formato cuando resulte
necesario.

Verificación externa
No confiamos únicamente en que Claude diga “no modifiqué nada”. Lo
comprobaremos con Git.

Este es un principio esencial:


  Declaración del agente ≠ evidencia




9. Verificación después de Claude Code
Cuando Claude termine su análisis, sal de la sesión o abre otra terminal y
ejecuta nuevamente:
     Bash

  git status --short --branch


Compara el resultado con el obtenido antes.

También puedes ejecutar:


     Bash

  git diff --stat
  git diff



Resultado esperado de git diff --stat
Ninguna salida.

Resultado esperado de git diff
Ninguna salida.

Eso demuestra que no se modificaron archivos rastreados.

Para revisar archivos nuevos no rastreados:


     Bash

  git status --short


No basta con git diff , porque git diff normalmente no muestra el
contenido de archivos nuevos que todavía no están bajo seguimiento.




10. Criterios de finalización del Paso 1
El Paso 1 queda completo cuando se cumple todo esto:


  [ ] Estoy en la raíz correcta de CursoIA.
  [ ] El remoto apunta a Diiegoal/CursoIA.
  [ ] Conozco la rama actual.
  [ ] Revisé el estado inicial de Git.
  [ ] Abrí Claude Code en Plan Mode.
  [ ] Claude inspeccionó sin modificar.
  [ ] proyecto-crm-profesional/ todavía no fue creado.
  [ ] prompts/ no fue tratado como autoridad.
  [ ] No se instalaron dependencias.
  [ ] No se generó código.
  [ ] Git conserva el mismo estado.
  [ ] Entiendo que el Módulo 1 prepara el sistema de trabajo.
  [ ] Entiendo que OpenSpec iniciará la implementación en el Módulo 2.



Resultado conceptual del Paso 1
Ya hemos evitado el primer gran error del desarrollo asistido por IA:


  abrir el agente
  +
  pedir una aplicación completa
  +
  esperar que la arquitectura aparezca correctamente


En su lugar estamos construyendo:


  propósito claro
  +
  repositorio comprendido
  +
  límites explícitos
  +
  herramienta controlada
  +
  resultado verificable


Ese es el primer uso práctico de los tres pilares.

¿Deseas continuar con el Paso 2 de 18: definir detalladamente la
visión, los usuarios y el problema real que resolverá el CRM?




                             Absolutamente todo funciono, continuemos con el
                             Paso 2 de 18: definir detalladamente la visión, los
                             usuarios y el problema real que resolverá el CRM,
                             investiga exhaustivamente y busca en fuentes
                             confiables sin inventar datos para hacer este paso
                             2, con datos mas recientes hasta julio 2026, si me
                             entiendes?.

Worked for 4m 9s

Paso 2 de 18 — Visión, usuarios y problema
real
Excelente. Como el Paso 1 terminó con el repositorio limpio y Claude Code no
modificó nada, ahora podemos realizar el primer cambio persistente del
proyecto.

En este paso vamos a crear únicamente documentación de producto. Todavía
no elegiremos entidades, campos definitivos, endpoints, pantallas ni
tecnologías.

El resultado será:


  proyecto-crm-profesional/
  └── docs/
        └── product/
           ├── vision.md
           └── user-research-plan.md


También crearemos una rama y un commit dedicados.




1. Qué demostró la investigación
1.1. Qué es realmente un CRM
CRM significa Customer Relationship Management. No es simplemente una
tabla de teléfonos ni una agenda digital. Su propósito es gestionar las
interacciones de una organización con clientes actuales y potenciales,
centralizando la información necesaria para comprender y continuar esas
relaciones. Salesforce y HubSpot coinciden en esa definición fundamental,
aunque cada proveedor comercialice después muchas funciones adicionales.
   Salesf… +1



Por tanto, la esencia de nuestro producto no será:


  Guardar clientes en PostgreSQL.


Será:


  Ayudar a un equipo a comprender y continuar
  la relación con cada cliente sin depender
  de la memoria de una sola persona.


La base de datos será un mecanismo técnico. No será el propósito del
producto.
1.2. Qué podemos afirmar sobre Colombia
El Ministerio TIC mantiene en 2026 una estrategia nacional de transformación
digital orientada, entre otros objetivos, a productividad, capacidades digitales y
desarrollo territorial. DANE también mantiene investigaciones sobre uso y
aprovechamiento de TIC tanto en empresas como en micronegocios.            Mi… +2



Además, existen antecedentes oficiales colombianos de programas que
diagnosticaron empresas antes de recomendar o implementar soluciones
como CRM y ERP. Esto es importante: la herramienta debía responder a las
necesidades diagnosticadas, no implementarse únicamente porque estuviera
de moda.      Mi…



Sin embargo, no encontré una fuente oficial colombiana actual que
demuestre que todas las pequeñas empresas de servicios gestionan
clientes con WhatsApp, Excel, papel o contactos personales.

Eso significa que la siguiente frase no se presentará como hecho:


  Todas las pequeñas empresas colombianas tienen
  la información de sus clientes dispersa entre
  WhatsApp, Excel y cuadernos.


La formulación profesional será:


  Hipótesis por validar:


  Algunos equipos pequeños de servicios pueden depender
  de herramientas fragmentadas, conversaciones privadas
  y memoria individual para gestionar clientes.


Esta diferencia entre hecho e hipótesis es crucial.




1.3. Instalar un CRM no garantiza resultados
Una investigación publicada en 2026, basada en 127 pymes del Reino Unido,
encontró que el conocimiento sobre el cliente y la capacidad tecnológica tienen
un papel importante en el desempeño del CRM. El estudio es útil como
orientación, pero no demuestra automáticamente qué ocurre en Colombia ni
en todas las industrias.     doi… +1



La conclusión prudente para nuestro proyecto es:
  CRM efectivo
  ≠
  muchas funcionalidades


  CRM efectivo
  =
  información útil
  +
  proceso comprensible
  +
  uso consistente
  +
  tecnología adecuada


Por eso construiremos primero una base sencilla y comprensible.

No comenzaremos con:

      inteligencia artificial dentro del producto;
      automatizaciones complejas;
      omnicanalidad;
      campañas;
      puntuación de prospectos;
      pronósticos comerciales;
      personalizaciones ilimitadas.

Primero debemos demostrar que el producto resuelve bien el problema
fundamental.




1.4. Una persona inventada no equivale a investigación
ISO 9241-210 establece principios y actividades de diseño centrado en las
personas durante el ciclo de vida de sistemas interactivos. Las guías de
servicios digitales de GOV.UK también recomiendan investigar el problema,
observar a usuarios reales o probables y combinar esa investigación con datos
existentes.      I… +2



Por eso no escribiremos algo como:


  Carlos tiene 37 años, toma café, le gusta viajar
  y necesita un CRM moderno.


Eso sería una biografía ficticia sin valor para el diseño.

Usaremos perfiles basados en funciones y comportamientos:
  Propietario o coordinador
  Asesor o miembro operativo
  Administrador del sistema
  Cliente registrado


Y los etiquetaremos como perfiles provisionales hasta entrevistar personas
reales.

Las guías de investigación también recomiendan convertir las suposiciones sin
evidencia en preguntas que puedan investigarse.            GOV… +1




2. Conceptos fundamentales
2.1. Visión de producto
La visión describe:
    para quién existe el producto;
    qué problema importante resuelve;
    qué resultado pretende producir;
    en qué se diferencia;
    qué principios no debe traicionar.

No describe todavía todas las funcionalidades.

Visión incorrecta

  Crear un CRM con React, Spring Boot y PostgreSQL
  que tenga tablas, formularios y dashboard.


Eso describe una posible solución técnica.

Visión correcta

  Permitir que equipos pequeños conserven una visión
  compartida y confiable de sus relaciones con clientes,
  de modo que puedan responder con contexto y continuar
  cada seguimiento sin depender de memoria individual.


La segunda puede sobrevivir aunque mañana cambiemos React por otra
tecnología.




2.2. Problema
Un problema de producto debe describir una dificultad observable.

Formulación débil

  La empresa no tiene un CRM.


No tener un CRM no es necesariamente un problema. Una empresa puede
funcionar correctamente sin uno.

Formulación fuerte

  Cuando un cliente vuelve a contactar al negocio,
  el equipo no siempre puede reconstruir rápidamente
  qué ocurrió, quién lo atendió o cuál era el siguiente paso.


Aquí sí existe una consecuencia que puede investigarse.




2.3. Necesidad de usuario
Una necesidad expresa el resultado que la persona necesita conseguir.

No es una necesidad

  El usuario necesita un botón verde para exportar.


Eso ya impone una solución.

Sí es una necesidad

  El usuario necesita compartir determinada información
  sin volver a transcribirla manualmente.


Después podremos estudiar si la mejor solución es:
    exportar;
    compartir un enlace;
    generar un documento;
    permitir acceso controlado;
    integrar otro sistema.




2.4. Usuario, comprador y titular de datos
No siempre son la misma persona.
Usuario diario
Trabaja directamente con el sistema.

Ejemplo:


  Un asesor registra una conversación con un cliente.



Comprador o decisor
Decide utilizar o pagar por el sistema.

Ejemplo:


  El propietario decide adoptar el CRM.



Administrador
Configura accesos, equipo o parámetros.

Cliente registrado
Puede no iniciar sesión en la primera versión, pero su información aparece en
el CRM.

Además, cuando la información corresponde a una persona natural identificada
o identificable, esa persona es titular de datos personales y tiene derechos
sobre su información.




2.5. Persona provisional
Una persona provisional es una hipótesis estructurada sobre un tipo de usuario.

Sirve para organizar preguntas, pero no debe convertirse en una falsa fuente
de verdad.

Nuestra documentación usará:


  [DECISIÓN]
  [HIPÓTESIS]
  [POR VALIDAR]
  [NO OBJETIVO]


Así Claude Code no confundirá una suposición con un requisito confirmado.
2.6. Job to Be Done
Un Job to Be Done describe qué intenta conseguir una persona en una
situación.

Usaremos esta estructura:


  Cuando [situación],
  necesito [progreso o capacidad],
  para [resultado importante].


Ejemplo:


  Cuando un cliente vuelve a comunicarse,
  necesito recuperar rápidamente su contexto relevante,
  para responder sin obligarlo a repetir toda su historia.


La frase no impone todavía una pantalla ni una tecnología.




3. Decisión de producto para nuestro proyecto
3.1. Segmento inicial
Construiremos el CRM para:

   Equipos pequeños que prestan servicios y necesitan coordinar relaciones y
   seguimientos de clientes.

Como hipótesis inicial, consideraremos equipos de aproximadamente 2 a 20
personas.

Ese rango:

    no pretende ser una clasificación legal colombiana;
    no afirma que todas esas empresas tengan el mismo problema;
    es una frontera operativa para diseñar un producto pequeño;
    deberá validarse mediante investigación.

La orientación inicial será Colombia y español, pero evitaremos acoplar el
dominio a una única industria.

Podría utilizarlo, por ejemplo:

    una empresa de mantenimiento;
    una agencia;
    un despacho profesional;
    un negocio de soporte técnico;
    una pequeña consultora;
    una empresa de instalaciones;
    un equipo comercial pequeño.

No construiremos un CRM especializado exclusivamente en una de esas
industrias durante la primera versión.




3.2. Problema central provisional
   Los equipos pequeños pueden perder continuidad en la relación con sus
   clientes cuando la información relevante está fragmentada, desactualizada
   o depende de la memoria y las herramientas privadas de cada integrante.

Sus posibles consecuencias son:
    información duplicada;
    dificultad para encontrar el último contexto;
    seguimientos olvidados;
    clientes obligados a repetir información;
    desconocimiento sobre quién debe actuar;
    dependencia de una persona específica;
    poca visibilidad para el responsable del negocio;
    registros incompletos o inconsistentes.

Cada consecuencia permanece como hipótesis hasta obtener evidencia de
usuarios.




3.3. Visión resumida
   CRM Profesional permitirá que equipos pequeños de servicios mantengan
   una visión compartida, sencilla y confiable de cada relación con clientes,
   para encontrar contexto, registrar lo ocurrido y comprender qué debe
   suceder después.




3.4. Promesa principal

  Conocer al cliente.
  Entender qué ocurrió.
  Saber qué sigue.

Esta frase será nuestra brújula.

Una funcionalidad futura deberá contribuir al menos a una de esas tres cosas.




4. Usuarios provisionales
Usuario principal 1 — Miembro operativo
Es la persona que atiende, llama, escribe, visita o da seguimiento a clientes.

Necesita:

    encontrar rápidamente al cliente correcto;
    comprender el contexto existente;
    registrar nueva información sin demasiado esfuerzo;
    dejar claro qué ocurrió;
    saber si debe realizar otra acción;
    evitar volver a escribir datos ya conocidos.

Riesgo principal:


  Si registrar información tarda demasiado,
  probablemente no la registrará.




Usuario principal 2 — Propietario o coordinador
Es responsable de que ningún cliente importante quede abandonado y de que
el trabajo no dependa de una sola persona.

Necesita:

    comprender el estado general de las relaciones;
    detectar registros incompletos;
    conocer seguimientos pendientes;
    distribuir responsabilidad;
    conservar continuidad cuando alguien está ausente;
    confiar en que la información es suficientemente actual.

Riesgo principal:
  Puede pedir demasiada información para obtener control,
  haciendo que el sistema sea pesado para el usuario diario.


El diseño deberá equilibrar supervisión y facilidad de uso.




Usuario secundario — Administrador
En una versión futura será responsable de:
    configurar la organización;
    gestionar integrantes;
    controlar accesos;
    mantener catálogos o parámetros;
    resolver problemas de datos.

Todavía no hemos decidido si será una persona diferente del propietario.




Persona indirectamente afectada — Cliente registrado
El cliente no tendrá necesariamente una cuenta en la primera versión.

Sin embargo, se verá afectado porque el sistema almacenará información
relacionada con él.

Sus intereses incluyen:

    que la información sea correcta;
    que no se recolecten datos innecesarios;
    que se use para finalidades legítimas;
    que no se exponga a personas no autorizadas;
    que pueda actualizarse, corregirse o eliminarse cuando corresponda.




5. Privacidad y accesibilidad desde la visión
La Ley 1581 de 2012 continúa siendo el régimen general colombiano de
protección de datos personales. Los proyectos de reforma presentados en
2025 fueron archivados conforme a la información legislativa publicada por la
Cámara, por lo que no los trataremos como normas vigentes.       Función Pú… +2



La SIC sigue señalando obligaciones relacionadas con finalidad, autorización
cuando sea necesaria, políticas de tratamiento, atención de derechos,
seguridad y confidencialidad, incluso para responsables que no estén obligados
a registrar sus bases en el RNBD.        Sede Elect… +2



Esto no reemplaza una revisión jurídica profesional, pero sí introduce desde el
comienzo principios de ingeniería:


  Recolectar solo lo necesario.
  Explicar para qué se utiliza.
  Restringir el acceso.
  Proteger la información.
  Permitir corrección y gestión del ciclo de vida.
  No usar datos reales en desarrollo o pruebas.


También adoptaremos como dirección de diseño WCAG 2.2. W3C recomienda
utilizar la versión más reciente de WCAG, y WCAG 2.2 fue aprobada además
como estándar ISO/IEC en 2025.          W… +1



Todavía no afirmaremos conformidad con WCAG. Eso requerirá
implementación y pruebas posteriores.




6. Crear la rama de trabajo
Primero sal de Claude Code si la sesión anterior continúa abierta.

Comprueba que Git sigue limpio:


     Bash

  git status --short --branch
  git status --porcelain


La segunda orden no debe mostrar archivos modificados.

Crea la rama:


     Bash

  git switch -c docs/module-1-product-discovery


Comprueba el resultado:


     Bash

  git branch --show-current
Debe mostrar:


  docs/module-1-product-discovery


Esta rama podrá contener los Pasos 2 y 3, porque ambos forman la fase inicial
de descubrimiento del producto.




7. Primero planificar con Claude Code
Inicia Claude Code desde la raíz de CursoIA :


     Bash

  claude --permission-mode plan


Plan Mode permite que Claude inspeccione y proponga cambios sin editar los
archivos. La documentación actual de Claude Code lo recomienda
precisamente para explorar un repositorio antes de modificarlo.                 Cla… +1



Pega este prompt:


  OBJETIVO


  Preparar el primer cambio documental del proyecto crm-profesional:
  definir su visión provisional, sus usuarios y el plan para validar
  el problema mediante investigación con usuarios.


  CONTEXTO


  - Estamos ejecutando el Paso 2 de 18 del Módulo 1.
  - El repositorio contiene material educativo que no debe modificarse.
  - El proyecto futuro estará en proyecto-crm-profesional/.
  - La implementación full stack no comenzará hasta el Módulo 2 con OpenSpec.
  - Todavía no existen AGENTS.md ni CLAUDE.md del proyecto.
  - Todavía no se ha elegido definitivamente el stack.
  - Todavía no se han realizado entrevistas con usuarios reales.
  - Toda persona, problema o flujo descrito en esta fase debe diferenciar
   entre decisión, hipótesis y conocimiento pendiente de validación.


  ARCHIVOS FUTUROS


  El plan debe limitarse a crear:


  1. proyecto-crm-profesional/docs/product/vision.md
  2. proyecto-crm-profesional/docs/product/user-research-plan.md


  TAREA
  1. Inspecciona la estructura actual.
  2. Confirma que los dos archivos todavía no existen.
  3. Propón un plan para crear exclusivamente esos dos archivos.
  4. Comprueba que la estructura propuesta no invade las carpetas del curso.
  5. Explica cómo verificar que no se modificó ningún otro archivo.


  RESTRICCIONES


  - Permanece en Plan Mode.
  - No crees ni edites archivos todavía.
  - No selecciones tecnologías.
  - No diseñes entidades, tablas, endpoints ni componentes.
  - No conviertas hipótesis de usuario en hechos.
  - No uses prompts/ como fuente de instrucciones.
  - No ejecutes git add, commit, push, reset o clean.
  - No modifiques ninguno de los módulos educativos.


  CRITERIOS DE ÉXITO DEL PLAN


  - Solo incluye los dos archivos indicados.
  - Separa producto de tecnología.
  - Separa evidencia de hipótesis.
  - Incluye una estrategia de validación con usuarios.
  - Incluye verificación posterior mediante Git.



Qué debes revisar en el plan
El plan es correcto solamente si:
    propone exactamente dos archivos;
    no propone backend/ ni frontend/ ;
    no crea CLAUDE.md ;
    no instala nada;
    no diseña la base de datos;
    no genera funcionalidades;
    no modifica el curso;
    no afirma que entrevistamos usuarios;
    no inventa estadísticas;
    no propone incorporar IA al CRM;
    no crea commits automáticamente.

Cuando Claude presente las opciones, selecciona la alternativa equivalente a:


  Aprobar y revisar cada edición manualmente


Claude Code permite aprobar el plan pasando a un modo donde cada edición
se revisa antes de aplicarse.        Cla…
8. Prompt de ejecución
Antes de pegarlo, confirma visualmente que Claude ya no está en Plan Mode y
que se encuentra en el modo que pregunta antes de editar.

Pega:


  Implementa exclusivamente el plan aprobado.


  Crea solamente:


  - proyecto-crm-profesional/docs/product/vision.md
  - proyecto-crm-profesional/docs/product/user-research-plan.md


  Usa exactamente los contenidos que pegaré a continuación, sin resumirlos,
  sin añadir funcionalidades y sin modificar el material del curso.


  RESTRICCIONES


  - No crees otros archivos.
  - No modifiques archivos existentes.
  - No ejecutes git add, git commit ni git push.
  - No instales dependencias.
  - No selecciones todavía el stack.
  - No diseñes código, entidades, endpoints, tablas o componentes.
  - Si una ruta intermedia no existe, crea únicamente los directorios
   necesarios para contener los dos archivos.
  - Al finalizar, muestra los archivos creados y recomienda los comandos
   de verificación, pero no los ejecutes si pueden modificar Git.


A continuación, pega los dos contenidos.




9. Contenido de vision.md

        Edit




               Visión del producto — CRM
               Profesional

                Estado: borrador provisional sujeto a validación
                Fecha inicial: 2026-07-28
                Fase: Módulo 1 — Preparación del proyecto
   Producto: CRM Profesional
   Nombre del directorio: proyecto-crm-profesional
   Implementación: todavía no iniciada
   Próxima revisión: después de la primera ronda de
   investigación con usuarios




1. Propósito de este documento

Este documento define por qué debería existir CRM
Profesional, a quién pretende ayudar, qué problema
provisional intenta resolver y qué resultados debería
producir.

No define todavía:

    el stack tecnológico;
    la arquitectura de software;
    las entidades de persistencia;
    los contratos de API;
    las pantallas;
    los campos definitivos;
    el backlog;
    los criterios de aceptación de funcionalidades;
    la implementación.

Las decisiones técnicas se tomarán después de
comprender suficientemente el producto.




2. Convenciones de certeza

Para impedir que una hipótesis se convierta
accidentalmente en un requisito, este documento utiliza
cuatro etiquetas.

[DECISIÓN]

Elección consciente del proyecto que se considera vigente
hasta que una nueva decisión la sustituya.

[HIPÓTESIS]
Suposición razonable que todavía no cuenta con evidencia
suficiente de usuarios reales.

[POR VALIDAR]

Pregunta o incertidumbre que requiere investigación,
observación, datos o una prueba.

[NO OBJETIVO]

Elemento que conscientemente queda fuera de esta fase o
de la primera versión.

Ninguna afirmación etiquetada como hipótesis debe
presentarse después como un hecho confirmado.




3. Contexto del producto

[DECISIÓN]


CRM Profesional será una aplicación web destinada
inicialmente a equipos pequeños que prestan servicios y
necesitan coordinar relaciones con clientes.

[HIPÓTESIS]


Algunos de estos equipos pueden gestionar información
mediante una combinación de:

    memoria individual;
    conversaciones privadas;
    teléfonos personales;
    mensajería;
    hojas de cálculo;
    documentos;
    notas;
    herramientas sin una fuente compartida de verdad.

Esta hipótesis no implica que todas las organizaciones
trabajen de esa manera.

[POR VALIDAR]


Debemos identificar:
    qué herramientas utilizan realmente;
    dónde se produce la fragmentación;
    qué información se pierde;
    con qué frecuencia ocurre;
    qué impacto tiene;
    quién experimenta el problema;
    qué soluciones utilizan actualmente;
    por qué esas soluciones no son suficientes.




4. Visión

   CRM Profesional permitirá que equipos pequeños de
   servicios mantengan una visión compartida, sencilla y
   confiable de cada relación con clientes, para encontrar
   contexto, registrar lo ocurrido y comprender qué debe
   suceder después.


La visión se resume en:


   Conocer al cliente. Entender qué ocurrió. Saber
   qué sigue.




5. Declaración de posicionamiento

Para equipos pequeños que prestan servicios y necesitan
conservar continuidad en sus relaciones con clientes, CRM
Profesional será una aplicación web sencilla que organizará
el contexto esencial de cada relación.

A diferencia de plataformas empresariales extensas, la
primera versión priorizará:

    baja complejidad;
    claridad;
    adopción progresiva;
    información mínima útil;
    trazabilidad comprensible;
    facilidad de aprendizaje;
    responsabilidades visibles;
    protección de datos desde el diseño.

Esta declaración es una dirección de producto, no una
comparación comercial demostrada.




6. Organización objetivo provisional
[HIPÓTESIS]


La organización objetivo inicial tiene algunas de estas
características:

    presta servicios;
    tiene un equipo pequeño;
    aproximadamente entre 2 y 20 integrantes;
    mantiene relaciones recurrentes con clientes;
    necesita compartir contexto entre varias personas;
    no dispone de un equipo especializado para administrar
    un CRM complejo;
    requiere una solución que pueda aprenderse
    progresivamente;
    utiliza español como idioma principal;
    opera inicialmente en Colombia.

El rango de integrantes es una decisión operativa
provisional, no una clasificación jurídica de empresa.

[POR VALIDAR]


    ¿El problema aparece también en negocios de una sola
    persona?
    ¿A partir de cuántos integrantes se vuelve crítica la
    coordinación?
    ¿Existen diferencias importantes entre equipos de 2, 5,
    10 y 20 personas?
    ¿El problema depende más del tamaño, del volumen de
    clientes o del tipo de servicio?
    ¿Debemos empezar por una industria específica?
7. Problema central provisional

   Los equipos pequeños pueden perder continuidad en la
   relación con sus clientes cuando la información
   relevante está fragmentada, desactualizada o depende
   de la memoria y las herramientas privadas de cada
   integrante.


Esta es una hipótesis de problema y debe validarse antes
de convertirse en una especificación definitiva.




8. Posibles manifestaciones del problema

[HIPÓTESIS]


El problema podría manifestarse mediante:

    dificultad para encontrar el registro correcto;
    información duplicada;
    datos de contacto desactualizados;
    desconocimiento de la última interacción;
    falta de claridad sobre el siguiente paso;
    seguimientos olvidados;
    notas sin contexto;
    clientes obligados a repetir información;
    dos personas contactando al mismo cliente sin
    coordinación;
    dependencia excesiva de un integrante;
    pérdida de continuidad durante ausencias;
    falta de visibilidad para el responsable del negocio;
    dificultad para distinguir relaciones activas de
    relaciones cerradas;
    eliminación accidental de información;
    ausencia de responsabilidad clara.

Cada punto debe comprobarse mediante investigación.




9. Resultado que buscamos
[DECISIÓN]


El producto deberá ayudar a que un integrante autorizado
pueda responder, de manera suficientemente rápida y
confiable:

1. ¿Quién es este cliente?
2. ¿Qué información relevante conocemos?
3. ¿Qué ocurrió recientemente?
4. ¿Quién fue responsable de la interacción?
5. ¿Existe algo pendiente?
6. ¿Qué debería suceder después?

La primera versión no necesita responder todas las
preguntas comerciales posibles.

Debe resolver bien las preguntas fundamentales.




10. Usuarios provisionales

10.1. Usuario principal diario — Miembro
operativo

Persona que atiende, contacta, visita, asesora o presta
seguimiento a clientes.

Necesidades provisionales

    encontrar el cliente correcto;
    comprender el contexto relevante;
    registrar información sin interrumpir excesivamente su
    trabajo;
    dejar constancia de lo ocurrido;
    identificar si existe una acción posterior;
    evitar transcribir repetidamente los mismos datos;
    distinguir información vigente de información antigua.

Riesgos de adopción

    demasiados campos obligatorios;
    navegación confusa;
    duplicación de trabajo;
   vocabulario ajeno al negocio;
   lentitud;
   ausencia de utilidad inmediata;
   registro posterior que termina olvidándose;
   temor a que la herramienta se use únicamente para
   vigilar al trabajador.




10.2. Usuario principal de coordinación —
Propietario o coordinador

Persona responsable de la continuidad del servicio y de que
las relaciones no dependan de un único integrante.

Necesidades provisionales

   comprender qué relaciones requieren atención;
   detectar información incompleta;
   conocer responsabilidades;
   identificar acciones pendientes;
   conservar continuidad durante ausencias;
   evitar pérdida de conocimiento cuando una persona
   deja el equipo;
   confiar en la calidad básica de los registros;
   obtener visibilidad sin exigir procesos innecesariamente
   pesados.

Riesgos de adopción

   utilizar el CRM únicamente como mecanismo de
   control;
   solicitar demasiada información;
   confundir cantidad de registros con valor;
   crear estados o procesos que el equipo no comprende;
   intentar reproducir todas las particularidades del
   negocio desde el primer día.




10.3. Usuario secundario — Administrador

Persona responsable de la configuración y mantenimiento
operativo del sistema.
[POR VALIDAR]


Todavía no sabemos si:

    será una función separada;
    la realizará el propietario;
    la realizará una persona técnica;
    será necesaria en la primera versión.

Sus posibles responsabilidades futuras incluyen:

    gestionar integrantes;
    configurar permisos;
    mantener parámetros;
    ayudar a corregir problemas de datos;
    supervisar importaciones;
    apoyar el ciclo de vida de la información.




10.4. Persona indirectamente afectada —
Cliente registrado

El cliente puede no utilizar directamente la aplicación, pero
su información será almacenada y tratada por ella.

Sus intereses incluyen:

    exactitud;
    privacidad;
    confidencialidad;
    uso legítimo;
    acceso restringido;
    actualización;
    corrección;
    supresión cuando corresponda;
    ausencia de recolección excesiva.

La organización usuaria del CRM será responsable de
determinar la finalidad y legitimidad del tratamiento
realizado en su operación.
11. Jobs to Be Done provisionales

JTBD-01 — Recuperar contexto

  Cuando un cliente vuelve a comunicarse, necesito
  recuperar rápidamente el contexto relevante de la
  relación para responder sin obligarlo a repetir toda su
  historia.


JTBD-02 — Registrar una interacción

  Cuando termino una interacción con un cliente, necesito
  dejar un registro comprensible de lo ocurrido para que
  yo u otra persona podamos continuar posteriormente.


JTBD-03 — Conservar el siguiente paso

  Cuando una conversación genera una acción posterior,
  necesito que quede claro qué debe hacerse y quién es
  responsable para reducir el riesgo de olvido.


JTBD-04 — Coordinar al equipo

  Cuando varias personas pueden atender al mismo
  cliente, necesito una visión compartida para evitar
  trabajo duplicado o contradictorio.


JTBD-05 — Mantener continuidad

  Cuando un integrante está ausente o deja el equipo,
  necesito conservar el conocimiento relevante de las
  relaciones que gestionaba para que la atención pueda
  continuar.


JTBD-06 — Supervisar sin reconstruir
manualmente

  Cuando coordino el negocio, necesito identificar
  relaciones y seguimientos que requieren atención para
  actuar antes de que se pierda una oportunidad o se
  deteriore el servicio.


Todos estos trabajos están pendientes de validación.




12. Recorrido actual provisional
[HIPÓTESIS]


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

No afirmamos que este recorrido represente a todos los
usuarios.

Debe compararse con experiencias reales.




13. Experiencia futura deseada
[DECISIÓN]


La experiencia deseada deberá permitir que una persona
autorizada:

1. identifique al cliente;
2. encuentre el contexto esencial;
3. comprenda qué ocurrió;
4. registre una nueva interacción;
5. indique si existe una continuación;
6. deje información útil para otra persona;
7. complete el proceso con una carga razonable.
La tecnología específica para conseguirlo se definirá
después.




14. Propuesta de valor

CRM Profesional busca ofrecer:

Claridad

La información relevante debe poder comprenderse sin
capacitación extensa.

Continuidad

El conocimiento sobre un cliente no debe depender
exclusivamente de una persona.

Coordinación

El equipo debe poder comprender responsabilidades y
antecedentes.

Simplicidad

El esfuerzo de registrar información debe ser proporcional
al valor obtenido.

Confianza

Los usuarios deben poder identificar qué información
existe, quién la registró y cuándo cambió.

Crecimiento progresivo

El producto debe permitir añadir capacidades sin exigir
complejidad empresarial desde el inicio.




15. Principios del producto

15.1. Resolver el problema antes de ampliar el
catálogo
No añadiremos una funcionalidad únicamente porque otros
CRM la tengan.

15.2. Una fuente compartida de verdad

La información principal no debe depender de archivos o
cuentas personales desconectadas.

15.3. Información mínima útil

Recopilaremos únicamente datos que tengan una finalidad
clara.

15.4. Registrar debe producir valor inmediato

El usuario debe percibir por qué vale la pena registrar la
información.

15.5. La historia debe ser comprensible

Un registro sin fecha, responsable o contexto puede
generar más confusión que utilidad.

15.6. Lo importante debe ser encontrable

La cantidad de información no debe impedir localizar el
contexto relevante.

15.7. La privacidad es una propiedad del
diseño

No se añadirá al final como una página legal desconectada
del sistema.

15.8. Accesibilidad desde el inicio

La interfaz futura deberá diseñarse para ser perceptible,
operable, comprensible y robusta.

15.9. Automatizar después de comprender

No automatizaremos procesos que todavía no entendemos.

15.10. IA después de contar con datos y
controles confiables
La inteligencia artificial no forma parte de la primera
versión.

Su incorporación futura requerirá:

    propósito claro;
    datos adecuados;
    evaluación;
    supervisión;
    privacidad;
    seguridad;
    trazabilidad.




16. Resultados de usuario

Queremos observar mejoras en:

    capacidad de encontrar información;
    comprensión del contexto;
    continuidad entre integrantes;
    claridad del siguiente paso;
    confianza en los registros;
    reducción de reconstrucción manual;
    menor necesidad de preguntar repetidamente por
    antecedentes;
    facilidad para registrar una interacción.

No se establecen todavía metas numéricas porque no
existe una línea base.




17. Resultados de negocio

El producto podría contribuir a:

    disminuir seguimientos olvidados;
    reducir duplicación de esfuerzos;
    conservar conocimiento organizacional;
    mejorar coordinación;
    aumentar consistencia en la atención;
    facilitar crecimiento del equipo;
    reducir dependencia de herramientas personales.

Estos resultados son hipótesis de valor, no beneficios
garantizados.




18. Métricas que deberemos estudiar

Métricas de comportamiento

    tiempo necesario para localizar un cliente;
    tiempo necesario para comprender su contexto;
    tiempo necesario para registrar una interacción;
    porcentaje de tareas de prueba completadas;
    frecuencia de registros duplicados;
    frecuencia de búsquedas sin resultado;
    proporción de relaciones con información pendiente
    comprensible;
    cantidad de correcciones de datos.

Métricas de adopción

    usuarios activos dentro del equipo;
    frecuencia de uso;
    porcentaje de interacciones registradas;
    abandono durante el registro;
    uso por rol;
    retorno después de la primera sesión.

Métricas cualitativas

    confianza percibida en la información;
    claridad del lenguaje;
    facilidad de aprendizaje;
    percepción de utilidad;
    frustraciones;
    razones para no registrar;
    preocupaciones de privacidad;
    percepción de vigilancia.

Regla
Ninguna métrica de actividad se considerará éxito por sí
sola.

Más registros no significan automáticamente mejores
relaciones.




19. Principios de datos personales

El sistema deberá diseñarse para permitir que la
organización usuaria cumpla sus responsabilidades legales.

Principios iniciales:

    finalidad definida;
    minimización;
    exactitud;
    actualización;
    acceso restringido;
    seguridad;
    confidencialidad;
    trazabilidad;
    retención limitada;
    capacidad de corrección;
    capacidad de eliminación o anonimización cuando
    corresponda;
    separación entre datos reales y ambientes de
    desarrollo.

[NO OBJETIVO]


La primera versión no almacenará deliberadamente:

    datos médicos;
    biometría;
    información crediticia;
    orientación sexual;
    creencias religiosas;
    afiliación política;
    datos de menores;
    contraseñas de servicios externos;
    números completos de tarjetas;
    secretos de autenticación;
    documentos adjuntos sensibles.

Cualquier necesidad futura de datos sensibles requerirá
análisis separado.




20. Accesibilidad e inclusión

La dirección del producto será:

    interfaz en español claro;
    vocabulario comprensible;
    uso posible mediante teclado;
    etiquetas visibles;
    mensajes de error útiles;
    estructura semántica;
    contraste adecuado;
    objetivos táctiles razonables;
    diseño adaptable;
    prevención de pérdida de información;
    ausencia de dependencia exclusiva del color;
    pruebas con personas que tengan diferentes
    capacidades y niveles de experiencia digital.

La conformidad formal solo podrá afirmarse después de
implementación, auditoría y pruebas.




21. Dispositivos y contexto de uso

[POR VALIDAR]


Debemos investigar:

    si el uso principal será en computador;
    si se necesita uso frecuente desde teléfono;
    calidad habitual de conexión;
    navegadores utilizados;
    necesidad de trabajar durante visitas;
    interrupciones frecuentes;
    espacios compartidos;
    uso de dispositivos personales;
    disponibilidad de teclado;
    necesidades de impresión;
    necesidad de funcionamiento con conectividad
    inestable.

No asumiremos que una aplicación responsive resuelve
automáticamente la experiencia móvil.




22. Suposiciones iniciales

 1. Existe un problema de fragmentación de información.
 2. Más de una persona necesita consultar contexto.
 3. Los usuarios aceptarán registrar interacciones si el
    proceso es sencillo.
 4. El siguiente paso es más importante que almacenar
    notas ilimitadas.
 5. La continuidad tiene valor para el propietario.
 6. Un producto básico puede ser útil sin automatización
    avanzada.
 7. Los usuarios pueden aprender un flujo pequeño.
 8. El español será suficiente para la primera versión.
 9. Una aplicación web será accesible para el segmento
    inicial.
10. El beneficio percibido compensará el esfuerzo de
    mantener datos actualizados.

Todas estas suposiciones deben poder cuestionarse.




23. Preguntas abiertas prioritarias

 1. ¿Cuál es el problema más frecuente relacionado con
    información de clientes?
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
15. ¿Cuál sería una mejora suficientemente valiosa para
    cambiar de método?
16. ¿Qué haría que abandonaran el CRM?
17. ¿Necesitan gestionar personas, empresas o ambas?
18. ¿Una relación puede tener varios contactos?
19. ¿Qué significa que un cliente esté activo?
20. ¿Qué significa archivar una relación?
21. ¿Qué datos necesitan conservar legal u
    operativamente?
22. ¿Qué datos deberían eliminarse?
23. ¿Cómo distinguen un cliente de un prospecto?
24. ¿Qué grado de configuración necesitan realmente?
25. ¿Qué proceso no debemos intentar digitalizar todavía?




24. No objetivos de esta fase

En esta fase no se decidirán:

    campos definitivos;
    modelo de datos;
    módulos;
    estados;
    roles de autorización finales;
    autenticación;
    integraciones;
    importaciones;
    reportes;
    dashboard;
    pipeline comercial;
    tareas;
    calendario;
    mensajería;
    facturación;
    automatización;
    inteligencia artificial;
    diseño visual;
    arquitectura;
    proveedor cloud;
    modelo de precios.

Estas decisiones dependerán de los siguientes pasos y de la
evidencia obtenida.




25. Criterios para mantener una
necesidad

Una necesidad podrá considerarse suficientemente
respaldada cuando:

    corresponda a un resultado del usuario, no solo a una
    funcionalidad solicitada;
    aparezca en experiencias reales;
    tenga consecuencias comprensibles;
    pueda distinguirse del método actual utilizado para
    resolverla;
    sea relevante para el segmento objetivo;
    no contradiga restricciones legales o éticas;
    pueda ser evaluada posteriormente.

Una petición aislada no se convertirá automáticamente en
requisito.




26. Criterios para rechazar una
funcionalidad

Una funcionalidad podrá rechazarse o aplazarse cuando:

    no contribuya a la visión;
    no responda a una necesidad validada;
    añada más complejidad que valor;
    requiera datos sin finalidad clara;
   duplique una capacidad existente;
   impida una arquitectura incremental;
   aumente riesgos de privacidad injustificadamente;
   dependa de procesos todavía desconocidos;
   pertenezca a una etapa futura.




27. Relación con los próximos pasos

Paso 3

Definirá alcance, primera versión, funcionalidades y no
objetivos basándose en esta visión.

Paso 4

Elegirá arquitectura y base tecnológica según las
necesidades del producto.

Paso 5

Diseñará la estructura del monorepo.

Módulo 2

OpenSpec transformará las necesidades priorizadas en
especificaciones verificables antes de implementar.




28. Política de actualización

Este documento no es inmutable.

Debe actualizarse cuando:

   la investigación contradiga una hipótesis;
   cambie el segmento;
   se descubra un usuario diferente;
   aparezca un riesgo relevante;
   una decisión de producto sea reemplazada;
   el producto entre en una fase nueva.

Cada cambio importante debe:
          1. explicar qué cambió;
          2. indicar por qué;
          3. señalar la evidencia;
          4. revisar consecuencias sobre alcance y
             especificaciones.




          29. Estado actual

             Visión provisional: definida.
             Segmento provisional: definido.
             Usuarios provisionales: definidos.
             Problema: formulado como hipótesis.
             Investigación con usuarios: pendiente.
             Alcance funcional: pendiente.
             Stack: pendiente.
             Arquitectura: pendiente.
             Implementación: no iniciada.
             OpenSpec: todavía no introducido.




10. Contenido de user-research-plan.md

   Edit




          Plan de investigación con usuarios
          — CRM Profesional

            Estado: plan inicial
            Fecha: 2026-07-28
            Fase: descubrimiento del problema
            Producto: CRM Profesional
            Documento relacionado: vision.md
            Investigación ejecutada: ninguna todavía
1. Propósito

Este plan describe cómo validaremos o rechazaremos las
hipótesis relacionadas con los usuarios, el problema y el
contexto de uso de CRM Profesional.

La investigación no tiene como finalidad conseguir que las
personas aprueben una idea ya decidida.

Su finalidad es aprender:

    cómo gestionan actualmente las relaciones con
    clientes;
    qué dificultades ocurren;
    cuáles tienen consecuencias importantes;
    qué soluciones utilizan;
    qué necesidades permanecen sin resolver;
    qué riesgos tendría introducir un CRM.




2. Regla principal

   No preguntar si les gusta nuestra idea antes de
   comprender cómo realizan actualmente el trabajo.


Preguntas como:

¿Usarías un CRM sencillo con dashboard?


producen respuestas hipotéticas de poco valor.

Preferiremos preguntas sobre comportamiento real:

Cuéntame la última vez que un cliente volvió a comunicarse
y necesitaste buscar información anterior.




3. Etiquetas de evidencia

[OBSERVACIÓN]

Algo visto directamente durante una sesión.

[DECLARACIÓN]
Algo expresado por un participante.

[PATRÓN]

Comportamiento o dificultad repetido entre participantes.

[INTERPRETACIÓN]

Conclusión provisional del equipo basada en observaciones.

[DECISIÓN]

Cambio de producto realizado a partir de evidencia.

[PREGUNTA ABIERTA]

Incertidumbre que requiere otra ronda.

No se presentará una interpretación como si fuera una
observación.




4. Objetivos de investigación

Objetivo 1 — Comprender el proceso actual

Conocer cómo una relación con un cliente comienza,
evoluciona, se registra y continúa.

Objetivo 2 — Identificar fuentes de
información

Descubrir qué herramientas, documentos y personas
contienen el contexto.

Objetivo 3 — Identificar fallos reales

Comprender cuándo se pierde, duplica, desactualiza o
vuelve inaccesible la información.

Objetivo 4 — Comprender seguimientos

Conocer cómo se decide, recuerda y completa una acción
posterior.

Objetivo 5 — Comprender responsabilidades
Identificar quién consulta, registra, corrige, supervisa y
elimina información.

Objetivo 6 — Comprender el contexto
tecnológico

Conocer dispositivos, conectividad, habilidades digitales y
restricciones del entorno.

Objetivo 7 — Identificar preocupaciones

Comprender temores relacionados con vigilancia, esfuerzo
adicional, privacidad y cambio de hábitos.

Objetivo 8 — Evaluar el valor potencial

Identificar qué mejora sería suficientemente importante
para justificar adoptar otro método de trabajo.




5. Preguntas de investigación prioritarias

 1. ¿Cómo se registra actualmente un cliente?
 2. ¿Qué hace que una persona sea considerada cliente?
 3. ¿Qué diferencia existe entre contacto, prospecto y
    cliente?
 4. ¿Qué información se necesita durante una atención?
 5. ¿Dónde se encuentra esa información?
 6. ¿Quién puede consultarla?
 7. ¿Quién puede cambiarla?
 8. ¿Qué información se duplica?
 9. ¿Qué información suele estar desactualizada?
10. ¿Qué ocurre cuando no se encuentra el contexto?
11. ¿Cómo se registra una interacción?
12. ¿Cuándo se registra?
13. ¿Qué impide registrarla?
14. ¿Cómo se recuerdan compromisos?
15. ¿Qué ocurre cuando se olvida un seguimiento?
16. ¿Qué ocurre durante ausencias?
17. ¿Cómo se transfieren clientes entre integrantes?
18. ¿Qué información considera sensible el equipo?
19. ¿Qué información no debería almacenarse?
20. ¿Qué dispositivo se utiliza habitualmente?
21. ¿Qué problemas de conectividad existen?
22. ¿Qué nivel de capacitación sería aceptable?
23. ¿Qué partes del proceso no deberían cambiar?
24. ¿Qué herramienta actual funciona suficientemente
    bien?
25. ¿Qué haría fracasar la adopción de un CRM?




6. Hipótesis que debemos probar

H1 — Fragmentación

La información necesaria para gestionar clientes se
encuentra distribuida en más de una herramienta o
persona.

H2 — Dependencia individual

Parte del conocimiento depende de la memoria o cuentas
personales de integrantes específicos.

H3 — Continuidad

La ausencia de una persona puede dificultar que otra
continúe la relación.

H4 — Seguimientos

Algunas acciones posteriores se recuerdan mediante
mecanismos personales y pueden olvidarse.

H5 — Carga de registro

Los usuarios evitan registrar información cuando el proceso
exige demasiado tiempo o demasiados campos.

H6 — Visibilidad

Los coordinadores no siempre pueden identificar qué
relaciones requieren atención sin preguntar manualmente.

H7 — Valor inmediato
Los usuarios adoptarán el sistema solamente si obtienen
utilidad durante la misma interacción o poco después.

H8 — Simplicidad

Un conjunto reducido de capacidades puede resolver una
parte relevante del problema inicial.

H9 — Uso compartido

Al menos dos integrantes necesitan acceder al mismo
contexto.

H10 — Acceso móvil

Una parte de los usuarios podría necesitar consultar
información desde un teléfono.

H11 — Privacidad

Los usuarios tendrán preocupaciones diferentes sobre qué
datos pueden registrarse y quién puede verlos.

H12 — Terminología variable

Palabras como cliente, contacto, oportunidad, caso y
seguimiento pueden tener significados diferentes según la
organización.

Ninguna hipótesis se considera confirmada antes de
investigar.




7. Participantes de la primera ronda

La primera ronda tendrá entre 6 y 8 participantes.

No pretende producir representatividad estadística.

Busca obtener profundidad, detectar patrones iniciales y
corregir hipótesis.

Distribución deseada

Propietarios o coordinadores
Entre 3 y 4 personas que:

    dirijan un equipo pequeño de servicios;
    conozcan el proceso de atención;
    supervisen relaciones o seguimientos;
    tomen decisiones sobre herramientas.

Miembros operativos

Entre 3 y 4 personas que:

    atiendan clientes;
    registren información;
    realicen seguimientos;
    utilicen las herramientas actuales diariamente.

Cuando una persona cumpla ambos papeles, deberá
indicarse durante el análisis.




8. Criterios de inclusión

Los participantes deberán cumplir varios de estos criterios:

    trabajar en una organización que presta servicios;
    interactuar con clientes;
    gestionar información de clientes;
    realizar seguimientos;
    utilizar herramientas digitales o manuales para ello;
    compartir o necesitar compartir contexto;
    haber experimentado recientemente una situación
    donde faltó información;
    trabajar en un equipo pequeño;
    desarrollar su actividad principalmente en Colombia.

Buscaremos diversidad en:

    tamaño del equipo;
    nivel de habilidad digital;
    edad;
    tipo de servicio;
    volumen aproximado de clientes;
    dispositivo utilizado;
    ubicación;
    experiencia con CRM;
    necesidades de accesibilidad.




9. Criterios de exclusión para la primera
ronda

No utilizaremos como fuente principal:

    desarrolladores del proyecto;
    vendedores de software CRM;
    consultores que no utilicen el proceso diariamente;
    personas que solo hablen de experiencias ajenas;
    participantes interesados únicamente en promocionar
    una herramienta;
    respuestas completamente hipotéticas sin experiencia
    reciente.

Un experto puede entrevistarse posteriormente, pero no
sustituye a los usuarios.




10. Métodos

10.1. Entrevista semiestructurada

Permitirá comprender:

    experiencias;
    decisiones;
    frustraciones;
    vocabulario;
    excepciones;
    consecuencias.

Duración prevista:

45 a 60 minutos


10.2. Investigación contextual
Cuando sea posible, observaremos al participante en su
entorno habitual mostrando:

    cómo busca un cliente;
    dónde consulta información;
    cómo registra una interacción;
    cómo recuerda seguimientos;
    cómo comparte contexto.

No solicitaremos que muestre datos personales reales sin
medidas adecuadas.

Preferiremos:

    registros de demostración;
    datos anonimizados;
    ejemplos ficticios;
    reconstrucción verbal del proceso;
    pantallas con información ocultada.

10.3. Mapa de experiencia

Después de las entrevistas reconstruiremos:

1. inicio del contacto;
2. búsqueda de información;
3. atención;
4. registro;
5. seguimiento;
6. cierre o continuidad.

10.4. Pruebas de usabilidad posteriores

No se realizarán durante la primera ronda porque todavía
no existe prototipo.

Se planificarán cuando exista una propuesta de interacción
evaluable.




11. Preparación de la sesión

Antes de cada entrevista:
 1. confirmar que la persona pertenece al segmento;
 2. explicar el propósito;
 3. obtener consentimiento informado;
 4. aclarar que se evalúa el proceso, no a la persona;
 5. explicar si habrá grabación;
 6. permitir continuar sin grabación;
 7. recordar que no debe compartir información sensible;
 8. preparar un mecanismo de notas;
 9. asignar identificador anónimo;
10. probar audio y herramientas.

Ejemplo de identificador:

P01-COORD-SERVICIOS
P02-OPERATIVO-SERVICIOS


No usar el nombre del participante en los archivos de
análisis.




12. Introducción sugerida

   Gracias por participar. Estamos intentando comprender
   cómo equipos pequeños gestionan actualmente la
   información y los seguimientos de sus clientes. No
   estamos evaluando tu desempeño y no buscamos
   venderte una herramienta. Nos interesa conocer
   situaciones reales, incluso cuando el proceso funciona
   bien. Puedes omitir cualquier pregunta y no debes
   mostrar datos personales o confidenciales. Con tu
   permiso, tomaremos notas para analizar patrones de
   manera anonimizada.




13. Guía de entrevista

Bloque A — Rol y contexto

 1. Cuéntame qué haces normalmente en el negocio.
 2. ¿Cómo participas en la atención o seguimiento de
    clientes?
 3. ¿Cuántas personas pueden interactuar con un mismo
    cliente?
 4. ¿Qué herramientas utilizas durante ese trabajo?
 5. ¿Desde qué dispositivos trabajas?

Bloque B — Última experiencia real

 6. Piensa en el último cliente que volvió a comunicarse.
    ¿Qué ocurrió?
 7. ¿Cómo supiste quién era?
 8. ¿Dónde buscaste información anterior?
 9. ¿Encontraste todo lo que necesitabas?
10. ¿Tuviste que preguntarle a otra persona?
11. ¿El cliente tuvo que repetir información?
12. ¿Cuánto esfuerzo requirió reconstruir el contexto?

Bloque C — Registro

13. Después de atenderlo, ¿registraste algo?
14. Muéstrame o descríbeme cómo lo registraste.
15. ¿Qué información decidiste guardar?
16. ¿Qué información no guardaste?
17. ¿En qué momento hiciste el registro?
18. ¿Qué hace que a veces no registres algo?
19. ¿Qué ocurre cuando el registro queda incompleto?

Bloque D — Seguimiento

20. ¿Quedó algo por hacer?
21. ¿Cómo recuerdas ese pendiente?
22. ¿Alguien más puede verlo?
23. ¿Cómo sabes que ya fue completado?
24. Cuéntame una ocasión reciente en que un seguimiento
    se olvidó o retrasó.
25. ¿Qué consecuencia tuvo?

Bloque E — Coordinación

26. ¿Qué ocurre cuando otra persona atiende al mismo
    cliente?
27. ¿Cómo transfieren la responsabilidad?
28. ¿Qué ocurre cuando alguien está ausente?
29. ¿Han contactado dos veces al mismo cliente por error?
30. ¿Cómo identifica el coordinador qué requiere atención?

Bloque F — Datos

31. ¿Qué información es indispensable?
32. ¿Qué información se solicita pero casi nunca se utiliza?
33. ¿Qué datos cambian con frecuencia?
34. ¿Cómo corrigen un dato incorrecto?
35. ¿Qué información no debería ver todo el equipo?
36. ¿Qué información no debería almacenarse?
37. ¿Han tenido problemas por utilizar datos
    desactualizados?

Bloque G — Cambio

38. ¿Qué parte del método actual funciona bien?
39. ¿Qué no aceptarías perder al cambiar de herramienta?
40. ¿Qué hace que una herramienta sea demasiado
    complicada?
41. ¿Has utilizado un CRM anteriormente?
42. ¿Por qué funcionó o no funcionó?
43. ¿Qué mejora justificaría adoptar una herramienta
    nueva?
44. ¿Qué haría que dejaras de utilizarla?

Cierre

45. ¿Hay algo importante que no haya preguntado?
46. ¿Podríamos contactarte posteriormente para revisar un
    prototipo?




14. Preguntas que debemos evitar

Pregunta dirigida

¿No crees que un dashboard te ayudaría?


Pregunta doble

¿Te parece fácil y seguro el proceso?


Pregunta hipotética sin contexto
¿Usarías inteligencia artificial para gestionar clientes?


Pregunta que busca validación

¿Te gusta nuestra idea?


Pregunta con solución incorporada

¿Necesitas un botón para archivar clientes?


Alternativa

Cuéntame qué ocurre actualmente cuando una relación
ya no requiere seguimiento activo.




15. Plantilla de notas
ID del participante:
Rol:
Tipo de organización:
Tamaño aproximado del equipo:
Fecha:
Investigador:
Observador:


SITUACIÓN REAL DESCRITA
-


HERRAMIENTAS UTILIZADAS
-


PASOS DEL PROCESO
1.
2.
3.


INFORMACIÓN CONSULTADA
-


INFORMACIÓN REGISTRADA
-


FRICCIONES OBSERVADAS
-


CONSECUENCIAS
-


SOLUCIONES ACTUALES
-


VOCABULARIO UTILIZADO
-


DATOS CONSIDERADOS SENSIBLES
-


DISPOSITIVO Y ENTORNO
-


CITAS ANONIMIZADAS
-


HIPÓTESIS RESPALDADAS
-


HIPÓTESIS CONTRADICHAS
-


NUEVAS PREGUNTAS
-




16. Protección de participantes

Durante la investigación:

    no se recopilarán contraseñas;
    no se copiarán bases de clientes;
    no se almacenarán documentos de identidad;
    no se registrarán números reales de tarjetas;
    no se solicitarán datos médicos;
    no se publicarán nombres;
    no se incluirán nombres de clientes en Git;
    no se subirán grabaciones al repositorio;
    no se pegarán conversaciones privadas en Claude
    Code;
    no se usarán datos reales para prompts;
    no se conservará información más tiempo del
    necesario.

Las grabaciones, cuando existan, deberán mantenerse
fuera del repositorio y con acceso restringido.




17. Uso de IA durante la investigación

Claude Code u otra IA podrá ayudar a:

    preparar preguntas;
    estructurar notas anonimizadas;
    proponer categorías;
    comparar hallazgos;
    detectar contradicciones;
    resumir resultados ya desidentificados.

No deberá recibir:

    nombres reales;
    teléfonos;
    correos;
    documentos de identidad;
    direcciones;
    conversaciones privadas completas;
    secretos comerciales;
    grabaciones sin autorización;
    información sensible.

La IA no sustituirá la interpretación humana.

Cualquier conclusión propuesta por la IA deberá revisarse
contra las notas originales.




18. Análisis de resultados

Después de cada sesión:
 1. revisar las notas;
 2. separar observación de interpretación;
 3. eliminar identificadores;
 4. registrar preguntas nuevas;
 5. marcar evidencia relacionada con hipótesis;
 6. evitar conclusiones definitivas con una sola entrevista.

Después de cada ronda:

 1. agrupar observaciones similares;
 2. identificar patrones;
 3. identificar contradicciones;
 4. preservar casos atípicos;
 5. construir el recorrido real;
 6. actualizar usuarios provisionales;
 7. reformular necesidades;
 8. actualizar vision.md ;
 9. decidir qué investigar después;
10. registrar qué decisiones cambiaron.




19. Matriz de hipótesis
HIPÓTESIS:
H1 — La información está fragmentada.


EVIDENCIA A FAVOR:
-


EVIDENCIA EN CONTRA:
-


PARTICIPANTES RELACIONADOS:
-


NIVEL ACTUAL:
[ ] Sin investigar
[ ] Evidencia débil
[ ] Patrón inicial
[ ] Respaldada en el segmento estudiado
[ ] Contradicha
[ ] Requiere otra ronda
DECISIÓN:
-


PREGUNTAS ABIERTAS:
-


La misma estructura se utilizará para cada hipótesis.




20. Reglas para convertir hallazgos en
decisiones

Regla 1

Una solicitud de funcionalidad no se convierte directamente
en necesidad.

Regla 2

Buscaremos el problema situado detrás de la solicitud.

Regla 3

Una sola declaración no representa automáticamente al
segmento.

Regla 4

Una conducta observada puede tener más peso que una
preferencia declarada.

Regla 5

Los casos contradictorios no se eliminarán para producir
una historia más sencilla.

Regla 6

Cuando dos roles tengan necesidades incompatibles, se
documentará el conflicto.

Regla 7
No diseñaremos para todos los casos desde la primera
versión.

Regla 8

No añadiremos información personal sin una finalidad
clara.

Regla 9

Una necesidad crítica deberá relacionarse con un resultado
o una consecuencia real.

Regla 10

Cada decisión deberá indicar qué evidencia la motivó.




21. Posibles resultados de una hipótesis

Confirmada dentro del segmento estudiado

Existe un patrón consistente y suficientemente relevante.

Parcialmente respaldada

Ocurre únicamente bajo ciertas condiciones o roles.

Contradicha

La evidencia muestra que la suposición era incorrecta.

No concluyente

La ronda no produjo evidencia suficiente.

Fuera del segmento

El problema existe, pero pertenece a otro tipo de
organización.

No utilizaremos la palabra “confirmada” como verdad
universal.
22. Salidas de la primera ronda

La primera ronda deberá producir:

   resumen de participantes;
   mapa del proceso actual;
   herramientas utilizadas;
   principales necesidades;
   dificultades observadas;
   consecuencias;
   vocabulario del dominio;
   diferencias por rol;
   hipótesis respaldadas;
   hipótesis contradichas;
   preguntas abiertas;
   actualización de la visión;
   insumos para definir alcance;
   recomendaciones para la segunda ronda.




23. Señales de un problema prioritario

Un problema tendrá mayor prioridad cuando:

   ocurra repetidamente;
   afecte a varios roles;
   tenga consecuencias importantes;
   no tenga una solución actual satisfactoria;
   esté alineado con la visión;
   pueda resolverse progresivamente;
   el equipo esté dispuesto a cambiar su comportamiento;
   no requiera una complejidad desproporcionada.




24. Señales de que no debemos construir
todavía

No construiremos una capacidad cuando:

   solo apareció como deseo hipotético;
   no conocemos su proceso;
    no entendemos quién la utiliza;
    no conocemos sus datos;
    no sabemos cómo verificar su éxito;
    depende de una integración no investigada;
    introduce datos sensibles sin justificación;
    intenta resolver demasiados problemas
    simultáneamente;
    pertenece a un segmento distinto;
    la solución actual funciona suficientemente bien.




25. Sesgos que debemos vigilar

Sesgo de confirmación

Buscar únicamente evidencia favorable a la idea.

Sesgo de selección

Entrevistar solo personas cercanas o muy tecnológicas.

Sesgo de cortesía

El participante dice que le gusta la idea para no incomodar.

Sesgo retrospectivo

La persona reconstruye los hechos de forma incompleta.

Sesgo de solución

Hablar demasiado pronto de pantallas y funcionalidades.

Sesgo del experto

Suponer que el vocabulario técnico es natural para los
usuarios.

Sesgo de autoridad

El propietario define lo que supuestamente necesita el
usuario operativo sin observarlo.

Sesgo de automatización
Asumir que automatizar siempre mejora el proceso.




26. Inclusión

La investigación deberá considerar personas que:

    tengan diferentes niveles de experiencia digital;
    utilicen teclado o tecnologías de asistencia;
    tengan dificultades visuales;
    trabajen principalmente desde teléfono;
    tengan conectividad limitada;
    necesiten apoyo para aprender sistemas nuevos;
    trabajen en ambientes con interrupciones;
    compartan dispositivos;
    utilicen lenguaje diferente al vocabulario habitual de
    CRM.

No diseñaremos únicamente para participantes
técnicamente avanzados.




27. Rondas previstas

Ronda 1 — Comprensión del problema

Métodos:

    entrevistas;
    observación contextual;
    mapa de experiencia.

Objetivo:

    comprender el proceso actual;
    revisar hipótesis;
    definir necesidades.

Ronda 2 — Priorización y modelo conceptual

Métodos posibles:

    entrevistas de seguimiento;
    clasificación de información;
    revisión de flujos conceptuales;
    prototipos de baja fidelidad.

Objetivo:

    probar si el modelo mental del producto coincide con el
    de los usuarios.

Ronda 3 — Usabilidad inicial

Métodos:

    prueba moderada con prototipo navegable.

Objetivo:

    evaluar tareas fundamentales.

Rondas posteriores

Se definirán según los resultados, no de forma automática.




28. Criterios de finalización de este
descubrimiento inicial

El descubrimiento inicial estará suficientemente avanzado
cuando podamos explicar con evidencia:

    quién experimenta el problema;
    en qué contexto;
    qué intenta conseguir;
    cómo lo resuelve actualmente;
    dónde falla el proceso;
    qué consecuencias tiene;
    qué información necesita;
    qué responsabilidades existen;
    qué parte del problema abordará la primera versión;
    qué quedará fuera;
    cómo sabremos si la solución ayuda.

Eso no significa que la investigación termine para siempre.
            La investigación continuará durante diseño,
            implementación y operación.




            29. Estado actual

               Plan preparado: sí.
               Participantes reclutados: no.
               Consentimiento preparado: pendiente.
               Entrevistas realizadas: 0.
               Observaciones realizadas: 0.
               Hipótesis respaldadas: 0.
               Hipótesis contradichas: 0.
               Necesidades validadas: 0.
               Prototipo: no existe.
               Implementación: no iniciada.




11. Verificar las modificaciones
Cuando Claude termine, no aceptes ninguna edición fuera de las dos rutas
autorizadas.

Ejecuta:


     Bash

  git status --short


El resultado esperado será similar a:


  ?? proyecto-crm-profesional/


Esto ocurre porque Git agrupa inicialmente el directorio nuevo completo.

Lista los archivos:


     Bash

  find proyecto-crm-profesional -type f -print
El resultado debe mostrar exactamente:


  proyecto-crm-profesional/docs/product/vision.md
  proyecto-crm-profesional/docs/product/user-research-plan.md


Comprueba que no existe un tercer archivo:


       Bash

  find proyecto-crm-profesional -type f | wc -l


Resultado esperado:


  2


Comprueba los tamaños:


       Bash

  wc -l \
      proyecto-crm-profesional/docs/product/vision.md \
      proyecto-crm-profesional/docs/product/user-research-plan.md


No estamos imponiendo un límite artificial. Solo verificamos que Claude no
haya truncado los documentos.

Revisa sus comienzos y finales:


       Bash

  sed -n '1,80p' proyecto-crm-profesional/docs/product/vision.md
  tail -n 40 proyecto-crm-profesional/docs/product/vision.md


  sed -n '1,80p' proyecto-crm-profesional/docs/product/user-research-plan.md
  tail -n 40 proyecto-crm-profesional/docs/product/user-research-plan.md


Busca elementos que no deberían aparecer:


       Bash

  grep -RniE \
      'Spring Boot|React|PostgreSQL|endpoint|controller|entity|repository|OpenSpec|opsx' \
      proyecto-crm-profesional/docs/product


Es normal que aparezcan palabras como OpenSpec en la sección que explica
que todavía no se ha introducido. No debe aparecer diseño técnico ni
instrucciones de implementación.
12. Revisión humana obligatoria
Antes de hacer git add , confirma:


  [ ] La visión describe resultados y no tecnologías.
  [ ] El problema está etiquetado como provisional.
  [ ] No se afirma que entrevistamos usuarios.
  [ ] Los usuarios son perfiles funcionales.
  [ ] No hay biografías ficticias irrelevantes.
  [ ] Las necesidades no están escritas como botones o pantallas.
  [ ] No se diseñaron campos definitivos.
  [ ] No se diseñó la base de datos.
  [ ] No se seleccionó arquitectura.
  [ ] No se añadieron funcionalidades de IA.
  [ ] No se recopilan datos sensibles deliberadamente.
  [ ] Existe un plan concreto para validar hipótesis.
  [ ] Solo se crearon dos archivos.
  [ ] El material del curso permanece intacto.




13. Registrar el cambio en Git
Añade exclusivamente las dos rutas:


       Bash

  git add -- \
      proyecto-crm-profesional/docs/product/vision.md \
      proyecto-crm-profesional/docs/product/user-research-plan.md


Comprueba el área de preparación:


       Bash

  git status --short
  git diff --cached --name-only


Resultado esperado:


  A   proyecto-crm-profesional/docs/product/vision.md
  A   proyecto-crm-profesional/docs/product/user-research-plan.md


Verifica espacios y errores de parche:


       Bash
  git diff --cached --check


No debe mostrar nada.

Revisa el resumen:


     Bash

  git diff --cached --stat


Crea el commit:


     Bash

  git commit -m "docs: define CRM product vision and research plan"


Comprueba:


     Bash

  git log -1 --oneline
  git status --short --branch


El árbol debe quedar limpio.

Para respaldar la rama en GitHub sin mezclarla con main :


     Bash

  git push -u origin docs/module-1-product-discovery




14. Qué acabamos de practicar de los tres
pilares
Herramienta
Usamos Claude Code en dos estados diferentes:


  Plan Mode
  → analizar sin editar


  Modo con aprobación
  → crear únicamente los archivos revisados
Contexto
Le explicamos:
    qué contiene el repositorio;
    dónde comienza el producto;
    que prompts/ no es autoridad;
    que todavía no hay stack;
    que no existen entrevistas;
    que OpenSpec llegará después;
    qué rutas puede modificar.

Prompt
Definimos:
    objetivo;
    archivos autorizados;
    restricciones;
    formato;
    criterios de éxito;
    verificación.

El prompt no reemplazó el contexto y el contexto no reemplazó los permisos.

Los tres trabajaron juntos.




15. Criterios de finalización del Paso 2
El Paso 2 queda completo cuando:


  [ ] Existe la rama docs/module-1-product-discovery.
  [ ] Existe vision.md.
  [ ] Existe user-research-plan.md.
  [ ] Solo se crearon esos dos archivos.
  [ ] La visión diferencia decisiones e hipótesis.
  [ ] Los usuarios provisionales están definidos por función.
  [ ] El problema no se presenta como hecho demostrado.
  [ ] Existe un plan para investigar usuarios reales.
  [ ] No se seleccionó tecnología.
  [ ] No se diseñaron funcionalidades definitivas.
  [ ] No se generó código.
  [ ] Git diff --cached --check no presentó errores.
  [ ] Se creó el commit documental.
  [ ] La rama fue respaldada en GitHub.
  [ ] El árbol de trabajo quedó limpio.
Resultado conceptual
Ahora el proyecto ya no comienza con:


  Quiero hacer un CRM.


Comienza con:


  Tenemos una visión.
  Tenemos usuarios provisionales.
  Tenemos un problema formulado.
  Sabemos qué es hipótesis.
  Sabemos qué falta investigar.
  Sabemos qué no debemos construir todavía.


¿Deseas continuar con el Paso 3 de 18: definir detalladamente el
alcance, la primera versión funcional, las funcionalidades y los no
objetivos del CRM?




                                     Today 5:49 PM


                              Absolutamente todo funciono, continuemos con el
                              Paso 3 de 18: definir detalladamente el alcance, la
                              primera versión funcional, las funcionalidades y los
                              no objetivos del CRM
                              (https://github.com/Diiegoal/CursoIA/tree/docs/mod
                              ule-1-product-discovery), investiga
                              exhaustivamente y busca en fuentes confiables sin
                              inventar datos para hacer este paso 3, con datos
                              mas recientes hasta julio 2026, aclaracion: los
                              modulos solo viviran en la rama main y no en docs,
                              si me entiendes?.

Worked for 3m 1s

Paso 3 de 18 — Alcance, primera versión
funcional y no objetivos
Entendí la aclaración y verifiqué la rama.

Separación actual de ramas
La estructura será:
  main
  └── Material del curso
     ├── Módulo_1_...
     ├── Módulo_2_...
     ├── ...
     └── prompts/




  docs/module-1-product-discovery
  └── Proyecto CRM
     └── proyecto-crm-profesional/
         └── docs/
               └── product/
                  ├── vision.md
                  └── user-research-plan.md


En la rama del proyecto encontré correctamente los dos documentos del Paso
2. vision.md define que todavía no existe implementación ni stack definitivo y
que el producto debe ayudar a conocer al cliente, entender lo ocurrido y saber
qué sigue.

El plan de investigación también conserva las doce hipótesis como no
confirmadas y señala que todavía no se ha ejecutado ninguna entrevista.

Regla crítica de Git
La rama docs/module-1-product-discovery se deriva de main , pero contiene la
eliminación de los módulos. Por eso:

   Nunca debes abrir ni fusionar un pull request desde docs/module-1-
   product-discovery hacia main .


Un PR de esa rama hacia main propondría:
    añadir el proyecto;
    eliminar los siete módulos;
    eliminar prompts/ .

En nuestro flujo:


  main = curso
  docs/module-1-product-discovery = proyecto CRM


Los commits del CRM se enviarán directamente a su rama independiente. No
se fusionarán con main .
1. Qué significa realmente definir el alcance
El alcance responde:


  ¿Qué resolverá esta versión?
  ¿Qué podrá hacer el usuario?
  ¿Qué quedará conscientemente fuera?
  ¿En qué condiciones podrá usarse?
  ¿Cómo sabremos que está terminada?


No responde todavía:


  ¿Qué clases Java crearemos?
  ¿Qué endpoints tendrá la API?
  ¿Qué tablas tendrá PostgreSQL?
  ¿Qué componentes React construiremos?


Eso pertenece a la especificación y la arquitectura posteriores.

La guía de servicios digitales de GOV.UK advierte que un alcance demasiado
amplio oculta el problema que se intenta resolver, mientras que uno
demasiado estrecho puede no completar el resultado que necesita el usuario.
También recomienda que la forma del servicio responda al recorrido del
usuario y no a la estructura técnica u organizativa.   GOV.…



Nuestro alcance, por tanto, debe cubrir un recorrido completo pequeño, no
muchas funcionalidades inconexas.




2. Qué será nuestra primera versión
2.1. No la llamaremos producción
Todavía no hemos:
    entrevistado usuarios reales;
    validado las hipótesis;
    diseñado autenticación;
    implementado autorización;
    ejecutado pruebas de seguridad;
    definido una política de respaldos;
    desplegado infraestructura;
    realizado pruebas con datos reales;
    comprobado cumplimiento de accesibilidad.
Por eso, el primer software que construiremos no será todavía un “CRM listo
para producción”.

Lo llamaremos:


   Development Preview: primera versión funcional integrada para
   aprendizaje y validación técnica.

Después construiremos:

   Pilot Candidate: versión protegida y preparada para pruebas
   controladas con usuarios.

Solamente después de validación, seguridad y operación podrá existir una
versión de producción.

Esta distinción evita un error frecuente:


  La aplicación compila
  ≠
  la aplicación es viable
  ≠
  la aplicación está lista para datos reales




2.2. Diferencias entre las etapas
Etapa                 Objetivo                   Usuarios           Datos

Prototipo             Probar ideas de            Participantes de   Ficticios
                      interacción                investigación


Development           Probar el recorrido y la   Equipo de          Ficticios
Preview               integración full stack     desarrollo


Pilot Candidate       Preparar seguridad,        Equipo y           Ficticios o
                      acceso y operación         evaluadores        anonimizados


Piloto                Validar utilidad con       Usuarios           Controlados
                      usuarios limitados         autorizados


Producción            Operación real             Organizaciones     Reales, con
                      sostenida                  usuarias           controles
Un MVP no debe entenderse simplemente como “una aplicación incompleta”.
Es la versión más sencilla que permite poner a prueba una propuesta y
aprender de usuarios reales.            Atlas…



Nuestro Development Preview será anterior al MVP validado.




3. Investigación sobre el núcleo funcional de un
CRM
Las plataformas actuales de CRM incluyen cientos de capacidades, pero sus
documentaciones convergen en un núcleo reconocible:
       registros de clientes, contactos u organizaciones;
       historial de interacciones;
       actividades o tareas;
       responsables;
       fechas y seguimientos;
       búsqueda y consulta compartida.

Microsoft documenta en Dynamics 365 la administración separada de
organizaciones y contactos, la conservación de registros inactivos y la
asociación de actividades a clientes.                 Microsoft L…



También explica que registrar llamadas, reuniones, correos y tareas crea un
historial compartido, evita duplicar esfuerzos y permite continuar el
seguimiento con contexto.            Microsoft … +1



HubSpot presenta como funciones centrales la gestión de contactos, el registro
de actividades, el historial de comunicaciones y las tareas. En cambio, pipeline,
informes, automatización, inteligencia artificial e integraciones amplían el
producto más allá de ese núcleo.                 Hub…   +1



Zoho también separa gestión de contactos y actividades de capacidades más
amplias como leads, oportunidades, automatización, omnicanalidad, analítica e
inteligencia artificial.     Z… +1



No copiaremos ninguna plataforma. La comparación sirve para distinguir:


  Núcleo relacional
  de
  Suite comercial completa
4. El recorrido mínimo completo
La primera versión deberá completar este ciclo:


  Encontrar o registrar un cliente
                    ↓
  Consultar su contexto
                    ↓
  Registrar una interacción
                    ↓
  Crear un seguimiento
                    ↓
  Encontrar el seguimiento pendiente
                    ↓
  Completar o cancelar el seguimiento
                    ↓
  Conservar el historial


Ese ciclo conecta directamente con la visión:


  Conocer al cliente
         ↓
  Entender qué ocurrió
         ↓
  Saber qué sigue


Una aplicación que solo permita crear, editar y eliminar clientes no completaría
la visión. Sería únicamente un CRUD de contactos.




5. Capacidades que estarán dentro
Aplicaremos una clasificación MoSCoW:
    Must Have: sin esto, la versión no cumple su objetivo.
    Should Have: importante, pero la primera entrega puede sobrevivir
    temporalmente sin ello.
    Could Have: aporta valor, pero se elimina primero cuando amenaza el
    alcance.
    Won’t Have for now: queda expresamente fuera.

La definición oficial actual de MoSCoW considera los Must Have como no
negociables para el éxito del alcance y recomienda acordar criterios objetivos
para diferenciar Should y Could.        Agile Busine… +1




Must Have
Gestión de clientes
   registrar un cliente;
   listar clientes activos;
   consultar el detalle;
   actualizar información básica;
   archivar;
   restaurar un cliente archivado;
   conservar fechas de creación y actualización.

Búsqueda
   buscar por información identificadora;
   distinguir resultados activos y archivados;
   comunicar claramente cuando no existen resultados.

Historial de interacciones
   registrar una interacción relacionada con un cliente;
   indicar cuándo ocurrió;
   indicar quién la registró;
   guardar un resumen;
   consultar las interacciones en orden cronológico;
   conservarlas al archivar el cliente.

Seguimientos
   registrar una acción pendiente;
   asociarla con un cliente;
   asignarla a un integrante provisional;
   establecer fecha límite;
   distinguir pendiente, completada y cancelada;
   marcarla como completada;
   conservar el historial.

Vista de trabajo
   mostrar seguimientos vencidos;
   mostrar seguimientos para hoy;
   mostrar próximos seguimientos;
   abrir el cliente relacionado desde el seguimiento.

Persistencia real
   los datos deben almacenarse en PostgreSQL;
   reiniciar la aplicación no debe borrar los registros;
   frontend y backend deben comunicarse mediante la API;
   el frontend no utilizará arreglos temporales como almacenamiento final.

Validación y errores
   impedir registros estructuralmente inválidos;
   mostrar errores comprensibles;
   evitar fallos silenciosos;
   impedir operaciones sobre registros inexistentes;
   manejar errores de concurrencia básica o actualización obsoleta cuando se
   introduzca.

Should Have
   ordenar listas;
   paginar resultados;
   filtrar por estado;
   filtrar seguimientos por responsable;
   mostrar actividad reciente;
   advertir posibles duplicados;
   permitir notas generales del cliente;
   mostrar estados vacíos útiles;
   ofrecer confirmación antes de archivar;
   conservar el último criterio de búsqueda durante la navegación.

Could Have
   etiquetas;
   acciones rápidas;
   filtros guardados;
   búsqueda parcial tolerante;
   indicador visual de información incompleta;
   vista compacta y vista detallada;
   accesos rápidos desde el dashboard;
   conteos básicos por estado;
   restauración directa desde resultados archivados.




6. Lo que no tendrá esta primera versión
Quedarán fuera:
   leads como entidad separada;
   oportunidades;
   pipeline de ventas;
   cotizaciones;
   facturación;
   productos;
   inventario;
   campañas;
   marketing;
   correo integrado;
   WhatsApp integrado;
   telefonía;
   reuniones virtuales;
   calendario externo;
   automatizaciones;
   workflows configurables;
   notificaciones por correo o SMS;
   importación masiva;
   exportación masiva;
   archivos adjuntos;
   personalización de campos;
   formularios públicos;
   portal del cliente;
   aplicaciones móviles nativas;
   funcionamiento sin conexión;
   multitenancy;
   múltiples organizaciones por cuenta;
   suscripciones;
   pagos;
   inteligencia artificial;
   recomendaciones predictivas;
   scoring;
   forecasting;
   analítica avanzada;
   reportes personalizados;
   microservicios;
   Kafka;
   Redis;
   Kubernetes.

No significa que estén prohibidos permanentemente. Significa que no forman
parte del problema que necesitamos validar primero.
7. Autenticación y datos reales
La Development Preview funcionará con:
    un espacio de trabajo ficticio;
    integrantes de demostración;
    datos inventados;
    acceso únicamente del equipo de desarrollo;
    ningún dato personal real.

La autenticación y la autorización básica serán requisitos obligatorios del Pilot
Candidate, antes de utilizar información real.

Esto permite aprender arquitectura e integración sin presentar una aplicación
insegura como sistema utilizable.


  Development Preview
  ├── sin usuarios externos
  ├── sin datos reales
  ├── identidades demostrativas
  └── acceso local o entorno restringido


  Pilot Candidate
  ├── autenticación
  ├── autorización
  ├── aislamiento de datos
  ├── gestión de secretos
  ├── HTTPS
  ├── respaldo
  ├── registros operativos
  └── revisión de privacidad




8. Archivos que crearemos
Solo se crearán:


  proyecto-crm-profesional/docs/product/scope.md
  proyecto-crm-profesional/docs/product/release-strategy.md


No modificaremos:
    vision.md ;
    user-research-plan.md ;
    la rama main ;
    los módulos;
    archivos de código;
    configuraciones de Claude Code.




9. Preparar la rama correcta
En Git Bash:


     Bash

  git fetch origin
  git switch docs/module-1-product-discovery
  git pull --ff-only origin docs/module-1-product-discovery


Comprueba:


     Bash

  git branch --show-current
  git status --short --branch


Debe indicar:


  docs/module-1-product-discovery


Comprueba que el proyecto está presente:


     Bash

  find proyecto-crm-profesional -type f -print


Comprueba que los módulos no viven en esta rama:


     Bash

  git ls-tree -d --name-only HEAD | grep '^Módulo_'


Resultado esperado:


  sin salida


Comprueba que sí viven en main sin cambiarte de rama:


     Bash
  git ls-tree -d --name-only origin/main | grep '^Módulo_'


Debe mostrar los siete directorios.

No ejecutes:


      Bash

  git merge main
  git rebase main
  git checkout main -- .


Cualquiera de esas operaciones puede volver a introducir el curso en la rama
del CRM.




10. Planificar con Claude Code
Inicia:


      Bash

  claude --permission-mode plan


Pega:


  OBJETIVO


  Preparar el Paso 3 del proyecto CRM Profesional definiendo el alcance,
  la primera versión funcional, las capacidades incluidas, los no objetivos
  y la estrategia de liberación progresiva.


  CONTEXTO DEL REPOSITORIO


  - main contiene exclusivamente el material del curso.
  - docs/module-1-product-discovery contiene exclusivamente el proyecto CRM.
  - Estas dos líneas no se deben fusionar.
  - No debes recuperar, copiar ni recrear los módulos dentro de esta rama.
  - El proyecto está en proyecto-crm-profesional/.
  - Ya existen:
    - docs/product/vision.md
    - docs/product/user-research-plan.md
  - Todavía no existe código.
  - Todavía no se ha elegido definitivamente el stack.
  - Todavía no se han realizado entrevistas con usuarios.
  - La implementación comenzará posteriormente con OpenSpec.


  OBJETIVO DEL PRODUCTO
Permitir que equipos pequeños conozcan al cliente, entiendan qué ocurrió
y sepan qué debe suceder después.


RECORRIDO CENTRAL PROPUESTO


1. Encontrar o registrar un cliente.
2. Consultar su contexto.
3. Registrar una interacción.
4. Crear un seguimiento.
5. Encontrar el seguimiento pendiente.
6. Completarlo o cancelarlo.
7. Conservar el historial.


ARCHIVOS AUTORIZADOS


El plan debe limitarse a crear:


1. proyecto-crm-profesional/docs/product/scope.md
2. proyecto-crm-profesional/docs/product/release-strategy.md


TAREA


1. Lee vision.md y user-research-plan.md.
2. Verifica que los dos archivos autorizados no existen.
3. Evalúa si el alcance propuesto es coherente con la visión.
4. Identifica contradicciones entre alcance, hipótesis y no objetivos.
5. Propón un plan exacto para crear únicamente los dos archivos.
6. Incluye una verificación de que los módulos no fueron introducidos.
7. Incluye verificación mediante Git.


RESTRICCIONES


- Permanece en Plan Mode.
- No edites ningún archivo.
- No cambies de rama.
- No fusiones main.
- No recuperes archivos del curso.
- No crees backend ni frontend.
- No diseñes endpoints, tablas o clases.
- No selecciones definitivamente tecnologías.
- No conviertas hipótesis en hechos.
- No uses datos reales.
- No ejecutes git add, commit, push, merge, rebase, reset o clean.
- No amplíes el alcance con funciones comunes de otros CRM.
- No introduzcas autenticación dentro de Development Preview.
- Señala que autenticación y autorización serán obligatorias antes del piloto.


CRITERIOS DE ÉXITO


- Solo se proponen dos archivos nuevos.
- Existe un recorrido end-to-end pequeño.
  - Must, Should, Could y Won't están claramente separados.
  - Se diferencia Development Preview, Pilot Candidate, Pilot y Producción.
  - Se prohíben datos reales en Development Preview.
  - Existe una Definition of Done verificable.
   N       difi       i




11. Revisar el plan
Rechaza el plan si Claude propone:
    copiar los módulos;
    fusionar main ;
    crear código;
    instalar dependencias;
    crear un backlog detallado;
    diseñar la base de datos;
    añadir pipeline de ventas;
    añadir autenticación a la Development Preview;
    utilizar datos reales;
    crear más de dos archivos;
    modificar los documentos anteriores;
    abrir un pull request hacia main .

Aprueba la opción equivalente a revisar manualmente cada edición.




12. Prompt de ejecución
Después de aprobar el plan y salir de Plan Mode:


  Implementa exclusivamente el plan aprobado.


  Crea únicamente:


  - proyecto-crm-profesional/docs/product/scope.md
  - proyecto-crm-profesional/docs/product/release-strategy.md


  Usa exactamente los contenidos proporcionados a continuación.


  RESTRICCIONES


  - No modifiques vision.md.
  - No modifiques user-research-plan.md.
  - No crees otros archivos.
  - No escribas código.
  - No instales dependencias.
 - No cambies de rama.
 - No fusiones, rebases ni copies contenido desde main.
 - No recuperes los módulos del curso.
 - No ejecutes git add, commit o push.
 - No abras pull requests.
 - Al finalizar, informa solamente:
  1. archivos creados;
  2. archivos modificados;
  3. confirmación de que no se tocó main;
  4. comandos de verificación recomendados.




13. Contenido de scope.md

    Edit




           Alcance del producto — CRM
           Profesional

              Estado: alcance inicial aprobado para preparación
              Fecha: 2026-07-28
              Fase: Módulo 1 — Definición del producto
              Producto: CRM Profesional
              Rama del proyecto: docs/module-1-product-discovery
              Implementación: no iniciada
              Documentos relacionados: vision.md , user-research-
              plan.md
              Próxima revisión obligatoria: después de
              investigación con usuarios y antes de aprobar el piloto




           1. Propósito

           Este documento define qué pretende resolver la primera
           etapa de CRM Profesional, qué capacidades tendrá, qué
           quedará fuera y qué condiciones deben cumplirse para
           considerar completa cada versión.

           No sustituye:

               la investigación con usuarios;
   una especificación OpenSpec;
   el diseño de interacción;
   la arquitectura;
   el modelo de datos;
   los contratos de API;
   el backlog;
   la Definition of Done técnica de cada cambio.




2. Política de ramas
[DECISIÓN]


El repositorio mantiene dos líneas independientes:

main
└── material del curso

docs/module-1-product-discovery
└── proyecto CRM Profesional


Reglas:

   los módulos del curso solo viven en main ;
   el proyecto CRM no se fusionará hacia main ;
   no se abrirán pull requests desde la rama del proyecto
   hacia main ;
   no se recuperarán los módulos dentro de la rama del
   proyecto;
   no se fusionará ni rebasará la rama del proyecto sobre
       main ;
   cualquier futura reorganización de ramas requerirá una
   decisión explícita y una copia de seguridad.




3. Convenciones de certeza

[DECISIÓN]

Elección vigente del producto.

[HIPÓTESIS]
Suposición pendiente de evidencia.

[POR VALIDAR]

Pregunta que necesita investigación o experimentación.

[NO OBJETIVO]

Elemento expresamente excluido.

[GATE]

Condición obligatoria antes de avanzar de etapa.




4. Conceptos utilizados

Visión

Explica por qué existe el producto y qué resultado pretende
producir.

Alcance

Define qué problema y qué capacidades se abordarán en
una etapa.

Especificación

Define posteriormente el comportamiento exacto y
verificable.

Backlog

Ordena el trabajo necesario para cumplir especificaciones.

Development Preview

Primera aplicación integrada, restringida al equipo de
desarrollo y a datos ficticios.

Pilot Candidate

Versión endurecida y preparada para evaluación
controlada.
Piloto

Uso limitado por personas autorizadas en condiciones
supervisadas.

Producción

Operación sostenida con datos reales, seguridad, soporte y
responsabilidades definidas.




5. Objetivo del producto

   Permitir que equipos pequeños mantengan una visión
   compartida de cada relación con clientes para conocer
   al cliente, entender qué ocurrió y saber qué debe
   suceder después.


Este objetivo permanece provisional hasta ser contrastado
con usuarios reales.




6. Principio de alcance

La primera versión no intentará reproducir una suite CRM
completa.

Construirá un recorrido pequeño de principio a fin:

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


Una funcionalidad solo pertenecerá al alcance inicial
cuando contribuya directamente a ese recorrido.
7. Usuarios provisionales

Miembro operativo

Necesita consultar contexto, registrar lo ocurrido y dejar
claro el siguiente paso.

Propietario o coordinador

Necesita identificar relaciones y seguimientos que
requieren atención.

Administrador

No será todavía un rol separado en Development Preview.

Cliente registrado

No utilizará directamente la aplicación inicial, pero sus
datos se verán afectados por el sistema.

Todos estos perfiles siguen sujetos a investigación.




8. Resultado mínimo de usuario

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




9. Recorrido funcional central

Escenario central
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




10. Development Preview

10.1. Objetivo

Comprobar que el producto puede ejecutar el recorrido
central mediante una aplicación full stack integrada.

10.2. Audiencia

Exclusivamente:

    desarrolladores;
    revisores técnicos;
    evaluadores internos;
    participantes de demostraciones controladas sin datos
    reales.

10.3. Datos

Solo:

    ficticios;
    sintéticos;
    generados para pruebas;
    anonimizados de manera irreversible cuando exista
    autorización.

Está prohibido utilizar:
    clientes reales;
    conversaciones reales;
    correos personales;
    teléfonos reales;
    documentos de identidad;
    información sensible;
    credenciales reutilizadas.

10.4. Identidades

Development Preview podrá utilizar integrantes
demostrativos preconfigurados para representar autoría y
asignaciones.

Estas identidades:

    no equivalen a autenticación;
    no deben utilizarse para control de acceso;
    no permiten datos reales;
    deberán reemplazarse antes del piloto.




11. Capacidades Must Have

Una capacidad Must Have es indispensable para completar
el recorrido central.

M-01 — Registrar clientes

El sistema permitirá crear un registro de cliente con la
información mínima necesaria para distinguirlo.

Los campos definitivos se especificarán posteriormente.

M-02 — Listar clientes activos

El usuario podrá consultar clientes no archivados.

M-03 — Consultar detalle

El usuario podrá abrir un cliente y comprender:

    su identidad;
    su estado;
    su información disponible;
    su actividad;
    sus seguimientos.

M-04 — Actualizar información

El usuario podrá corregir o actualizar información del
cliente.

M-05 — Archivar

El usuario podrá retirar un cliente del flujo activo sin
destruir su historial.

M-06 — Restaurar

Un cliente archivado podrá volver al estado activo.

M-07 — Buscar

El usuario podrá buscar clientes mediante información
identificadora.

El comportamiento exacto de búsqueda se definirá en
OpenSpec.

M-08 — Registrar interacción

El usuario podrá registrar que ocurrió una interacción con
el cliente.

La interacción deberá conservar, como mínimo conceptual:

    cliente relacionado;
    momento;
    resumen;
    tipo o contexto;
    autor demostrativo;
    fecha de creación.

M-09 — Consultar historial

Las interacciones deberán mostrarse de forma cronológica
y comprensible.
M-10 — Crear seguimiento

El usuario podrá crear una acción posterior relacionada con
un cliente.

M-11 — Asignar seguimiento

El seguimiento podrá asociarse con un integrante
demostrativo.

M-12 — Establecer vencimiento

El seguimiento permitirá indicar cuándo debe completarse.

M-13 — Cambiar estado del seguimiento

Los estados mínimos serán conceptualmente:

    pendiente;
    completado;
    cancelado.

La representación técnica se definirá posteriormente.

M-14 — Consultar pendientes

El usuario podrá consultar seguimientos:

    vencidos;
    para hoy;
    próximos.

M-15 — Navegar del seguimiento al cliente

El usuario podrá recuperar el contexto del cliente desde su
seguimiento.

M-16 — Conservar historial

Completar, cancelar o archivar no deberá borrar el
contexto histórico.

M-17 — Persistencia

La información deberá mantenerse después de reiniciar la
aplicación y almacenarse en la base de datos definida para
el proyecto.

M-18 — Validación

El sistema deberá impedir entradas estructuralmente
inválidas y explicar el problema.

M-19 — Manejo de inexistencia

El sistema deberá responder claramente cuando el registro
solicitado no existe.

M-20 — Estados de interfaz

La interfaz deberá representar:

    carga;
    éxito;
    ausencia de resultados;
    error recuperable;
    error no recuperable.




12. Capacidades Should Have

Son importantes, pero pueden introducirse después del
primer recorrido integrado.

S-01 — Ordenar clientes

S-02 — Paginar listas

S-03 — Filtrar por estado activo o archivado

S-04 — Filtrar seguimientos por responsable

S-05 — Filtrar por estado temporal

S-06 — Mostrar actividad reciente

S-07 — Confirmar operaciones de archivo

S-08 — Estados vacíos con orientación

S-09 — Advertir posibles duplicados
S-10 — Conservar criterios de búsqueda
durante la navegación

S-11 — Mostrar información incompleta

S-12 — Mostrar fecha y autor de los cambios
relevantes



13. Capacidades Could Have

Se considerarán solamente si no comprometen los Must
Have.

C-01 — Etiquetas

C-02 — Filtros guardados

C-03 — Acciones rápidas

C-04 — Búsqueda tolerante a pequeñas
variaciones

C-05 — Vista compacta

C-06 — Conteos básicos

C-07 — Atajos desde la vista de trabajo

C-08 — Restauración rápida

C-09 — Preferencias visuales locales

C-10 — Datos demostrativos preconfigurados



14. Won’t Have for Now

Gestión comercial avanzada

   leads independientes;
   oportunidades;
   deals;
   pipeline;
   forecast;
   scoring;
   metas comerciales;
   territorios;
   cotizaciones.

Marketing

   campañas;
   formularios públicos;
   newsletters;
   segmentación avanzada;
   automatización de marketing;
   redes sociales.

Comunicaciones integradas

   correo;
   WhatsApp;
   SMS;
   telefonía;
   videollamadas;
   chat en vivo.

Operación avanzada

   workflows configurables;
   reglas de automatización;
   aprobaciones;
   escalamiento;
   calendarios externos;
   notificaciones externas.

Datos y personalización

   campos personalizados;
   módulos personalizados;
   importaciones masivas;
   exportaciones masivas;
   deduplicación automática;
   enriquecimiento de datos;
   archivos adjuntos.
Plataforma comercial

    multitenancy;
    suscripciones;
    facturación;
    pagos;
    marketplace;
    administración de planes;
    personalización por organización.

Inteligencia artificial

    generación de mensajes;
    resúmenes automáticos;
    clasificación;
    scoring;
    predicciones;
    agentes autónomos;
    recomendaciones;
    análisis de sentimiento.

Infraestructura innecesaria

    microservicios;
    Kafka;
    Redis;
    Kubernetes;
    service mesh;
    arquitectura multirregión.




15. Reglas de negocio provisionales

RB-01

Un cliente archivado no aparece en la lista activa por
defecto.

RB-02

Archivar un cliente no elimina sus interacciones ni
seguimientos.
RB-03

Un cliente archivado puede restaurarse.

RB-04

Una interacción siempre pertenece a un cliente.

RB-05

Un seguimiento siempre pertenece a un cliente.

RB-06

Un seguimiento pendiente tiene una responsabilidad visible.

RB-07

Completar un seguimiento conserva su información.

RB-08

Cancelar un seguimiento conserva su información y estado.

RB-09

No habrá eliminación destructiva disponible desde la
interfaz inicial.

RB-10

Development Preview utiliza únicamente identidades y
datos ficticios.

RB-11

Ninguna identidad demostrativa representa seguridad o
autorización.

RB-12

Antes del piloto, toda acción que consulte o modifique
datos requerirá control de acceso.

Estas reglas deberán convertirse posteriormente en
escenarios verificables.
16. Límites de información

La primera versión podrá trabajar conceptualmente con:

Perfil de cliente

    identidad;
    información de contacto;
    organización o contexto comercial opcional;
    estado;
    notas generales limitadas;
    fechas relevantes.

Interacción

    cliente;
    tipo;
    momento;
    resumen;
    autor;
    metadatos.

Seguimiento

    cliente;
    descripción;
    responsable;
    fecha límite;
    estado;
    fecha de finalización;
    metadatos.

Esta sección no define todavía tablas, nombres de campos
ni tipos de datos.




17. Calidad mínima

Comprensibilidad

El usuario debe poder identificar:
    qué está viendo;
    qué acción puede realizar;
    si la acción funcionó;
    cómo recuperarse de un error.

Accesibilidad

El recorrido principal deberá ser utilizable mediante teclado
y no depender exclusivamente del color.

Integridad

La aplicación no deberá perder datos por una navegación
normal o reinicio controlado.

Validación

Frontend y backend deberán validar en sus respectivas
fronteras.

El backend será la autoridad final.

Seguridad de la etapa

Development Preview no podrá exponerse como servicio
público con datos reales.

Trazabilidad

Los registros deberán conservar metadatos suficientes
para comprender cuándo fueron creados y actualizados.

Mantenibilidad

El código deberá respetar la arquitectura definida
posteriormente y contar con verificaciones automatizadas
acordes con cada etapa.

Observabilidad mínima

La aplicación deberá permitir detectar:

    si backend está disponible;
    si la base de datos está disponible;
    si una operación falla;
    qué clase de error ocurrió sin exponer secretos.




18. Matriz de trazabilidad

Necesidad provisional         Capacidad

Encontrar al cliente           listado, búsqueda y detalle


Comprender el contexto         perfil e historial


Registrar lo ocurrido          interacciones


Saber qué sigue                seguimientos


Conocer responsabilidad        asignación


Evitar olvidos                 vista de pendientes


Mantener continuidad           historial compartido


Evitar pérdida destructiva     archivo y restauración




19. Condiciones de aceptación de
Development Preview

[GATE]


La Development Preview estará completa cuando:

1. el recorrido central funcione de extremo a extremo;
2. frontend, backend y base de datos estén integrados;
3. los datos persistan;
4. sea posible crear y encontrar un cliente;
5. sea posible registrar y consultar una interacción;
6. sea posible crear, consultar y completar un
    seguimiento;
7. sea posible archivar y restaurar;
8. los estados de error principales sean comprensibles;
9. las validaciones principales estén presentes;
10. existan pruebas automatizadas para el recorrido
    crítico;
11. no se utilicen datos reales;
12. no se presente como producción;
13. el código pueda levantarse mediante comandos
    documentados;
14. no haya secretos versionados;
15. la documentación coincida con el comportamiento.




20. Condiciones adicionales del Pilot
Candidate

 [GATE]


Antes de ser Pilot Candidate deberá incluir:

    autenticación;
    autorización;
    administración básica de usuarios;
    aislamiento del espacio de trabajo;
    HTTPS;
    configuración segura;
    secretos externos al repositorio;
    revisión de privacidad;
    política de respaldo;
    estrategia de recuperación;
    registro operativo;
    monitoreo;
    gestión de errores;
    pruebas de seguridad;
    accesibilidad revisada;
    términos de uso del piloto;
    canal de soporte;
    procedimiento para corregir y eliminar datos.




21. Hipótesis principales

H-SCOPE-01
El recorrido cliente → interacción → seguimiento resuelve
una parte valiosa del problema.

H-SCOPE-02

Un historial sencillo puede producir valor sin pipeline de
ventas.

H-SCOPE-03

La vista de pendientes será más útil inicialmente que un
dashboard analítico.

H-SCOPE-04

El archivo reversible es suficiente sin eliminación
destructiva inicial.

H-SCOPE-05

Un conjunto reducido de datos puede sostener la
coordinación.

H-SCOPE-06

Los usuarios aceptarán registrar interacciones si el proceso
es corto.

H-SCOPE-07

La asignación visible reduce dependencia de memoria
personal.

Estas hipótesis deben relacionarse con investigación futura.




22. Riesgos

R-01 — Construir sin evidencia

Mitigación: conservar etiquetas de hipótesis y actualizar el
alcance después de investigar.

R-02 — Convertir el CRM en agenda de
contactos
Mitigación: exigir interacción, seguimiento e historial.

R-03 — Sobrecargar el registro

Mitigación: minimizar campos obligatorios y probar el flujo.

R-04 — Añadir funciones por comparación
comercial

Mitigación: toda capacidad debe vincularse con una
necesidad.

R-05 — Tratar Development Preview como
producción

Mitigación: prohibir datos reales y documentar gates.

R-06 — Confundir identidades demostrativas
con seguridad

Mitigación: reemplazarlas antes del piloto.

R-07 — Crecimiento descontrolado

Mitigación: aplicar MoSCoW y retirar Could Have primero.

R-08 — Eliminar accidentalmente el curso

Mitigación: no fusionar la rama del proyecto hacia main .




23. Control de cambios

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

Añadir una capacidad sin retirar o replanificar otra se
considera crecimiento de alcance.




24. Preguntas abiertas

    ¿El concepto principal debe ser cliente, contacto o
    relación?
    ¿Deben distinguirse personas y organizaciones?
    ¿Puede una organización tener varios contactos?
    ¿Qué tipos de interacción reconocen los usuarios?
    ¿Qué datos identifican suficientemente a un cliente?
    ¿Qué información es obligatoria?
    ¿Qué significa archivar para cada negocio?
    ¿Quién puede restaurar?
    ¿Deben poder corregirse interacciones?
    ¿Se necesita una razón de cancelación?
    ¿Qué ventana temporal define “próximo”?
    ¿Qué dispositivos son prioritarios?
    ¿Qué datos consideran sensibles?
    ¿Qué permisos necesita cada rol?

Estas preguntas no deben resolverse por intuición cuando
puedan investigarse.




25. Estado

    Visión: definida provisionalmente.
    Usuarios: provisionales.
    Investigación ejecutada: pendiente.
    Recorrido central: definido.
    Development Preview: delimitada.
    Pilot Candidate: delimitado.
    Must Have: definidos.
    Should Have: definidos.
    Could Have: definidos.
    Won’t Have: definidos.
    Arquitectura: pendiente.
             Stack: pendiente.
             OpenSpec: pendiente.
             Implementación: no iniciada.




14. Contenido de release-strategy.md

   Edit




          Estrategia de versiones y
          validación — CRM Profesional

            Estado: estrategia inicial
            Fecha: 2026-07-28
            Fase: Módulo 1 — Definición del producto
            Rama actual: docs/module-1-product-discovery
            Producción autorizada: no
            Uso de datos reales autorizado: no




          1. Propósito

          Este documento define cómo CRM Profesional avanzará
          desde documentación hasta una aplicación de producción
          sin confundir progreso técnico con validación de producto.

          La estrategia busca:

             aprender antes de ampliar;
             mantener versiones pequeñas;
             evitar datos reales prematuros;
             establecer gates verificables;
             permitir retroceder;
             separar demostración, piloto y producción;
             conservar trazabilidad entre evidencia, alcance,
             especificaciones y código.
2. Política de ramas

main

Contiene exclusivamente el material del curso.

docs/module-1-product-discovery

Contiene el proyecto CRM Profesional en su fase actual.

Reglas obligatorias

   no fusionar la rama del CRM hacia main ;
   no abrir pull requests del CRM hacia main ;
   no fusionar main dentro de la rama del CRM;
   no recuperar los módulos en la rama del CRM;
   verificar la rama antes de cada commit;
   crear copias remotas frecuentes;
   revisar cualquier operación destructiva.

Antes de iniciar implementación se evaluará si la rama
debe renombrarse a una línea permanente como
project/crm-profesional .


Ese cambio no se realizará durante este paso.




3. Principio de liberación

  Cada etapa debe responder una pregunta distinta.


No se avanza porque “ya escribimos suficiente código”.

Se avanza cuando existe evidencia para responder la
pregunta de la etapa.




4. Etapa 0 — Descubrimiento

Pregunta
¿Comprendemos suficientemente el problema y sus
usuarios?

Artefactos

    visión;
    plan de investigación;
    alcance;
    estrategia de versiones;
    hipótesis;
    preguntas abiertas.

Datos

No se recopilan datos operativos dentro del producto.

Gate de salida

    problema claramente formulado;
    usuarios provisionales identificados;
    hipótesis registradas;
    recorrido central definido;
    no objetivos acordados;
    plan para conseguir evidencia.

Estado

En progreso.




5. Etapa 1 — Definición con OpenSpec

Pregunta

¿Podemos describir el comportamiento deseado de manera
inequívoca y verificable?

Actividades

    crear especificaciones;
    definir escenarios;
    definir criterios de aceptación;
    identificar edge cases;
    establecer restricciones;
    revisar dependencias;
    dividir el trabajo.

Salidas

    especificaciones aprobadas;
    plan de implementación;
    tareas verificables;
    trazabilidad con scope.md .

Gate de salida

    cada Must Have necesario para el primer recorrido
    tiene especificación;
    los escenarios incluyen errores y estados vacíos;
    no existen contradicciones conocidas;
    las decisiones abiertas críticas están resueltas;
    existe criterio para comprobar cada comportamiento.




6. Etapa 2 — Development Preview

Pregunta

¿Puede el sistema completar el recorrido central mediante
el stack real?

Audiencia

    equipo de desarrollo;
    revisores;
    demostraciones internas.

Capacidades

    clientes;
    búsqueda;
    interacciones;
    seguimientos;
    vista de trabajo;
    archivo y restauración;
    persistencia;
    validación;
    manejo de errores.

Datos

Solo ficticios o sintéticos.

Entorno

    local;
    contenedor aislado;
    entorno de demostración restringido.

Prohibiciones

    datos reales;
    acceso público;
    promesas de producción;
    tratamiento de información sensible;
    integraciones externas reales.

Gate de salida

    recorrido crítico completado;
    pruebas principales verdes;
    persistencia verificada;
    instrucciones reproducibles;
    secretos ausentes;
    errores principales manejados;
    revisión técnica realizada.




7. Etapa 3 — Evaluación con prototipo o
Preview

Pregunta

¿Las personas comprenden el modelo del producto y
pueden completar las tareas?

Métodos

    pruebas moderadas;
    observación;
    entrevistas de seguimiento;
    análisis de errores;
    medición de tareas;
    revisión de terminología.

Datos

Casos de prueba ficticios.

Tareas mínimas

1. encontrar un cliente;
2. interpretar su contexto;
3. registrar una interacción;
4. crear un seguimiento;
5. encontrarlo posteriormente;
6. completarlo;
7. archivar y restaurar.

Gate de salida

    problemas críticos identificados;
    terminología revisada;
    necesidades actualizadas;
    alcance corregido;
    decisiones documentadas.

Esta etapa puede provocar volver a OpenSpec antes de
continuar.




8. Etapa 4 — Pilot Candidate

Pregunta

¿El sistema está suficientemente protegido y operable para
una prueba limitada?

Capacidades obligatorias adicionales

    autenticación;
    autorización;
    usuarios;
    aislamiento de datos;
    configuración segura;
    HTTPS;
    respaldos;
    restauración;
    monitoreo;
    logs;
    manejo de secretos;
    procedimiento de soporte;
    revisión de privacidad;
    accesibilidad revisada.

Datos

Preferiblemente ficticios durante la preparación.

Los datos reales solo podrán introducirse después de
aprobar el gate del piloto.

Gate de salida

    revisión de seguridad aprobada;
    pruebas automatizadas aprobadas;
    procedimiento de respaldo probado;
    procedimiento de restauración probado;
    acceso no autorizado verificado;
    errores no exponen secretos;
    responsables operativos identificados;
    participantes y consentimiento definidos;
    canal de soporte preparado.




9. Etapa 5 — Piloto controlado

Pregunta

¿El producto aporta valor en condiciones reales y
controladas?

Audiencia

Un grupo pequeño y expresamente autorizado.

Condiciones
   alcance limitado;
   duración definida;
   soporte directo;
   monitoreo activo;
   mecanismo de reporte;
   capacidad de detener el piloto;
   política de datos comunicada;
   participantes informados.

Métricas de aprendizaje

   tareas completadas;
   tiempo para encontrar contexto;
   seguimientos identificados;
   registros abandonados;
   errores;
   necesidad de soporte;
   confianza percibida;
   razones para no utilizar el sistema.

Regla

Una métrica de actividad no demuestra valor por sí sola.

Gate de salida

   evidencia de utilidad;
   riesgos aceptables;
   errores críticos resueltos;
   privacidad y soporte sostenibles;
   decisión explícita de continuar, cambiar o detener.




10. Etapa 6 — Producción inicial

Pregunta

¿Podemos operar el producto de forma confiable y
responsable?

Requisitos

   organización responsable;
    soporte;
    monitoreo;
    copias de seguridad;
    recuperación;
    seguridad;
    actualización;
    documentación;
    gestión de incidentes;
    gestión de vulnerabilidades;
    política de retención;
    derechos sobre datos;
    accesibilidad;
    despliegue repetible;
    rollback probado.

Gate de salida

La producción no se declara automáticamente.

Requiere una decisión formal basada en evidencia técnica,
operativa, legal y de producto.




11. Priorización

Se utilizará MoSCoW para el alcance de cada etapa.

Must Have

Sin la capacidad, el objetivo de la etapa no puede
cumplirse.

Should Have

La ausencia reduce significativamente el valor, pero existe
una alternativa temporal.

Could Have

Aporta valor, pero no compromete el objetivo si se aplaza.

Won’t Have for Now

No se incluirá en la etapa.
Regla de descope

Cuando el tiempo o la complejidad crezcan:

1. retirar Could Have;
2. aplazar Should Have que tengan alternativa;
3. conservar Must Have;
4. reducir la amplitud del escenario;
5. nunca degradar seguridad necesaria para la etapa.




12. Unidad de entrega

La unidad preferida será una capacidad vertical verificable.

Ejemplo:

Crear seguimiento
├── comportamiento definido
├── interfaz
├── API
├── persistencia
├── validación
├── errores
├── pruebas
└── documentación

No se considerará completa una capacidad cuando solo
exista en una capa.




13. Definition of Done general

Una capacidad estará terminada cuando:

    cumple la especificación vigente;
    incluye comportamiento de éxito;
    incluye errores relevantes;
    incluye validación;
    cuenta con pruebas adecuadas;
    no rompe pruebas existentes;
    no contiene secretos;
    no introduce dependencias sin justificar;
    mantiene accesibilidad del flujo;
    actualiza documentación cuando corresponde;
    fue revisada;
    puede demostrarse;
    no deja trabajo crítico oculto.

La Definition of Done específica se perfeccionará cuando el
stack sea elegido.




14. Criterios de parada

El proyecto deberá detener o replantear una etapa cuando:

    la investigación contradiga el problema central;
    los usuarios no perciban valor;
    el registro introduzca más carga que beneficio;
    el producto requiera datos cuyo tratamiento no pueda
    justificarse;
    el alcance dependa de capacidades excluidas;
    los riesgos de seguridad no puedan controlarse;
    el equipo no pueda operar el sistema;
    una solución existente resuelva mejor el problema;
    la complejidad exceda el aprendizaje esperado.

Detenerse o cambiar no se considera fracaso.

Se considera una decisión basada en evidencia.




15. Criterios de rollback

Toda liberación posterior a Development Preview deberá
contar con:

    versión anterior identificable;
    artefacto reproducible;
    migraciones reversibles o procedimiento documentado;
    respaldo previo;
    validación posterior;
    responsable de decidir el rollback;
    comunicación del incidente.
Las migraciones destructivas requerirán precauciones
adicionales.




16. Datos por ambiente

Desarrollo local

    datos sintéticos;
    secretos locales ignorados;
    base reemplazable.

Integración y pruebas

    datos generados;
    entorno aislado;
    limpieza automatizada.

Demostración

    datos ficticios;
    acceso restringido;
    reinicio posible.

Piloto

    datos autorizados;
    acceso controlado;
    respaldo;
    monitoreo;
    retención definida.

Producción

    datos reales;
    controles completos;
    responsabilidades contractuales y legales;
    auditoría operativa.




17. Validación por etapa

Descubrimiento
Validar problema y usuarios.

OpenSpec

Validar claridad y consistencia.

Development Preview

Validar integración técnica.

Evaluación de uso

Validar comprensión y usabilidad.

Pilot Candidate

Validar seguridad y operación.

Piloto

Validar valor real.

Producción

Validar sostenibilidad.




18. Métricas iniciales

No se fijarán objetivos numéricos definitivos sin una línea
base.

Se observarán:

Resultado de usuario

    éxito al encontrar clientes;
    éxito al comprender contexto;
    éxito al registrar interacciones;
    éxito al crear y completar seguimientos.

Esfuerzo

    pasos;
    tiempo;
    errores;
   solicitudes de ayuda;
   abandonos.

Calidad

   fallos;
   datos inválidos;
   duplicados;
   recuperaciones;
   incidencias.

Adopción futura

   usuarios activos;
   interacciones registradas;
   seguimientos gestionados;
   recurrencia;
   razones de abandono.




19. Evidencia necesaria para cambiar el
alcance

Una propuesta deberá incluir:

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


Las peticiones de funcionalidades se registrarán, pero no
entrarán automáticamente.




20. Registro de decisiones

Las decisiones importantes deberán conservar:
    fecha;
    contexto;
    opciones;
    elección;
    razón;
    consecuencias;
    evidencia;
    estado.

Los ADR técnicos se introducirán cuando corresponda.

Las decisiones de producto permanecerán en la
documentación de producto.




21. Estrategia de demostración

Cada demostración deberá mostrar un recorrido, no una
colección de pantallas.

Demostración mínima:

1. abrir la vista de trabajo;
2. localizar un cliente;
3. consultar su historial;
4. registrar una interacción;
5. crear un seguimiento;
6. encontrar el seguimiento;
7. completarlo;
8. comprobar que permanece en el historial.




22. Estrategia de feedback

Cada sesión deberá distinguir:

    observación;
    declaración;
    interpretación;
    decisión.

No se preguntará únicamente:
¿Te gusta?


Se observará:

    qué intenta hacer;
    dónde duda;
    qué espera;
    qué interpreta;
    qué omite;
    qué error comete;
    qué resultado obtiene.




23. Estrategia de documentación

Cada etapa deberá mantener:

    alcance vigente;
    especificaciones vigentes;
    decisiones;
    instrucciones de ejecución;
    restricciones;
    riesgos;
    notas de versión;
    cambios incompatibles;
    pendientes conocidos.

La documentación debe describir el sistema real, no la
intención antigua.




24. Preparación para OpenSpec

El Módulo 2 deberá transformar este alcance en
especificaciones para:

    clientes;
    búsqueda;
    archivo y restauración;
    interacciones;
    seguimientos;
    vista de trabajo;
               validaciones;
               errores;
               persistencia.

            Cada especificación deberá enlazar:

            Necesidad
            → capacidad
            → escenarios
            → implementación
            → pruebas




            25. Estado

               Descubrimiento: en progreso.
               Alcance inicial: definido.
               Estrategia de versiones: definida.
               OpenSpec: pendiente.
               Development Preview: pendiente.
               Pilot Candidate: pendiente.
               Piloto: no autorizado.
               Producción: no autorizada.
               Datos reales: no autorizados.




15. Verificar los cambios
Cuando Claude termine:


     Bash

  git status --short


Esperado:


  ?? proyecto-crm-profesional/docs/product/scope.md
  ?? proyecto-crm-profesional/docs/product/release-strategy.md


Git puede agruparlos como directorio dependiendo del estado.
Lista todos los archivos del proyecto:


       Bash

  find proyecto-crm-profesional -type f -print


Deben existir exactamente cuatro:


  proyecto-crm-profesional/docs/product/vision.md
  proyecto-crm-profesional/docs/product/user-research-plan.md
  proyecto-crm-profesional/docs/product/scope.md
  proyecto-crm-profesional/docs/product/release-strategy.md


Cuenta:


       Bash

  find proyecto-crm-profesional -type f | wc -l


Resultado:


  4


Comprueba que no reaparecieron módulos:


       Bash

  git ls-tree -d --name-only HEAD | grep '^Módulo_'


Sin salida.

Comprueba que Claude no modificó los documentos anteriores:


       Bash

  git diff -- \
      proyecto-crm-profesional/docs/product/vision.md \
      proyecto-crm-profesional/docs/product/user-research-plan.md


Sin salida.

Revisa los nuevos documentos:


       Bash

  sed -n '1,120p' proyecto-crm-profesional/docs/product/scope.md
  tail -n 60 proyecto-crm-profesional/docs/product/scope.md
  sed -n '1,120p' proyecto-crm-profesional/docs/product/release-strategy.md
  tail -n 60 proyecto-crm-profesional/docs/product/release-strategy.md

Busca tecnologías o código introducidos indebidamente:


     Bash

  grep -RniE \
    'class |interface |@Entity|@RestController|CREATE TABLE|package.json|pom.xml|docker-com
    proyecto-crm-profesional/docs/product


No debería encontrar diseño técnico.




16. Revisión humana
Confirma:


  [ ] Continúo en docs/module-1-product-discovery.
  [ ] Los módulos no existen en esta rama.
  [ ] Los módulos siguen existiendo en origin/main.
  [ ] No se fusionó main.
  [ ] Solo se crearon dos archivos.
  [ ] El recorrido central es end-to-end.
  [ ] El producto no es solamente un CRUD de clientes.
  [ ] Development Preview no se presenta como producción.
  [ ] Se prohíben datos reales en Development Preview.
  [ ] Autenticación es obligatoria antes del piloto.
  [ ] Must, Should, Could y Won’t están separados.
  [ ] No se diseñaron endpoints ni tablas.
  [ ] No se seleccionó definitivamente el stack.
  [ ] No se añadieron funciones por imitar otros CRM.
  [ ] Existe un gate verificable para cada etapa.




17. Commit y respaldo remoto
Añade únicamente los nuevos archivos:


     Bash

  git add -- \
    proyecto-crm-profesional/docs/product/scope.md \
    proyecto-crm-profesional/docs/product/release-strategy.md


Verifica:
     Bash

  git diff --cached --name-only
  git diff --cached --check
  git diff --cached --stat


git diff --cached --check no debe mostrar errores.


Commit:


     Bash

  git commit -m "docs: define CRM scope and release strategy"


Envía a la misma rama:


     Bash

  git push origin docs/module-1-product-discovery


No abras un pull request hacia main .

Comprueba:


     Bash

  git status --short --branch
  git log -2 --oneline


El árbol debe quedar limpio.




18. Qué aprendimos en este paso
Visión no es alcance

  Visión
  ¿Por qué existe?




  Alcance
  ¿Qué resolverá esta etapa?



Alcance no es especificación
  Alcance:
  El usuario puede crear un seguimiento.




  Especificación futura:
  Qué campos recibe, qué estados existen,
  qué errores devuelve y qué escenarios debe pasar.



MVP no significa producto descuidado

  Mínimo
  =
  menor alcance coherente


No significa:


  sin validación
  sin seguridad
  sin pruebas
  sin manejo de errores



Un CRUD no es todavía el producto

  CRUD de clientes
  =
  almacenar registros




  CRM inicial
  =
  cliente
  +
  contexto
  +
  interacción
  +
  seguimiento
  +
  continuidad




19. Criterios de finalización del Paso 3

  [ ] scope.md existe.
  [ ] release-strategy.md existe.
 [ ] Solo hay cuatro archivos en el proyecto.
 [ ] main conserva el curso.
 [ ] La rama del CRM no contiene módulos.
 [ ] No se abrió PR hacia main.
 [ ] El recorrido funcional central está definido.
 [ ] Development Preview está diferenciada del piloto.
 [ ] Está prohibido utilizar datos reales en Preview.
 [ ] Must, Should, Could y Won’t están documentados.
 [ ] Los no objetivos están explícitos.
 [ ] Existen gates de liberación.
 [ ] Existe Definition of Done general.
 [ ] No existe código.
 [ ] El commit fue creado.
 [ ] La rama remota fue actualizada.
 [ ] El árbol de trabajo quedó limpio.

¿Deseas continuar con el Paso 4 de 18: elegir y justificar
profesionalmente la arquitectura y la base tecnológica del CRM,
verificando compatibilidad y versiones vigentes hasta julio de 2026?




                         ChatGPT can make mistakes. Check important info.
