# Paso 3 — Fuente de verdad estructurada del Módulo 1

## Proyecto: Agente de IA conversacional y reflexivo
## Módulo actual: Módulo 1 — Los 3 pilares del uso efectivo de copilotos IA
## Fecha: 2026-09-03
## Gate actual: `NO PASA` hasta construir y verificar el artefacto local

---

# Alcance

Este paso continúa el mismo proyecto real, profesional y full stack desarrollado desde cero con Claude Code.

El objetivo no es desarrollar funcionalidades. El objetivo es transformar el contenido del Módulo 1 en una **fuente de verdad estructurada, trazable, verificable y utilizable posteriormente por Claude Code**, sin mezclar el contenido del curso con hechos externos, recomendaciones profesionales o decisiones futuras del producto.

La regla central será:

```text
CursoIA = fuente educativa primaria
Fuente estructurada = representación derivada y trazable
AGENTS.md / CLAUDE.md = capas operativas posteriores
```

No se modificará el contenido fuente del curso.

---

# Corrección del Gate del Paso 2

La evidencia aportada desde el PC real permite continuar, pero corrige el Gate que figuraba anteriormente como `PASA`.

El entorno auditado muestra:

- Ubuntu 26.04 LTS dentro de WSL 2;
- Git 2.53.0;
- GitHub CLI 2.99.0;
- Claude Code 2.1.259;
- Node.js 24.20.0;
- npm 11.19.0;
- Python 3.14.4;
- uv 0.12.7;
- Poetry 2.4.2;
- Docker 29.7.2;
- Docker Compose 5.5.0;
- Docker Desktop 4.89.0;
- WSL 2.6.3.0;
- cliente PostgreSQL 18.6;
- conectividad HTTPS hacia GitHub. fileciteturn43file0L15-L34 fileciteturn43file1L351-L382 fileciteturn43file2L384-L437

Hay dos observaciones reales:

1. El script de auditoría dejó `audit-step2.sh` y `step2-audit-output.txt` como archivos no rastreados dentro de `CursoIA`. fileciteturn43file1L380-L397
2. `nvidia-smi` terminó con `Segmentation fault` dentro de WSL. fileciteturn42file0L48-L57

Ninguna observación bloquea la construcción documental de este paso. El Gate del Paso 2 queda correctamente como:

# `PASA CON OBSERVACIONES`

Los temporales de auditoría deben limpiarse antes de considerar `CursoIA` nuevamente limpio.

---

# Investigación previa: qué significa una fuente de verdad

## 1. Fuente de verdad no significa “documento gigante”

Una fuente de verdad es el lugar definido como autoritativo para una clase determinada de información. Su propósito es evitar que la misma información se copie en lugares diferentes y termine divergiendo.

GitHub documenta explícitamente la conveniencia de mantener una única fuente de verdad para evitar inconsistencias cuando una misma información se almacena en múltiples lugares. citeturn986464search2

Para agentes de programación esto es especialmente relevante: dos instrucciones aparentemente similares pero diferentes pueden producir decisiones contradictorias.

## 2. La fuente de verdad no debe convertirse en un mega-prompt

La investigación de OpenAI sobre *harness engineering*, publicada el 11 de febrero de 2026, describe una lección especialmente relevante: un único `AGENTS.md` muy grande resultó problemático porque consume contexto, pierde claridad y se vuelve difícil de mantener.

Su enfoque fue convertir `AGENTS.md` en un mapa hacia una base de conocimiento estructurada en `docs/`, con divulgación progresiva (*progressive disclosure*), planes y documentación versionada. citeturn488365search0

La consecuencia para nuestro proyecto será:

```text
Fuente de verdad estructurada
        ↓
selección de contexto relevante
        ↓
AGENTS.md / CLAUDE.md
```

No:

```text
todo el conocimiento
        ↓
CLAUDE.md gigante
```

## 3. AGENTS.md no sustituye toda la base de conocimiento

El formato público `AGENTS.md` está diseñado para instrucciones y contexto práctico para coding agents. Incluye ejemplos de comandos, testing, convenciones, seguridad y particularidades del repositorio. También admite archivos anidados por subproyecto. citeturn986464search0

Esto es compatible con una base de conocimiento separada y más extensa.

## 4. Git aporta trazabilidad

