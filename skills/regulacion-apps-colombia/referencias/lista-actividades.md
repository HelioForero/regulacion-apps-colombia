# Lista de actividades: funcionalidad → norma → rol → qué confirmar

Ruta financiera: úsela solo si el paso 0 de `SKILL.md` concluyó que la app está en el sector financiero.

Normas sin copia en `../normas/` (Decreto 2555 de 2010, Ley 964 de 2005, Ley 1735 de 2014, Decretos 222 de 2020, 2673 de 2012, 34 de 2015, 2123 de 2018, 1357 de 2018, 1692 de 2020 y 1234 de 2020): sus citas se revisaron contra el texto oficial en octubre de 2026, pero quien use esta skill debe abrir el enlace de `fuentes-oficiales.md` o marcarlas **[verificar]**. Datos, seguridad y consumidor van siempre por la ruta general (`datos-y-seguridad.md`, `consumidor-y-comercio.md`). Orientación, no asesoría legal. Lo marcado **[interpretación]** es lectura propia de las normas citadas, no texto de ellas. Normas revisadas en octubre de 2026; confirme el texto vigente (enlaces en `fuentes-oficiales.md`).

## Roles posibles

| Rol | Qué significa | Norma |
|---|---|---|
| Ninguno + leyenda | La app, sin vigilancia de la SFC, publica información general con la leyenda de "no constituye recomendación profesional" | Decreto 2555 de 2010, art. 2.40.1.1.3 (incorporado por el Decreto 661 de 2018) |
| Corresponsal digital | La app pone su aplicación web o móvil al servicio de una entidad vigilada, que responde plenamente, muestra su marca y atiende las quejas | Decreto 1297 de 2022 (art. 2.36.9.1.21 del Decreto 2555 de 2010); Decreto 222 de 2020 |
| Fuerza de ventas (fondos) | Vinculada por contrato a la sociedad administradora, que responde por sus actos | Decreto 2555 de 2010, Parte 3, Libro 1 (distribución de fondos de inversión colectiva) |
| Aliado licenciado | Una entidad vigilada hace el acto regulado; la app solo refiere | Decreto 2555 de 2010, Libro 40, Título 3 (prestación de la asesoría) |
| Licencia propia | La empresa misma es vigilada (comisionista, SEDPE, aseguradora, plataforma de crowdfunding) | Ley 964 de 2005, art. 3; Ley 1735 de 2014 |
| Tercero en finanzas abiertas | Receptor de datos vigilado, o no vigilado en el esquema voluntario | Decreto 368 de 2026 |

## Paso 1: ¿qué hace la funcionalidad?

Clasifique cada funcionalidad por separado. Si varias filas aplican, manda la más exigente (la que pide un rol vigilado o licencia): mostrar datos es menos que personalizar, y personalizar es menos que tocar dinero.

