---
name: regulacion-apps-colombia
description: Revisa una app o un diseño de software en Colombia contra la ley. Para cualquier app aplica habeas data (Ley 1581 de 2012), seguridad (¿el diseño filtra información?) y consumidor (Ley 1480 de 2011). Si la app toca el sector financiero, revisa también asesoría vs. promoción, comisiones, corresponsal digital, finanzas abiertas, pagos, seguros e inversión (Decreto 2555 de 2010 y otros). Cita norma, artículo y enlace oficial. Orientación, no asesoría legal.
---

# Revisión regulatoria de apps en Colombia

**Orientación, no asesoría legal.** Las normas cambian. Antes de lanzar, un abogado colombiano debe confirmar.

## Paso 0: ¿la app está en el sector financiero?

Responde sí o no con la evidencia del diseño, **por funcionalidad**. Es financiera si alguna funcionalidad:

- muestra, compara, recomienda o vende productos financieros (cuentas, CDT, fondos, créditos, seguros, inversiones);
- recibe comisiones o pagos de entidades financieras o aseguradoras;
- lee datos bancarios (API de finanzas abiertas, extractos, correos del banco);
- guarda, mueve o liquida dinero, o inicia pagos;
- funciona como canal, aliado o corresponsal de una entidad vigilada por la Superintendencia Financiera (SFC);
- organiza préstamos, ahorro colectivo o crowdfunding.

**No es financiera** por cobrarle a sus propios clientes con tarjeta o PSE a través de una pasarela de pagos: quien mueve el dinero es la pasarela. Lo sería si guarda saldos, cobra a nombre de terceros, financia en cuotas con recursos propios o inicia pagos como servicio.

Una app de finanzas personales casi siempre es financiera en alguna funcionalidad y no en otras: clasifica cada una. **En la duda**, trata esa funcionalidad como financiera y dilo. Di qué decidiste y por qué, y nombra la señal que cambiaría la conclusión (por ejemplo, "si mañana cobra comisión a un banco").

## Cargar según el resultado

| Ruta | Cuándo | Lee |
|---|---|---|
| **General** | Siempre, toda app | `referencias/datos-y-seguridad.md` (habeas data y "¿filtra información?"); `referencias/consumidor-y-comercio.md` (venta, suscripciones, publicidad, contratos electrónicos, mensajes) |
| **Financiera** | Solo si el paso 0 dio sí | `referencias/lista-actividades.md` (funcionalidad → norma → rol); `referencias/rutas-normativas.md` (pregunta → artículo); `referencias/linea-asesoria-vs-promocion.md` (análisis de fondo: asesoría, canales, comisiones) |
| **Cierre** | Al final, con los hallazgos ya escritos | `referencias/preguntas-abogado.md`: solo la sección "Toda app" y, si el paso 0 dio sí, "Solo si la app es financiera" |
| **Verificar** | Solo para confirmar un artículo concreto o dar un enlace | `normas/README.md` dice qué PDF tiene cada norma: extrae su texto (por ejemplo con `pdftotext` o `pdfplumber`) y busca `ARTÍCULO <número>`. Si no puedes, deja la cita como **[verificar]**. `referencias/fuentes-oficiales.md` tiene los enlaces oficiales |

No cargues la ruta financiera para una app que no es financiera.

## Flujo

1. **Lee el diseño:** descripción del producto, decisiones de arquitectura (ADR), modelo de amenazas, decisiones de negocio y textos públicos (publicidad, términos). Antes de citar un ADR, mira si fue reemplazado o enmendado; busca las decisiones que tocan servidores, nube, aliados, telemetría, anuncios y promesas de privacidad: ahí suelen estar las contradicciones. Luego haz el **paso 0** por funcionalidad.
2. **Ruta general:** recorre las listas de `datos-y-seguridad.md` y `consumidor-y-comercio.md`. Todo lo que el diseño **no especifique** en seguridad o datos es un **hallazgo**: pide que lo defina por escrito (conexiones sin cifrar o con TLS 1.0/1.1 filtran datos).
3. **Ruta financiera** (si aplica): clasifica cada funcionalidad con `lista-actividades.md`; si varias filas aplican, manda la más exigente. Busca el artículo en `rutas-normativas.md`.
4. **Responde** con hallazgos ordenados por gravedad, cada uno con norma (con año), artículo, dónde está en el diseño y qué hacer. En los financieros, añade qué queda del lado permitido, qué cruza la línea y qué rol necesitaría la app. Cierra con preguntas numeradas para el abogado, adaptadas de `preguntas-abogado.md` a este diseño (no las copies todas), y con lo que la skill no cubre. Responde en español; traduce las citas del diseño y conserva los nombres de archivo.

| Gravedad | Criterio |
|---|---|
| CRÍTICO | Tal como está diseñado, incumple la ley o expone datos sensibles: bloquea el lanzamiento |
| ALTO | Exige cambiar el diseño, un contrato o una autorización antes de lanzar |
| MEDIO | Falta un documento o un procedimiento (política, aviso, retención, plan de incidentes) |
| BAJO | Confirmar o mejorar; no bloquea |

Lo que el diseño **no especifica** es MEDIO, y ALTO si toca datos sensibles, menores o conexiones sin cifrar. Una funcionalidad solo propuesta y ya condicionada a revisión legal se califica por su efecto en el lanzamiento y se dice que está condicionada.

## Reglas

- Cita norma (con año), artículo y fuente oficial; no respondas de memoria. Verifica en `normas/` o en el enlace oficial; si la norma no tiene copia en `normas/` y no pudiste abrir el enlace, márcala **[verificar]**.
- Marca **[interpretación]** lo que sea lectura propia y **[verificar]** lo que no se confirmó contra el texto.
- Di qué no cubre esta skill (circulares de la SFC, exposición penal, tributario, texto vigente a la fecha) en vez de adivinar.
- Si una conclusión obliga a cambiar el diseño (ofertas de aliados, consentimiento, datos compartidos, servidores), recomienda registrarla como decisión de arquitectura (ADR) y señala qué decisión existente contradice.