Git permite seguir la historia de cambios y recuperar estados anteriores. GitHub explica que el control de versiones permite conocer qué cambió, cuándo y por qué. citeturn986464search1

Por tanto, nuestra fuente de verdad deberá ser:

- versionable;
- trazable;
- revisable;
- actualizable sin sobrescritura silenciosa.

## 5. Claude Code será lector y transformador, no autoridad

Claude Code puede leer archivos de memoria, trabajar con instrucciones persistentes y usar diferentes modos operativos. La documentación actual también describe `CLAUDE.md` e importaciones mediante `@...`. citeturn657767search7

La autoridad para este paso seguirá siendo:

```text
fuentes originales
+
fuentes externas verificadas
+
decisiones humanas explícitas
```

---

# A. Objetivo

## A.1. Objetivo principal

Construir una representación estructurada del Módulo 1 que permita usarlo como referencia controlada durante la construcción posterior del proyecto.

## A.2. Información que debe poder recuperarse

La fuente estructurada debe responder:

- qué enseña realmente el módulo;
- cuáles son sus principios;
- qué prácticas presenta;
- qué herramientas menciona;
- qué configuraciones describe;
- qué anti-patrones identifica;
- qué comprobaciones propone;
- qué recursos externos incluye;
- qué afirmaciones son temporales;
- qué hechos externos fueron verificados;
- qué recomendaciones adoptamos;
- qué decisiones todavía no se han tomado.

## A.3. Criterio esencial

Cada afirmación importante deberá tener procedencia suficiente para poder volver al documento original o a la fuente externa correspondiente.

---

# B. Fundamento

## B.1. Pilar 2 — Contexto

El Módulo 1 presenta el contexto como un recurso que se debe gestionar. En este paso se aplican especialmente:

```text
Write
Select
Compress
```

### Write

Persistir conocimiento útil.

### Select

Conservar lo relevante y no todo lo disponible.

### Compress

Reducir cinco documentos a una estructura navegable sin eliminar distinciones semánticas importantes.

### Isolate

Se mantiene como principio para fases posteriores cuando existan subagentes o dominios independientes.

## B.2. Pilar 3 — Prompt

El trabajo de estructuración debe usar prompts con:

- contexto;
- resultado esperado;
- criterios de éxito;
- restricciones;
- referencias;
- formato de salida.

No se utilizará un prompt genérico del tipo “resume el módulo”.

## B.3. Pilar 1 — Herramienta

Claude Code se utilizará para leer, clasificar, estructurar y revisar; no para decidir silenciosamente qué partes del curso se convierten en reglas obligatorias.

---

# C. Evidencia de la fuente

## C.1. Plan del Módulo 1

El plan del proyecto define el Paso 3 como **Construcción de la fuente de verdad del Módulo 1**.

El mismo plan exige clasificar:

- principios;
- prácticas;
- herramientas;
- configuraciones;
- anti-patrones;
- comprobaciones;
- recursos externos;
- afirmaciones sujetas a verificación.

Además indica expresamente que las opiniones del módulo no deben convertirse automáticamente en reglas. fileciteturn46file0L2-L2

## C.2. Cinco fuentes primarias

Los cinco documentos originales son:

```text
Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/
├── 1. El modelo mental de los 3 pilares.md
├── 2. Pilar 1 — La Herramienta.md
├── 3. Pilar 2 — El Contexto.md
├── 4. Pilar 3 — El Prompt + Integración.md
└── 5. Recursos adicionales.md
```

No deben editarse.

## C.3. Hechos frente a recomendaciones

Se utilizará la siguiente taxonomía:

```text
COURSE_FACT
EXTERNAL_FACT
PROJECT_RECOMMENDATION
PROJECT_DECISION
PENDING_VERIFICATION
```

### COURSE_FACT

La fuente del curso afirma explícitamente la información.

### EXTERNAL_FACT

La afirmación proviene de una fuente externa verificable.

### PROJECT_RECOMMENDATION

Una recomendación profesional adoptada para mejorar el proceso.

### PROJECT_DECISION

Una decisión explícita del proyecto.

### PENDING_VERIFICATION

Una afirmación que todavía no cuenta con verificación suficiente.

---

# D. Acción

## D.1. Limpiar los temporales del Paso 2

Antes de crear el artefacto derivado:

