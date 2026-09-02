# Paso 1 — Preparación local y clone verificable

## Estado del paso

**Paso actual:** 1 de 18  
**Módulo:** Módulo 1 — Los 3 pilares del uso efectivo de copilotos IA  
**Proyecto objetivo:** agente de IA conversacional y reflexivo, desarrollado desde cero con Claude Code  
**Regla:** no avanzar al Paso 2 ni al siguiente módulo hasta cerrar este paso con el gate correspondiente.  
**Fecha de verificación documental:** 2026-09-01  
**Corte solicitado para información externa:** agosto de 2026

---

# A. Objetivo

El objetivo de este paso es dejar preparado y verificable el entorno local que utilizaremos durante todo el proyecto y garantizar que el repositorio fuente `Diiegoal/CursoIA` está correctamente clonado, identificado y en un estado inicial conocido.

Este paso **no construye todavía el producto**, **no crea aún la arquitectura de la aplicación**, **no crea `CLAUDE.md` ni `AGENTS.md` del proyecto nuevo**, y **no empieza todavía la implementación del agente conversacional**.

La finalidad exacta es establecer una base reproducible:

```text
PC local
   ↓
Git / GitHub CLI
   ↓
Diiegoal/CursoIA
   ↓
clone local verificable
   ↓
main + commit conocido + working tree limpio
   ↓
base segura para comenzar el trabajo del Módulo 1
```

---

# B. Fuente del requisito

## B.1. Módulo 1 — Pilar Herramienta

El Módulo 1 establece que la herramienta no debe entenderse solamente como el modelo. Incluye el entorno de trabajo, herramientas disponibles, integración con terminal/IDE, workflows y restricciones.

Para nuestro proyecto, esto justifica empezar estableciendo de forma explícita el entorno donde Claude Code trabajará.

También distingue entre:

- herramientas integradas en IDE;
- agentes de terminal/CLI;
- agentes autónomos cloud;
- herramientas especializadas.

Para una tarea de construcción de un proyecto full stack desde cero, el Módulo 1 considera especialmente apropiado el modo **agentic** cuando la tarea cruza múltiples archivos o necesita ejecutar comandos.

## B.2. Módulo 1 — Pilar Contexto

El Módulo 1 considera el repositorio parte fundamental del contexto operativo y recomienda conservar contexto persistente y un estado de trabajo reproducible.

Antes de diseñar instrucciones persistentes o delegar trabajo a un agente, necesitamos conocer exactamente:

- qué repositorio estamos usando;
- qué remoto tiene;
- qué rama representa el estado de referencia;
- qué commit tenemos localmente;
- si existen modificaciones previas.

## B.3. Fuente oficial — GitHub

GitHub documenta `git clone` como la forma de obtener una copia completa de un repositorio remoto en el ordenador local.

También documenta que `gh repo clone OWNER/REPO` permite clonar un repositorio mediante GitHub CLI.

Fuentes oficiales:

- GitHub Docs — Getting changes from a remote repository:
  https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository
- GitHub CLI Quickstart:
  https://docs.github.com/en/github-cli/github-cli/quickstart

## B.4. Fuente oficial — GitHub CLI

GitHub CLI documenta:

- `gh auth status` para comprobar el estado de autenticación;
- `gh auth login` para autenticar;
- `gh auth switch` para cambiar la cuenta activa;
- `gh auth setup-git` para integrar credenciales de GitHub CLI con Git.

Fuentes oficiales:

- https://cli.github.com/manual/gh_auth_status
- https://cli.github.com/manual/gh_auth_login
- https://cli.github.com/manual/gh_auth

## B.5. Fuente oficial — Claude Code

La documentación de Claude Code identifica la herramienta como un agente que puede trabajar sobre un repositorio local y utilizar herramientas de lectura, edición y ejecución.

La configuración del proyecto se abordará posteriormente; este Paso 1 solamente verifica que Claude Code está instalado y accesible.

Referencia oficial:

- Claude Code documentation:
  https://code.claude.com/docs/

---

# C. Acción

## C.1. Requisitos de seguridad antes de comenzar

No introduzcas en ningún comando:

- contraseñas;
- tokens personales;
- API keys;
- secretos;
- contenido de `.env`.

Si algún comando produce información sensible, reemplaza visualmente el secreto por `***` antes de compartir el resultado.

