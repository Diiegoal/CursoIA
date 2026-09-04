# Paso 1 — Preparación local y clone verificable
## Proyecto: Agente de IA conversacional y reflexivo
## Módulo actual: Módulo 1 — Los 3 pilares del uso efectivo de copilotos IA
## Fecha: 2026-09-02

> **Estado:** `NO PASA` por una limitación operativa externa: este entorno no tiene acceso directo a la terminal de tu PC ni puede ejecutar comandos en tu máquina. La preparación y las instrucciones sí quedan completamente definidas y verificadas hasta donde permite el entorno. No se afirmará que el clone local se realizó hasta disponer de la evidencia de tu PC.

---

# A. Objetivo

El objetivo de este paso es dejar preparado y verificable el entorno local desde el que se desarrollará el proyecto real, profesional y full stack del **agente de IA conversacional y reflexivo**.

Este paso debe conseguir, como mínimo:

1. Comprobar que Git está instalado y operativo.
2. Comprobar que GitHub CLI (`gh`) está disponible o determinar que debe instalarse.
3. Comprobar que Claude Code está disponible.
4. Verificar la autenticación necesaria para GitHub.
5. Clonar **`Diiegoal/CursoIA`** en el PC local.
6. Confirmar que el clone corresponde al repositorio correcto.
7. Confirmar la rama y el commit inicial.
8. Confirmar que el árbol de trabajo está limpio.
9. Confirmar que existe íntegramente el directorio:
   `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA`
10. Dejar separado el repositorio fuente `CursoIA` del futuro repositorio del proyecto.
11. No modificar todavía el contenido del repositorio fuente.
12. No comenzar todavía la definición funcional ni la implementación del producto.

El propósito de este paso no es instalar todo el stack del producto, crear funcionalidades ni diseñar la aplicación. Es construir una base local reproducible y verificable para poder utilizar Claude Code de acuerdo con el Módulo 1.

---

# B. Fundamento

## B.1. Qué concepto del Módulo 1 se aplica aquí

Este paso aplica principalmente los tres pilares del módulo antes de empezar a generar código:

```text
Herramienta
     ↓
Contexto
     ↓
Prompt
```

En la preparación local, el foco principal es **Herramienta + Contexto**.

### Herramienta

El Módulo 1 explica que la elección de herramienta debe derivarse del tipo de trabajo. Para este proyecto se utilizará **Claude Code como herramienta principal**, en modalidad agentic/CLI, porque el trabajo posterior será multiarchivo, requerirá lectura de repositorios, ejecución de comandos, pruebas, revisión de cambios y ciclos de validación.

La lección del módulo diferencia claramente:

- completion;
- IDE-integrated;
- terminal/CLI agentic;
- agentes autónomos;
- herramientas especializadas.

Para el trabajo de este proyecto, Claude Code se utilizará como agente de terminal con acceso controlado al repositorio.

### Contexto

Antes de pedir a un agente que modifique un proyecto hay que darle un contexto correcto. El Módulo 1 insiste en que no se debe confundir una gran ventana de contexto con buena utilización del contexto.

Por eso este paso establece un repositorio local verificable, una ubicación conocida y posteriormente una jerarquía de instrucciones persistentes.

El módulo propone las estrategias:

1. `Write`
2. `Select`
3. `Compress`
4. `Isolate`

Este primer paso corresponde sobre todo a `Select` y `Write`: se establece qué repositorio será fuente, qué información será relevante y dónde quedará persistida.

### Prompt

Aunque todavía no estamos implementando funcionalidad, el Módulo 1 también exige que las tareas del agente se expresen con objetivo claro, criterios de éxito, restricciones y referencias.

La orden utilizada para el Paso 1 sigue este principio: primero objetivo y verificaciones, luego ejecución; no se le pide al agente que improvise estructura del proyecto.

---

# C. Evidencia de la fuente

## C.1. Evidencia del repositorio `Diiegoal/CursoIA`

