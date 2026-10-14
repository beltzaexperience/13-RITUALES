# 13 RITUALES · EJERCICIOS BELTZA — NOTAS DE PROYECTO

## Repositorio
```
https://github.com/beltzaexperience/13-RITUALES
https://beltzaexperience.github.io/13-RITUALES/
```

## Estructura de archivos
```
13-RITUALES/
├── index.html                     ← homepage
├── style.css                      ← estilos separados
├── NOTAS.md                       ← este archivo
├── CNAME                          ← 13rituales.beltzarecords.com
├── favicon.ico                    ← favicon 13 Rituales
├── favicon-magic-bus.ico          ← favicon Magic Bus
├── logo13.png                     ← logo 13
├── logo-p13-circle.svg            ← logo circular P13 (favicon + intro)
├── beltza-puno.png                ← puño Beltza
├── cartel-template.html           ← plantilla genérica de cartel (campos [ENTRE CORCHETES])
├── rastros-jupiter-05-26.html     ← cartel Mayo 2026
├── image.jpg                      ← foto cartel Mayo 2026
├── 29-08-26-verano-fest.html      ← cartel Verano Fest, 29/08/26
├── CHICATEQUILA-DOPAMINE.jpg      ← foto tratada cartel Verano Fest
├── 31-10-26-otono-fest.html       ← cartel Otoño Fest, 31/10/26
├── rastros-jupiter-31-10-26.jpg   ← imagen cartel Otoño Fest (dibujo Mae Jemison)
└── (futuros carteles .html)
```

## Red de proyectos Beltza Experience
| Proyecto | URL | Repo |
|---|---|---|
| Manifiesto | beltzaexperience.github.io/Manifiesto-Beltza/ | Manifiesto-Beltza |
| UR-SAPIENS | beltzaexperience.github.io/UR-SAPIENS/ | UR-SAPIENS |
| Magic Bus | beltzaexperience.github.io/magic-bus/ | magic-bus |
| 13 Rituales | beltzaexperience.github.io/13-RITUALES/ | 13-RITUALES |
| DUB²BEAT | dubbeat.beltzarecords.com | DUB2BEAT-PHOTOGRAPHY |

---

## Paleta y tipografías

### Colores
```css
--black:  #0a0a0a
--white:  #f2ede6
--red:    #b01a1a
--amber:  #c8922a
```
Intro: `#82C8E5` · Cartel: `#142240` · Fondo cartel web: `#0F4336`

### Tipografías
- **Bebas Neue** — títulos, brand slash, topband
- **Courier Prime** — cuerpo texto (justificado en intro)
- **Playfair Display** — hero, testimonios

---

## Estructura index.html

### 1. TOPBAND
`BELTZARECORDS.COM · DONOSTIA _ DONEZTEBE | MANIFIESTO · MAGIC BUS · DUB²BEAT · UR-SAPIENS`
- Bebas Neue `clamp(1.07rem,2.25vw,1.47rem)` · padding `1.1rem clamp(1rem,4vw,3rem)`
- Links ámbar · `²` rojo · `flex-wrap:wrap`

### 2. BRAND SLASH (fondo rojo, centrado)
`[logo13.png] &nbsp;&nbsp; RITUALES &nbsp;&nbsp; + &nbsp;&nbsp; EJERCICIOS &nbsp;&nbsp; [beltza-puno.png]`
- Logo 13: `clamp(3.2rem,9vw,8rem)` · RITUALES/EJERCICIOS: `.b-eventos` (caja negra texto rojo)
- `+`: blanco `clamp(5rem,14vw,12rem)`
- Puño: `beltza-puno.png` (el `index.html` lo carga desde el repo `TALLERES-HERIOTZA-`) · Todo `justify-content:center`

### 3. MARQUEE TOP — negro, texto blanco, 55s

### 4. HERO — foto completa sin recorte
- Foto: fachada Ultramarinos Parroquia 13 (Flickr)
- `.hero-eyebrow-top`: rojo negrita arriba: `Doneztebe · Nafarroa / Azken Muga of Soul`
- `.hero-title`: Playfair blanca abajo: `Rituales de CultURa Popular. / Ejercicios del Espíritu Beltza.`