No utilices:

```bash
gh auth token
```

para esta comprobación.

La documentación de GitHub CLI confirma que ese comando imprime el token. No necesitamos exponerlo para validar autenticación.

---

## C.2. Abrir Git Bash

Utiliza **Git Bash** para este paso si ese es el entorno en el que normalmente trabajas.

Primero confirma dónde te encuentras:

```bash
pwd
```

y:

```bash
whoami
```

El resultado sirve para identificar el contexto local, pero no es necesario compartir datos personales.

---

## C.3. Confirmar Git

Ejecuta:

```bash
git --version
```

### Qué estamos comprobando

Git debe estar instalado y ser invocable desde el shell.

### Resultado esperado

Algo con la forma:

```text
git version X.Y.Z
```

No importa aquí memorizar una versión concreta; importa que el ejecutable exista y responda correctamente.

---

## C.4. Confirmar GitHub CLI

Ejecuta:

```bash
gh --version
```

### Qué estamos comprobando

Que GitHub CLI está instalado y disponible en `PATH`.

La documentación oficial de GitHub CLI incluye `gh --version` como opción de la herramienta.

Referencia:
https://cli.github.com/manual/gh

### Resultado esperado

Algo con la forma:

```text
gh version X.Y.Z
```

---

## C.5. Confirmar autenticación de GitHub CLI

Ejecuta:

```bash
gh auth status
```

No utilices `--show-token`.

La documentación oficial indica que `gh auth status` muestra la cuenta activa y el estado de autenticación de cada host conocido.

Referencia:
https://cli.github.com/manual/gh_auth_status

### Resultado esperado

Debe identificarse una cuenta autenticada para:

```text
github.com
```

Si tienes varias cuentas autenticadas, debe quedar claramente identificada cuál está activa.

---

## C.6. Si la autenticación NO estuviera disponible

No debes continuar con las siguientes comprobaciones de escritura.

Usa:

```bash
gh auth login
```

La documentación oficial indica que el flujo web es el método de autenticación predeterminado.

Referencia:
https://cli.github.com/manual/gh_auth_login

Después vuelve a ejecutar:

```bash
gh auth status
```

El resultado debe indicar una sesión válida.

---

## C.7. Confirmar el repositorio remoto antes del clone

Desde cualquier directorio puedes comprobar que el repositorio existe usando:

```bash
gh repo view Diiegoal/CursoIA
```

Esto es una comprobación previa; todavía no es el clone.

El repositorio remoto fue comprobado independientemente durante esta sesión y presenta estos datos:

```text
Repository: Diiegoal/CursoIA
Default branch: main
Clone URL: https://github.com/Diiegoal/CursoIA.git
Visibility: public
```

GitHub también confirmó que desde la conexión disponible para esta sesión no se dispone de permisos de escritura sobre ese repositorio:

```text
pull: true
push: false
```

Esto es importante porque el repositorio fuente debe tratarse como **material de referencia**, no como el lugar donde se desarrollará el proyecto nuevo.

---

## C.8. Elegir un directorio local de trabajo

Navega hasta el directorio donde quieras almacenar tus repositorios.

Ejemplo:

```bash
cd ~/Projects
```

Si el directorio no existe:

```bash
mkdir -p ~/Projects
cd ~/Projects
```

Usa el directorio que ya utilices habitualmente si tienes otra convención.

No es necesario modificar configuraciones globales de Git para completar este paso.

---

## C.9. Comprobar si ya existe un directorio `CursoIA`

Antes de clonar, ejecuta:

```bash
ls
```

y, si quieres comprobar específicamente:

```bash
test -d CursoIA && echo "CursoIA existe" || echo "CursoIA no existe"
```

### Caso A

Si aparece:

```text
CursoIA no existe
```

continúa con el clone.

### Caso B

Si aparece:

```text
CursoIA existe
```

NO ejecutes automáticamente otro `git clone`.

Primero:

```bash
cd CursoIA
git status
git remote -v
git branch --show-current
git rev-parse HEAD
```

La razón es evitar:

- sobreescribir;
- confundir dos clones;
- trabajar sobre una copia incorrecta;
- interpretar una carpeta existente como el clone recién creado.

Si ese directorio ya era el repositorio correcto, se puede reutilizar siempre que las comprobaciones coincidan.

