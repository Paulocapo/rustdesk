# mis_logos - Archivos de marca (White-Label)

Depositá aquí tus archivos de imagen **antes** de que el workflow de compilación los
distribuya automáticamente a las rutas del proyecto.

## Archivos requeridos

| Archivo | Formato | Tamaño recomendado | Uso |
|---------|---------|--------------------|-----|
| `icon.ico` | ICO multi-resolución | contiene 16, 24, 32, 48, 64, 128, 256 px (fuente 256x256) | Ícono del ejecutable y bandeja del sistema (Windows) |
| `logo.png` | PNG con fondo transparente | 256x256 px (o 512x512) | Logo principal de la interfaz |
| `logo.svg` | SVG vectorial | sin tamaño (vectorial) | Logo principal (versión escalable) |

## Recomendaciones

- **`icon.ico`**: generá un solo `.ico` que incluya todos los tamaños. Podés crearlo a partir
  de un PNG 256x256 con herramientas como https://icoconvert.com o ImageMagick.
- **`logo.png`**: fondo transparente para que se vea bien en modo claro y oscuro.
- Mantené el mismo nombre de archivo exacto (`icon.ico`, `logo.png`, `logo.svg`).

## Notas

- Esta carpeta es la fuente de origen (`CARPETA_LOGOS_ORIGEN` en el plan).
- El paso de rebranding (Etapa 3) copiará estos archivos a:
  - `res/icon.ico`, `res/tray-icon.ico`
  - `flutter/windows/runner/resources/app_icon.ico`
  - `flutter/assets/` (logos de la interfaz)