### 5. INTRO — fondo `#82C8E5`, grid `2fr 1fr`
- Columna izq: label rojo + texto Courier Prime justificado `clamp(1.1rem,1.55vw,1.27rem)`
- Columna drch: logo circular P13 al 75%

### 6. PHOTO MARQUEE
- `.foto-marquee-wrap` / `.foto-marquee-track` · 60s · franjas rojas 7px
- Arranca tras `window.load` · sin pausa
- 13 fotos únicas duplicadas = 26 en track

### 7. EVENTS GRID (masonry)
- `columns:3` · gap `1.2rem` · `break-inside:avoid`
- Tarjetas: borde rojo 2px · padding 4px · pie fondo `#142240`
- Título: `flex:1` `text-overflow:ellipsis` · Link: **Ver →** ámbar `flex-shrink:0`
- Testimonios: `rgba(176,26,26,0.04)` borde ámbar · Playfair itálica blanca
- Contador dinámico (cuenta todos los `.event-card`, testimonios incluidos)
- Header: `[contador] RITUALES VUDÚ-BEAT + EJERCICIOS AFRO-ESPIRITUALES` centrado
- Botón **CRONOLÓGICO** — ordena por `data-fecha` asc/desc

### 8. MARQUEE BOTTOM — mismo que top · línea roja 4px encima

### 9. PANORÁMICA — foto ancho completo entre marquee y footer

### 10. FOOTER — clon topband · línea roja 4px encima · coords blancas

---

## Carteles en el grid (en el mismo orden que en index.html)
| data-fecha | Título | Link |
|---|---|---|
| 2026-10 | Rastros de Júpiter · Otoño Fest | `13-RITUALES/31-10-26-otono-fest.html` |
| 2026-08 | Rastros de Júpiter · Verano Fest | `13-RITUALES/29-08-26-verano-fest.html` |
| 2026-05 | Rastros de Júpiter | `13-RITUALES/rastros-jupiter-05-26.html` |
| — | *Testimonio Enriqueta* | — |
| 2026-01 | Rastros de Júpiter | beltzablog/740 |
| 2025-12 | Amairu Bizi · Ripe Red Apple | beltzablog/737 |
| 2025-09 | Talleres Heriötza | beltzablog/732 |
| 2025-03 | Amairu Bizi · NI | beltzablog/731 |
| 2025-08 | Rastros de Júpiter | beltzablog/730 |
| 2025-05 | Rastros de Júpiter | beltzablog/729 |
| — | *Testimonio Kikillo* | — |
| 2025-03 | Rastros de Júpiter (cartel) | beltzablog/726 |
| 2025-03 | La Momia Trio Ensemble | beltzablog/726 |
| 2025-01 | Amairu Bizi · Joseba Irazoki | beltzablog/723 |
| 2024-11 | Rastros de Júpiter | beltzablog/722 |
| 2024-10 | Amairu Bizi · Victor Herrero | beltzablog/721 |
| 2024-08 | El Circo de Júpiter | beltzablog/688 |

Total: 15 carteles + 2 testimonios = 17 tarjetas (el contador muestra 017).
Talleres Heriötza: 2025-09 según beltzablog/732 (publicado 23/09/25, primer taller 30/09/25).
El botón **CRONOLÓGICO** reordena por `data-fecha`.

### Testimonios intercalados
- Enriqueta (Mayo 2025) — entre Rastros Mayo 2026 y Rastros Enero 2026
- Kikillo (Mayo 2025) — entre Rastros Mayo 2025 y Rastros Marzo 2025 (cartel)

---

## Añadir nuevo cartel
0. Partir de `cartel-template.html` (rellenar campos `[ENTRE CORCHETES]`)
1. Subir `.html` o foto a repo / Flickr — nombres de archivo sin tildes ni eñes
2. Añadir tarjeta en `.events-grid` con `data-fecha="AAAA-MM"`
3. Contador sube automáticamente
4. Actualizar link en Magic Bus si tiene post

