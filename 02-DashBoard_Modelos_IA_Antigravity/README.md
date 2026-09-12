# Portafolio — Kairossonn

Repositorio: **Kairossonn/Portafolio**
Rama principal: **main**
Git LFS: habilitado para archivos binarios grandes

---

## 1. Opción recomendada: clonar con Git

Recomendada si vas a trabajar o modificar el proyecto.

### Requisitos

- Git
- Git LFS

Verificar instalación:

```bash
git --version
git lfs version
```

Si Git LFS no está inicializado:

```bash
git lfs install
```

### Clonar el repositorio

Desde PowerShell:

```bash
cd D:\
git clone https://github.com/Kairossonn/Portafolio.git
cd D:\Portafolio
```

Verificar estado:

```bash
git status
```

Salida esperada:

```
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

### Verificar archivos administrados por Git LFS

El proyecto usa Git LFS para archivos binarios grandes, incluido:

```
02-DashBoard_Modelos_IA_Antigravity\DashboardInstaller.exe
```

Comprobar:

```bash
git lfs ls-files
```

---

## 2. Descargar el proyecto como ZIP (GitHub)

Adecuado solo para consultar o usar el contenido, **sin** trabajar con Git.

1. Entrar a: `https://github.com/Kairossonn/Portafolio`
2. Pulsar **Code**
3. Seleccionar **Download ZIP**
4. Descomprimir en la ubicación deseada, ej. `D:\Portafolio`

**Importante:** si vas a modificar archivos, crear commits, sincronizar cambios o trabajar con Git LFS, usa `git clone` en su lugar.

---

## 3. Descargar solamente una carpeta (Sparse Checkout)

GitHub no ofrece descarga ZIP directa de una única carpeta. Usa Sparse Checkout.

Ejemplo con la carpeta `02-DashBoard_Modelos_IA_Antigravity`:

```bash
cd D:\
git clone --filter=blob:none --no-checkout https://github.com/Kairossonn/Portafolio.git Portafolio
cd D:\Portafolio
git sparse-checkout init --cone
git sparse-checkout set 02-DashBoard_Modelos_IA_Antigravity
git checkout main
```

La carpeta quedará disponible en:

```
D:\Portafolio\02-DashBoard_Modelos_IA_Antigravity
```

Nota: para archivos administrados con Git LFS, instalar Git LFS y ejecutar `git lfs install`.

---

## 4. Actualizar una copia ya clonada

Si el repositorio ya fue clonado previamente, **no** volver a clonar.

```bash
cd D:\Portafolio
git pull origin main
git lfs pull
```

---

## 5. Flujo recomendado de trabajo

```bash
# Después de clonar
cd D:\Portafolio
git status

# Antes de comenzar a trabajar
git pull origin main

# Después de realizar cambios
git status
git add .
git commit -m "Descripción del cambio"
git push origin main
```

---

## 6. Comprobar la conexión con GitHub

```bash
git remote -v
```

Salida esperada:

```
origin  https://github.com/Kairossonn/Portafolio.git (fetch)
origin  https://github.com/Kairossonn/Portafolio.git (push)
```

Comprobar rama activa:

```bash
git branch
```

Debe mostrar:

```
* main
```

Comprobar Git LFS:

```bash
git lfs ls-files
```

---

## 7. Estructura general del proyecto

```
Portafolio/
│
├── .github/
├── .Proyecto/
├── .vscode/
│
├── 01-landing-page/
├── 02-pc-inspector/
├── 02-DashBoard_Modelos_IA_Antigravity/
├── 03-control-dash-ia/
├── 04-texto_voz_tr.../
├── 05-Proyecto_Conquer_Web/
├── 06-Figma_Project/
│
├── .gitattributes
└── ...
```

---

## 8. ¿Qué método utilizar?

| Necesidad | Método recomendado |
|---|---|
| Solo mirar o descargar el proyecto | Download ZIP |
| Trabajar y modificar el proyecto | git clone |
| Mantenerlo actualizado | git pull |
| Trabajar con archivos LFS | git clone + Git LFS |
| Descargar solamente una carpeta | Sparse Checkout |
| Contribuir al repositorio | git clone + Git |

---

## 9. Comando recomendado para este proyecto

```bash
cd D:\
git lfs install
git clone https://github.com/Kairossonn/Portafolio.git
cd D:\Portafolio
git status
git lfs ls-files
```

Con esto se obtiene una copia local completa del repositorio, incluyendo correctamente los archivos administrados por Git LFS.

---

## Método principal recomendado

- **Principal:** `git clone` + Git LFS
- **Alternativa:** `Download ZIP` (solo consulta/uso, sin edición)

**Repositorio oficial:** https://github.com/Kairossonn/Portafolio