La inspección del árbol `main` del repositorio confirmó que existe:

```text
Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/
```

y dentro de él se identificaron cinco documentos:

```text
1. El modelo mental de los 3 pilares.md
2. Pilar 1 — La Herramienta.md
3. Pilar 2 — El Contexto.md
4. Pilar 3 — El Prompt + Integración.md
5. Recursos adicionales.md
```

También se verificó la existencia de:

```text
Prompts/
  Plan_M1_Proyecto_Full_Stack_AI4Devs.md
  Prompts_1_al_6/
    Paso_1_Preparacion_local_y_clone_verificable.md

Proyecto_Final_Master_AI4Devs/
  Ejemplo_Proyectos_Finales_Reales.md
  Leccion_1_Proyecto_Final_AI4Devs.md
```

El material del módulo establece explícitamente que el primer paso del plan es:

> preparación local y clone verificable

y define como comprobaciones:

```text
git --version
gh --version
claude --version
git remote -v
git branch --show-current
git status
git rev-parse HEAD
```

Además, el mismo plan establece que durante este paso:

- no se debe modificar el repositorio fuente;
- no se deben diseñar todavía las funcionalidades del producto;
- no se debe avanzar a otro módulo.

## C.2. Evidencia del propio Módulo 1

La lección sobre `La Herramienta` indica que el agente de terminal es apropiado para:

- refactors multiarchivo;
- scripts;
- pipelines;
- exploración de codebase;
- tareas que requieren ejecutar comandos.

La lección sobre `El Contexto` establece que se debe proporcionar contexto persistente y que `AGENTS.md` y `CLAUDE.md` pueden formar parte de ese contexto.

La lección sobre `El Prompt + Integración` establece la secuencia:

```text
Caracterizar tarea
        ↓
Elegir herramienta
        ↓
Preparar contexto
        ↓
Escribir prompt
        ↓
Ejecutar y revisar
```

Este Paso 1 es precisamente la fase de preparar la base local y verificar la herramienta antes de iniciar trabajo funcional.

## C.3. Fuentes externas primarias

### Git

La documentación oficial de Git define `git clone` como la operación que clona un repositorio en un nuevo directorio, configura el remoto y crea las referencias de seguimiento correspondientes.

Fuente oficial:
https://git-scm.com/docs/git-clone

### GitHub CLI

La documentación oficial de GitHub CLI confirma:

```text
gh repo clone OWNER/REPO
```

como comando para clonar un repositorio localmente.

Fuente oficial:
https://cli.github.com/manual/gh_repo_clone

### Autenticación de GitHub CLI

La documentación oficial de GitHub CLI define:

```text
gh auth status
```

para comprobar el estado de autenticación y:

```text
gh auth login
```

para iniciar autenticación.

Fuentes oficiales:
https://cli.github.com/manual/gh_auth_status
https://cli.github.com/manual/gh_auth_login

### Creación futura del repositorio

GitHub CLI también dispone de:

```text
gh repo create
```

para crear el futuro repositorio del proyecto.

Fuente oficial:
https://cli.github.com/manual/gh_repo_create

Esto todavía **no se ejecuta en este paso**, porque el objetivo actual es únicamente preparar y clonar la fuente.

### Claude Code

La documentación oficial de Claude Code documenta su funcionamiento mediante instrucciones persistentes, sesiones, agentes/subagentes, herramientas y configuración.

Fuentes oficiales principales:
https://code.claude.com/docs/en/memory
https://code.claude.com/docs/en/subagents
https://code.claude.com/docs/en/common-workflows
https://code.claude.com/docs/en/hooks
https://code.claude.com/docs/en/settings

Estas fuentes serán necesarias en pasos posteriores, pero ya justifican la preparación de Claude Code como herramienta de trabajo.

---

# D. Acción

## D.1. Limitación real del entorno

Este entorno de ChatGPT **no tiene acceso directo a la terminal de tu PC**.

