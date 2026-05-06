# 13 EVENTOS · EJERCICIOS BELTZA — NOTAS DE PROYECTO

## Repositorio
```
https://github.com/beltzaexperience/13-EVENTOS
https://beltzaexperience.github.io/13-EVENTOS/
```

## Estructura de archivos
```
13-EVENTOS/
├── index.html                     ← homepage 13 Eventos
├── beltza-puno.png                ← logo puño Beltza (raw GitHub)
├── rastros-jupiter-05-26.html     ← cartel Rastros de Júpiter Mayo 2026
└── (futuros carteles .html)
```

## Red de proyectos Beltza Experience
| Proyecto | URL | Repo |
|---|---|---|
| Manifiesto | beltzaexperience.github.io/Manifiesto-Beltza/ | Manifiesto-Beltza |
| UR-SAPIENS | beltzaexperience.github.io/UR-SAPIENS/ | UR-SAPIENS |
| Magic Bus | beltzaexperience.github.io/magic-bus/ | magic-bus |
| 13 Eventos | beltzaexperience.github.io/13-EVENTOS/ | 13-EVENTOS |
| DUB²BEAT | dubbeat.beltzarecords.com | DUB2BEAT-PHOTOGRAPHY |
| beltzarecords.com | www.beltzarecords.com | (servidor Karlos) |

---

## Paleta y tipografías

### Colores
```css
--black:  #0a0a0a   /* fondo principal */
--white:  #f2ede6   /* texto principal */
--red:    #b01a1a   /* rojo sangre */
--amber:  #c8922a   /* ámbar links */
--muted:  #666      /* texto secundario */
--cream:  #f0e8d8   /* fondo citas/intro */
```
Color especial intro: `#82C8E5` (azul cielo)

### Tipografías (Google Fonts)
- **Bebas Neue** — títulos, brand slash, topband, labels
- **Courier Prime** — cuerpo de texto, captions
- **Playfair Display** — títulos hero, citas literarias

---

## Estructura del index.html

### 1. TOPBAND
```
BELTZARECORDS.COM · DONOSTIA _ DONEZTEBE  |  MANIFIESTO · MAGIC BUS · DUB²BEAT · UR-SAPIENS
```
- Font: Bebas Neue `clamp(1.07rem,2.25vw,1.47rem)` · letter-spacing: 0.15em
- Padding: `1.1rem clamp(1rem,4vw,3rem)`
- Links en ámbar, `²` de DUB en rojo
- `flex-wrap: wrap` — en móvil fluye solo

### 2. BRAND SLASH (fondo rojo)
```
[logo 13]  EVENTOS  +  EJERCICIOS  BELTZA  [puño-logo]
```
- Logo 13: base64 extraído del Manifiesto · `clamp(3.2rem,9vw,8rem)`
- EVENTOS / EJERCICIOS: `.b-eventos` — Bebas Neue, caja negra, texto rojo
- `+`: blanco, `clamp(5rem,14vw,12rem)`
- BELTZA: sin caja, negro, `clamp(2.8rem,7.8vw,6.5rem)`
- Puño logo: `https://raw.githubusercontent.com/beltzaexperience/13-EVENTOS/main/beltza-puno.png`
- Todos centrados con `justify-content:center` y `&nbsp;&nbsp;` entre elementos

### 3. MARQUEE TOP (fondo negro)
- Texto blanco · `clamp(1.07rem,2.25vw,1.47rem)` · mismo padding que topband
- Contenido: BROCANTE · MÚSICA · CINE · TAROT · DISCOS · etc.

### 4. HERO (foto completa sin recorte)
- Foto: `https://live.staticflickr.com/65535/55250584412_e982256c3d_h.jpg`
  (Ultramarinos Parroquia 13, letrero verde, mesa brocante)
- **Texto arriba** en rojo negrita — `.hero-eyebrow-top`:
  ```
  Ultramarinos Parroquia 13
  Doneztebe · Nafarroa
  Azken Muga of Soul
  ```
- **Texto abajo** en blanco — `.hero-title` (Playfair itálica):
  ```
  Rituales de CultURa Popular.
  Ejercicios del Espíritu Beltza.
  ```
  (UR en rojo)