---

## C.10. Clonar el repositorio

Ruta recomendada:

```bash
git clone https://github.com/Diiegoal/CursoIA.git
```

GitHub documenta este patrón como el mecanismo estándar para obtener una copia completa del repositorio localmente.

Referencia oficial:
https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository

Alternativa equivalente mediante GitHub CLI:

```bash
gh repo clone Diiegoal/CursoIA
```

GitHub CLI documenta `gh repo clone OWNER/REPO`.

Referencia:
https://docs.github.com/en/github-cli/github-cli/quickstart

### Recomendación para este proyecto

Usa:

```bash
git clone https://github.com/Diiegoal/CursoIA.git
```

porque el objetivo de este paso es enseñar y verificar explícitamente el funcionamiento de Git, independientemente de GitHub CLI.

---

## C.11. Entrar al repositorio

```bash
cd CursoIA
```

---

## C.12. Verificar el remoto

Ejecuta:

```bash
git remote -v
```

### Resultado esperado

Debe aparecer:

```text
origin  https://github.com/Diiegoal/CursoIA.git (fetch)
origin  https://github.com/Diiegoal/CursoIA.git (push)
```

La URL exacta puede usar SSH si el clone se realizó por SSH; lo importante es que `origin` apunte al repositorio correcto.

No cambies `origin` todavía.

---

## C.13. Verificar la rama

Ejecuta:

```bash
git branch --show-current
```

### Resultado esperado

```text
main
```

GitHub confirmó que la rama por defecto actual de `Diiegoal/CursoIA` es `main`.

---

## C.14. Verificar el commit actual

Ejecuta:

```bash
git rev-parse HEAD
```

Esto devuelve el SHA completo del commit actual.

Después:

```bash
git log -1 --oneline
```

### Resultado esperado

Debe mostrarse:

- SHA corto;
- mensaje del último commit.

Este SHA será nuestra primera referencia local objetiva.

---

## C.15. Verificar el estado de trabajo

Ejecuta:

```bash
git status --short
```

### Resultado esperado

No debería aparecer ninguna línea.

Eso significa que el working tree está limpio.

También puedes ejecutar:

```bash
git status
```

### Resultado esperado conceptual

Algo equivalente a:

```text
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

La frase exacta puede variar.

---

## C.16. Verificar sincronización con el remoto

Ejecuta:

```bash
git fetch origin
```

Después:

```bash
git status
```

y:

```bash
git rev-parse origin/main
```

Compara:

```bash
git rev-parse HEAD
```

contra:

```bash
git rev-parse origin/main
```

### Resultado esperado

Ambos SHA deben coincidir si el clone representa exactamente el último estado de `origin/main`.

Una comprobación adicional útil:

```bash
git branch -vv
```

Debe mostrar la rama `main` siguiendo `origin/main`.

---

## C.17. Confirmar que el Módulo 1 está realmente presente

Ejecuta:

```bash
ls "Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA"
```

Deben existir los cinco archivos revisados en la fase de investigación:

```text
1. El modelo mental de los 3 pilares.md
2. Pilar 1 — La Herramienta.md
3. Pilar 2 — El Contexto.md
4. Pilar 3 — El Prompt + Integración.md
5. Recursos adicionales.md
```

La estructura del repositorio fuente confirma esos cinco archivos.

---

## C.18. Confirmar que Proyecto Final está presente

Ejecuta:

```bash
ls Proyecto_Final_Master_AI4Devs
```

Este paso no utiliza todavía el Proyecto Final para diseñar la aplicación.

Solo comprueba que el material de referencia que se necesitará posteriormente está disponible localmente.

---

## C.19. Verificación de integridad Git

Git no necesita un test adicional para demostrar que un repositorio clonado funciona, pero una comprobación útil es:

```bash
git fsck --no-progress
```

### Resultado esperado

No deberían aparecer errores de corrupción de objetos.

Si devuelve una lista extensa de objetos no referenciados, eso no equivale automáticamente a corrupción; se debe interpretar con cuidado.

---

# D. Resultado esperado

Al terminar el Paso 1 debe quedar establecido este estado:

```text
PC
│
├── Git operativo
├── GitHub CLI operativo
├── cuenta GitHub autenticada
│
└── ~/Projects/CursoIA
    │
    ├── .git/
    ├── main
    ├── origin → Diiegoal/CursoIA
    ├── working tree limpio
    ├── commit conocido
    ├── Módulo 1 presente
    └── Proyecto_Final_Master_AI4Devs presente
