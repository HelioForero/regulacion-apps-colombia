# Habeas data y seguridad: ¿la app trata bien los datos y los protege?

Aplica a **toda app**, financiera o no. Orientación, no asesoría legal. Citas sin marca: verificadas en octubre de 2026 contra los textos de `../normas/` (Ley 1581 de 2012, Ley 1266 de 2008, Decreto 1074 de 2015, Ley 1273 de 2009 y guía de la SIC en `../normas/`). **[verificar]**: no confirmado contra el texto. **[interpretación]**: lectura propia.

**Idea central:** la ley no dice "use TLS 1.3" ni "cifre con AES". Exige medidas técnicas, humanas y administrativas **suficientes** para evitar adulteración, pérdida, consulta, uso o acceso no autorizado o fraudulento (Ley 1581 de 2012, art. 4 lit. g), y el responsable debe poder **demostrarlas** ante la SIC (Decreto 1074 de 2015, arts. 2.2.2.25.6.1 y 2.2.2.25.6.2). **[interpretación]** Un diseño que no dice cómo protege conexiones, almacenamiento y accesos no puede demostrar esa suficiencia.

## 1. ¿Qué rol tiene la app frente a los datos?

| Situación | Rol probable | Norma |
|---|---|---|
| La app decide para qué y cómo se tratan los datos (su servidor, su base de usuarios) | **Responsable** | Ley 1581 de 2012, art. 17 |
| La app trata datos por cuenta de otro (por ejemplo, de una empresa cliente) | **Encargado** | Ley 1581 de 2012, art. 18 |
| Todo se procesa en el dispositivo y la empresa no recibe datos personales | Posiblemente ninguno sobre esos datos **[interpretación]**; sí responde por lo que reciba (cuentas, pagos, analítica, soporte) | Pregúntelo al abogado |
| El servidor solo guarda datos cifrados que la empresa no puede leer (cifrado de extremo a extremo) | **[interpretación]** Siguen siendo datos personales del titular; la empresa probablemente es encargada o responsable de su almacenamiento, y los **metadatos** (cuenta, IP, fechas, tamaños) sí los lee | Pregúntelo al abogado |
| Proveedores de nube, analítica, anuncios, correo, soporte | Encargados de la app (transmisión) o terceros que reciben datos (transferencia). La transmisión exige contrato con contenido mínimo | Decreto 1074 de 2015, arts. 2.2.2.25.5.1 y 2.2.2.25.5.2; Ley 1581 de 2012, art. 26 |
| Un usuario sube datos de **otras personas** (familia, compañeros de gastos, contactos) | **[interpretación]** Esas personas son titulares que no autorizaron nada; defina qué ve cada uno y si el uso queda en el "ámbito personal o doméstico" | Decreto 1074 de 2015, art. 2.2.2.25.1.2; pregúntelo al abogado |
| La app comparte datos con un aliado comercial | Transferencia: autorización específica para esa finalidad | Ley 1581 de 2012, arts. 4 y 9 |
| Telemetría, "datos anonimizados" o programas para mejorar el producto | **[interpretación]** Si se pueden reidentificar (por combinación, por identificador estable), siguen siendo datos personales. Defina por escrito qué significa "anónimo" | Ley 1581 de 2012, art. 3 lit. c (dato personal: información vinculada o que pueda asociarse a personas determinadas o determinables) |

## 2. Lista de cumplimiento (habeas data)