### 5. INTRO (fondo azul #82C8E5)
- Label rojo: `Ejercicios Espirituales de Cultura Popular · Doneztebe · Nafarroa`
- Cuerpo: texto Vudú-Beat, Xabatenea Etxea, Ritualismo POP, Smart Dress Style
- Sin columna izquierda, texto a ancho completo

### 6. PHOTO MARQUEE
- Franjas rojas 7px arriba y abajo
- Fotos: `clamp(180px,26vw,320px)` de alto
- `line-height:0` para eliminar línea negra inferior
- Pausable al clicar

### 7. EVENTS GRID
- Grid `auto-fill minmax(280px,1fr)` con gap 3px
- Cada tarjeta: `aspect-ratio: 2/3`, foto con overlay oscuro
- Hover: escala + oscurece
- Campos: fecha, título, subtítulo, link "Ver cartel →"

### 8. FOOTER (clon de topband)
- Misma estructura y tamaño que topband
- Coords en blanco: `clamp(0.95rem,1.6vw,1.2rem)`
  `43°07'55"N · 2°01'05"O · Xabatenea Etxea (1538) · C/ Parroquia 13, Doneztebe, Nafarroa`

---

## CSS — Clases principales

| Clase | Uso |
|---|---|
| `.topband` | Barra superior navegación |
| `.brand-slash` | Título principal rojo |
| `.b-eventos` | Bebas caja negra texto rojo |
| `.marquee-bar / .marquee-inner` | Marquee texto |
| `.hero` | Foto completa sin recorte |
| `.hero-eyebrow-top` | Texto rojo arriba de la foto |
| `.hero-title` | Título Playfair abajo foto |
| `.intro` | Sección azul con texto |
| `.intro-label` | Etiqueta roja intro |
| `.intro-body` | Cuerpo texto intro |
| `.photo-marquee` | Marquee de fotos |
| `.events-section` | Sección grid de carteles |
| `.event-card` | Tarjeta de cada evento |
| `.event-card-body` | Contenido inferior tarjeta |
| `.footer` | Footer clon topband |
| `.footer-coords` | Coordenadas GPS blancas |

---

## Carteles — Convención de nombres
```
nombre-evento-MM-AA.html
```
Ejemplo: `rastros-jupiter-05-26.html`

### Carteles existentes
| Archivo | Evento | Fecha |
|---|---|---|
| `rastros-jupiter-05-26.html` | 4º Aniversario Los Rastros de Júpiter | 30 Mayo 2026 |

### Añadir nuevo cartel
1. Subir el `.html` del cartel al repo 13-EVENTOS con la convención de nombres
2. Añadir tarjeta en el `.events-grid` del `index.html`
3. Actualizar el link en el Magic Bus si tiene post

---

## Mobile — Notas
- Topband: `flex-wrap:wrap` — fluye en varias líneas, mismo tamaño que desktop
- Brand slash: `flex-wrap:wrap` en móvil desde 700px
- Events grid: 2 columnas en móvil, 1 en muy pequeño (420px)
- Hero: foto completa sin recorte, texto arriba y abajo posicionado absolute

---

## Magic Bus — Post Rastros de Júpiter
- Sección: `data-secciones="musica eventos euskal-herria"`
- ID: `rastros-4-aniversario`
- Link cartel: `https://beltzaexperience.github.io/13-EVENTOS/rastros-jupiter-05-26.html`
- Comentario firmado: **CLAUDIUS · Siglo I d.C. · Vía Láctea, Brazo de Orión**
- Número: Magic Bus Nº2 · Secundus

---

## Fonema UR — Identidad Visual Beltza
El fonema **UR** aparece en rojo `#b01a1a` en todo el texto visible. Es una marca de identidad del universo Beltza — presente en todas las webs del ecosistema (Manifiesto, Magic Bus, UR-SAPIENS).

### Implementación
```html
Cult<span style="color:#b01a1a;">ur</span>a
CULT<span style="color:#b01a1a;">UR</span>ALES
```

### Aplicar en textos nuevos
Buscar manualmente: cultura, cultural, culturales, natural, espiritual, Doneztebe (no tiene UR), ritual (no tiene UR), Ultramarinos (ULTR**A**M**AR**INOS — no aplica), UR-SAPIENS (ya tiene UR destacado).

### Palabras con UR en el proyecto
- CULT**UR**A / CULT**UR**ALES — marquee, intro, hero
- Espirit**u**ales — intro label (u en rojo)