| # | La funcionalidad… | Norma que activa | Rol | Confirmar con el abogado |
|---|---|---|---|---|
| 1 | Muestra información o educación general (qué es un CDT, cómo funciona un fondo) | La comunicación general no es asesoría si lleva la leyenda y no sugiere que el producto le conviene al lector: Decreto 2555 de 2010, art. 2.40.1.1.3 | Ninguno + leyenda **[interpretación]** | Texto exacto de la leyenda; qué frases hacen sonar personal un contenido general |
| 2 | Compara productos por atributos públicos (tasas, comisiones), la misma tabla para todos | Misma lógica de comunicación general; contenido veraz y verificable. Deberes de información de las entidades: Ley 1328 de 2009 | Ninguno + leyenda **[interpretación]** | ¿Una tabla ordenable con nuestros criterios sigue siendo "general"? ¿Quién responde por tasas desactualizadas? |
| 3 | Perfila al usuario (cuestionario de riesgo, metas, horizonte) | El perfil del cliente es pieza de la asesoría; perfil del cliente + perfil del producto = recomendación: Decreto 2555 de 2010, art. 2.40.1.1.2 | Aliado licenciado, o corresponsal digital donde la entidad hace el perfilamiento | ¿Quién es dueño del cuestionario? ¿Un perfil que solo vive en el teléfono sigue siendo "nuestro"?  **[interpretación]** Si el perfil se calcula solo en el teléfono, sigue siendo la app la que personaliza: trátelo como la fila 4 hasta que el abogado diga lo contrario. |
| 4 | Recomienda un producto de forma personal ("este CDT es para usted", ranking personalizado) | La recomendación profesional está reservada a entidades vigiladas, con personas certificadas y reglas de conflictos: Decreto 2555 de 2010, art. 2.40.1.1.2 y Libro 40, Título 3 | Aliado licenciado o licencia propia. **[interpretación]** La línea se cruza cuando la app personaliza | ¿Un CDT está dentro del Libro 40? ¿Dónde pone la SFC la línea? |
| 5 | Usa un algoritmo o IA para sugerir productos | La asesoría puede usar herramientas tecnológicas; la entidad no puede eximirse de sus fallas: Decreto 2555 de 2010, Libro 40, Título 5 | La entidad responde; la app es, a lo sumo, un componente **[interpretación]** | Reparto de responsabilidad; quién valida el modelo |
| 6 | Recibe órdenes, vinculaciones o documentos de un producto | Los corresponsales recogen documentos y no deciden la celebración de contratos: Decreto 222 de 2020; el uso de red exige usuarios vigilados: Decreto 2673 de 2012 | Corresponsal digital o fuerza de ventas, por contrato | Mínimos del contrato, límites por operación, con quién contrata el usuario |
| 7 | Cobra comisión o pago por referido a la entidad | La remuneración del uso de red y del corresponsal se pacta con la entidad; el corresponsal no puede cobrarle al cliente: Decretos 2673 de 2012 y 222 de 2020. Los beneficios de terceros hacen la asesoría "no independiente" y deben revelarse: Libro 40, Título 3. Gestión de conflictos: Ley 1328 de 2009 | Dentro de un contrato de corresponsal o de fuerza de ventas | ¿Se permite pago por lead o por conversión? ¿Cómo se revela? El ranking no puede seguir la comisión |
| 8 | Lee los extractos en PDF o el correo del propio usuario, con su consentimiento | No es finanzas abiertas (el usuario aporta los archivos); aplica protección de datos: Ley 1581 de 2012 (arts. 4, 9, 12; datos sensibles arts. 5–6) y Ley 1266 de 2008 | Ninguno **[interpretación]**; si hay servidor, responsable del tratamiento | Texto de la autorización, retención, si la Ley 1266 de 2008 aplica. Las descripciones de compras pueden revelar datos sensibles (salud, religión, sindicato) |
| 9 | Lee datos bancarios por las API de finanzas abiertas | Autorización específica por finalidad y plazo, sin autorizaciones generales ni condicionar el servicio: Decreto 368 de 2026 (arts. 2.35.8.3.2 a 2.35.8.3.5) | Tercero receptor: vigilado o esquema voluntario no vigilado, evaluado por cada proveedor (arts. 2.35.8.6.1 y 2.35.8.6.2) | Criterios de evaluación (Circular Básica Jurídica de la SFC), plazos (en revisión en 2026), tarifas |
| 10 | Inicia pagos o transferencias por el usuario | La iniciación de pagos envía una orden con autorización del pagador y no puede guardar credenciales: Decreto 1297 de 2022 | Participante del sistema de pagos; no disponible para una app común **[interpretación]** | Si existe algún rol intermedio para una empresa no vigilada |
| 11 | Guarda, mueve o liquida dinero (billetera, cuentas comunes, compensación de gastos compartidos con pago) | Depósitos y pagos son actividades vigiladas: Ley 1735 de 2014 (SEDPE); Decreto 1692 de 2020 | Licencia propia (SEDPE o entidad de pagos) o aliado | Cualquier función que toque fondos, aunque sea por un momento |
| 12 | Ofrece, vende o intermedia seguros, incluido el "endoso" | La intermediación está reservada a corredores, agencias y agentes; los seguros masivos sencillos llegan por redes de crédito o corresponsales: Decreto 2555 de 2010, Libro 30; Decreto 34 de 2015. Condicionar un crédito a comprar otros productos es práctica abusiva: Ley 1328 de 2009, art. 12 lit. a | Aliado licenciado (corredor o aseguradora), o ruta de corresponsal para líneas elegibles | ¿Presentar una póliza externa es intermediación? ¿Qué significa "endoso" en el flujo previsto? |
| 13 | Distribuye participaciones en fondos o CDT | Fondos: la sociedad administradora o un distribuidor especializado; canales: fuerza de ventas propia, uso de red, corresponsalía (Decreto 2555 de 2010, Parte 3, Libro 1). CDT: listas de uso de red y corresponsales (Decreto 2673 de 2012) | Fuerza de ventas o corresponsal digital de la entidad | ¿Una persona jurídica puede ser promotora? Certificación del personal (RNPMV) |
| 14 | Organiza crowdfunding o préstamos entre personas | Solo entidades autorizadas de financiación colaborativa: Decreto 1357 de 2018 | Licencia propia | Fuera de alcance salvo cambio de producto |
| 15 | Divide gastos compartidos entre usuarios sin mover dinero | No se identifica servicio financiero **[interpretación]** | Ninguno | ¿"Marcar como saldado" y los recordatorios se quedan fuera de pagos? ¿Un enlace profundo con monto y destinatario cuenta como iniciar un pago? |
| 16 | Empuja al usuario hacia un producto (valores por defecto, recordatorios, escasez) | Principios de transparencia y prácticas abusivas para entidades: Ley 1328 de 2009. Publicidad engañosa prohibida: Ley 1480 de 2011, art. 30 | Ninguno, pero tratarlo como riesgo de conducta **[interpretación]** | ¿Las reglas de publicidad de la SIC y la SFC alcanzan a la app? |
| 17 | Envía datos del usuario a una entidad o aliado (lead, prellenado de solicitud) | Es transferencia de datos: autorización específica para esa finalidad (Ley 1581 de 2012, arts. 4 y 9); si además es canal de la entidad, filas 6 y 7 | Corresponsal digital o referido, según el contrato | ¿Qué datos mínimos viajan? ¿El usuario puede negarse sin perder el servicio? |

## Paso 2: elegido el rol, revise las condiciones

- **Sin rol:** leyenda; nada de lenguaje personal; revelar cualquier comisión; la misma respuesta con la función comercial apagada.
- **Corresponsal digital:** contrato escrito con la entidad; su marca siempre visible; su canal de quejas; no cobrar al cliente; no decidir la celebración de contratos; proteger los datos (Decreto 1297 de 2022).
- **Aliado licenciado:** el aliado perfila, recomienda y vende; la app refiere y registra el consentimiento.
- **Tercero en finanzas abiertas:** elegir estatus vigilado o esquema voluntario; pedir solo las categorías necesarias; registrar cada autorización (Decreto 368 de 2026).
- **Licencia propia o sandbox:** lo lidera una entidad y es exigente: Decreto 1234 de 2020; Manual del Espacio Controlado de Prueba de la SFC.

## Paso 3: siempre pregunte al abogado

Ver `preguntas-abogado.md`.