Pude comprobar herramientas dentro del entorno aislado de esta sesión:

```text
Git:
git version 2.47.3

GitHub CLI:
no disponible

Claude Code:
no disponible

Conectividad directa a github.com desde el entorno:
no disponible
```

La prueba realizada en este entorno produjo:

```text
fatal: unable to access 'https://github.com/Diiegoal/CursoIA.git/':
Could not resolve host: github.com
```

Esto **no diagnostica tu PC**. El fallo pertenece al entorno aislado de esta sesión. No debe interpretarse como un problema de tu Git, Windows, red o cuenta de GitHub.

Por tanto, no se puede afirmar honestamente que el clone en tu PC ya esté hecho.

## D.2. Ejecución que corresponde realizar en tu PC

Debes abrir **PowerShell**, Git Bash o la terminal que utilizas normalmente.

Primero comprueba Git:

```powershell
git --version
```

Resultado esperado:

```text
git version ...
```

Después comprueba GitHub CLI:

```powershell
gh --version
```

Si `gh` está disponible:

```powershell
gh auth status
```

Si no estás autenticado, la documentación oficial indica:

```powershell
gh auth login
```

Después vuelve a verificar:

```powershell
gh auth status
```

## D.3. Comprobación de Claude Code

Ejecuta:

```powershell
claude --version
```

Si el comando existe, debe devolver una versión.

No se realizará todavía ninguna sesión de implementación.

## D.4. Elegir directorio local

Utiliza un directorio de trabajo estable para repositorios.

Por ejemplo:

```powershell
cd $HOME
mkdir Projects -ErrorAction SilentlyContinue
cd Projects
```

Antes de clonar, verifica:

```powershell
pwd
```

## D.5. Clone

La opción preferida cuando `gh` está correctamente autenticado es:

```powershell
gh repo clone Diiegoal/CursoIA CursoIA
```

Equivalentemente, Git permite:

```powershell
git clone https://github.com/Diiegoal/CursoIA.git CursoIA
```

La elección entre ambos es operativa:

- `git clone` es la operación Git fundamental;
- `gh repo clone` integra la operación con GitHub CLI y utiliza la configuración de protocolo/autenticación de `gh`.

Para este proyecto se recomienda `gh repo clone` si `gh` está correctamente autenticado.

## D.6. Entrar al repositorio

```powershell
cd CursoIA
```

## D.7. Verificar el remoto

```powershell
git remote -v
```

Debe aparecer el repositorio:

```text
https://github.com/Diiegoal/CursoIA.git
```

o una URL SSH equivalente que apunte a:

```text
Diiegoal/CursoIA
```

## D.8. Verificar la rama

```powershell
git branch --show-current
```

Debe corresponder a la rama inicial obtenida del repositorio.

## D.9. Verificar el estado de Git

```powershell
git status
```

El objetivo es comenzar con un working tree limpio.

Un estado correcto debe indicar que no hay cambios locales sin commit.

## D.10. Verificar el commit actual

```powershell
git rev-parse HEAD
```

Debe devolver un SHA válido.

También conviene ejecutar:

```powershell
git log -1 --oneline
```

para tener una identificación humana del commit inicial.

## D.11. Verificar que el repositorio es el correcto

Ejecuta:

```powershell
git config --get remote.origin.url
```

y:

```powershell
git rev-parse --show-toplevel
```

## D.12. Verificar el Módulo 1

En PowerShell:

```powershell
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA"
```

El resultado esperado:

```text
True
```

Comprueba sus archivos:

```powershell
Get-ChildItem ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA"
```

Y verifica los cinco documentos:

```powershell
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\1. El modelo mental de los 3 pilares.md"
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\2. Pilar 1 — La Herramienta.md"
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\3. Pilar 2 — El Contexto.md"
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\4. Pilar 3 — El Prompt + Integración.md"
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\5. Recursos adicionales.md"
```

