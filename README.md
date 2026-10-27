# Regulación de apps en Colombia: una skill para Claude

**¿Tu app está filtrando datos o rompiendo la ley sin saberlo?** Pedir la cédula y una foto para entrar al gimnasio, mandar promociones un domingo, guardar todo en una nube extranjera o prometer "datos 100 % seguros" tienen reglas en Colombia. Y si tu app toca plata, más: decirle a alguien "este CDT es para usted", cobrar comisión por referir o leer extractos también.

Esta skill le enseña a Claude a **revisar tu app o tu diseño contra la ley colombiana**, con **norma, artículo y enlace oficial**. Primero decide si la app está en el sector financiero:

- **Toda app** pasa por la ruta general: habeas data, seguridad ("¿tu diseño filtra información?") y consumidor.
- **Si la app es financiera**, además clasifica cada funcionalidad: qué norma activa, qué rol necesitarías (ninguno, corresponsal digital, aliado licenciado, licencia propia) y qué preguntarle a tu abogado.

Pensada para fundadores y equipos que construyen software en Colombia, con una ruta más profunda para apps de finanzas personales, pagos, inversión o seguros.

## Qué cubre

**Ruta general (toda app)**

- **Habeas data:** ¿eres responsable o encargado?, autorización con prueba, datos sensibles escondidos en descripciones o notas, retención y supresión, política de tratamiento, RNBD (quién está obligado), proveedores y transferencias al exterior, datos de terceros que suben tus usuarios (Ley 1581 de 2012, Decreto 1074 de 2015).
- **Seguridad: ¿tu diseño filtra información?** Lo que el diseño no especifica se reporta como hallazgo: protocolos sin cifrar, TLS 1.0/1.1, certificados sin validar, llaves y recuperación, autenticación, sincronización entre dispositivos, permisos de integraciones, SDK de anuncios y analítica, metadatos, borrado, respaldos y el deber de avisar a la SIC ante incidentes. Con referencias a OWASP MASVS/ASVS, NIST y delitos informáticos (Ley 1273 de 2009).
- **Consumidor y comercio electrónico:** identidad del vendedor, suscripciones, retracto, términos y condiciones, prueba de aceptación, publicidad engañosa (tus promesas de privacidad deben ser demostrables), límites a los mensajes comerciales (Ley 1480 de 2011, Ley 527 de 1999, Ley 2300 de 2023).

**Ruta financiera (solo si aplica)**

- **Asesoría vs. promoción:** la recomendación profesional (Decreto 2555 de 2010, Libro 40, incorporado por el Decreto 661 de 2018) y la leyenda de las comunicaciones generales.
- **Canales:** corresponsal digital (Decreto 1297 de 2022), corresponsales (Decreto 222 de 2020), uso de red (Decreto 2673 de 2012), fuerza de ventas de fondos.
- **Comisiones y conflictos de interés:** cuándo tu remuneración vuelve la asesoría "no independiente".
- **Seguros:** intermediación, comercialización masiva, el "endoso".
- **Finanzas abiertas:** el sistema obligatorio del Decreto 368 de 2026, consentimiento, terceros no vigilados.
- **Pagos y billeteras:** SEDPE, iniciación de pagos, Bre-B, crowdfunding, sandbox de la Superfinanciera.
- **Consumidor financiero:** Ley 1328 de 2009; habeas data financiero, Ley 1266 de 2008.

Todo en español, solo con fuentes oficiales públicas. Normas revisadas en **octubre de 2026**. Las citas sin marca se verificaron contra el texto; **[verificar]** e **[interpretación]** te dicen dónde no.

> **Orientación, no asesoría legal.** Las normas cambian (el Decreto 2555 de 2010 se modifica constantemente). Úsala para hacer mejores preguntas y llegar preparado; un abogado colombiano debe confirmar antes de lanzar.

## Cómo instalarla

1. Copia la carpeta `skills/regulacion-apps-colombia` en `~/.claude/skills/` (en Windows: `C:\Users\<usuario>\.claude\skills\`).
2. Reinicia Claude Code. La skill se activa sola cuando preguntes, por ejemplo:
   - "Revisa el diseño de mi app contra la ley colombiana."
   - "¿Puedo mostrarle al usuario los CDT que mejor se ajustan a su perfil?"
   - "¿Leer los extractos del correo del usuario me obliga a algo?"

## Cómo está organizada (carga progresiva)

`SKILL.md` es corto: decide si la app es financiera y le dice a Claude qué archivos abrir.

| Ruta | Archivo | Para qué |
|---|---|---|
| General | `referencias/datos-y-seguridad.md` | Habeas data y "¿filtra información?" |
| General | `referencias/consumidor-y-comercio.md` | Venta, suscripciones, retracto, publicidad, mensajes |
| Financiera | `referencias/lista-actividades.md` | 17 funcionalidades típicas → norma → rol → qué confirmar |
| Financiera | `referencias/rutas-normativas.md` | Pregunta → norma y artículo |
| Financiera | `referencias/linea-asesoria-vs-promocion.md` | Dónde está la línea para una app no vigilada |
| Cierre | `referencias/preguntas-abogado.md` | Preguntas para tu primera consulta, generales y financieras |
| Cierre | `referencias/fuentes-oficiales.md` | Enlaces oficiales de cada norma |
| Verificar | `normas/` | Textos oficiales de 13 normas (Ley 1581 de 2012, Decreto 1074 de 2015, Circular 005 de 2017 de la SIC, Estatuto del Consumidor, finanzas abiertas y más), separados por ruta |

## Más skills recomendadas

- **[ECC](https://github.com/affaan-m/ecc)**: una colección amplia de agentes, skills, comandos y hooks para Claude Code (revisión de código, TDD, seguridad, planeación y más).

## Licencia

MIT: úsala, cópiala, modifícala y compártela, también en proyectos privados o comerciales. Las normas citadas son textos públicos del Estado colombiano; este repositorio solo las organiza y comenta.

Hecho por Helio Forero mientras construye una app de finanzas personales para Colombia. Sugerencias y correcciones: abre un *issue*.
