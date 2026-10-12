---
version: 1
name: demo-carpinteria-bricomecanizado
description: Propuesta de rediseño para Bricomecanizado 2011 S.A.L., taller de corte, canteado y mecanizado de tablero para profesionales en el polígono La Font Santa (Sant Joan Despí). Habla como una hoja de despiece, no como una tienda de bricolaje.
colors:
  fondo: "#F3F4F1"
  superficie: "#E4E7E2"
  tinta: "#1A1F1C"
  texto-suave: "#4A524D"
  linea: "#C9CEC8"
  senal: "#F2C318"
  sobre-senal: "#1A1F1C"
  suelo: "#1E4436"
  sobre-suelo: "#F3F4F1"
typography:
  display:
    fontFamily: "'Archivo', system-ui, sans-serif"
    fontStretch: "118%"
    fontWeight: 800
    fontSize: "clamp(2.1rem, 1.2rem + 4.2vw, 5rem)"
    lineHeight: 1.02
    letterSpacing: "-0.02em"
  titulo:
    fontFamily: "'Archivo', system-ui, sans-serif"
    fontStretch: "112%"
    fontWeight: 760
    fontSize: "clamp(1.6rem, 1.2rem + 1.6vw, 2.6rem)"
    lineHeight: 1.06
  cuerpo:
    fontFamily: "'Archivo', system-ui, sans-serif"
    fontStretch: "100%"
    fontWeight: 400
    fontSize: 1.0625rem
    lineHeight: 1.6
rounded:
  ninguno: 0
  s: 4px
spacing:
  s: 8px
  m: 16px
  l: 24px
  xl: 56px
  xxl: 112px
components:
  boton-principal:
    backgroundColor: "{colors.senal}"
    textColor: "{colors.sobre-senal}"
    radius: 4px
    padding: 14px 22px
  boton-secundario:
    backgroundColor: transparent
    border: "2px solid {colors.tinta}"
    textColor: "{colors.tinta}"
    radius: 4px
---

## Visión

Bricomecanizado 2011 S.A.L. es un taller del polígono La Font Santa (Av. de la Generalitat, 49, Sant
Joan Despí) que corta, cantea, mecaniza y prensa tablero para profesionales: carpinteros,
interioristas, montadores de stands, hostelería, cabinas sanitarias, decorados. La empresa es de 2011;
las personas, del sector desde 1980 (dato de su propia web). Su web actual es un Divi de 2016 con
fondo de textura de madera, menú apretado, el texto repetido dos veces y el HTTPS roto.

Lectura del encargo: *taller industrial de tablero que trabaja para otros profesionales; quien entra
quiere saber en cinco segundos qué procesos hacen, con qué materiales y cómo les mandan un trabajo;
lenguaje de oficio, directo y técnico, apoyado en fotos reales de sus máquinas y de piezas que han
sacado.*

Modo: **Convencer**. Nivel: **Cuidado**. Diales: Variación 6 / Movimiento 3 / Densidad 5 (es un
público profesional que agradece información apretada y clara).

## Ambiente

**Técnico, limpio, de taller.** El mundo del negocio: melamina blanca, MDF crudo, el suelo verde del
taller con sus líneas amarillas de seguridad, la seccionadora, la CNC, los cantos.

**El gesto audaz:** la cota de plano. La foto de su nombre recortado en tablero sobre la mesa de la
CNC ocupa todo el ancho, y encima va una línea de cota amarilla con sus topes, como en un plano de
despiece. La misma línea fina, en pequeño, separa los procesos de la lista de servicios. Nada más.

## Color

- `fondo` / `superficie`: blanco de melamina, ligeramente frío, y su variante gris para alternar.
- `tinta`: grafito casi negro, del metal de las máquinas.
- `senal` (amarillo de línea de seguridad del suelo del taller): botón principal, cotas y nada más.
  Nunca como color de texto sobre fondo claro.
- `suelo` (el verde del pavimento del taller): un solo bloque, el de contacto y ubicación.
- Descartados: crema + serif + terracota (uniforme 1) y beige + latón (uniforme 5), que son el
  default de «carpintería»; también negro + acento ácido (uniforme 2): el amarillo va sobre claro.

## Tipografía

- **Archivo** variable (SIL OFL, ejes `wght` y `wdth`), una sola familia con dos papeles: titulares
  anchos y pesados (wdth 112-118) que recuerdan a la rotulación de maquinaria; texto en ancho normal.
- Autoalojada en `/fonts`, subconjunto latino, `font-display: swap`, precargada.
- Horarios y teléfonos con `tabular-nums`. Sin etiquetas en mayúsculas espaciadas.

## Composición

```
móvil (375)                         escritorio (1440)
┌───────────────────────┐           ┌──────────────────────────────────────────┐
│ franja propuesta      │           │ franja propuesta                         │
│ [logo]      93 373…   │           │ [logo]  Servicios Materiales …  [Llamar] │
│ Tablero cortado,      │           │ Tablero cortado, canteado y              │
│ canteado y mecanizado │           │ mecanizado a medida                      │
│ a medida              │           │ texto · [Llamar] [Pedir presupuesto]     │
│ texto                 │           │ ├──────────── cota amarilla ───────────┤ │
│ [Llamar] [Presupuesto]│           │ FOTO A SANGRE: BricoMecanitzat en la CNC │
│ 4,9 en Google         │           └──────────────────────────────────────────┘
│ ├─ cota ─┤ FOTO       │
└───────────────────────┘
```

Secciones y familia de composición:

1. Franja de propuesta.
2. Cabecera: logo real + navegación + teléfono.
3. Hero: titular ancho, acciones, valoración real de Google, foto a sangre con cota.
4. Qué hacemos: lista de procesos con filetes, cada fila con nombre, texto y foto si existe.
5. Para quién: un párrafo grande con los sectores que nombra su web.
6. Piezas del taller: rejilla de fotos de tamaños distintos con pie.
7. Materiales y cómo trabajamos: dos columnas asimétricas, lista de definición + foto del taller.
8. La empresa: texto corto + foto de la escuadradora.
9. Dónde estamos y contacto: bloque verde `suelo`, horario, dirección, cómo llegar.
10. Pie con datos completos.

## Formas

Radio 0 en fotos y bloques; 4 px en botones. Sin sombras. Filetes de 1 px en `linea`.

## Movimiento

Un único momento: la cota del hero se dibuja de izquierda a derecha al cargar (600 ms). Con
`prefers-reduced-motion` aparece ya dibujada. Hover y foco instantáneos.

## Imagen

Solo fotografía real de su web actual (taller, máquinas y piezas). Se descartan las fotos de rótulos
con nombres de terceros para no sugerir clientes. El logo actual (letras con textura de madera) se
mantiene tal cual en la cabecera: es su marca.
