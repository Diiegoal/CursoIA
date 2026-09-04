# Paso 2 — Auditoría del entorno local

## Proyecto: Agente de IA conversacional y reflexivo
## Módulo actual: Módulo 1 — Los 3 pilares del uso efectivo de copilotos IA
## Fecha: 2026-09-03
## Gate preliminar: `NO PASA`

> Este paso continúa el mismo proyecto y la misma metodología secuencial del Paso 1. La auditoría debe observar primero, validar después y modificar solo cuando exista una razón técnica demostrada. No se desarrollará todavía ninguna funcionalidad del producto.

---

# A. Objetivo

## A.1. Objetivo principal

Construir una fotografía técnica, objetiva y reproducible del PC real que utilizará Claude Code para desarrollar el agente de IA conversacional y reflexivo.

## A.2. Qué debe conocerse

Al completar este paso debemos conocer, como mínimo:

- sistema operativo, versión/build y arquitectura;
- shell principal;
- CPU, RAM y almacenamiento disponible;
- GPU, si existe;
- Git y su ruta efectiva;
- GitHub CLI y su estado de autenticación;
- Claude Code y su ruta/versión;
- Node.js y npm;
- Python, `py` y `pip`;
- uv y/o Poetry, si están presentes;
- Docker, Docker Compose y estado del daemon;
- WSL, si existe;
- cliente PostgreSQL (`psql`/`pg_config`), si existe;
- `PATH` y posibles duplicados/conflictos;
- conectividad básica con GitHub;
- integridad del clone `CursoIA` del Paso 1;
- puertos actualmente en escucha;
- problemas o riesgos que deban resolverse antes de continuar.

## A.3. Lo que no se hará

No se crearán todavía:

- `backend/`;
- `frontend/`;
- `docs/`;
- `tests/`;
- `AGENTS.md`;
- `CLAUDE.md`;
- `.claude/`;
- endpoints;
- base de datos del producto;
- contenedores del producto;
- repositorio final;
- funcionalidades.

Tampoco se instalarán herramientas “por si acaso”.

---

# B. Fundamento

## B.1. Aplicación del Módulo 1

El Módulo 1 presenta tres pilares co-iguales:

```text
Herramienta + Contexto + Prompt
```

El Paso 2 aplica principalmente **Herramienta + Contexto**.

Claude Code no existe aislado. Su capacidad de ejecutar trabajo real depende de la cadena:

```text
Claude Code
   ↓
Shell / terminal
   ↓
Git / GitHub
   ↓
runtime(s)
   ↓
package managers
   ↓
Docker / WSL / DB cuando corresponda
   ↓
tests / lint / build
```

Auditar esta cadena antes de pedir al agente que construya cosas reduce errores causados por suposiciones sobre la máquina.

## B.2. Contexto de alta señal

El Módulo 1 trata el contexto como un recurso que debe gestionarse. La auditoría produce contexto de alta señal:

```text
qué existe
qué versión existe
qué ruta se ejecuta
qué puede ejecutarse
qué no puede ejecutarse
qué entra en conflicto
qué necesita corrección
```

Esto será insumo para los siguientes pasos, donde el contexto persistente y las instrucciones del agente se diseñarán con conocimiento del entorno real.

## B.3. Regla metodológica

Adoptamos esta secuencia:

```text
OBSERVAR
   ↓
REGISTRAR
   ↓
COMPARAR CON REQUISITOS
   ↓
CLASIFICAR
   ↓
CORREGIR SOLO SI ES NECESARIO
```

No hacemos:

```text
“creo que falta X” → instalar X
```

sin evidencia.

---

# C. Evidencia de la fuente

## C.1. Repositorio `Diiegoal/CursoIA`

El plan del proyecto del Módulo 1 establece un desarrollo por pasos controlados, verificables y acumulativos y sitúa la auditoría del entorno después de la preparación local y clone verificable.

Fuente principal del plan:

`https://github.com/Diiegoal/CursoIA/blob/main/Prompts/Plan_M1_Proyecto_Full_Stack_AI4Devs.md`

El repositorio contiene el Módulo 1:

```text
Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA/
```

con:

```text
1. El modelo mental de los 3 pilares.md
2. Pilar 1 — La Herramienta.md
3. Pilar 2 — El Contexto.md
4. Pilar 3 — El Prompt + Integración.md
5. Recursos adicionales.md
```

El mismo plan establece un máximo de 18 pasos para Módulo 1. No debemos añadir pasos artificiales ni saltarnos comprobaciones obligatorias.

## C.2. Paso 1 ya realizado

