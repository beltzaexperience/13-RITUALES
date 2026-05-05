# LOS RASTROS DE JÚPITER — NOTAS DE PROYECTO

## Estructura del repositorio
```
/
├── index.html       ← Cartel web principal
├── style.css        ← Estilos base (no cambiar entre carteles)
└── NOTAS.md         ← Este archivo
```

---

## Lienzo
- **Ancho fijo:** 1100px
- **Proporción:** ~1:2 (formato 35mm)
- **Fondo:** `#142240` (panelDark azul)
- **Paleta activa:** AZUL

| Variable    | Valor     | Uso                          |
|-------------|-----------|------------------------------|
| `panelDark` | `#142240` | Fondo principal              |
| `amber`     | `#d4900a` | Acentos, links, separadores  |
| `cream`     | `#e8ecf4` | Texto principal              |
| `red`       | `#b01a1a` | Acento secundario            |
| `black`     | `#060e1c` | Fondo marquee/footer         |

---

## Tipografías
- **Bebas Neue** — Títulos, nombres de artistas, footer
- **Barlow Condensed** — Etiquetas (DJ'S, LIVE, fechas)

Ambas vía Google Fonts (ver `<head>` de index.html).

---

## Mobile — Solución definitiva (Mayo 2026)

Después de una odisea de un día largo, la solución que funciona:

**1. Viewport meta tag:**
```html
<meta name="viewport" content="width=1100"/>
```
Le dice al navegador móvil "este contenido es de 1100px" y él escala solo. Solo funciona en navegadores móviles reales y en el simulador de DevTools (Ctrl+Shift+M). **No funciona redimensionando la ventana del escritorio.**

**2. Orden correcto en el script:**
`scaleCartel()` debe: resetear → llamar a `fit()` → aplicar transform. Si `fit()` corre después del transform, mide dimensiones ya escaladas y produce valores incorrectos. En móvil real con `viewport=1100`, `scaleCartel()` no aplica ningún transform (el browser ya lo hace), pero en desktop sí actúa.

**Para testear en local:** F12 → icono móvil (Ctrl+Shift+M) → seleccionar iPhone 12 o similar → recargar.

---

## Elementos que CAMBIAN por cartel

### 1. Línea de fecha/horario
```html
<!-- id="aniversariolinea" -->
4º ANIVERSARIO · 30/05/26 · 11H TO 20H
```

### 2. Imagen/módulo central
```html
<img src="image.jpg" style="display:block; width:100%; height:auto;">
```
- Proporción recomendada: ~3:4 (vertical)
- Sin recorte — se muestra completa como "cuadro en la pared"

### 3. Línea de artistas
```html
<span style="color:#e8ecf4">ARTISTA1 </span>
<span style="color:#d4900a">· TIPO </span>
<span style="color:#e8ecf4">ARTISTA2 </span>
<span style="color:#d4900a">· LIVE</span>
```
- Tamaño: `font-size: 70px` — centrado con flexbox
- Añadir links si procede: `<a href="..." style="color:#e8ecf4; text-decoration:none;">`

### 4. Marquee (franja ámbar)
```html
<!-- Editar los <span> dentro del div de animación marqueeScroll -->
BROCANTE · VERMÚ · MÚSICA · CINE · TAROT · DISCOS · ...
```
- Velocidad: `animation: marqueeScroll 28s linear infinite` (reducir segundos = más rápido)
- El contenido está duplicado dentro del div para el loop continuo

---

## Elementos que NO cambian
- Tipografías y paleta de colores
- Sistema `scaleX` para justificación de textos (`fit()`)
- Footer: `BELTZA RECORDS · links`
- Marquee: estructura y animación
- Proporciones del lienzo (1100px)
- Viewport meta `width=1100`

---

## Footer (fijo en todos los carteles)
```
BELTZA RECORDS · DONOSTIA _ DONEZTEBE · MANIFIESTO · MAGIC BUS · DUB²BEAT · UR-SAPIENS
```
Links en `<a href>` — ver sección `#footercontainer` en index.html.

---

## Para nuevo cartel
1. Duplicar el repositorio
2. Sustituir imagen central (`image.jpg`)
3. Editar línea fecha/horario (`#aniversariolinea`)
4. Editar línea artistas
5. Ajustar marquee si procede
6. Exportar JPG desde navegador (zoom 100%, captura)

---

## CSS nuevo — No hay style.css nuevo
El `style.css` no cambió. Todo el fix mobile fue en el `<script>` del `index.html`. El CSS base sigue siendo válido para futuros carteles sin modificación.
