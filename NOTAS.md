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

---

## Paleta activa: AZUL
| Variable     | Valor     | Uso                          |
|--------------|-----------|------------------------------|
| `panelDark`  | `#142240` | Fondo principal              |
| `amber`      | `#d4900a` | Acentos, links, separadores  |
| `cream`      | `#e8ecf4` | Texto principal              |
| `red`        | `#b01a1a` | Acento secundario            |
| `black`      | `#060e1c` | Fondo marquee/footer         |

---

## Tipografías
- **Bebas Neue** — Títulos, nombres de artistas, footer
- **Barlow Condensed** — Etiquetas (DJ'S, LIVE, fechas)

Ambas vía Google Fonts (ver `<head>` de `index.html`).

---

## Elementos que CAMBIAN por cartel

### 1. Línea de fecha/horario
```jsx
// En LayoutVertical → bloque título (id="aniversariolinea")
'4º ANIVERSARIO · 30/05/26 · 11H TO 20H'
```

### 2. Imagen/módulo central
```jsx
// Sustituir src= por la nueva imagen (base64 o URL)
<img src="data:image/jpeg;base64,..." style={{display:'block', width:'100%', height:'auto'}}/>
```
- Proporción recomendada: ~3:4 (vertical)
- Sin recorte — se muestra completa como "cuadro en la pared"

### 3. Línea de artistas
```jsx
// En LayoutVertical → bloque NOMBRES
<span style={{color:p.cream}}>ARTISTA1 </span>
<span style={{color:p.amber}}>· TIPO </span>
<span style={{color:p.cream}}>ARTISTA2 </span>
<span style={{color:p.amber}}>· LIVE</span>
```
- Tamaño: `fontSize:70` — centrado con flexbox
- Añadir links si procede: `<a href="..." style={{color:p.cream, textDecoration:'none'}}>`

### 4. Marquee (franja ámbar)
```js
// Array de items en el <Ticker> de LayoutVertical
['BROCANTE','·','VERMÚ', ... ,'AZKEN MUGA OF SOUL']
```
- Velocidad: `animation:'mq 28s linear infinite'` (reducir segundos = más rápido)

---

## Elementos que NO cambian
- Tipografías y paleta de colores
- Sistema `scaleX` para justificación de textos (fit())
- Footer: BELTZA RECORDS · links
- Marquee: estructura y animación
- Estructura HTML/React
- Proporciones del lienzo (1100px × ~2200px)

---

## Footer (fijo en todos los carteles)
`BELTZA RECORDS · DONOSTIA _ DONEZTEBE · MANIFIESTO · MAGIC BUS · DUB²BEAT · UR-SAPIENS`

Links en `<a href>` — ver sección footer en `index.html`.

---

## Para nuevo cartel
1. Duplicar este repositorio
2. Sustituir imagen central (base64 o URL)
3. Editar línea fecha/horario
4. Editar línea artistas
5. Ajustar marquee si procede
6. Exportar JPG desde navegador (zoom 100%, captura)