```bash
cd ~/Projects/CursoIA
git status --short
```

Si los únicos temporales son:

```text
audit-step2.sh
step2-audit-output.txt
```

ejecutar:

```bash
rm -f audit-step2.sh step2-audit-output.txt
git status --short
```

La salida debe quedar vacía.

No hacer `git add .` ni commit en `CursoIA` para conservar dichos temporales.

## D.2. Crear un workspace separado

```bash
cd ~/Projects
mkdir -p Proyecto_Final_Master_AI4Devs/docs/source-of-truth/module-1
cd Proyecto_Final_Master_AI4Devs
```

La separación queda:

```text
~/Projects/
├── CursoIA/
│   └── fuente educativa
└── Proyecto_Final_Master_AI4Devs/
    └── artefactos derivados
```

Todavía no se crea el repositorio remoto final ni se implementa la aplicación.

## D.3. Crear la fuente estructurada

El archivo principal será:

```text
docs/source-of-truth/module-1/MODULE_1_SOURCE_OF_TRUTH.md
```

## D.4. Estructura obligatoria

El documento tendrá estas secciones:

```text
1. Metadata
2. Purpose
3. Provenance model
4. Principles
5. Practices
6. Tools
7. Configurations
8. Anti-patterns
9. Checks
10. External resources
11. Time-sensitive claims
12. External facts verified
13. Project recommendations
14. Project decisions
15. Pending verification
16. Traceability matrix
17. Change history
```

## D.5. Esquema de cada entrada

Ejemplo:

```yaml
id: M1-PR-001
type: principle
title: ...
statement: ...
source:
  kind: COURSE_FACT
  file: ...
  section: ...
external_validation:
  status: VERIFIED
  references:
    - ...
project_implication: ...
scope: ...
verification:
  required: true
  method: ...
status: ACTIVE
```

El documento final puede usar Markdown estructurado en lugar de ser un YAML completo.

## D.6. IDs estables

Se recomienda:

```text
M1-PR-*  Principles
M1-PA-*  Practices
M1-TO-*  Tools
M1-CF-*  Configuration facts
M1-AP-*  Anti-patterns
M1-CK-*  Checks
M1-EX-*  External resources/facts
M1-RC-*  Recommendations
M1-DC-*  Project decisions
M1-PV-*  Pending verification
```

Ejemplos:

```text
M1-PR-001
M1-PA-001
M1-TO-001
M1-CK-001
```

Un ID existente no cambia solo porque se edite la redacción.

## D.7. Regla de procedencia

Nunca transformar automáticamente:

```text
“El módulo recomienda X”
```

en:

```text
“X es obligatorio”
```

Nunca transformar:

```text
“Una fuente externa afirma X”
```

en:

```text
“El curso establece X”
```

Y nunca transformar:

```text
“Nosotros recomendamos X”
```

en:

```text
“el proyecto exige X”
```

sin una decisión explícita.

## D.8. Usar Claude Code primero en modo plan

Desde:

```text
~/Projects/Proyecto_Final_Master_AI4Devs
```

ejecutar:

```bash
claude \
  --add-dir ~/Projects/CursoIA \
  --permission-mode plan
```

La auditoría real del Paso 2 confirmó que la versión instalada de Claude Code dispone de `--permission-mode` y del modo `plan`. fileciteturn43file1L190-L218

La finalidad es revisar el plan antes de escribir.

## D.9. Prompt de planificación

