# AI y Hardware DashBoard HUBS



Conexiones externas Api 

Iniciar MySQL  — Guía de Instalación

## Requisitos previos

- Windows 10/11 (64-bit)
- Conexión a internet (solo para la primera configuración de dependencias, si aplica)
- Acceso a servidor MySQL (host, puerto, usuario) — *si se usará esa fuente de datos*
- Archivo(s) de datos en formato CSV — *si se usará esa fuente de datos*

---

## Opción 1: Versión Portable (ZIP)

**Archivo:** `AIModelsDashBoard-Portable.zip`

### Instalación

1. Descargar y descomprimir `AIModelsDashBoard-Portable.zip` en la carpeta de tu preferencia (ej. `C:\AIModelsDashBoard\`).
2. No mover archivos sueltos fuera de la carpeta descomprimida — todos son necesarios.
3. Ejecutar `DashBoard.exe` (o el archivo ejecutable principal) dentro de la carpeta.
4. La app abrirá automáticamente en el navegador (o ventana propia).

### Notas

- No requiere permisos de administrador.
- No modifica el registro de Windows.
- Ideal para pruebas rápidas o uso desde USB.

---

## Opción 2: Instalador (Setup local)

**Archivo:** `DashboardInstaller.exe`

### Instalación

1. Ejecutar `DashboardInstaller.exe` como administrador (clic derecho → "Ejecutar como administrador").
2. Seguir el asistente de instalación:
   - Aceptar términos.
   - Elegir carpeta de destino (por defecto: `C:\Archivos de Programa\AIModelsDashBoard\`).
   - Confirmar instalación.
3. Al finalizar, se creará un acceso directo en el Escritorio y en el Menú Inicio.
4. Abrir la app desde el acceso directo.

### Notas

- Requiere permisos de administrador.
- Instala dependencias necesarias automáticamente (si el instalador las incluye).
- Se puede desinstalar desde "Agregar o quitar programas".

---

## Configuración de Base de Datos

La app admite dos fuentes de datos:

### CSV

- Colocar los archivos `.csv` en la carpeta `/data` (o la ruta que indique la app).
- No es necesaria configuración adicional de conexión.

### MySQL

Editar el archivo `.env` (ver plantilla en `.env.example`) con la cadena de conexión completa:

```
MYSQL_URL=mysql+pymysql://usuario:password@localhost:3306/ai_models_db

Configuración de acceso: ai_models_db es : (usuario: root / password: root12345)
```

- Pass_Default:`root12345`

> ⚠️ Reemplaza si lo deseas para BD en Local: `usuario`, `password`, `localhost:3306` y `ai_models_db` con tus datos reales de conexión.
>
> Si no defines `MYSQL_URL`, el dashboard usará el CSV local automáticamente — MySQL y CSV pueden convivir, pero el dashboard prioriza MySQL si la conexión es exitosa.
>
> Puedes también ingresar/cambiar esta conexión desde el panel superior izquierdo del DashBoard antes de explorar o filtrar los datos.
>
> Importante: hay modelos precargados; otros deberás cargarlos desde el panel izquierdo según los botones asignados. No se duplicará la carga de modelos — podrás eliminar, modificar o guardar modelos existentes, así como agregar modelos nuevos a las tablas.

> ⚠️ La clave (`DB_PASSWORD POR DEFECTO`) es genérica y **no viene incluida** en el paquete. Debe ser ingresada manualmente por el usuario en el campo indicado al momento de comenzar la instalación y dentro del DashBoard arriba a la izquierda si quieres conectar o iniciar MySQL antes de la navegación por la página de la app y antes de comenzar a filtrar y explorar los datos. MySQL y los SCV trabajan individual y simultaneo.
>
> Importante: Hay modelos precargados, otros deberas cargarlos desde el panel izquierdo segun los botones asignados. No se duplicara la carga de modelos, podras eliminar modelos existentes, modificar, guardar también asi modelos inexistentes agregarlos a los grids o tablas.

---

## Problemas comunes

| Problema                   | Solución                                                                    |
| -------------------------- | ---------------------------------------------------------------------------- |
| La app no abre             | Verificar que no falte ningún archivo de la carpeta portable / reinstalar   |
| Error de conexión a MySQL | Revisar host, puerto y clave ingresada                                       |
| No carga datos CSV         | Verificar que el archivo esté en la ruta correcta y con el formato esperado |

---


## 🔌 Integración con Hugging Face (API)



El dashboard se conecta al **endpoint público de Hugging Face** para buscar y descargar información de modelos de IA en tiempo real, complementando la base de datos local (MySQL/CSV).


### Endpoint utilizado

GET [https://huggingface.co/api/models](https://huggingface.co/api/models)



### Parámetros según el caso de uso

**Búsqueda de modelos** (función `search_hf_models`):

[huggingface.co/api/models?search={query}&amp;limit={limit}&amp;full=true](https://huggingface.co/api/models?search={query}&limit={limit}&full=true)

**Descarga masiva / Top modelos por popularidad** (función `fetch_top_hf_models`):

[huggingface.co/api/models?sort=downloads&amp;direction=-1&amp;limit={limit}&amp;full=true](https://huggingface.co/api/models?sort=downloads&direction=-1&limit={limit}&full=true)


### ¿Qué hace esta integración?

- 🔍 **Búsqueda interactiva**: desde el panel "Explorar y Añadir Modelos desde Hugging Face" puedes buscar por nombre (ej. `llama`, `deepseek`, `mistral`) y agregar los resultados a tu base local.
- 📥 **Descarga masiva**: botones de Top 150 / 250 / 500 modelos más descargados en Hugging Face, evitando duplicados contra los modelos ya existentes.
- 🆘 **Auto-recuperación**: si no encuentra ni CSV ni conexión MySQL al iniciar, el dashboard descarga automáticamente el Top 100 de Hugging Face para inicializar la base de datos.

### Autenticación

No requiere token para las consultas de lectura (`GET /api/models`), ya que es un endpoint público. Si defines `HF_TOKEN` en tu `.env` (ver `_env.example`), puedes usarlo para operaciones con límites de tasa más altos o funciones adicionales de la API.

```bash
# Variables opcionales en .env

HF_TOKEN=tu_token_aqui
HF_LIMIT=500
HF_FILTER=text-generation
```

### Ejemplo de prueba manual

```bash
curl "https://huggingface.co/api/models?search=deepseek&limit=5&full=true"
```

## Soporte

Para reportar problemas, o si deseas mejoras o agregar funcionalidades puedes dejar tu comentario. Contactar a: *(viktoremdy@gmail.com)*
