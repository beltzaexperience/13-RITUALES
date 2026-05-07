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
├── logo13.png                     ← logo 13
├── logo-p13-circle.svg            ← logo circular P13 (favicon + intro)
├── beltza-puno.png                ← puño Beltza
├── rastros-jupiter-05-26.html     ← cartel Mayo 2026
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
`[logo13.png] &nbsp;&nbsp; RITUALES &nbsp;&nbsp; + &nbsp;&nbsp; EJERCICIOS &nbsp;&nbsp; BELTZA &nbsp;&nbsp; [beltza-puno.png]`
- Logo 13: `clamp(3.2rem,9vw,8rem)` · RITUALES/EJERCICIOS: `.b-eventos` (caja negra texto rojo)
- `+`: blanco `clamp(5rem,14vw,12rem)` · BELTZA: sin caja negro `clamp(2.8rem,7.8vw,6.5rem)`
- Puño: `beltza-puno.png` · Todo `justify-content:center`

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
- Contador dinámico (cuenta `.event-card`)
- Header: `010 RITUALES VUDÚ-BEAT + EJERCICIOS AFRO-ESPIRITUALES` centrado
- Botón **CRONOLÓGICO** — ordena por `data-fecha` asc/desc

### 8. MARQUEE BOTTOM — mismo que top · línea roja 4px encima

### 9. PANORÁMICA — foto ancho completo entre marquee y footer

### 10. FOOTER — clon topband · línea roja 4px encima · coords blancas

---

## Carteles en el grid (orden HTML, más reciente primero)
| data-fecha | Título | Link |
|---|---|---|
| 2026-05 | Rastros de Júpiter | `13-RITUALES/rastros-jupiter-05-26.html` |
| 2026-01 | Rastros de Júpiter | beltzablog/740 |
| 2025-12 | Amairu Bizi · Ripe Red Apple | beltzablog/737 |
| 2025-08 | Talleres Heriötza | beltzablog/732 |
| 2025-08 | Rastros de Júpiter | beltzablog/730 |
| 2025-05 | Rastros de Júpiter | beltzablog/729 |
| 2025-03 | Amairu Bizi · NI | beltzablog/731 |
| 2025-03 | Rastros de Júpiter (cartel) | beltzablog/726 |
| 2025-03 | La Momia Trio Ensemble | beltzablog/726 |
| 2025-01 | Amairu Bizi · Joseba Irazoki | beltzablog/723 |
| 2024-11 | Rastros de Júpiter | beltzablog/722 |
| 2024-10 | Amairu Bizi · Victor Herrero | beltzablog/721 |
| 2024-08 | El Circo de Júpiter | beltzablog/688 |

### Testimonios intercalados
- Enriqueta (Mayo 2025) — entre Rastros Mayo 2026 y Rastros Enero 2026
- Kikillo (Mayo 2025) — al final del grid

---

## Añadir nuevo cartel
1. Subir `.html` o foto a repo / Flickr
2. Añadir tarjeta en `.events-grid` con `data-fecha="AAAA-MM"`
3. Contador sube automáticamente
4. Actualizar link en Magic Bus si tiene post

---

## Cartel rastros-jupiter-05-26.html
- Fondo web: `#0F4336` inline en `<style>` del `<head>` — sin `link` a `style.css`
- `image.jpg` desde mismo repo · viewport `width=1100` + `scaleCartel()`

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

## CNAME pendiente
- Archivo `CNAME` en repo: `13rituales.beltzarecords.com`
- Karlos DNS: CNAME `13rituales` → `beltzaexperience.github.io`
- GitHub Settings → Pages → Custom domain

## Magic Bus — Post Rastros Mayo 2026
- Link cartel: `https://beltzaexperience.github.io/13-RITUALES/rastros-jupiter-05-26.html`
- Comentario: **CLAUDIUS · Siglo I d.C. · Vía Láctea, Brazo de Orión**
- Magic Bus Nº2 · Secundus