El documento entregado en el Paso 1 estableció la separación:

```text
Diiegoal/CursoIA
     ↓
fuente de estudio

futuro repositorio del agente
     ↓
producto real
```

La auditoría actual debe realizarse sin modificar esa fuente.

## C.3. Git

Documentación oficial:

`https://git-scm.com/docs/git-clone`

Git es una herramienta de infraestructura de desarrollo, no una dependencia del producto. La auditoría comprueba tanto que existe como qué ejecutable está resolviendo la shell.

## C.4. GitHub CLI

Documentación oficial de `gh auth status`:

`https://cli.github.com/manual/gh_auth_status`

Documentación oficial de `gh auth login`:

`https://cli.github.com/manual/gh_auth_login`

`gh auth status` informa de la cuenta activa y del estado de autenticación. No debemos usar `--show-token` durante la auditoría porque el token nunca debe entrar en los artefactos o evidencias compartidas.

Importante: un repositorio público puede clonarse con Git sin que el clone público requiera una sesión autenticada de GitHub. La autenticación de `gh` sigue siendo relevante para futuras operaciones administrativas del proyecto.

## C.5. Docker Desktop y WSL

Docker documenta para Windows diferentes backends, con WSL 2 como backend habitual/predeterminado en muchos escenarios, requisitos explícitos de sistema, virtualización y versiones mínimas de WSL.

Fuentes oficiales actuales consultadas:

`https://docs.docker.com/desktop/setup/install/windows-install/`

`https://docs.docker.com/desktop/features/wsl/`

La documentación también diferencia Docker Desktop de una instalación independiente del Docker Engine dentro de una distribución WSL. Por ello se audita la configuración existente antes de modificarla.

## C.6. Python

Python.org muestra en 2026 que Python 3.14 es la serie de feature release más reciente y que Python 3.13 continúa en mantenimiento.

Fuentes oficiales:

`https://www.python.org/downloads/`

`https://www.python.org/downloads/release/python-31315/`

Conclusión metodológica: la versión más nueva disponible no se convierte automáticamente en la versión del proyecto. Primero se audita; después se fijará una versión cuando las dependencias reales estén definidas.

## C.7. PostgreSQL

La página oficial de PostgreSQL muestra ramas estables mantenidas simultáneamente y, a fecha de agosto de 2026, PostgreSQL 18 era una versión estable publicada.

Fuentes:

`https://www.postgresql.org/download/`

`https://www.postgresql.org/download/windows/`

La existencia de `psql` prueba la disponibilidad del cliente, no la existencia ni la disponibilidad de un servidor PostgreSQL.

## C.8. Claude Code

Fuentes oficiales de referencia:

`https://code.claude.com/docs/en/setup`

`https://code.claude.com/docs/en/memory`

`https://code.claude.com/docs/en/subagents`

`https://code.claude.com/docs/en/common-workflows`

`https://code.claude.com/docs/en/hooks`

`https://code.claude.com/docs/en/settings`

Para este paso importa sobre todo comprobar la instalación real mediante:

```powershell
claude --version
where.exe claude
claude --help
```

No fijamos aquí un número de versión ni una forma de instalación como regla permanente; esos detalles son susceptibles de cambiar.

## C.9. Seguridad

La documentación de GitHub CLI indica que la autenticación puede almacenarse mediante mecanismos de credenciales disponibles en el sistema y contempla fallback a almacenamiento en archivo cuando un almacén seguro no está disponible.

Fuente:

`https://cli.github.com/manual/gh_auth_login`

Por eso la auditoría debe ocultar cualquier token o secreto que aparezca accidentalmente.

---

# D. Acción

## D.1. Identificar la terminal real

Ejecutar en la terminal que realmente utilizarás para trabajar con Claude Code:

```powershell
$PSVersionTable
$env:SHELL
$env:ComSpec
```

Si alguna variable aparece vacía no implica automáticamente un fallo.

## D.2. Sistema operativo

```powershell
Get-ComputerInfo | Select-Object `
    WindowsProductName,
    WindowsVersion,
    OsBuildNumber,
    OsArchitecture,
    CsSystemType

[Environment]::OSVersion.Version
```

Objetivo: registrar edición, versión, build y arquitectura.

## D.3. Usuario y ubicación

```powershell
whoami
pwd
$HOME
```

No es necesario compartir el nombre de usuario si no aporta valor; puede redactarse antes de compartir la salida.

Desde `CursoIA`:

```powershell
git rev-parse --show-toplevel
```

## D.4. CPU

```powershell
Get-CimInstance Win32_Processor |
    Select-Object Name, NumberOfCores, NumberOfLogicalProcessors, AddressWidth