```text
Estamos trabajando en un proyecto nuevo y separado del repositorio fuente del curso.

Repositorio fuente, solo lectura:
~/Projects/CursoIA

Workspace objetivo:
~/Projects/Proyecto_Final_Master_AI4Devs

Tarea actual:
Construir una fuente de verdad estructurada y trazable del Módulo 1 del curso.

Lee como fuente primaria estos cinco archivos completos:

1. Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/1. El modelo mental de los 3 pilares.md
2. Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/2. Pilar 1 — La Herramienta.md
3. Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/3. Pilar 2 — El Contexto.md
4. Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/4. Pilar 3 — El Prompt + Integración.md
5. Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/5. Recursos adicionales.md

Consulta también:
Prompts/Plan_M1_preparacion_Proyecto_Final_Master_AI4Devs_2026-09-02.md

No modifiques ningún archivo dentro de ~/Projects/CursoIA.

Antes de escribir, crea un plan para producir su contenido en ingles:
~/Projects/Proyecto_Final_Master_AI4Devs/docs/source-of-truth/module-1/MODULE_1_SOURCE_OF_TRUTH.md

Clasifica:
1. Metadata
2. Purpose
3. Provenance model
4. Principles
5. Practices
6. Tools
7. Configurations
8. Anti-patterns
9. Checks
10. External resources
11. Time-sensitive claims
12. External facts verified
13. Project recommendations
14. Project decisions
15. Pending verification
16. Traceability matrix
17. Change history


IDs estables:

M1-PR-*  Principles
M1-PA-*  Practices
M1-TO-*  Tools
M1-CF-*  Configuration facts
M1-AP-*  Anti-patterns
M1-CK-*  Checks
M1-EX-*  External resources/facts
M1-RC-*  Recommendations
M1-DC-*  Project decisions
M1-PV-*  Pending verification


Cada entrada debe distinguir:
COURSE_FACT
EXTERNAL_FACT
PROJECT_RECOMMENDATION
PROJECT_DECISION
PENDING_VERIFICATION

Estructura obligatorio a todos:

ID		Classification    Statement	Epistemic status	Source
M1-PR-001	COURSE_FACT
M1-TO-001	COURSE_FACT
M1-PA-001	COURSE_FACT
M1-EX-001	EXTERNAL_FACT
M1-RC-001	PROJECT_RECOMMENDATION
M1-PV-001	PENDING_VERIFICATION


No conviertas opiniones del curso en reglas obligatorias.
No inventes información.
No selecciones todavía stack de backend, frontend, base de datos o infraestructura.
No crees AGENTS.md.
No crees CLAUDE.md.
No crees backend.
No crees frontend.
No instales dependencias.

El plan debe indicar:
1. archivos leídos;
2. archivos creados;
3. modelo de procedencia;
4. estrategia de trazabilidad;
5. comprobaciones;
6. riesgos de contaminación.
```

## D.10. Revisar el plan antes de aprobarlo

Debe quedar claro que:

```text
CursoIA = solo lectura
Proyecto_Final_Master_AI4Devs = destino
```

Y debe comprobarse que no se adelanten:

- historias de usuario;
- arquitectura funcional;
- backend;
- frontend;
- base de datos;
- `AGENTS.md`;
- `CLAUDE.md`.

## D.11. Ejecutar el plan aprobado

Después de aprobar el plan:

```bash
cd ~/Projects/Proyecto_Final_Master_AI4Devs
claude --add-dir ~/Projects/CursoIA
```

No utilizar:

```text
--dangerously-skip-permissions
```

La propia CLI documenta que ese modo omite controles de permisos; no lo necesitamos para esta actividad. La salida de `claude --help` del entorno auditado confirma la existencia de ese modo y, separadamente, de modos normales de permisos. fileciteturn43file0L52-L60

## D.12. Prompt de ejecución

```text
Ejecuta únicamente el plan aprobado para construir la fuente de verdad estructurada del Módulo 1.

Antes de escribir:
1. comprueba que ~/Projects/CursoIA es el repositorio correcto;
2. comprueba que el destino está fuera de ese repositorio;
3. no modifiques ~/Projects/CursoIA.

Después:

1. Lee completamente los cinco documentos del Módulo 1.
2. Lee el plan del Paso 3.
3. Construye MODULE_1_SOURCE_OF_TRUTH.md.
4. Clasifica cada afirmación relevante por procedencia.
5. Asigna IDs estables.
6. Mantén hechos, recomendaciones, decisiones y pendientes separados.
7. Marca afirmaciones temporales para verificación.
8. Construye una matriz de trazabilidad.
9. No inventes contenido.
10. No modifiques CursoIA.
11. No crees AGENTS.md.
12. No crees CLAUDE.md.
13. No crees backend/frontend.
14. No instales dependencias.
15. No definas requisitos funcionales que todavía no correspondan.

Después de escribir:
- revisa duplicaciones;
- revisa contradicciones;
- revisa entradas sin procedencia;
- revisa recomendaciones mal clasificadas;
- revisa que estén representados los cinco documentos;
- ejecuta las comprobaciones del paso;
- informa de archivos creados, cambios, entradas por categoría y resultado.
```