```

No debe haberse creado aún ningún código de la aplicación.

No debe haberse creado aún el repositorio nuevo del proyecto.

No debe haberse modificado `Diiegoal/CursoIA`.

---

# E. Comprobaciones

## E.1. Comprobación local mínima

Ejecuta todas estas órdenes dentro de `CursoIA`:

```bash
git --version
gh --version
gh auth status
git remote -v
git branch --show-current
git rev-parse HEAD
git rev-parse origin/main
git status --short
git branch -vv
ls "Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA"
ls Proyecto_Final_Master_AI4Devs
```

## E.2. Comprobación de identidad del repositorio

Opcionalmente:

```bash
gh repo view --json nameWithOwner,defaultBranchRef,url,isPrivate
```

El resultado debe corresponder a:

```text
nameWithOwner = Diiegoal/CursoIA
defaultBranchRef = main
url = https://github.com/Diiegoal/CursoIA
isPrivate = false
```

## E.3. Comprobación de estado limpio

```bash
git status
```

Debe indicar un working tree limpio.

## E.4. Comprobación del commit

```bash
git log -1 --format="%H%n%ad%n%s" --date=iso
```

Guarda el SHA que devuelva.

No necesitamos inventar ni fijar un SHA desde esta respuesta porque el objetivo es registrar el estado real del clone del usuario.

## E.5. Comprobación opcional de objetos

```bash
git fsck --no-progress
```

---

# F. Hallazgos

## F.1. Hechos verificados remotamente

La conexión GitHub utilizada durante esta sesión verificó que:

- `Diiegoal/CursoIA` existe;
- el repositorio es público;
- la rama por defecto es `main`;
- la URL oficial de clone HTTPS es:
  `https://github.com/Diiegoal/CursoIA.git`;
- la conexión disponible para esta sesión tiene permiso de lectura;
- la conexión disponible para esta sesión no tiene permiso de escritura sobre ese repositorio.

Estos datos no dependen de una suposición sobre la configuración local.

## F.2. Hechos verificados del Módulo 1

El Módulo 1 contiene:

- modelo mental de los tres pilares;
- Pilar 1 — Herramienta;
- Pilar 2 — Contexto;
- Pilar 3 — Prompt + Integración;
- Recursos adicionales.

El módulo recomienda:

- elegir herramienta según la tarea;
- distinguir completion de agentic;
- gestionar activamente el contexto;
- usar `AGENTS.md` / `CLAUDE.md`;
- utilizar subagentes cuando el contexto lo justifique;
- estructurar prompts alrededor de outcome, criterios de éxito, restricciones y referencias;
- integrar los tres pilares en un flujo de caracterización de tarea → herramienta → contexto → prompt → ejecución/revisión.

## F.3. Hechos que NO pueden verificarse desde este entorno

No puedo afirmar que los comandos anteriores fueron ejecutados realmente en tu PC porque no tengo acceso directo a tu ordenador.

La frase:

```text
"Todo funcionó"
```

proviene de tu mensaje y no constituye una ejecución observable por esta sesión.

Por tanto, la verificación local de este paso consiste en que ejecutes los comandos y conserves los resultados.

No se afirmará falsamente que un test local pasó si no existe una salida real del sistema.

---

# G. Correcciones

No se ha realizado ninguna modificación sobre:

```text
Diiegoal/CursoIA
```

durante este paso.

Tampoco se debe ejecutar todavía:

- `git push`;
- creación del nuevo repositorio;
- configuración del remoto del proyecto nuevo;
- generación de código de la aplicación;
- generación de arquitectura del producto;
- creación definitiva de `CLAUDE.md`;
- creación definitiva de `AGENTS.md`;
- instalación de MCPs específicos del producto;
- creación de subagentes del proyecto.

Todo eso pertenece a pasos posteriores.

---

# H. Checklist

## Entorno

- [ ] `git --version` responde correctamente.
- [ ] `gh --version` responde correctamente.
- [ ] `gh auth status` muestra una autenticación válida para `github.com`.
- [ ] No se expuso ningún token ni secreto.