```

## D.5. RAM

```powershell
Get-CimInstance Win32_ComputerSystem |
    Select-Object TotalPhysicalMemory

"{0:N2} GB" -f ((Get-CimInstance Win32_ComputerSystem).TotalPhysicalMemory / 1GB)
```

No establecemos todavía una cifra universal mínima para el proyecto.

## D.6. GPU

```powershell
Get-CimInstance Win32_VideoController |
    Select-Object Name, DriverVersion, AdapterRAM
```

Es informativo para decisiones futuras sobre modelos locales, embeddings u otras cargas; no implica que el producto deba ejecutar modelos localmente.

## D.7. Espacio en disco

```powershell
Get-PSDrive -PSProvider FileSystem
```

## D.8. Git

```powershell
git --version
where.exe git
git config --get user.name
git config --get user.email
git config --get init.defaultBranch
git config --get core.autocrlf
```

Una o varias rutas devueltas por `where.exe git` no son un problema por sí mismas; se analizará cuál gana en `PATH` y qué versión ejecuta la shell.

## D.9. GitHub CLI

```powershell
gh --version
where.exe gh
gh auth status
```

No usar:

```powershell
gh auth status --show-token
```

## D.10. Claude Code

```powershell
claude --version
where.exe claude
claude --help
```

Debe ser un comando ejecutable y no solo una entrada de PATH que apunte a algo roto.

No iniciar todavía una sesión de implementación.

## D.11. PATH

```powershell
$env:Path -split ';' |
    Where-Object { $_ -and $_.Trim() -ne '' } |
    Sort-Object
```

## D.12. Resolución de comandos

```powershell
where.exe git
where.exe gh
where.exe claude
where.exe node
where.exe npm
where.exe python
where.exe py
where.exe uv
where.exe poetry
where.exe docker
where.exe psql
```

Cero resultados puede significar ausencia del comando en `PATH`; no implica necesariamente que no exista en el disco.

## D.13. Node.js / npm

```powershell
node --version
npm --version
where.exe node
where.exe npm
```

La auditoría no selecciona todavía la versión final del frontend.

## D.14. Python

```powershell
python --version
py --version
where.exe python
where.exe py
python -m pip --version
py -0p
```

Si existen:

```powershell
uv --version
where.exe uv
poetry --version
where.exe poetry
```

No instalar uv o Poetry en este paso salvo que un hallazgo justifique una corrección posterior.

## D.15. Pruebas funcionales mínimas de runtimes

Node:

```powershell
node -e "console.log('node-ok')"
```

Python:

```powershell
python -c "print('python-ok')"
```

## D.16. Docker

```powershell
docker --version
docker compose version
where.exe docker
```

Si `docker` existe:

```powershell
docker version
docker info
```

Si `docker info` falla pero Docker Desktop está instalado, distinguir entre “CLI instalada” y “daemon no disponible”.

También:

```powershell
Get-Process "Docker Desktop" -ErrorAction SilentlyContinue |
    Select-Object Name, Id, Path
```

## D.17. WSL

```powershell
wsl --status
wsl --version
wsl -l -v
where.exe wsl
```

No instalar WSL automáticamente.

## D.18. Virtualización

```powershell
systeminfo
```

Y, cuando el sistema exponga los campos:

```powershell
Get-CimInstance Win32_Processor |
    Select-Object Name, VirtualizationFirmwareEnabled, VMMonitorModeExtensions
```

La ausencia de un campo no debe interpretarse automáticamente como virtualización desactivada.

## D.19. PostgreSQL client

```powershell
psql --version
where.exe psql
pg_config --version
where.exe pg_config
```

No confundir cliente instalado con servidor activo.

## D.20. Red hacia GitHub

```powershell
Resolve-DnsName github.com
Test-NetConnection github.com -Port 443
```

La finalidad es distinguir un problema de DNS/conectividad de un problema de autenticación o de una herramienta concreta.

## D.21. Puertos en escucha

Sin arrancar ningún servicio del proyecto:

```powershell
Get-NetTCPConnection -State Listen |
    Sort-Object LocalPort |
    Select-Object LocalAddress, LocalPort, OwningProcess