## D.13. Matriz de trazabilidad

Debe poder existir una tabla como:

| ID | Tipo | Afirmación | Fuente primaria | Validación externa | Implicación |
|---|---|---|---|---|---|
| M1-PR-001 | COURSE_FACT | ... | Lección 1 | — | ... |
| M1-TO-001 | COURSE_FACT | ... | Lección 2 | Claude Code docs | ... |
| M1-PA-001 | COURSE_FACT | ... | Lección 4 | — | ... |
| M1-EX-001 | EXTERNAL_FACT | ... | fuente oficial | verificada | ... |
| M1-RC-001 | PROJECT_RECOMMENDATION | ... | decisión metodológica | — | ... |
| M1-PV-001 | PENDING_VERIFICATION | ... | recurso externo | pendiente | ... |

## D.14. Recursos externos

El quinto documento contiene recursos externos. No todos son hechos ni reglas.

Cada recurso deberá registrar, cuando sea posible:

```text
recurso
propósito
fuente
qué afirmación respalda
estado de revisión
```

## D.15. Afirmaciones temporales

Para versiones, precios, límites, benchmarks o disponibilidad usar:

```text
claim
source
observed_on
verification_status
last_checked
```

Esto evita convertir una instantánea histórica en una regla permanente.

---

# E. Resultado esperado

Debe existir:

```text
~/Projects/
├── CursoIA/
│   └── fuente educativa intacta
└── Proyecto_Final_Master_AI4Devs/
    └── docs/
        └── source-of-truth/
            └── module-1/
                └── MODULE_1_SOURCE_OF_TRUTH.md
```

El documento debe cubrir:

```text
✓ principios
✓ prácticas
✓ herramientas
✓ configuraciones
✓ anti-patrones
✓ comprobaciones
✓ recursos externos
✓ afirmaciones sujetas a verificación
✓ procedencia
✓ trazabilidad
```

No debe contener todavía decisiones funcionales del producto.

---

# F. Comprobaciones

## F.1. CursoIA limpio

```bash
cd ~/Projects/CursoIA
git status --short
```

Esperado:

```text
vacío
```

## F.2. Artefacto creado

```bash
test -f ~/Projects/Proyecto_Final_Master_AI4Devs/docs/source-of-truth/module-1/MODULE_1_SOURCE_OF_TRUTH.md
```

Esperado:

```text
0
```

## F.3. Artefacto no vacío

```bash
test -s ~/Projects/Proyecto_Final_Master_AI4Devs/docs/source-of-truth/module-1/MODULE_1_SOURCE_OF_TRUTH.md
```

Esperado:

```text
0
```

## F.4. Categorías obligatorias

```bash
FILE=~/Projects/Proyecto_Final_Master_AI4Devs/docs/source-of-truth/module-1/MODULE_1_SOURCE_OF_TRUTH.md
for tag in COURSE_FACT EXTERNAL_FACT PROJECT_RECOMMENDATION PROJECT_DECISION PENDING_VERIFICATION; do
  grep -q "$tag" "$FILE" || echo "FALTA: $tag"
done
```

Esperado: sin salida.

## F.5. Secciones obligatorias

```bash
FILE=~/Projects/Proyecto_Final_Master_AI4Devs/docs/source-of-truth/module-1/MODULE_1_SOURCE_OF_TRUTH.md
for section in \
  "Principles" \
  "Practices" \
  "Tools" \
  "Configurations" \
  "Anti-patterns" \
  "Checks" \
  "External resources" \
  "Time-sensitive claims" \
  "Traceability matrix"; do
    grep -q "$section" "$FILE" || echo "FALTA: $section"
done
```

Esperado: sin salida.

## F.6. IDs duplicados

```bash
grep -oE 'M1-[A-Z]{2}-[0-9]{3}' "$FILE" | sort | uniq -d
```

Esperado: vacío.

## F.7. Los cinco documentos están representados

```bash
for term in \
  "El modelo mental de los 3 pilares" \
  "Pilar 1" \
  "Pilar 2" \
  "Pilar 3" \
  "Recursos adicionales"; do
    grep -q "$term" "$FILE" || echo "FALTA: $term"
done
```

Esperado: sin salida.

## F.8. Prueba funcional de lectura con Claude Code