| # | Revise que… | Norma |
|---|---|---|
| 1 | Hay **autorización previa, expresa e informada**, obtenida por un medio que permita consultarla después, y se guarda la **prueba** | Ley 1581 de 2012, arts. 4 y 9; Decreto 1074 de 2015, arts. 2.2.2.25.2.2, 2.2.2.25.2.4 y 2.2.2.25.2.5 |
| 2 | Al pedirla, se informa la finalidad, el carácter facultativo de responder datos sensibles, los derechos y los datos de contacto del responsable | Ley 1581 de 2012, art. 12 |
| 3 | Los **datos sensibles** (salud, religión, política, afiliación sindical, biométricos, vida sexual…) solo se tratan con autorización explícita, y ninguna función depende de entregarlos. Ojo: descripciones de compras, notas o fotos pueden revelarlos | Ley 1581 de 2012, arts. 5 y 6; Decreto 1074 de 2015, art. 2.2.2.25.2.3 |
| 3b | Si se usan **biometría** (huella, rostro) o **datos de salud**, existe una alternativa para quien no los entregue (por ejemplo, entrar sin reconocimiento facial): ninguna actividad puede condicionarse a que el titular suministre datos sensibles | Decreto 1074 de 2015, art. 2.2.2.25.2.3 |
| 4 | Se usan solo para la finalidad informada y se piden solo los datos necesarios | Ley 1581 de 2012, art. 4 |
| 5 | Se conservan solo el tiempo razonable y necesario para la finalidad, y luego se suprimen | Decreto 1074 de 2015, art. 2.2.2.25.2.8 |
| 6 | El titular puede revocar la autorización y pedir la supresión por un medio gratuito y fácil | Decreto 1074 de 2015, art. 2.2.2.25.2.6 |
| 6b | El titular puede conocer, actualizar, rectificar y pedir prueba de su autorización, y la app responde consultas en máximo 10 días hábiles y reclamos en máximo 15 días hábiles | Ley 1581 de 2012, arts. 8, 14 y 15 |
| 7 | Existe una **política de tratamiento** publicada con su contenido mínimo, un aviso de privacidad cuando aplique, y un procedimiento de **consultas y reclamos** en los plazos legales | Ley 1581 de 2012, arts. 14, 15 y 17; Decreto 1074 de 2015, arts. 2.2.2.25.3.1 a 2.2.2.25.3.3 |
| 8 | Se conocen los casos en que **no** se necesita autorización (y no se abusa de ellos) | Ley 1581 de 2012, art. 10 |
| 9 | **Registro Nacional de Bases de Datos (RNBD):** obligatorio para sociedades y entidades sin ánimo de lucro con activos totales superiores a 100.000 UVT, y para personas jurídicas públicas. Una empresa pequeña probablemente no está obligada, pero el resto de la ley sí la obliga | Ley 1581 de 2012, art. 25; Decreto 1074 de 2015, art. 2.2.2.26.1.2 (modificado por el Decreto 90 de 2018) |
| 10 | Si los datos salen de Colombia (nube extranjera), el país tiene nivel adecuado de protección o aplica una excepción; si es un encargado, hay contrato de transmisión | Ley 1581 de 2012, art. 26; Decreto 1074 de 2015, arts. 2.2.2.25.5.1 y 2.2.2.25.5.2; SIC, Circular Externa 005 de 2017, numeral 3.2 (lista de países con nivel adecuado: incluye Estados Unidos, México, Perú, Costa Rica, Reino Unido, República de Corea y la mayoría de la Unión Europea; texto en `../normas/`) |
| 11 | Datos de niños, niñas y adolescentes: el texto de la ley proscribe tratarlos salvo datos públicos, pero la Corte Constitucional lo condicionó (Sentencia C-748 de 2011) y el reglamento lo permite si responde a su interés superior y respeta sus derechos fundamentales; la autorización la da el representante legal después de escuchar al menor, según su madurez. Defina cómo se verifica quién autoriza y guarde la prueba. Trátelo como alto riesgo | Ley 1581 de 2012, art. 7; Decreto 1074 de 2015, art. 2.2.2.25.2.9 |
| 12 | Si hay datos de **comportamiento crediticio o financiero** de terceros (centrales de riesgo, reportes), aplica además el habeas data financiero | Ley 1266 de 2008, con las modificaciones de la Ley 2157 de 2021 (incluidas en el texto de `../normas/`) |

## 3. Lista de seguridad: ¿el diseño "filtra" información?

**[interpretación]** Cada punto es una forma práctica de cumplir el principio de seguridad (art. 4 lit. g) y el deber de conservar la información con seguridad (art. 17). Los estándares citados no son obligatorios por ley, pero dan una base demostrable.

**Regla para quien revisa:** todo punto que el diseño **no especifique** es un **hallazgo**, no algo resuelto. Pida que el diseño lo diga por escrito. Un protocolo sin cifrar o una versión obsoleta de TLS **filtra datos**: nunca es "un detalle de implementación".