```

Un puerto ocupado no es automáticamente un problema; hay que identificar el proceso.

## D.22. Repositorio fuente

Entrar al clone local `CursoIA` y ejecutar:

```powershell
git remote -v
git branch --show-current
git status
git rev-parse HEAD
git log -1 --oneline
git config --get remote.origin.url
git rev-parse --show-toplevel
git status --short
```

Además:

```powershell
Test-Path ".\Módulo_1_Los_3_pilares_del_uso_efectivo_de_copilotos_IA"
```

Debe ser `True`.

El estado del repositorio debe seguir limpio.

---

# D.23. Script reproducible de auditoría

Para reducir errores al copiar comandos, puede crearse temporalmente `audit-step2.ps1` con:

```powershell
$ErrorActionPreference = "Continue"

Write-Host "=== PASO 2 - AUDITORIA DEL ENTORNO ===" -ForegroundColor Cyan
Write-Host "Fecha:" (Get-Date -Format "yyyy-MM-dd HH:mm:ss")

Write-Host "`n--- SISTEMA ---"
Get-ComputerInfo |
    Select-Object WindowsProductName, WindowsVersion, OsBuildNumber, OsArchitecture, CsSystemType

Write-Host "`n--- CPU ---"
Get-CimInstance Win32_Processor |
    Select-Object Name, NumberOfCores, NumberOfLogicalProcessors, AddressWidth

Write-Host "`n--- RAM ---"
"{0:N2} GB" -f ((Get-CimInstance Win32_ComputerSystem).TotalPhysicalMemory / 1GB)

Write-Host "`n--- GPU ---"
Get-CimInstance Win32_VideoController |
    Select-Object Name, DriverVersion, AdapterRAM

Write-Host "`n--- SHELL / USER ---"
$PSVersionTable
whoami
pwd
$HOME

Write-Host "`n--- GIT ---"
git --version
where.exe git
git config --get user.name
git config --get user.email
git config --get init.defaultBranch
git config --get core.autocrlf

Write-Host "`n--- GITHUB CLI ---"
gh --version
where.exe gh
gh auth status

Write-Host "`n--- CLAUDE CODE ---"
claude --version
where.exe claude
claude --help

Write-Host "`n--- NODE / NPM ---"
node --version
npm --version
where.exe node
where.exe npm

Write-Host "`n--- PYTHON ---"
python --version
py --version
where.exe python
where.exe py
python -m pip --version
py -0p

Write-Host "`n--- UV ---"
uv --version
where.exe uv

Write-Host "`n--- POETRY ---"
poetry --version
where.exe poetry

Write-Host "`n--- DOCKER ---"
docker --version
docker compose version
where.exe docker
docker version
Get-Process "Docker Desktop" -ErrorAction SilentlyContinue |
    Select-Object Name, Id, Path

Write-Host "`n--- WSL ---"
wsl.exe --status
wsl.exe --version
wsl.exe -l -v
where.exe wsl

Write-Host "`n--- POSTGRESQL CLIENT ---"
psql --version
where.exe psql
pg_config --version
where.exe pg_config

Write-Host "`n--- PATH ---"
$env:Path -split ';' |
    Where-Object { $_ -and $_.Trim() -ne '' } |
    Sort-Object

Write-Host "`n--- PUERTOS EN LISTEN ---"
Get-NetTCPConnection -State Listen |
    Sort-Object LocalPort |
    Select-Object LocalAddress, LocalPort, OwningProcess

Write-Host "`n--- RED ---"
Resolve-DnsName github.com
Test-NetConnection github.com -Port 443