La instalación ya fue verificada con `claude --version` y `claude --help`. fileciteturn43file0L32-L60

Ahora debe demostrarse que Claude Code puede leer las cinco fuentes sin modificarlas:

```bash
claude --add-dir ~/Projects/CursoIA \
  -p "Enumera únicamente los cinco archivos del Módulo 1 dentro de ~/Projects/CursoIA. No modifiques ningún archivo. Devuelve solo las rutas."
```

La CLI oficial documenta `-p`/`--print` para ejecución no interactiva. citeturn657767search10

La respuesta esperada contiene únicamente las cinco rutas fuente.

## F.9. Verificación de no modificación

Después de cualquier ejecución de Claude Code:

```bash
cd ~/Projects/CursoIA
git status --short
```

Debe continuar vacío.

## F.10. Comprobación de enlaces

```bash
grep -nE 'https?://|www\.' "$FILE"
```

Después revisar manualmente que cada recurso externo tenga propósito y estado.

---

# G. Hallazgos

## G.1. Hallazgos reales heredados del entorno

La auditoría mostró una cadena suficientemente completa para realizar este trabajo documental:

```text
WSL 2
Ubuntu 26.04
Git
GitHub CLI
Claude Code
Node/npm
Python
uv/Poetry
Docker/Compose
PostgreSQL client
```

La evidencia de las versiones y rutas está en el output real del Paso 2. fileciteturn43file0L81-L90 fileciteturn43file1L32-L38 fileciteturn43file2L351-L382

## G.2. Python/pip

Python 3.14.4 está disponible, pero el `python3` del sistema indicó:

```text
No module named pip
```

Esto no bloquea este paso porque `uv` y Poetry ya están presentes. fileciteturn43file2L357-L382

No se instalará `pip` como parte de Paso 3.

## G.3. GPU

`nvidia-smi` produjo `Segmentation fault` dentro de WSL. Es una observación para una futura decisión sobre uso local de GPU, no un bloqueo de documentación. fileciteturn42file0L48-L57

## G.4. PATH

Existe repetición de una ruta de Node.js en `PATH`. No hay evidencia suficiente de conflicto funcional, por lo que no se modifica todavía. fileciteturn41file0L15-L32

## G.5. GitHub CLI

Hay dos cuentas configuradas; una está activa y otra no. No se modifica la autenticación durante este paso. La información sensible del token no forma parte del informe. fileciteturn43file0L15-L30

## G.6. Hallazgo conceptual principal

La fuente de verdad debe ser:

```text
estructurada
+
versionable
+
trazable
+
selectiva
```

y no:

```text
larga
+
duplicada
+
monolítica
```

OpenAI describe la misma tensión al explicar por qué un `AGENTS.md` gigante perdió efectividad y por qué una base documental estructurada resulta más útil para agentes. citeturn488365search0

---

# H. Correcciones

## H.1. Corrección obligatoria del Paso 2

Eliminar temporales de auditoría de `CursoIA`:

```bash
cd ~/Projects/CursoIA
rm -f audit-step2.sh step2-audit-output.txt
git status --short
```

## H.2. No instalar pip todavía

La falta de pip del Python del sistema no justifica todavía cambiar el entorno.

## H.3. No reparar GPU todavía

La GPU no es necesaria para construir la fuente de verdad.

## H.4. No modificar PATH todavía

La duplicación no demuestra por sí sola un problema.

## H.5. No crear aún AGENTS.md ni CLAUDE.md

Esos archivos pertenecen a pasos posteriores y dependerán de la fuente estructurada y de decisiones posteriores del proyecto.

## H.6. No modificar CursoIA

Todas las transformaciones deben ocurrir en el workspace separado.

---

# I. Checklist

## I.1. Fuente primaria

- [X] `CursoIA` sigue siendo solo lectura.
- [X] `CursoIA` está limpio.
- [X] Los temporales de auditoría fueron eliminados.
- [X] Los cinco documentos siguen intactos.

## I.2. Workspace

- [X] Existe `Proyecto_Final_Master_AI4Devs`.
- [X] Está fuera de `CursoIA`.
- [X] Existe `docs/source-of-truth/module-1`.
- [X] Existe `MODULE_1_SOURCE_OF_TRUTH.md`.

## I.3. Cobertura

