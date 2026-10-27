# Textos de normas (copias de referencia)

Copias descargadas en octubre de 2026 de fuentes oficiales del Estado colombiano (gestor normativo de Función Pública, SIC, Régimen Legal de Bogotá). Los PDF de Función Pública incluyen las notas de modificación. Pueden no reflejar cambios posteriores: confirme el texto vigente con `../referencias/fuentes-oficiales.md`.

Para verificar un artículo: extraiga el texto del PDF (con `pdfplumber` en Python, o `pdftotext` si lo tiene) y búsquelo sin distinguir mayúsculas ni tildes, por ejemplo con la expresión `(?i)art[íi]culo\s+5\b`. En Windows, defina `PYTHONIOENCODING=utf-8` para que las tildes se impriman bien. El Decreto 1074 de 2015 es largo: busque directamente `2.2.2.25.` (datos personales) o `2.2.2.26.` (RNBD).

## Ruta general (toda app)

| Archivo | Norma |
|---|---|
| `ley-1581-2012-proteccion-datos-personales.pdf` | Ley 1581 de 2012: régimen general de protección de datos personales |
| `decreto-1074-2015-comercio-industria-turismo.pdf` | Decreto 1074 de 2015: arts. 2.2.2.25.x (autorización, políticas, transmisión, responsabilidad demostrada; compila el Decreto 1377 de 2013) y 2.2.2.26.x (RNBD; compila el Decreto 886 de 2014) |
| `sic-circular-externa-005-2017-transferencia-internacional.md` | Circular Externa 005 de 2017 de la SIC: estándares y lista de países con nivel adecuado de protección |
| `sic-guia-responsabilidad-demostrada.pdf` | SIC: guía de responsabilidad demostrada (accountability) |
| `ley-1273-2009-delitos-informaticos.pdf` | Ley 1273 de 2009: delitos informáticos (art. 269F, violación de datos personales) |
| `ley-1480-2011-estatuto-consumidor.pdf` | Ley 1480 de 2011: Estatuto del Consumidor (con las modificaciones de la Ley 2439 de 2024) |
| `ley-527-1999-mensajes-de-datos.pdf` | Ley 527 de 1999: mensajes de datos, comercio electrónico y firmas digitales |
| `ley-2300-2023-intimidad-consumidores.pdf` | Ley 2300 de 2023: horarios y canales de contacto para cobranza y publicidad |

## Ruta financiera

| Archivo | Norma |
|---|---|
| `ley-1266-2008-habeas-data-financiero.pdf` | Ley 1266 de 2008: habeas data financiero (con las modificaciones de la Ley 2157 de 2021) |
| `ley-1328-2009-consumidor-financiero.pdf` | Ley 1328 de 2009: protección del consumidor financiero |
| `decreto-661-2018-asesoria-mercado-valores.pdf` | Decreto 661 de 2018: asesoría en el mercado de valores (Libro 40 del Decreto 2555 de 2010) |
| `decreto-1297-2022-finanzas-abiertas-corresponsal-digital.pdf` | Decreto 1297 de 2022: finanzas abiertas voluntarias, corresponsal digital, iniciación de pagos |
| `decreto-368-2026-finanzas-abiertas-obligatorio.pdf` | Decreto 368 de 2026: sistema de finanzas abiertas obligatorio |

No están aquí (consúltelos en línea): el Decreto 2555 de 2010 completo (muy extenso y modificado con frecuencia), la Ley 964 de 2005, la Ley 1735 de 2014 y los demás decretos financieros.