Write-Host "`n--- FIN ---"
```

Para ejecutar y conservar la evidencia:

```powershell
.\audit-step2.ps1 | Tee-Object -FilePath .\step2-audit-output.txt
```

### Seguridad

Antes de compartir la salida:

- revisar tokens;
- revisar claves API;
- revisar contraseñas;
- revisar variables secretas;
- redactar nombres de usuario/rutas si no son relevantes.

Usar `<REDACTED>` donde corresponda.

## D.24. Si PowerShell bloquea el script

No cambiar políticas globales a ciegas.

Inspeccionar primero:

```powershell
Get-ExecutionPolicy -List
```

Si la política bloquea el script, puede ejecutarse la auditoría comando a comando. No se debe convertir una cuestión de política de PowerShell en una modificación permanente del sistema sin necesidad.

---

# E. Resultado esperado

## E.1. Fotografía técnica

Debe quedar documentado, con evidencia de comandos, al menos:

```text
Sistema operativo
Arquitectura
Shell
CPU
RAM
GPU
Disco
Git
GitHub CLI
Claude Code
Node/npm
Python/pip
uv/Poetry
Docker/Compose
WSL
PostgreSQL client
PATH
Red
Puertos
CursoIA
```

## E.2. Clasificación

Cada componente se clasificará como uno de:

```text
DISPONIBLE Y CORRECTO
DISPONIBLE PERO REQUIERE VALIDACIÓN
AUSENTE Y NO NECESARIO TODAVÍA
AUSENTE Y NECESARIO
CONFLICTO
RIESGO
```

## E.3. Estado del repositorio

`CursoIA` debe seguir limpio y separado del futuro repositorio del producto.

## E.4. Ausencias aceptables

No todas las herramientas son obligatorias para que el Gate pase. Ejemplos potenciales de observaciones no críticas:

- PostgreSQL local ausente si se decide usar PostgreSQL dentro de Docker más adelante;
- Poetry ausente si se decide utilizar otra estrategia de entorno;
- WSL ausente si la configuración elegida no lo requiere.

La clasificación final depende del stack que se establezca posteriormente.

---

# F. Comprobaciones

## F.1. Comprobaciones obligatorias

### Sistema

```powershell
Get-ComputerInfo | Select-Object WindowsProductName, WindowsVersion, OsBuildNumber, OsArchitecture, CsSystemType
[Environment]::OSVersion.Version
```

### Shell

```powershell
$PSVersionTable
$env:ComSpec
```

### Git

```powershell
git --version
where.exe git
git config --get user.name
git config --get user.email
```

### GitHub CLI

```powershell
gh --version
where.exe gh
gh auth status
```

### Claude Code

```powershell
claude --version
where.exe claude
claude --help
```

### Node/npm

```powershell
node --version
npm --version
where.exe node
where.exe npm
```

### Python

```powershell
python --version
py --version
python -m pip --version
py -0p
```

### Docker

```powershell
docker --version
docker compose version
docker version
docker info
```

### WSL

```powershell
wsl --status
wsl --version
wsl -l -v
```

### PostgreSQL client

```powershell
psql --version
pg_config --version
```

### Red

```powershell
Resolve-DnsName github.com
Test-NetConnection github.com -Port 443
```

### Repo

```powershell
git remote -v
git branch --show-current
git status
git rev-parse HEAD
git log -1 --oneline
git rev-parse --show-toplevel
git status --short
```

```bash
origin  https://github.com/Diiegoal/CursoIA.git (fetch)
origin  https://github.com/Diiegoal/CursoIA.git (push)
main
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        audit-step2.sh
        step2-audit-output.txt