| # | Pregunta al diseño | Riesgo si falta | Referencia |
|---|---|---|---|
| 1 | ¿Todas las conexiones van cifradas? Hallazgo si usa o permite **HTTP, FTP, SMTP/IMAP/POP sin TLS, o TLS 1.0 o 1.1** (obsoletos, RFC 8996 de 2021), si no fija versión mínima (TLS 1.2; mejor 1.3), si desactiva la validación de certificados o si no dice nada | Datos legibles o alterables en tránsito | OWASP MASVS-NETWORK; OWASP ASVS; RFC 8996 |
| 2 | ¿Los datos en reposo están cifrados (dispositivo, servidor, cachés, archivos temporales) con llaves fuera del alcance de quien no debe leerlos? | Un robo o una copia expone todo | OWASP MASVS-STORAGE; NIST SP 800-57 |
| 3 | **Llaves y recuperación:** ¿dónde viven las llaves, quién puede recuperarlas, qué pasa si el usuario pierde su dispositivo o su clave? | Pérdida total de datos, o una "puerta de atrás" | NIST SP 800-57; OWASP MASVS-CRYPTO |
| 4 | **Autenticación:** ¿cómo entra el usuario (contraseña, passkey, segundo factor), cuánto dura la sesión, cómo se cierra en un equipo perdido? | Toma de cuentas | NIST SP 800-63B; OWASP MASVS-AUTH |
| 5 | **Dispositivos y sincronización:** ¿cómo se autoriza un dispositivo nuevo y qué ve el servidor intermedio (relay)? | Un dispositivo ajeno recibe todo | **[interpretación]** Defina el emparejamiento y qué viaja cifrado |
| 6 | **Integraciones con terceros** (correo, bancos, nube): ¿pide solo los permisos (scopes) mínimos, cómo guarda los tokens, cómo se revocan? | Un token robado da acceso a más de lo necesario | OWASP MASVS-AUTH; OWASP ASVS |
| 7 | ¿Logs, analítica, reportes de errores y SDK de anuncios **no** reciben datos personales, financieros ni identificadores innecesarios? | Filtración silenciosa a terceros; las etiquetas de privacidad de la tienda quedan falsas | Contratos y etiquetas de privacidad de las tiendas |
| 8 | **Metadatos:** ¿qué revelan IP, fechas, tamaños, frecuencia o nombres de archivo, aunque el contenido vaya cifrado? | Perfilamiento sin leer el contenido | **[interpretación]** Minimice y documente |
| 9 | **Retención y borrado seguro:** ¿cuándo se borran archivos descargados, respaldos y copias de proveedores? ¿Se borra de verdad? | Datos que sobreviven a la finalidad | Decreto 1074 de 2015, art. 2.2.2.25.2.8 |
| 10 | **Respaldos:** ¿van cifrados, quién tiene las llaves, se prueba la restauración? | El respaldo se vuelve la filtración | NIST SP 800-57 |
| 11 | ¿Quién en la empresa puede ver datos de usuarios, con qué control y registro de accesos? | Acceso interno indebido | Mínimo privilegio; acceso de emergencia registrado |
| 12 | ¿Hay contrato con cada proveedor que trate datos (nube, correo, soporte)? | El proveedor responde poco o nada | Ley 1581 de 2012, art. 18; Decreto 1074 de 2015, art. 2.2.2.25.5.2 |
| 13 | ¿Existe un plan de respuesta a incidentes que incluya **avisar a la SIC** de violaciones de seguridad con riesgo para los titulares? | Sanción por no informar; daño mayor | Ley 1581 de 2012, art. 17 lit. n (responsable) y art. 18 lit. k (encargado): informar a la SIC cuando haya violaciones a los códigos de seguridad y riesgos para los titulares **[verificar** canal y plazo actuales en la SIC**]** |
| 14 | ¿Las afirmaciones públicas sobre privacidad ("no vemos sus datos") se pueden demostrar? | Publicidad engañosa | Ley 1480 de 2011, art. 30 |

## 4. Otras normas relacionadas

| Norma | Por qué importa | Dónde |
|---|---|---|
| Ley 1273 de 2009 (delitos informáticos) | Crea el bien jurídico "de la protección de la información y de los datos". El art. 269F sanciona a quien, sin estar facultado, obtenga, compile, venda, intercambie, envíe, intercepte o divulgue datos personales | `../normas/` |
| Decreto 1074 de 2015, Capítulos 25 y 26 del Título 2, Parte 2, Libro 2 (compilan los Decretos 1377 de 2013 y 886 de 2014) | Autorización, políticas, transmisión, responsabilidad demostrada, RNBD | `../normas/` |
| Guía de responsabilidad demostrada (SIC) | Cómo demostrar que las medidas son adecuadas | `../normas/` |

## 5. Preguntas para el abogado

Están en `preguntas-abogado.md`, sección "Datos personales".