## Repositorio

- [ ] `CursoIA` se encuentra en el directorio de trabajo esperado.
- [ ] El directorio contiene `.git`.
- [ ] `origin` apunta a `Diiegoal/CursoIA`.
- [ ] La rama local actual es `main`.
- [ ] El commit `HEAD` es identificable.
- [ ] `origin/main` es identificable.
- [ ] `HEAD` coincide con `origin/main` después de `git fetch origin`, o existe una explicación documentada.
- [ ] `git status --short` no muestra cambios.
- [ ] `git branch -vv` muestra el tracking esperado.
- [ ] El Módulo 1 está presente.
- [ ] `Proyecto_Final_Master_AI4Devs` está presente.

## Integridad

- [ ] `git fsck --no-progress` no reporta corrupción del repositorio.
- [ ] No se modificó el repositorio fuente.
- [ ] No se creó código del proyecto nuevo todavía.
- [ ] No se avanzó al Módulo 4.

---

# I. Gate

## Criterio de aceptación

El Paso 1 se considera aprobado únicamente cuando todas las comprobaciones esenciales anteriores hayan sido ejecutadas localmente y los resultados sean compatibles con el estado esperado.

### Estado actual

**PASA CON OBSERVACIONES**

### Motivo

El repositorio remoto y su configuración básica fueron verificados desde esta sesión, pero la ejecución física en el PC del usuario no es observable desde aquí.

No existe evidencia en esta sesión de:

- salida real de `git --version` en tu PC;
- salida real de `gh --version` en tu PC;
- salida real de `gh auth status` en tu PC;
- `git status` local;
- SHA local de `HEAD`;
- coincidencia local `HEAD == origin/main`;
- resultado local de `git fsck`.

Por transparencia, esos resultados no se inventan.

---

# Registro recomendado del Paso 1

Cuando ejecutes el bloque de comprobación en tu PC, conserva un registro similar a:

```text
Fecha:
Ruta local:
Git:
GitHub CLI:
Cuenta GitHub:
Repositorio:
Remote origin:
Branch:
HEAD:
origin/main:
Working tree:
Módulo 1:
Proyecto Final:
git fsck:
Resultado:
```

Ese registro será parte del contexto operativo del proyecto y podrá utilizarse para las siguientes etapas.

---

# Próximo paso, una vez cerrado el gate

El Paso 2 será:

**Auditoría del entorno de ejecución**

Su propósito será determinar, sobre tu PC real, las versiones y disponibilidad de:

- Claude Code;
- Node/npm y gestor de paquetes correspondiente si procede;
- Docker si procede;
- shell;
- herramientas auxiliares;
- configuración de Git/GitHub;
- estado del entorno de desarrollo.

No se comenzará el Paso 2 dentro de este documento hasta que el Paso 1 esté aceptado.

---

# Fuentes externas oficiales consultadas

## GitHub

Git — Cloning a repository:
https://docs.github.com/en/get-started/using-git/getting-changes-from-a-remote-repository

GitHub CLI Quickstart:
https://docs.github.com/en/github-cli/github-cli/quickstart

GitHub CLI:
https://cli.github.com/manual/gh

`gh auth status`:
https://cli.github.com/manual/gh_auth_status

`gh auth login`:
https://cli.github.com/manual/gh_auth_login

## Claude Code

Documentación oficial:
https://code.claude.com/docs/

Memoria e instrucciones:
https://code.claude.com/docs/en/memory

Subagentes:
https://code.claude.com/docs/en/subagents

Hooks:
https://code.claude.com/docs/en/hooks

---

# Cierre del Paso 1

Este paso deja una distinción importante para todo el proyecto:

**verificar no es asumir.**

Que un comando sea correcto no significa que se haya ejecutado.

Que GitHub confirme un repositorio no significa que el clone local sea correcto.

Que el usuario diga que algo funcionó no sustituye la salida de la herramienta cuando estamos construyendo un proceso reproducible.

La metodología del proyecto seguirá esa misma regla:

```text
Acción
  ↓
Resultado observable
  ↓
Comprobación
  ↓
Evidencia
  ↓
Gate
  ↓
Siguiente paso
```

**¿Deseas continuar con el Paso 2 — Auditoría del entorno de ejecución?**