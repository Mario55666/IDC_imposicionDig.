Imposición Digital — Sistema Offset 4.0
Aplicativo educativo de imposición digital para producción offset industrial, con el módulo PDF Place & Export (printer spreads, nested, stack) y cálculo de papel, previsualización CTP y exportación.
index.html

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