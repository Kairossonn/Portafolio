# PC Device Inspector (mini “Administrador de dispositivos”)

App para identificar hardware y drivers en Windows, similar al Administrador de dispositivos.

## MVP (objetivo)
- Lista todos los dispositivos PnP con:
  - Nombre, clase, fabricante (si aplica), Hardware IDs / Compatible IDs, estado
- Agrega información del driver firmado (si existe):
  - Provider, versión, fecha, INF name
- UI con búsqueda/filtros.
- Exportación a JSON/HTML.

> Nota: el detalle exacto depende de lo que permita WMI/Windows.