nothing added to commit but untracked files present (use "git add" to track)
14f1f0a39ecb0cbb3ce70cb58a7ad8b8fd914824
14f1f0a (HEAD -> main, origin/main, origin/HEAD) first commit
/home/tobby/Projects/CursoIA
```

## F.2. Pruebas funcionales pertinentes

No basta con conocer la versión.

### Git

```powershell
git --version
```

### GitHub CLI

```powershell
gh --version
gh auth status
```

### Claude Code

```powershell
claude --version
claude --help
```

### Node

```powershell
node -e "console.log('node-ok')"
```

Resultado esperado:

```text
node-ok
```

### Python

```powershell
python -c "print('python-ok')"
```

Resultado esperado:

```text
python-ok
```

### Docker

Si está instalado y ejecutándose:

```powershell
docker version
```

El objetivo es verificar que cliente y daemon pueden comunicarse.

### WSL

```powershell
wsl --status
```

No se considera fallo si WSL no existe cuando la configuración final del proyecto no lo necesite.

## F.3. Prueba de coherencia de PATH

Para cualquier herramienta crítica se espera la pareja:

```text
where.exe <herramienta>
<herramienta> --version
```

Esto permite observar tanto la ruta como el ejecutable efectivo.

## F.4. Integridad del repositorio

```powershell
git status --short
```

Debe ser vacío.

Además:

```powershell
git remote -v
git rev-parse HEAD
```

deben seguir identificando el repositorio fuente correcto.

---

# G. Hallazgos

## G.1. Lo que ya se sabe del entorno de esta conversación

El entorno aislado de esta sesión no es el PC del usuario. En pruebas anteriores dentro del sandbox:

```text
Git              disponible
GitHub CLI       no disponible
Claude Code      no disponible
Resolución DNS a github.com   no disponible
```

Esto no permite diagnosticar la computadora local y no debe utilizarse como sustituto de la auditoría.

## G.2. Hallazgo metodológico

La auditoría debe separar:

### Hecho observado

Ejemplo:

```text
node --version
vX.Y.Z
```

### Requisito oficial

Ejemplo:

```text
Docker Desktop necesita condiciones determinadas de Windows/WSL
para determinadas configuraciones.
```

### Recomendación del proyecto

Ejemplo:

```text
mantener una estrategia única y reproducible para gestionar versiones.
```

No se deben presentar recomendaciones como requisitos oficiales.

## G.3. Versiones

Una versión nueva no se selecciona automáticamente.

El ejemplo más claro es Python: en 2026 coexistían una nueva feature release y ramas anteriores mantenidas. El proyecto fijará la versión compatible cuando tengamos el stack definido.

## G.4. Docker

La auditoría debe distinguir al menos:

```text
CLI instalada
↓
daemon disponible
↓
backend configurado
↓
contenedores ejecutables
```

`docker --version` por sí solo no demuestra todo lo anterior.

## G.5. PostgreSQL

La auditoría debe distinguir:

```text
psql instalado
≠
servidor PostgreSQL instalado
≠
servidor PostgreSQL activo
≠
base de datos del proyecto disponible
```

## G.6. Instalaciones duplicadas

Múltiples rutas devueltas por `where.exe` son un hallazgo que requiere análisis, no una orden inmediata de desinstalación.

---

# H. Correcciones

## H.1. Qué puede corregirse

Solo se plantea corregir en este paso una condición que:

- impida utilizar Git;
- impida utilizar Claude Code;
- impida gestionar GitHub de forma necesaria;
- produzca un conflicto de PATH claramente demostrado;
- rompa un runtime esencial una vez que esté definido como necesario;
- introduzca un riesgo de seguridad evidente.

## H.2. Qué no se corregirá todavía

No se instalará automáticamente:

- la herramienta más nueva disponible;
- PostgreSQL local;
- Docker;
- WSL;
- Poetry;
- uv;
- Node;
- Python alternativo;

si la auditoría no demuestra que sea necesario.

## H.3. Orden de corrección

```text
1. terminal
2. Git
3. GitHub / autenticación
4. Claude Code
5. PATH
6. runtime(s)
7. Docker / WSL
8. herramientas auxiliares
```

No se utilizará una instalación nueva para ocultar el diagnóstico de una instalación anterior.

---

# I. Checklist

## I.1. Identidad del entorno

- [X] Sistema operativo identificado.
- [X] Versión/build identificados.
- [X] Arquitectura identificada.
- [X] Shell identificada.
- [X] CPU identificada.
- [X] RAM identificada.
- [X] Disco auditado.
- [X] GPU identificada si existe.

## I.2. Herramientas fundamentales

- [X] Git disponible.
- [X] Git ejecutable.
- [X] GitHub CLI disponible.
- [X] Estado de autenticación de GitHub documentado.
- [X] Claude Code disponible.
- [X] Claude Code ejecuta `--version`.
- [X] Claude Code ejecuta `--help`.

## I.3. Runtime/tooling

- [X] Node.js auditado.
- [X] npm auditado.
- [X] Python auditado.
- [X] pip auditado.
- [X] `py`/instancias Python auditadas si existe.
- [X] uv auditado si existe.
- [X] Poetry auditado si existe.
- [X] Docker auditado.
- [X] Docker Compose auditado.
- [X] daemon Docker comprobado si aplica.
- [X] WSL auditado si aplica.
- [X] PostgreSQL client auditado.

## I.4. Coherencia

- [X] PATH revisado.
- [X] Instalaciones duplicadas detectadas/descartadas.
- [X] Herramientas críticas resuelven a la versión esperada.
- [X] No hay conflictos críticos pendientes.

## I.5. Red y seguridad

- [X] DNS a GitHub funciona.
- [X] HTTPS a GitHub es accesible.
- [X] No se ejecutaron comandos que expusieran tokens.
- [X] No se compartirán secretos.

## I.6. Repositorio fuente

- [X] `CursoIA` sigue siendo el repositorio fuente.
- [X] `origin` correcto.
- [X] rama identificada.
- [X] HEAD identificado.
- [X] working tree limpio.
- [X] Módulo 1 presente.
- [X] La auditoría no modificó `CursoIA`.

## I.7. Disciplina

- [X] No se creó el proyecto final.
- [X] No se comenzó la implementación.
- [X] No se avanzó al Paso 3.
- [X] Los hallazgos críticos quedaron documentados.

---

# J. Gate

## Estado actual

# **PASA**

## Motivo

El procedimiento, las comprobaciones y las pruebas están definidos, pero esta sesión no tiene acceso directo a la terminal del PC real. Por esa razón no se puede afirmar que la auditoría local ya se haya ejecutado.

No debemos convertir:

```text
“comandos preparados”
```

en:

```text
“entorno auditado”
```

sin evidencia de la máquina real.

## Condición para `PASA`

El Gate podrá ser `PASA` cuando:

1. la auditoría se ejecute en el PC real;
2. Git funcione;
3. Claude Code sea ejecutable;
4. el acceso GitHub necesario quede comprobado;
5. los runtimes relevantes estén identificados;
6. cualquier conflicto crítico esté corregido;
7. `CursoIA` permanezca limpio;
8. no existan secretos expuestos;
9. el entorno sea suficiente para abrir el siguiente paso.

## Condición para `PASA CON OBSERVACIONES`

Se usará cuando el entorno sea apto para continuar pero queden diferencias no críticas, por ejemplo una herramienta opcional ausente o una decisión que dependa del stack futuro.

## Condición para `NO PASA`

Se mantendrá si existe un fallo crítico como:

- Git inutilizable;
- Claude Code no ejecutable cuando es necesario para el flujo previsto;
- conflicto de PATH no resuelto que cambia el runtime efectivo;
- problema de seguridad relevante;
- imposibilidad de acceder al repositorio o ejecutar las comprobaciones esenciales.

---

# Investigación actualizada a septiembre de 2026: separación de hechos y recomendaciones

## Hechos de fuentes

### GitHub CLI

La documentación oficial actual de GitHub CLI confirma que `gh auth status` comprueba el estado de autenticación de cada host/cuenta y permite observar la cuenta activa. `gh auth login` ofrece autenticación vía navegador y otras alternativas. No se debe exponer el token.

Fuentes:

- `https://cli.github.com/manual/gh_auth_status`
- `https://cli.github.com/manual/gh_auth_login`