---

## Cartel rastros-jupiter-05-26.html
- Fondo web: `#0F4336` inline en `<style>` del `<head>` — sin `link` a `style.css`
- `image.jpg` desde mismo repo · viewport `width=1100` + `scaleCartel()`

## Cartel 29-08-26-verano-fest.html
- Mismo template que el cartel de mayo 2026 (fondo `#0F4336` inline, sin `link` a `style.css`)
- Evento: VERANO FEST · 29/08/26 · 11H TO 20H
- Cartel: CHICA TEQUILA · DJ (link IG `la_chica_tequila`) + DOPAMINE · LIVE (sin link — pendiente confirmar redes)
- `CHICATEQUILA-DOPAMINE.jpg` desde mismo repo — versión definitiva tratada: foto original (3024×4032) + 8 cápsulas DOPAMINE compuestas a mano (7 flotando estilo collage sobre las baldas desenfocadas de discos, respetando cara/cubetas/vestido/disco sujetado; 1 integrada como tatuaje real en el antebrazo, sin sombra, siguiendo el ángulo exacto del brazo) · viewport `width=1100` + `scaleCartel()`
- Tarjeta en `index.html` events-grid usa la versión Flickr de la foto tratada: `https://live.staticflickr.com/65535/55463708569_7021e7d973_k.jpg` ("CHICA TEQUILA + DOPAMINE")
- JPG de imprenta `verano-fest-29-08-26-IMPRIMIR.jpg` (cartel entero con foto tratada, 3300×6753px/300dpi): generado, no está en el repo
- Pendiente: si Dopamine confirma Bandcamp/redes, enlazar igual que Chica Tequila

## Cartel 31-10-26-otono-fest.html
- Creado desde `cartel-template.html` (fondo `#0F4336` inline, sin `link` a `style.css`)
- Evento: OTOÑO FEST · 31/10/26 · 11H TO 19H · eslogan SPACE IS THE PLACE
- Cartel: DJ'S · SRA. PLÁCIDA Y SR. JÚPITER (formato dúo, sin enlaces, sin live)
- `rastros-jupiter-31-10-26.jpg` desde mismo repo — dibujo de Mae Jemison sobre el pergamino de URTZ, fundido en multiplicar (1690×2576px; sustituye a la foto de la astronauta de 614×960px) · viewport `width=1100` + `scaleCartel()`
- Cartel resultante 1100×2445px (imagen más vertical que en carteles anteriores)
- Tarjeta en `index.html` usa la imagen Flickr `rastros-jupiter-31-10-26` (flic.kr/p/2sGeJCC): `https://live.staticflickr.com/65535/55589308220_b5d22ff080_k.jpg`
- Sin JPG de imprenta en esta edición

---

## Logo P13 circular
- SVG: `logo-p13-circle.svg` — fondo `#82C8E5`, borde rojo, dibujo de Luis
- JPG: `logo-p13-circle.jpg` 800x800px para archivo/Flickr
- Favicon: `<link rel="icon" href="logo-p13-circle.svg" type="image/svg+xml">`

---

## Fonema UR en rojo
```html
Cult<span style="color:#b01a1a;">ur</span>a
CULT<span style="color:#b01a1a;">UR</span>ALES
```

---

## GitHub — Seguridad
- Solo tú puedes modificar/borrar (con tu cuenta)
- Código visible en público — normal, no es riesgo

## CNAME ✓ ACTIVO
- URL definitiva: **https://13rituales.beltzarecords.com/**
- Archivo `CNAME` en repo: `13rituales.beltzarecords.com`
- DNS configurado por Karlos

## Magic Bus — Post Rastros Mayo 2026
- Link cartel: `https://beltzaexperience.github.io/13-RITUALES/rastros-jupiter-05-26.html`
- Comentario: **CLAUDIUS · Siglo I d.C. · Vía Láctea, Brazo de Orión**
- Magic Bus Nº2 · Secundus