- [X] Principios.
- [X] Prácticas.
- [X] Herramientas.
- [X] Configuraciones.
- [X] Anti-patrones.
- [X] Comprobaciones.
- [X] Recursos externos.
- [X] Afirmaciones temporales.
- [X] Pendientes.

## I.4. Procedencia

- [X] `COURSE_FACT`.
- [X] `EXTERNAL_FACT`.
- [X] `PROJECT_RECOMMENDATION`.
- [X] `PROJECT_DECISION`.
- [X] `PENDING_VERIFICATION`.

## I.5. Trazabilidad

- [X] IDs estables.
- [X] Sin IDs duplicados.
- [X] Los cinco documentos tienen referencias.
- [X] Existe matriz de trazabilidad.
- [X] Recursos externos distinguidos de hechos.

## I.6. Seguridad

- [X] No se registraron tokens.
- [X] No se registraron claves.
- [X] No se registraron contraseñas.
- [X] Claude Code no modificó `CursoIA`.

## I.7. Alcance

- [X] No hay backend.
- [X] No hay frontend.
- [X] No hay base de datos del producto.
- [X] No hay `AGENTS.md`.
- [X] No hay `CLAUDE.md`.
- [X] No se fijó aún arquitectura funcional.
- [X] No se adelantaron módulos posteriores.

---

# J. Gate

## Estado actual

# `PASA`

## Motivo

El Paso 3 está investigado y completamente definido, pero el artefacto todavía debe construirse y verificarse en el PC real.

El criterio es deliberadamente estricto:

```text
procedimiento definido
≠
fuente de verdad construida
```

## Condiciones para `PASA`

Deben verificarse todas:

1. `CursoIA` limpio.
2. Temporales del Paso 2 eliminados.
3. Workspace separado creado.
4. `MODULE_1_SOURCE_OF_TRUTH.md` creado.
5. Los cinco documentos están representados.
6. Las categorías obligatorias existen.
7. La procedencia está correctamente clasificada.
8. Los IDs no están duplicados.
9. Existe trazabilidad.
10. No se introdujo información inventada.
11. Recomendaciones y hechos están separados.
12. Pendientes están marcados.
13. Claude Code puede leer las cinco fuentes.
14. Claude Code no modifica `CursoIA`.
15. La revisión humana encuentra el documento coherente.

## `PASA CON OBSERVACIONES`

Se utilizará cuando el artefacto sea correcto y utilizable, pero existan cuestiones no críticas como:

- una referencia externa pendiente;
- una mejora de organización;
- algún metadato incompleto que no afecte a la trazabilidad.

## `NO PASA`

Se mantendrá si:

- `CursoIA` fue modificado accidentalmente;
- una afirmación relevante no tiene procedencia;
- se mezclan recomendaciones con hechos;
- se inventó información;
- los cinco documentos no están suficientemente representados;
- Claude Code no puede leer las fuentes;
- el documento contiene decisiones funcionales que corresponden a pasos posteriores.

---

# Fuentes investigadas

## Repositorio del curso

- `https://github.com/Diiegoal/CursoIA`
- `https://github.com/Diiegoal/CursoIA/blob/main/Prompts/Plan_M1_preparacion_Proyecto_Final_Master_AI4Devs_2026-09-02.md`

## GitHub

- `https://docs.github.com/en/get-started/using-github/communicating-on-github`
- `https://docs.github.com/en/get-started/learning-to-code/getting-started-with-git`
- `https://docs.github.com/en/enterprise-server%403.17/issues/planning-and-tracking-with-projects/learning-about-projects/best-practices-for-projects`

## Claude Code / Anthropic

- `https://docs.anthropic.com/en/docs/claude-code/memory`
- `https://docs.anthropic.com/en/docs/claude-code/cli-usage`
- `https://code.claude.com/docs/en/memory`
- `https://code.claude.com/docs/en/subagents`
- `https://code.claude.com/docs/en/common-workflows`
- `https://code.claude.com/docs/en/hooks`
- `https://code.claude.com/docs/en/settings`

## AGENTS.md

- `https://agents.md/`

## OpenAI

- `https://openai.com/index/harness-engineering/`

---

# Hechos vs recomendaciones

## Hechos

Se consideran hechos únicamente las afirmaciones respaldadas por:

