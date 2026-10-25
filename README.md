# totl-ps5-ui-mod-v143
mod para ui de the legend of zelda tears of the kingdom para mandos dualsense

# Simple PS5 UI para Tears of the Kingdom 1.4.3

Iconos de DualSense (PS5) en los textos de la interfaz de *Tears of the Kingdom* **1.4.3**.

Este mod es una **adaptación** de mods de otros autores (ver [Créditos](#créditos)). No es un mod original: lo que aporta es que funciona en 1.4.3 y un rediseño de dos iconos.

Probado en:
- **MacNativeGames** (port de TOTK para Mac), versión 1.4.3.
- **Astris** (emulador), versión 1.4.3.

## Qué hace

Los botones se asignan **por posición física**, igual que hacen los mandos PlayStation/Xbox en estos ports:

| Botón en Switch | Con este mod |
|---|---|
| A (derecha) | ○ Círculo |
| B (abajo) | ✕ Cruz |
| X (arriba) | △ Triángulo |
| Y (izquierda) | □ Cuadrado |
| L / R | L1 / R1 |
| ZL / ZR | L2 / R2 |
| Home | Logo PS |
| + | Options |
| − (abre la tableta) | Create |

## Instalación

### MacNativeGames

1. Descarga `Simple_PS5_UI_v143_v2.zip` (en *Releases*) y descomprímelo. Dentro hay una carpeta `romfs`.
2. Copia el **contenido** de `romfs/` (no la carpeta `romfs` en sí) a:
   `~/Library/Application Support/MacNativeGames/TOTK/mods/v143`
   Debe quedar con las carpetas `Font`, `System` y `UI`. Si ya tienes otro mod ahí, muévelo antes para que no se mezclen.
 
3. Genera el manifest desde la carpeta del proyecto:
   ```
   cd ~/MacNativeGames && python3.14 games/totk/scripts/make_mod_manifest.py ~/Library/Application\ Support/MacNativeGames/TOTK/mods/v143 --app "$HOME/Tears of the Kingdom.app"
   ```
   Debe decir **6 files (6 replaced, 0 added)**.
4. Si recompilas la app, vuelve a generar el manifest.
5. 
**Asistente de script:** si no sabes cómo armar estos comandos, hay una [página que los genera por ti](https://alanpiguaveruiz.github.io/totl-ps5-ui-mod-v143/). Escribes dónde está cada carpeta y te da el script listo para pegar en Terminal, incluido el manifest.

### Emuladores

en emuladores se instalan de la manera convencional. solo ha sido probado en astris y ryujinx

## Qué cambia respecto a los mods originales

- **Fuentes** (`Font/`, 4 archivos): glifos de botones del mod PS5. Los iconos de Options y Create los rediseñé (píldora con las líneas dentro, inclinada hacia el lado de cada botón).
- **Layouts y texturas** (`UI/LayoutArchive/Common.Product.140…`): sin cambios respecto al mod PS5 original.
- **Tabla de recursos** (`System/Resource/ResourceSizeTable.Product.143…`): la del mod Xbox, que ya es de 1.4.3. El mod PS5 original traía la de 1.4.2, y en mi port con ella el juego no arrancaba.

## Limitaciones

- Solo probado con 1.4.3. No es compatible con 1.4.2.

## Créditos

- **Proofeek** — autor del mod base: https://gamebanana.com/members/2122805
- **StavaasEVG** — iconos: https://gamebanana.com/members/1578286
- **mokapi47** — mod Xbox UI para 1.4.3, de donde sale la tabla de recursos: https://gamebanana.com/members/5407053
- Las líneas dentro de las píldoras están inspiradas en un mod de DualSense para *Breath of the Wild*.

## Cómo se hizo

Lo armé con ayuda de una IA (Claude). Comparé el mod PS5 (hecho para 1.4.2) con el mod Xbox (que sí funcionaba en 1.4.3): las fuentes y los layouts del mod PS5 ya coincidían con el juego 1.4.3, y lo único de 1.4.2 era la tabla de recursos, que sustituí. Los iconos de Options y Create los diseñé yo; la IA los convirtió al formato de la fuente.

## Retirar contenido

Este repositorio incluye archivos derivados de mods ajenos. Si eres autor de alguno y quieres que se retire o se cambie algo, abre un *issue* y lo atiendo.