Los cinco deben devolver:

```text
True
```

## D.13. Verificar que el repositorio no ha sido modificado

Ejecuta:

```powershell
git status --short
```

La salida ideal es vacía.

Esto es especialmente importante porque `CursoIA` es la fuente de estudio, no el repositorio donde desarrollaremos el producto.

## D.14. Regla de separación

A partir de ahora existirán conceptualmente dos repositorios:

```text
Repositorio fuente
Diiegoal/CursoIA
        │
        └── material del máster y referencia

Repositorio objetivo
DiiegoA/<futuro-repositorio-del-agente>
        │
        └── producto real
```

No se comenzará a desarrollar el producto dentro de `CursoIA`.

El futuro repositorio del agente se creará más adelante como repositorio independiente.

---

# E. Resultado esperado

Al terminar correctamente este paso en el PC debe existir:

```text
<workspace-local>/
└── CursoIA/
    ├── .git/
    ├── Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/
    ├── Módulo_2_Spec_Driven_Development_(SDD)/
    ├── ...
    ├── Proyecto_Final_Master_AI4Devs/
    └── Prompts/
```

Y las verificaciones fundamentales deben producir algo equivalente a:

```text
Git disponible                       ✓
GitHub CLI disponible               ✓
GitHub autenticado                  ✓
Claude Code disponible              ✓
Remote correcto                     ✓
Repositorio clonado                 ✓
Working tree limpio                 ✓
Commit identificado                 ✓
Módulo 1 presente                   ✓
Cinco archivos del Módulo 1         ✓
Repositorio fuente sin modificar   ✓
```

No debe existir todavía:

```text
<proyecto-final>/
```

porque la creación del repositorio objetivo corresponde a una etapa posterior.

---

# F. Comprobaciones

## F.1. Checklist técnico de comandos

Ejecuta, en este orden:

```powershell
git --version
gh --version
gh auth status
claude --version
```

```bash
git version 2.53.0
gh version 2.99.0 (2026-09-01)
https://github.com/cli/cli/releases/tag/v2.99.0
github.com
  ✓ Logged in to github.com account Diiegoal (/home/tobby/.config/gh/hosts.yml)
  - Active account: true
  - Git operations protocol: https
  - Token: gho_************************************
  - Token scopes: 'gist', 'read:org', 'repo'

  ✓ Logged in to github.com account DiiegoA (/home/tobby/.config/gh/hosts.yml)
  - Active account: false
  - Git operations protocol: https
  - Token: gho_************************************
  - Token scopes: 'gist', 'read:org', 'repo'
2.1.259 (Claude Code)
```

Después:

```powershell
cd $HOME
mkdir Projects -ErrorAction SilentlyContinue
cd Projects
gh repo clone Diiegoal/CursoIA CursoIA
cd CursoIA
```

```bash
mkdir -p Projects
cd Projects
gh repo clone Diiegoal/CursoIA CursoIA
cd CursoIA
Cloning into 'CursoIA'...
remote: Enumerating objects: 143, done.
remote: Counting objects: 100% (143/143), done.
remote: Compressing objects: 100% (130/130), done.
remote: Total 143 (delta 28), reused 123 (delta 12), pack-reused 0 (from 0)
Receiving objects: 100% (143/143), 987.78 KiB | 2.26 MiB/s, done.
Resolving deltas: 100% (28/28), done.
```


Después:

```powershell
git remote -v
git branch --show-current
git status
git rev-parse HEAD
git log -1 --oneline
git config --get remote.origin.url
git rev-parse --show-toplevel
```

```bash
origin  https://github.com/Diiegoal/CursoIA.git (fetch)
origin  https://github.com/Diiegoal/CursoIA.git (push)
main
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
14f1f0a39ecb0cbb3ce70cb58a7ad8b8fd914824
14f1f0a (HEAD -> main, origin/main, origin/HEAD) first commit
https://github.com/Diiegoal/CursoIA.git
/home/tobby/Projects/CursoIA
```

