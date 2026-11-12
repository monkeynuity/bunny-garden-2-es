# Bunny Garden 2 – Traducción al español / Spanish translation

**[Español](#español)** · **[English](#english)**

---

## Español

Archivos de traducción **inglés → español** no oficiales para *BUNNY GARDEN 2*, hechos para
[XUnity.AutoTranslator](https://github.com/bbepis/XUnity.AutoTranslator) + [BepInEx](https://github.com/BepInEx/BepInEx),
más un pequeño plugin listo para usar (DLL compilada) que hace que el efecto de máquina de escribir escriba directamente la línea en español.

**Versión del juego: v1.0.6.** Esta traducción es para esa versión; si el juego se actualiza, algunas líneas nuevas o cambiadas
pueden aparecer sin traducir.

Necesitas tu propia copia del juego. Este repositorio no contiene archivos del juego, solo texto traducido, una configuración y un plugin.
La traducción se hizo con ayuda de IA y se fue revisando jugando; puede haber líneas poco naturales. Las correcciones son bienvenidas.

### Qué hay aquí

| Ruta | Qué es |
|---|---|
| `BepInEx/Translation/es/Text/BG2_Dialogue_<Nombre>.txt` | Diálogos, un archivo por personaje (Haito, Kana, Rin, Erisa, Miuka, Kuon, Runa) |
| `BepInEx/Translation/es/Text/BG2_Menu_UI.txt`, `BG2_UI_Descriptions.txt`, `BG2_Narration_Texts.txt` | Menús, descripciones, narración y avisos |
| `BepInEx/Translation/es/Text/BG2_Linebreak_Variants.txt` | Las mismas entradas de varias líneas escritas con `<BR>` (el juego muestra algunos textos con `<BR>` y otros con saltos de línea reales, por eso hacen falta las dos formas) |
| `BepInEx/Translation/es/Text/BG2_Other_Strings.txt` | Textos que no están en el guion del juego (títulos, nombres de trajes, cantidades de dinero con signo…) |
| `BepInEx/Translation/es/Text/Yen.txt` | Reglas de formato del dinero |
| `BepInEx/config/` | Configuración de XUnity (español, inglés como idioma de origen) y la del plugin de máquina de escribir |
| `BepInEx/plugins/SubstringTypewriterTranslate/` | El plugin de máquina de escribir (compilado) |

Las líneas que contienen valores que el juego rellena al ejecutarse (nombre del jugador, números, dinero) se guardan como
entradas regex de XUnity, así que funciona con cualquier nombre de jugador.

### Instalación

1. Instala **BepInEx 5.4.23.6 (x64)** en la carpeta del juego (descomprímelo junto a `BUNNY GARDEN 2.exe` y ejecuta el juego una vez).
2. Instala **XUnity.AutoTranslator 5.6.3.1 (versión para BepInEx)** descomprimiéndolo en la carpeta del juego.
3. Copia la carpeta `BepInEx` de este repositorio encima de la carpeta `BepInEx` del juego (combínalas y sobrescribe cuando lo pida).
4. Inicia el juego. El texto en español aparece sin que antes se vea el inglés un instante.

El `AutoTranslatorConfig.ini` de aquí usa `Endpoint=GoogleTranslateV2` solo como respaldo para las pocas cadenas que no están
en los archivos; todo lo del guion ya está traducido sin conexión.

### Plugin de máquina de escribir

El juego construye cada fotograma del efecto de máquina de escribir como un fragmento creciente del texto en inglés
(`MessageManager.RefText(label, n)`), así que XUnity espera a que el texto termine de escribirse y la línea aparece primero en
inglés. El plugin modifica ese método para que se escriba la línea en español que ya está en la caché. La clase, el método y el
parámetro son configurables (`local.substringtypewritertranslate.cfg`), así que se puede reutilizar en otros juegos de Unity con el mismo patrón.

### Notas y aviso legal

* No oficial y sin relación con el desarrollador ni la editora del juego. Todos los derechos del juego y de su texto original
  pertenecen a sus propietarios. Si un titular de derechos lo solicita, los archivos se retirarán.
* Los nombres de los personajes, los honoríficos (-chan, -kun, -san) y los títulos de canciones y minijuegos se mantienen como en el original.

---

## English

Unofficial **English → Spanish** translation files for *BUNNY GARDEN 2*, made for
[XUnity.AutoTranslator](https://github.com/bbepis/XUnity.AutoTranslator) + [BepInEx](https://github.com/BepInEx/BepInEx),
plus a small ready-to-use plugin (compiled DLL) that makes the typewriter text effect type the Spanish line directly.

**Game version: v1.0.6.** This translation is for that version; if the game is updated, new or changed lines
may show up untranslated.

You need your own copy of the game. This repository contains no game files, only translation text, a config and a plugin.
The translation was produced with AI assistance and then proofread in play; expect some rough lines. Corrections welcome.

### What is in here

| Path | What it is |
|---|---|
| `BepInEx/Translation/es/Text/BG2_Dialogue_<Name>.txt` | Dialogue, one file per character (Haito, Kana, Rin, Erisa, Miuka, Kuon, Runa) |
| `BepInEx/Translation/es/Text/BG2_Menu_UI.txt`, `BG2_UI_Descriptions.txt`, `BG2_Narration_Texts.txt` | Menus, descriptions, narration and notices |
| `BepInEx/Translation/es/Text/BG2_Linebreak_Variants.txt` | The same multi-line entries written with `<BR>` (the game shows some text with `<BR>`, some with real line breaks, so both spellings are needed) |
| `BepInEx/Translation/es/Text/BG2_Other_Strings.txt` | Texts that are not in the game's script (titles, costume names, signed money amounts…) |
| `BepInEx/Translation/es/Text/Yen.txt` | Money formatting rules |
| `BepInEx/config/` | XUnity config (Spanish, English source) and the typewriter plugin's config |
| `BepInEx/plugins/SubstringTypewriterTranslate/` | The typewriter plugin (compiled) |

Lines that contain values the game fills in at runtime (player name, numbers, money) are stored as XUnity regex entries,
so any player name works.

### Install

1. Install **BepInEx 5.4.23.6 (x64)** into the game folder (unzip next to `BUNNY GARDEN 2.exe`, run the game once).
2. Install **XUnity.AutoTranslator 5.6.3.1 (BepInEx version)** by unzipping it into the game folder.
3. Copy this repository's `BepInEx` folder over the game's `BepInEx` folder (merge, overwrite when asked).
4. Start the game. Spanish text appears without English flashing first.

`AutoTranslatorConfig.ini` here uses `Endpoint=GoogleTranslateV2` only as a fallback for the few strings that are not in
the files; everything in the script is already translated offline.

### Typewriter plugin

The game builds each typewriter frame as a growing English substring (`MessageManager.RefText(label, n)`), so
XUnity waits for the text to settle and the line appears in English first. The plugin patches that method so the
cached Spanish line is typed instead. The target class, method and parameter are configurable
(`local.substringtypewritertranslate.cfg`), so it can be reused for other Unity games with the same pattern.

### Notes and disclaimer

* Unofficial and not affiliated with the game's developer or publisher. All rights to the game and its original text belong
  to their owners. If a rights holder asks for removal, the files will be taken down.
* Character names, honorifics (-chan, -kun, -san) and song/minigame titles are kept as in the source.

[↑ Español](#español)