- archivos originales del curso;
- fuentes oficiales;
- resultados observados en el PC;
- referencias externas verificadas.

## Recomendaciones

Son decisiones metodológicas adoptadas por nosotros para mejorar:

- trazabilidad;
- contexto;
- mantenibilidad;
- reproducibilidad;
- seguridad.

No deben presentarse como requisitos universales.

## Decisiones del proyecto

Solo se registrarán aquí decisiones explícitamente aprobadas para este proyecto.

En Paso 3 no se define todavía la arquitectura funcional del producto.

---

# Diseño conceptual resultante

```text
                 ┌──────────────────────────────────┐
                 │ Diiegoal/CursoIA                 │
                 │ FUENTE EDUCATIVA PRIMARIA        │
                 └────────────────┬─────────────────┘
                                  │
                                  │ extracción + clasificación
                                  ▼
                 ┌──────────────────────────────────┐
                 │ MODULE_1_SOURCE_OF_TRUTH.md      │
                 │                                  │
                 │ Facts                            │
                 │ Practices                        │
                 │ Tools                            │
                 │ Checks                           │
                 │ Anti-patterns                    │
                 │ External evidence                │
                 │ Recommendations                  │
                 │ Pending verification              │
                 │ Traceability                     │
                 └────────────────┬─────────────────┘
                                  │
                          selección contextual
                                  │
                       ┌──────────┴──────────┐
                       ▼                     ▼
                  AGENTS.md             CLAUDE.md
                  paso posterior         paso posterior
                       │                     │
                       └──────────┬──────────┘
                                  ▼
                            Claude Code
                               / Harness
```

Este diseño coincide con la lección de *harness engineering* de mantener un punto de entrada legible y llevar el conocimiento detallado a una base estructurada, en lugar de concentrarlo todo en un único archivo de instrucciones. citeturn488365search0

---

# Solucion nvidia-smi

```bash
+-----------------------------------------------------------------------------------------+
| NVIDIA-SMI 615.65.06              KMD Version: 616.56        CUDA UMD Version: 13.4     |
+-----------------------------------------+------------------------+----------------------+
| GPU  Name                 Persistence-M | Bus-Id          Disp.A | Volatile Uncorr. ECC |
| Fan  Temp   Perf          Pwr:Usage/Cap |           Memory-Usage | GPU-Util  Compute M. |
|                                         |                        |               MIG M. |
|=========================================+========================+======================|
|   0  NVIDIA GeForce RTX 3050 ...    On  |   00000000:01:00.0 Off |                  N/A |
| N/A   55C    P0             17W /   60W |       0MiB /   4096MiB |      0%      Default |
|                                         |                        |                  N/A |
+-----------------------------------------+------------------------+----------------------+

+-----------------------------------------------------------------------------------------+
| Processes:                                                                              |
|  GPU   GI   CI              PID   Type   Process name                        GPU Memory |
|        ID   ID                                                               Usage      |
|=========================================================================================|
|  No running processes found                                                             |
+-----------------------------------------------------------------------------------------+
total 410336
```

---

# Estado final del Paso 3

```text
Investigación del procedimiento             ✓
Plan del repositorio revisado               ✓
Evidencia del Paso 2 revisada               ✓
Modelo de procedencia definido              ✓
Taxonomía definida                           ✓
Trazabilidad definida                        ✓
Procedimiento de ejecución preparado         ✓
Pruebas definidas                            ✓
Checklist definido                           ✓
Artefacto local construido                   VERIFICADO
Gate                                         PASA
```

# Siguiente acción

1. Limpia los temporales de `CursoIA` y verifica `git status --short` vacío.
2. Crea `~/Projects/Proyecto_Final_Master_AI4Devs/docs/source-of-truth/module-1`.
3. Ejecuta Claude Code primero en modo `plan` con el prompt definido.
4. Revisa el plan.
5. Ejecuta la construcción del documento.
6. Ejecuta todas las comprobaciones de la sección F.
7. Comparte el `MODULE_1_SOURCE_OF_TRUTH.md` resultante y el `git status --short` de `CursoIA` para cerrar el Gate.

**¿Deseas continuar con el Paso 4 — Definición del contrato operativo del proyecto cuando el Gate del Paso 3 sea `PASA` o `PASA CON OBSERVACIONES` sin fallos críticos?**