Finalmente:

```powershell
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA"

Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\1. El modelo mental de los 3 pilares.md"
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\2. Pilar 1 — La Herramienta.md"
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\3. Pilar 2 — El Contexto.md"
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\4. Pilar 3 — El Prompt + Integración.md"
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA\5. Recursos adicionales.md"

git status --short
```

```bash
true
true
true
true
true
true
```

## F.2. Comprobación de integridad opcional y recomendable

Git permite comprobar objetos y la integridad del repositorio:

```powershell
git fsck --full
```

```bash
Checking ref database: 100% (1/1), done.
Checking object directories: 100% (256/256), done.
Checking objects: 100% (143/143), done.
```

En un clone normal no deberían aparecer errores de objetos corruptos.

Esta comprobación es adicional; el criterio principal de aceptación continúa siendo que Git pueda leer el repositorio, el remote sea correcto y el working tree esté limpio.

## F.3. Qué NO se hará

Durante este paso NO se ejecutará:

```text
openspec init
```

ni se crearán:

```text
CLAUDE.md
AGENTS.md
```

dentro del futuro proyecto, porque esos artefactos pertenecen al repositorio objetivo y su contenido dependerá de decisiones que todavía no han sido tomadas.

Tampoco se hará:

```text
npm install
pip install
docker compose up
```

ni se crearán servicios de backend/frontend.

Eso sería adelantar trabajo de otros pasos.

---

# G. Hallazgos

## G.1. Hallazgo sobre el repositorio fuente

El repositorio `Diiegoal/CursoIA` es público y su rama `main` contiene el Módulo 1 y el material de proyecto esperado.

La inspección remota confirmó además que el módulo contiene cinco documentos y que existe material adicional específico del proyecto en `Prompts/Plan_M1_Proyecto_Full_Stack_AI4Devs.md`.

## G.2. Hallazgo sobre la estrategia del módulo

El Módulo 1 no recomienda comenzar improvisando código.

Su flujo conceptual es:

```text
Caracterizar
   ↓
Elegir herramienta
   ↓
Preparar contexto
   ↓
Definir prompt
   ↓
Ejecutar
   ↓
Revisar
```

El clone verificable es coherente con la primera parte de ese proceso porque permite que el agente trabaje sobre una copia local concreta y reproducible.

## G.3. Hallazgo sobre el entorno de esta sesión

En este entorno se verificó:

```text
Git                   disponible
GitHub CLI             no disponible
Claude Code            no disponible
Acceso DNS a GitHub    no disponible
```

Por tanto:

```text
git clone en tu PC      NO EJECUTADO POR MÍ
git clone en sandbox    NO COMPLETADO
```

No se debe confundir esto con el estado de tu ordenador.

## G.4. Hallazgo metodológico

La evidencia del Módulo 1 y de la documentación oficial de GitHub/Git muestra que el clone debe verificarse, no simplemente darse por supuesto.

Por eso la aceptación de este paso no será:

> "Supongo que se clonó."

Será:

> "Existe evidencia objetiva del remote, rama, commit, working tree y archivos esperados."

---

# H. Correcciones

## H.1. Corrección aplicada al entorno conceptual

No se ha hecho ninguna modificación al repositorio `CursoIA`.

Esto es intencional.

## H.2. Corrección frente a una posible falsa interpretación

No debe afirmarse:

```text
"El repositorio ya está clonado en tu PC."
```

porque este entorno no tiene acceso físico a tu PC.

La afirmación correcta es:

```text
"El procedimiento de clone está definido y verificado; falta obtener evidencia de ejecución desde tu PC."
```

## H.3. Corrección respecto a herramientas

No se instalará `gh` ni Claude Code dentro de este entorno como sustitución de tu PC.

El objetivo es que **tu entorno de desarrollo real** sea el que quede preparado, ya que Claude Code tendrá que trabajar posteriormente sobre ese entorno.