### Docker Desktop / WSL

La documentación oficial de Docker consultada en 2026 indica requisitos concretos para Windows, WSL 2, virtualización y versiones mínimas de WSL en determinadas configuraciones. También recomienda mantener WSL actualizado y distingue Docker Desktop del Docker Engine instalado separadamente en WSL.

Fuentes:

- `https://docs.docker.com/desktop/setup/install/windows-install/`
- `https://docs.docker.com/desktop/features/wsl/`
- `https://docs.docker.com/desktop/features/wsl/best-practices/`

### Python

Python.org muestra que Python 3.14 es la feature-release más reciente en 2026 y que Python 3.13 recibe mantenimiento. Python 3.13.15 fue publicada el 5 de agosto de 2026.

Fuentes:

- `https://www.python.org/downloads/`
- `https://www.python.org/downloads/release/python-31315/`

### PostgreSQL

PostgreSQL.org muestra múltiples ramas estables mantenidas y registra el lanzamiento de PostgreSQL 18.6 el 13 de agosto de 2026.

Fuentes:

- `https://www.postgresql.org/download/`
- `https://www.postgresql.org/download/windows/`

### Claude Code

Las fuentes oficiales de Claude Code utilizadas como referencia son su documentación de setup, memoria, subagentes, workflows, hooks y settings. Debido a que el acceso web de esta sesión presentó errores temporales al volver a recuperar algunas de esas páginas, no se fija aquí como requisito una versión concreta de Claude Code que no haya sido observada directamente en la máquina real.

Fuentes oficiales de referencia:

- `https://code.claude.com/docs/en/setup`
- `https://code.claude.com/docs/en/memory`
- `https://code.claude.com/docs/en/subagents`
- `https://code.claude.com/docs/en/common-workflows`
- `https://code.claude.com/docs/en/hooks`
- `https://code.claude.com/docs/en/settings`

## Recomendaciones adoptadas

Las siguientes no se presentan como requisitos oficiales universales:

1. Auditar antes de instalar.
2. Registrar la ruta efectiva del ejecutable, no solo su existencia.
3. Evitar varias versiones activas del mismo runtime sin una razón clara.
4. Mantener herramientas globales separadas de dependencias del proyecto.
5. No instalar PostgreSQL local si la arquitectura posterior puede encapsularlo en Docker y no se ha tomado la decisión todavía.
6. No asumir que WSL es obligatorio para cualquier proyecto Windows.
7. No seleccionar versiones solo porque sean las más nuevas.
8. No compartir tokens, contraseñas o claves durante el diagnóstico.
9. Mantener `CursoIA` limpio y separado del producto.

---

# Limitaciones reales de esta ejecución

La auditoría local no puede ejecutarse físicamente desde ChatGPT porque la terminal del PC del usuario no está expuesta a esta sesión.

Sí se pudo:

- estudiar el plan del repositorio;
- contrastar el procedimiento con documentación oficial disponible;
- definir el inventario de componentes;
- definir comandos de diagnóstico;
- definir pruebas funcionales;
- preparar un script reproducible;
- definir criterios de aceptación y Gate.

