Imposición Digital — Sistema Offset 4.0
Aplicativo educativo de imposición digital para producción offset industrial, con el módulo PDF Place & Export (printer spreads, nested, stack) y cálculo de papel, previsualización CTP y exportación.
index.html

---

## Simulador educativo por etapas — `simulador.html`

`simulador.html` es un **simulador interactivo de producción industrial offset** diseñado
pedagógicamente. Guía al estudiante por un flujo secuencial de 5 etapas —
**01 Orden → 02 Máquina → 03 Papel/Imposición → 04 Imposición Digital/CTP → 05 Preflight & CTP** —
donde cada decisión se propaga automáticamente a la siguiente y se explica la relación
`DECISIÓN → CÁLCULO → REPRESENTACIÓN VISUAL → CONSECUENCIA INDUSTRIAL`.

Incluye:

- **Gating secuencial**: cada etapa se desbloquea solo cuando la anterior cumple sus condiciones mínimas.
- **Biblioteca de 8 máquinas** (GTO 52, Solna 125, Heidelberg Kord/Sorm/Speed Master 102, Roland Favorit, Miller TP41S, Lithrone L-528) con **medidas exactas** del taller: medidas de placa, área máxima de impresión, formato máximo y mínimo de papel, y **pinza normal = blanco de mordaza + pinza de papel** (bandas separadas en el diagrama). Primero se elige la máquina y sus dimensiones pasan a la imposición.
- **Ayuda contextual en cada campo**: todos los cuadros de texto tienen un botón ⓘ que abre un diálogo explicando qué información se ingresa.
- **Controles de montaje (Etapa 04)**: rotación 90°, alineación centrado/pegar a pinza, desplazamiento manual (nudge), y tira de control de color por **archivo propio (SVG/imagen)** o CMYK por defecto.
- **Carga de arte final (Etapa 04)**: dropzone para el **PDF** (o imagen) del producto; las páginas se montan automáticamente en cada pose de la plancha y se pueden exportar como **PDF Imposicionado** o **Reporte de producción**.
- Banda no imprimible correcta: **blanco de mordaza** (parte de la plancha) al extremo y **pinza de papel** (área del pliego) debajo.

Diseñado por **Mg Mario Quiroz Martínez** · d3magindesign 2026.
- **Cálculo automático** de poses, aprovechamiento, desperdicio, pliegos, peso y costo, con las mismas fórmulas del Excel *Cálculo de Papel* (`peso = w·h·gramaje/10⁷`, `poses = columnas×filas`, `utilización = poses·área_producto/área_pliego`).
- **Optimizador de imposición** que compara alternativas de montaje y marca la **★ imposición recomendada**.
- **Mesa de imposición SVG** con plancha, pinza, mordaza, márgenes, área imprimible, poses, sangrado, marcas de producción (corte, registro, tira CMYK, plegado, Plate ID, código de barras, SmartMarks), zoom y vistas técnica/imposición/marcas/separaciones.
- **Preflight** con estados 🟢🟡🔴 y diagnóstico `QUÉ OCURRE → POR QUÉ → CÓMO SOLUCIONARLO`.
- **Modales educativos** (ⓘ) `CONCEPTO → DEFINICIÓN → FUNCIÓN → CONSECUENCIA`, cambio de unidades mm/cm/in, flujo industrial clicable y **dashboard final** de producción.

Un solo archivo HTML/CSS/JS vanilla, sin backend; guarda la sesión en `localStorage`.
El `index.html` original (v2.0, con carga de PDF real y PDF Place & Export) se mantiene sin cambios.

---

Archivo principal: index.html (HTML/CSS/JS vanilla, sin servidor).
index.html

Qué hace
Herramienta de escritorio/navegador para montar un PDF en plancha offset: formatos de máquina, poses, merma, marcas técnicas y PDF listo para CTP.
index.html

Inspirada en Impostrip Automation 4.0 / Ultimate Impostrip y en el script PDF Place and Export de William Campbell (marspremedia.com).
index.html

Las fórmulas de papel (poses, peso de resma, hojas/kg, costo) siguen el Excel Cálculo de Papel.xlsx de taller offset.
index.html

Flujo (4 fases)
Documento y plancha — Carga PDF (o demo), plantillas comerciales/Origami, formato de pliego, pinza, márgenes y Printer Spreads.
index.html

Cálculo de papel — Tiraje, gramaje, precio, merma y arranque; compara 4 modalidades de corte; Imposition Agent recomienda la mejor.
index.html

Previsualización — Plancha con corte, registro, tira CMYK, Plate ID, plegado; tiro/retiro; esquema, didáctico o PDF real.
index.html

Exportación y preflight — PDF imposicionado, printer spreads, unspread, JPG RGB 300 dpi, variantes HV/Transcon, reporte de producción.
index.html

Requisitos
Navegador moderno (Chrome, Edge, Firefox).
index.html

Conexión inicial a CDN (PDF.js 3.11.174, pdf-lib 1.17.1, Google Fonts Inter).
index.html

No hay backend: todo corre en el cliente.
index.html

Cómo usarlo
Abre index.html en el navegador (doble clic o servidor local).
index.html

Arrastra un PDF o pulsa D para el PDF demo.
index.html

Elige plancha (GTO 52, Solna, Heidelberg Kord/Sorm, Speedmaster 102, etc.) o medidas en cm/mm/in.
index.html

Completa producto, sangrado, gap y datos de proyecto (salen en Plate ID y reporte).
index.html

Recorre las fases con Siguiente o atajos.
index.html

Printer Spreads
Modo	Uso
Páginas simples	Sin reordenar
Nested (cosido/grapa)	Pliegos anidados; múltiplos de 4 (se rellenan blancos)
Stack (apilado/corte)	Cada 4 páginas = un pliego de 2 caras
Reader → páginas	Descompone spreads de lector
Printer → páginas	Descompone spreads de imprenta
Crear reader spreads	Une pares de páginas
Opciones: rotar alternado (duplicadora), sangrado, efecto lomo, páginas enfrentadas.
index.html

Plantillas
Comerciales: tarjeta, hoja A4, sobre, carpeta (medidas y gramaje del Excel).
index.html

Origami / Impostrip: plano, díptico, tríptico, folio 4 pp, cuarto 8 pp, octavo 16 pp, libro grapado, libro cosido.
index.html

Marcas y CTP
Corte, cruces de registro, reglas, tira de control (CMYK, 4/6 color, 5-spot o archivo propio).
index.html

Plate ID, código de barras de finishing, líneas de plegado.
index.html

Gutters SmartMarks (Top, Left, Center, Mid, etc.).
index.html

Detección de tintas (CMYK y spot/Pantone).
index.html

Tutorial CTP: anatomía de plancha (pinza, mordaza, sangrado, marcas).
index.html

Atajos
Tecla	Acción
← →	Fases
1–4	Ir a fase
D	PDF demo
E	Exportar PDF
R	Reporte
Tecnologías
HTML, CSS, JavaScript (sin frameworks).
index.html

PDF.js — previsualización.
index.html

pdf-lib — imposición y exportación PDF.
index.html

SVG nativo para esquema de plancha.
index.html

localStorage para tema oscuro y estado.
index.html

Créditos
Curso: Diseño de la Información, UTP — DDD-2021 DI-08.
index.html

Autor: Mario Quiroz (marioquirozm@gmail.com).
index.html

Script base: PDF Place and Export — William Campbell.
index.html

Versión: 2.0 — módulo PDF Place & Export (abril 2026).
index.html

Uso académico y de taller; no sustituye RIP/CTP de producción.