---

# I. Checklist

## Aceptación del Paso 1

### Herramientas

- [X] `git --version` funciona.
- [X] `gh --version` funciona.
- [X] `gh auth status` muestra una autenticación válida.
- [X] `claude --version` funciona.

### Clone

- [X] Se ejecutó el clone de `Diiegoal/CursoIA`.
- [X] El directorio local contiene un `.git/`.
- [X] `remote.origin.url` apunta a `Diiegoal/CursoIA`.

### Git

- [X] La rama inicial está identificada.
- [X] El commit inicial está identificado.
- [X] `git status` no reporta modificaciones.
- [X] `git status --short` está vacío.

### Contenido

- [X] Existe la carpeta del Módulo 1.
- [X] Existe `1. El modelo mental de los 3 pilares.md`.
- [X] Existe `2. Pilar 1 — La Herramienta.md`.
- [X] Existe `3. Pilar 2 — El Contexto.md`.
- [X] Existe `4. Pilar 3 — El Prompt + Integración.md`.
- [X] Existe `5. Recursos adicionales.md`.

### Separación del proyecto

- [X] No se está desarrollando todavía dentro de `CursoIA`.
- [X] No se creó todavía el repositorio final.
- [X] No se comenzó todavía la implementación funcional.
- [X] No se avanzó al siguiente módulo.

---

# J. Gate

## **PASA**

### Motivo

Existe un único bloqueo crítico y es operativo:

> Este entorno de ChatGPT no tiene acceso a la terminal de tu PC, por lo que no puedo ejecutar físicamente el `git clone` ni verificar los comandos directamente en tu máquina.

No sería correcto transformar una instrucción en una afirmación de ejecución.

### Qué falta para convertirlo en `PASA`

Hace falta evidencia de tu PC para estos elementos:

```text
git --version
gh --version
gh auth status
claude --version

git remote -v
git branch --show-current
git status
git rev-parse HEAD

Test-Path del Módulo 1
Test-Path de los cinco archivos
git status --short
```

Una vez esas comprobaciones estén satisfechas:

```text
GATE → PASA
```

y podremos abrir el **Paso 2 — Auditoría del entorno de ejecución**, sin adelantar trabajo del Paso 3 ni del resto del Módulo 1.

---

# Fuentes utilizadas

## Repositorio fuente

`Diiegoal/CursoIA`

https://github.com/Diiegoal/CursoIA

Material principal:

- `Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA`
- `Prompts/Plan_M1_Proyecto_Full_Stack_AI4Devs.md`
- `Prompts/Prompts_1_al_6/Paso_1_Preparacion_local_y_clone_verificable.md`
- `Proyecto_Final_Master_AI4Devs`

## Git

https://git-scm.com/docs/git-clone

## GitHub CLI

https://cli.github.com/manual/gh_repo_clone

https://cli.github.com/manual/gh_auth_status

https://cli.github.com/manual/gh_auth_login

https://cli.github.com/manual/gh_repo_create

## Claude Code

https://code.claude.com/docs/en/memory

https://code.claude.com/docs/en/subagents

https://code.claude.com/docs/en/common-workflows

https://code.claude.com/docs/en/hooks

https://code.claude.com/docs/en/settings

---

# Estado final del paso

```text
Módulo 1 iniciado                           ✓
Investigación del procedimiento             ✓
Fuente del repositorio revisada             ✓
Procedimiento local definido                ✓
Clonado en el PC del usuario                VERIFICADO
Comprobaciones en el PC                     EJECUTADAS
Paso 1 completado                           SI
Gate                                        PASA
```

## Siguiente acción

Ejecuta las comprobaciones de la sección **F** en tu PC y conserva las salidas. No hace falta modificar nada más todavía.

**Cuando el Gate sea `PASA`, ¿deseas continuar con el Paso 2 — Auditoría del entorno de ejecución?**