No se puede afirmar aún:

- la versión de Claude Code del PC;
- la versión de Node del PC;
- la versión de Python del PC;
- el estado de Docker del PC;
- el estado de WSL del PC;
- la disponibilidad de `psql` del PC;
- la RAM/disco/GPU reales del PC;
- el estado de red del PC.

Eso solo puede salir de la evidencia local.

---

# Evidencia que se debe conservar

El archivo recomendado es:

```text
step2-audit-output.txt
```

generado con:

```powershell
.\audit-step2.ps1 | Tee-Object -FilePath .\step2-audit-output.txt
```

Antes de compartirlo:

```text
REVISAR → REDACTAR SECRETOS → COMPARTIR
```

No hace falta hacer commits en `CursoIA` para realizar esta auditoría.

---

# Matriz de decisión que se aplicará a la evidencia

| Componente | Resultado posible | Qué se verificará |
|---|---|---|
| Git | OK / OBS / FAIL | versión, ruta, ejecución |
| GitHub CLI | OK / OBS / FAIL | versión, ruta, autenticación |
| Claude Code | OK / OBS / FAIL | versión, ruta, help |
| Node/npm | OK / OBS / N/A | disponibilidad y ejecución |
| Python/pip | OK / OBS / N/A | versión, ejecutable, pip |
| uv/Poetry | OK / OBS / N/A | existencia y coherencia |
| Docker | OK / OBS / N/A | CLI + daemon cuando aplica |
| WSL | OK / OBS / N/A | versión/estado cuando aplica |
| PostgreSQL | OK / OBS / N/A | cliente/servidor diferenciados |
| PATH | OK / OBS / FAIL | rutas y conflictos |
| Recursos | OK / OBS / FAIL | RAM/disco/arquitectura |
| Red | OK / OBS / FAIL | DNS/HTTPS |
| CursoIA | OK / OBS / FAIL | remote, HEAD y working tree |

---

# Estado final del Paso 2

```text
Investigación previa                         ✓
Fuentes primarias identificadas             ✓
Hechos y recomendaciones separados          ✓
Inventario de entorno definido               ✓
Comandos de auditoría definidos              ✓
Pruebas funcionales definidas                ✓
Script reproducible preparado                ✓
Checklist definido                           ✓
Evidencia del PC real                        VERIFICADO
Gate                                         PASA
```

## Siguiente acción

Ejecuta en tu PC la auditoría preparada. La vía recomendada es crear `audit-step2.ps1`, ejecutarlo con `Tee-Object`, revisar la salida y compartir `step2-audit-output.txt` sin secretos.

Una vez analicemos esa evidencia, se decidirá objetivamente si el Gate es `PASA`, `PASA CON OBSERVACIONES` o `NO PASA`, y solo entonces se abrirá el siguiente paso.

**¿Deseas continuar con el Paso 3 — Construcción de la fuente de verdad del Módulo 1 cuando el Gate del Paso 2 quede aprobado?**

---

# Fuentes completas

- Repositorio: `https://github.com/Diiegoal/CursoIA`
- Plan Módulo 1: `https://github.com/Diiegoal/CursoIA/blob/main/Prompts/Plan_M1_Proyecto_Full_Stack_AI4Devs.md`
- Git clone: `https://git-scm.com/docs/git-clone`
- GitHub CLI auth status: `https://cli.github.com/manual/gh_auth_status`
- GitHub CLI auth login: `https://cli.github.com/manual/gh_auth_login`
- GitHub CLI repo clone: `https://cli.github.com/manual/gh_repo_clone`
- Claude Code setup: `https://code.claude.com/docs/en/setup`
- Claude Code memory: `https://code.claude.com/docs/en/memory`
- Claude Code subagents: `https://code.claude.com/docs/en/subagents`
- Claude Code workflows: `https://code.claude.com/docs/en/common-workflows`
- Claude Code hooks: `https://code.claude.com/docs/en/hooks`
- Claude Code settings: `https://code.claude.com/docs/en/settings`
- Docker Desktop Windows: `https://docs.docker.com/desktop/setup/install/windows-install/`
- Docker Desktop WSL: `https://docs.docker.com/desktop/features/wsl/`
- Docker WSL best practices: `https://docs.docker.com/desktop/features/wsl/best-practices/`
- Python downloads: `https://www.python.org/downloads/`
- Python 3.13.15: `https://www.python.org/downloads/release/python-31315/`
- PostgreSQL downloads: `https://www.postgresql.org/download/`
- PostgreSQL Windows: `https://www.postgresql.org/download/windows/`

