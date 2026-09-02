# Landing page de IAIdea Factory — especificación de ejecución

> Estado: **CONGELADO v1** (2026-09-02). Documento de proceso. Contiene el contexto suficiente para construir la landing sin leer el resto del repo. Si algo aquí contradice a `docs/` o a `decisiones/registro.md`, manda el repo y se corrige este documento. Decisiones que lo sustentan: D25 a D29.

## Cómo usar este documento

Este documento está escrito para quien construya la página, sea una persona o un modelo de lenguaje en otra sesión. Sigue estas reglas:

- Construye lo que está especificado. Si una sección exige contenido que no está aquí ni en `docs/`, no lo inventes: deja un marcador `POR_DEFINIR` y repórtalo.
- Respeta las fronteras de la sección "Lo que la página no hace". Son restricciones legales, no preferencias de diseño.
- El orden de construcción de la sección "Orden de construcción" es obligatorio: la etapa 1 sale sin cobro.
- Toda cifra de la página lleva su origen en este documento. No añadas cifras nuevas.

## Contexto en una página

**Qué vende IAIdea Factory.** Acciones físicas verificables ejecutadas por operadores humanos entrenados, con evidencia estructurada, garantía por tarea y trazabilidad completa. El cliente pide una tarea de un catálogo cerrado; un operador la ejecuta bajo un procedimiento estándar y con telemetría; el cliente recibe un paquete de evidencia con hash o, si la tarea no se cumple con el nivel de servicio pactado, un reembolso automático más un múltiplo acotado del precio. El servicio arranca en la Ciudad de México en beta privada durante 2027.

**Por qué existe.** Los agentes de IA ya razonan, planean y pagan, pero no tienen cuerpo. Todo lo que exige presencia física, como inspeccionar, entregar, recoger, esperar, supervisar o firmar, hoy termina en una persona coordinando por WhatsApp sin evidencia ni garantía. IAIdea Factory expone el mundo físico como un servicio estandarizado. Hoy lo compran personas y empresas; el mismo contrato sirve para que un agente de IA lo invoque por API cuando esa demanda llegue.

**El catálogo.** Todo lo que se puede pedir es una configuración de seis primitivas. No existe la tarea en texto libre. La tabla siguiente es la referencia para todo el contenido de la página:

| Primitiva | Qué hace | Evidencia que entrega | Ejemplos |
|---|---|---|---|
| Observar | Documenta el estado de un bien, espacio o situación contra una lista de verificación | Fotos georreferenciadas, timestamps, lista llenada, hash del paquete | Acta de entrada o salida de un inmueble, revisión de un auto usado, estado de un anaquel |
| Transferir | Mueve un documento u objeto con identidad verificada en ambos extremos y cadena de custodia | Cadena de custodia, acuse firmado, identidad verificada | Entrega de un contrato con acuse, notificación extrajudicial, llaves |
| Representar | Presencia física bajo mandato: fila, turno, ventanilla, recepción de un tercero | Mandato verificado, registro de la gestión, resultado documentado | Recoger un acta, recibir a un proveedor, guardar un turno |
| Supervisar | Observa a un tercero ejecutando un servicio y valida contra un criterio de conformidad | Sesión, lista de verificación, veredicto, registro de desviaciones | Supervisar al plomero, la limpieza de una renta corta, una reparación en casa de un familiar |
| Obtener | Consigue un documento, constancia u objeto emitido o vendido por un tercero | Comprobante, custodia hasta la entrega | Copias certificadas, constancias, compras específicas |
| Acreditar | Recolecta firmas y consentimientos con verificación presencial de identidad | Identidad verificada, firma, registro audiovisual con consentimiento, timestamp | Firma de un contrato de renta, consentimientos |

**Lo que no es.** No es un marketplace de tareas: no subasta, despacha con nivel de servicio y responde por el resultado. No es mensajería: el producto es la evidencia, no el traslado. No maneja efectivo ni valores. No ejecuta oficios licenciados ni actos de fe pública: los rutea a notarios, actuarios y técnicos certificados. No vende personas: vende acciones verificadas, y el operador es sustituible por diseño.

**Las cuatro garantías de confianza.** Mandato: cada tarea se ejecuta bajo un mandato del cliente con alcance enumerado y topes; sin mandato vigente no se despacha. Evidencia: cada tarea cierra con un paquete de evidencia con hash encadenado, que el cliente puede verificar. Garantía: cubre el incumplimiento propio con tope por tarea; no cubre daño consecuencial; no se cobra prima separada. Privacidad: observación estructurada por default; video solo con consentimiento explícito; interiores de vivienda solo con autorización explícita del titular.

**Estado del proyecto.** Blueprint completo y operación en construcción. Celda inicial en la Ciudad de México con tres a cuatro operadores. Beta privada en 2027. Sin fecha pública de inicio.

**Glosario para la página.** La página usa vocabulario de cliente; el repo usa vocabulario interno. Equivalencias: tarea = acción; operador = ejecutor; nivel de servicio = SLA; catálogo = primitivas y SKU; paquete de evidencia = cadena de evidencia. Usa siempre el término de cliente en la página.

## Decisiones congeladas para la landing

La tabla siguiente reúne las decisiones que este documento aplica. Cada una está en `decisiones/registro.md` con su razón:

| Tema | Decisión | Registro |
|---|---|---|
| Nombre | IAIdea Factory nombra empresa, servicio y API. PULPO es codename interno y no aparece en la página | D25 |
| Visibilidad | Página pública e indexable, con listas de espera y venta de capacidad futura. El fundador no se nombra, no se muestra ni se enlaza hasta 2028 | D26 |
| Fecha | Sin cuenta regresiva. La página anuncia "Beta privada · 2027" sin día | D27 |
| Precios | Precio de lista $500 MXN por tarea. Paquetes de 10, 50, 100, 200 y 1,000 tareas con descuento máximo de 25%. El paquete de 1,000 se vende solo con contrato | D28 |
| Cupo y vigencia | 1,000 tareas de cupo total para la beta; paquetes con vigencia de 12 meses desde el inicio de la beta; reembolso total si la beta no abre | D28 |
| Elegibilidad | Empresas y personas físicas. Pago por transferencia SPEI y tarjeta. Factura CFDI en todo pedido. El cobro a personas físicas abre solo tras la revisión legal de consumo | D29 |
| Idioma | Solo español en v1 | — |
| Celda inicial | Cuauhtémoc, Miguel Hidalgo y Benito Juárez, por confirmar contra la ubicación real de los activos de Fase 0 | — |
| Operadores | Sin bloque de reclutamiento hasta la opinión laboral | — |
| Redes y prensa | Sin redes sociales ni nota de prensa en v1. Sí Open Graph para previsualizar enlaces | — |

## Lo que la página no hace

Estas restricciones son obligatorias y vienen de decisiones legales congeladas del blueprint:

- No nombra al fundador, no muestra su foto, no enlaza su perfil ni menciona a su empleador.
- No publica documentación de API, ni sandbox, ni fechas de la API. La API existe solo como lista de espera.
- No promete velocidad, cobertura o resultados con superlativos. No usa "garantiza" fuera del término contractual "garantía".
- No menciona manejo de efectivo, ni ofrece pagos a terceros por cuenta del cliente fuera del canal digital de la plataforma.
- No ofrece actos de fe pública, notificaciones judiciales ni oficios técnicos como servicios propios.
- No usa cuenta regresiva, ni fecha exacta de inicio, ni "lanzamiento".
- No usa imágenes de stock ni fotos de personas reales. Ilustración propia o interfaz real.
- No incluye cifras que no estén en este documento.
- No abre el cobro antes de cumplir los requisitos de la etapa 2.

## Trabajos de la página y prioridad

La página cumple cuatro trabajos, en este orden de prioridad cuando compitan por el mismo espacio:

1. Vender capacidad de la beta mediante reservas y, en etapa 2, paquetes pagados.
2. Explicar el concepto completo a quien no conoce el proyecto.
3. Capturar suscriptores al newsletter por segmento.
4. Presentar la tesis a inversionistas sin convertir la página en un deck.

## Audiencias y selector

La página tiene un selector con tres audiencias y **cliente** como default: cliente, inversionista y partner. El contenido base es el mismo para todas; cambian el texto del hero, los bloques marcados por audiencia y los botones de acción. La tabla siguiente define cada modo:

| Audiencia | Quién es | Hero | Botón principal | Secciones destacadas |
|---|---|---|---|---|
| Cliente | Despachos legales, administradores de propiedades, operadores de renta corta y personas que necesitan una gestión física en CDMX | Acciones físicas con evidencia y garantía | Reservar paquete de beta | Cómo funciona, catálogo, casos de uso, paquetes |
| Inversionista | Inversionista ángel o fondo con interés en infraestructura de IA física en LatAm | La capa de actuación física para agentes de IA en LatAm | Recibir el informe mensual | Por qué ahora, el moat, el modelo, la ruta |
| Partner | Quien construye agentes o plataformas y necesita ejecución física | Seis llamadas para darle manos a un agente | Entrar a la lista de espera de la API | Cómo funciona, protocolo, lista de espera |

El selector persiste en `localStorage` y se refleja en la URL con el parámetro `?a=cliente|inversionista|partner`, para que un enlace compartido abra en el modo correcto.

## Reglas de copy

El copy de la página sigue estas reglas. Aplícalas a todo texto visible:

- Segunda persona, tú. Presente. Voz activa. Oraciones de menos de 26 palabras.
- Sin exclamaciones, sin metáforas, sin jerga de internet, sin "simplemente" ni "fácil".
- Sin superlativos ni claims sin fuente. Las cifras de terceros llevan su fuente en el pie de la sección.
- Hecho y opinión separados: las estimaciones propias se presentan como estimaciones.
- Cifras con convención mexicana: coma de millares, punto decimal, porcentaje pegado. Precios en pesos con "MXN" en la primera mención de cada sección.
- Vocabulario de cliente según el glosario. Un término por concepto.
- Los botones nombran la acción y su objeto: "Reservar paquete de beta", no "Empezar".

## Mapa de secciones

La tabla siguiente fija el orden de la página, el trabajo que cumple cada sección y su fuente en el repo:

| Orden | Sección | Trabajo | Fuente |
|---|---|---|---|
| 0 | Barra de navegación | venta | — |
| 1 | Hero | concepto, venta | `README.md` nivel 1 |
| 2 | El problema | concepto | `docs/01-tesis.md`, benchmark |
| 3 | Qué es IAIdea Factory | concepto | `README.md` nivel 2, `docs/03-primitivas.md` |
| 4 | Cómo funciona una tarea | concepto, confianza | `docs/05-arquitectura.md` |
| 5 | Catálogo y fronteras | concepto, legal | `docs/03`, `docs/08-legal.md` |
| 6 | Casos de uso con costo real | venta | benchmark, `docs/04b-unit-economics.md` |
| 7 | Garantía, evidencia y privacidad | confianza | `docs/04`, `docs/05`, `docs/08` |
| 8 | Beta y paquetes | venta | D28, D29 |
| 9 | Cobertura y calendario | expectativas | `docs/07-ruta-critica.md` |
| 10 | Para inversionistas | pitch | `docs/01`, `02`, `06`, `04b`, `pitch/` |
| 11 | Para partners y agentes | lista de espera | `docs/05`, D07 |
| 12 | Newsletter | newsletter | — |
| 13 | Preguntas frecuentes | confianza, legal | `docs/08-legal.md` |
| 14 | Pie legal | legal | `docs/08-legal.md` |

## Especificación por sección

### Barra de navegación

**Objetivo.** Que la reserva y el cambio de audiencia estén siempre a un clic.

**Contenido.** Marca IAIdea Factory a la izquierda. Enlaces: Cómo funciona, Catálogo, Paquetes, Inversionistas, Newsletter. Selector de audiencia. Botón persistente a la derecha.

**Estados del botón.** En etapa 1: **Reservar lugar en la beta**. En etapa 2: **Comprar paquete**. Con la beta en curso: **Pedir una tarea**. Con el cupo agotado: **Entrar a la lista de espera**.

**Móvil.** La barra colapsa a marca, selector y botón. Los enlaces van en un menú.

### Hero

**Objetivo.** En cinco segundos el visitante entiende qué compra, dónde y cuándo.

**Copy propuesto, modo cliente.**

- Etiqueta superior: "Beta privada · Ciudad de México · 2027".
- Título: "Acciones físicas verificables, con garantía".
- Subtítulo: "Pide una inspección, una entrega con acuse, una firma o una gestión. Un operador entrenado la ejecuta bajo tu mandato, con evidencia con hash y garantía por tarea. Si no se cumple, se reembolsa por regla."
- Botones: **Reservar paquete de beta** y **Recibir actualizaciones**.
- Línea de contexto: "Cupo de la beta: 1,000 tareas. Reserva sin cargo; reembolso total si la beta no abre."

**Copy propuesto, modo inversionista.**

- Título: "La capa de actuación física para agentes de IA en LatAm".
- Subtítulo: "Hoy, humanos instrumentados ejecutan acciones físicas con evidencia y garantía. El mismo contrato sirve para agentes de IA y, después, para robots. El activo que se acumula es el registro de cómo se ejecuta el trabajo físico."
- Botón: **Recibir el informe mensual**.

**Copy propuesto, modo partner.**

- Título: "Seis llamadas para darle manos a un agente".
- Subtítulo: "observar, transferir, representar, supervisar, obtener y acreditar. Cada llamada devuelve evidencia estructurada y corre bajo un mandato con topes. La API se enciende sobre una operación probada."
- Botón: **Entrar a la lista de espera de la API**.

**Componentes.** Ilustración propia del flujo pedir, despachar y evidencia, o el bloque de sesión del pitch en modo estático. Sin video.

### El problema

**Objetivo.** Que el visitante se reconozca en el problema antes de ver la solución.

**Contenido.** Tres situaciones con su costo actual. Copy propuesto:

- "Necesitas fe de que algo ocurrió. Un notario a domicilio cobra hasta $6,869 MXN por hora o fracción, según el arancel de la Ciudad de México de enero de 2026, aunque la mayoría de las veces no necesitas fe pública: necesitas evidencia."
- "Necesitas entregar un contrato con acuse. Mandas al pasante: de 3 a 4 horas de una persona con sueldo promedio de $13,606 MXN al mes, sin evidencia estructurada y sin garantía."
- "Necesitas supervisar un mantenimiento a distancia. No existe un servicio unitario para eso: contratas a alguien de tiempo completo, o confías."

Cierre: "La coordinación por WhatsApp no deja evidencia, no tiene nivel de servicio y no tiene garantía."

**Fuentes en el pie.** Arancel notarial de la Ciudad de México, enero de 2026; sueldo promedio de abogado junior en la Ciudad de México, Indeed, julio de 2026.

**Variante inversionista.** El problema desde el agente: "Un agente de IA puede razonar, buscar, escribir, pagar y coordinar. No puede tocar. Cada cadena autónoma que llega a un paso físico se rompe y vuelve a un humano."

### Qué es IAIdea Factory

**Objetivo.** El concepto completo en un párrafo y seis nombres.

**Copy propuesto.** "IAIdea Factory produce acciones físicas estandarizadas. Todo lo que puedes pedir es una configuración de seis primitivas, ejecutada por operadores entrenados con procedimientos fijos y telemetría, bajo tu mandato, con evidencia con hash y garantía. Empezamos en la Ciudad de México con demanda real de hoy: administración de propiedades, despachos legales y gestiones personales. El mismo servicio está diseñado para que lo invoque un agente de IA."

**Componentes.** Seis tarjetas, una por primitiva, con nombre, definición de una línea y un ejemplo. Cada tarjeta enlaza a su entrada del catálogo. Una frase final sobre el operador sustituible: "El contrato no cambia cuando el operador deje de ser humano."

### Cómo funciona una tarea

**Objetivo.** Mostrar el proceso completo y dónde entra la garantía.

**Copy propuesto, cuatro pasos.**

1. "Pides una tarea del catálogo con sus parámetros. Firmas un mandato con alcance y topes, una sola vez si eres cliente recurrente."
2. "Un operador entrenado la ejecuta con un procedimiento fijo y telemetría. Ves el avance con observaciones estructuradas, no con video, salvo que lo autorices."
3. "Recibes el paquete de evidencia con hash: fotos georreferenciadas, timestamps, lista de verificación y acuses. Puedes comprobar que nadie lo editó después de cerrarlo."
4. "Si la tarea no se cumple con el nivel de servicio, la garantía se dispara por regla: reembolso más un múltiplo acotado del precio. Sin negociación."

**Componentes.** El bloque de sesión de `pitch/index.html`, reutilizado con el mismo ejemplo de inspección, en modo estático o con reproducción. La línea de estados de la tarea: solicitada, validada, despachada, en sesión, evidencia entregada, verificada, cerrada o fallida con garantía.

### Catálogo y fronteras

**Objetivo.** Que el visitante sepa qué puede pedir y qué no, antes de reservar.

**Contenido.** Una entrada expandible por primitiva con: qué hace, evidencia que entrega, ejemplos y frontera cuando aplique. Los textos salen de la tabla de la sección "Contexto en una página". Bloque de fronteras siempre visible, sin plegar, con este copy:

- "No manejamos efectivo ni valores. Los pagos a terceros van siempre por el canal digital de la plataforma."
- "No hacemos actos de fe pública ni notificaciones judiciales. Acreditamos el hecho y armamos el expediente; el notario o el actuario ponen el acto."
- "No ejecutamos oficios técnicos. El operador supervisa al plomero; no es el plomero."
- "No es un marketplace. No subastamos tu tarea: la despachamos y respondemos por ella."

### Casos de uso con costo real

**Objetivo.** Convertir el concepto en una comparación de costo por tipo de cliente.

**Contenido.** Cuatro casos en una tabla, con la alternativa actual, su costo y la tarea equivalente:

| Caso | Quién | Alternativa actual | Costo actual | Tarea y precio de lista |
|---|---|---|---|---|
| Notificación con acuse | Despacho legal | Fedatario, o pasante de 3 a 4 horas | $1,500 a $4,000 MXN, o ~$340 de costo interno más horas no facturadas | Transferir, $500 |
| Acta de entrada de un departamento en renta | Administrador de propiedades | Inspector profesional, o el dueño en persona | $1,500 a $4,500 MXN | Observar, $500 |
| Supervisión de un plomero para un dueño a distancia | Operador de renta corta | No existe unitaria | Un administrador de tiempo completo | Supervisar, $500 |
| Reparación en casa de tus padres, supervisada | Persona que vive fuera | Un familiar o nadie | Sin evidencia | Supervisar, $500 |

**Pie de tabla.** "Precios de alternativas: estimaciones a partir de aranceles y cotizaciones públicas de la Ciudad de México en 2026. Precio de lista de IAIdea Factory por tarea; los paquetes tienen descuento."

**Variante inversionista.** La tabla se sustituye por los tres pisos de valor de la misma ejecución: el servicio paga la operación, el proceso sube el margen, el dato es el activo de la década.

### Garantía, evidencia y privacidad

**Objetivo.** Responder las tres objeciones antes de que aparezcan.

**Copy propuesto.**

- Garantía: "Cubre el incumplimiento propio: no ejecución, evidencia inválida o nivel de servicio roto. Reembolso más un múltiplo acotado del precio, con tope por tarea. No cubre daños consecuenciales. No cobramos prima aparte: la garantía está en el precio."
- Evidencia: "Cada tarea cierra con un paquete de evidencia con hash encadenado. Puedes verificar que el paquete no cambió después de cerrarse."
- Mandato: "Cada tarea se ejecuta bajo tu mandato, con alcance enumerado y topes. Sin mandato vigente, no se despacha."
- Privacidad: "Observación estructurada por default. Video solo con tu consentimiento explícito. Interiores de vivienda solo con autorización del titular. Aviso de privacidad por rol."

**Componentes.** Cuatro bloques cortos con enlace a los términos completos.

### Beta y paquetes

**Objetivo.** Vender capacidad de la beta sin prometer lo que la celda no puede entregar.

**Contenido.**

- Encabezado: "Beta privada · 2027 · Ciudad de México".
- Cupo: "Cupo total de la beta: 1,000 tareas". Contador en vivo de tareas disponibles, leído de la base de datos.
- Tabla de paquetes, con la escalera de D28.
- Condiciones: vigencia de 12 meses desde el inicio de la beta; reembolso total si la beta no abre; transferencia SPEI o tarjeta; factura CFDI en todo pedido; el paquete de 1,000 tareas se contrata con firma, no en línea.
- Qué incluye cada tarea: despacho con nivel de servicio, paquete de evidencia con hash, garantía por tarea. Qué no incluye: derechos y pagos a terceros en tareas de obtener, que se cobran aparte por el canal digital.

**Escalera de paquetes.** La tabla siguiente es la única fuente de precios de la página:

| Paquete | Tareas | Precio por tarea | Descuento | Total | Cómo se compra |
|---|---|---|---|---|---|
| Prueba | 10 | $500 | 0% | $5,000 | En línea |
| Despacho | 50 | $460 | 8% | $23,000 | En línea |
| Operación | 100 | $430 | 14% | $43,000 | En línea |
| Cartera | 200 | $400 | 20% | $80,000 | En línea |
| Ancla | 1,000 | $375 | 25% | $375,000 | Con contrato; botón **Solicitar contrato** |

**Estados.**

- Etapa 1, sin cobro: los botones registran una reserva sin cargo. Mensaje de confirmación: "Reservaste N tareas. Te avisamos por correo cuando abra el cobro. Sin compromiso." La reserva descuenta del contador de cupo.
- Etapa 2, con cobro abierto para empresas: los botones llevan al checkout. Las personas físicas ven "Cobro para personas físicas: próximamente" hasta que se complete la revisión legal de consumo.
- Etapa 2 completa: checkout para todos.
- Cupo agotado: los botones cambian a **Entrar a la lista de espera** y el texto explica que la segunda celda abre por saturación de la primera.

**Razón económica, para quien construya.** El descuento se financia con certeza de utilización: un paquete prepagado es capacidad reservada, y la capacidad reservada permite ruteo denso. El prepago produce capital de trabajo negativo, lo que resuelve el pendiente D24 del modelo económico. El paquete Ancla deja un margen muy corto por tarea; por eso exige contrato.

### Cobertura y calendario

**Objetivo.** Fijar dónde y cuándo, sin fecha exacta.

**Copy propuesto.** "Celda inicial: Cuauhtémoc, Miguel Hidalgo y Benito Juárez. Abrimos una alcaldía nueva cuando la celda actual pasa de 70% de utilización sostenida durante dos meses. Beta privada en 2027. API para partners en beta privada después, sin fecha."

**Componentes.** Mapa simple con las tres alcaldías, hecho con SVG propio, o lista. Sin mapa de terceros.

**Notas.** Las alcaldías son `POR_CONFIRMAR` hasta que se validen contra la ubicación de los activos de Fase 0. No se publica el calendario interno de fases.

### Para inversionistas

**Objetivo.** La tesis completa en cuatro bloques y un enlace al manual del operador.

**Copy propuesto.**

- Por qué ahora: "El PIB por hora trabajada en paridad de poder adquisitivo es de cerca de $97 USD en Estados Unidos y $25 USD en México, según la OCDE con datos de 2024 y 2025. Esa brecha es una capa de trabajo físico sin instrumentar, sin estandarizar y sin datos. La ventana para instrumentarla antes del despliegue robótico en LatAm es de años, no de décadas."
- El moat: "No somos una cámara que graba trabajo. Somos una fundición de datos de habilidades físicas: especificación antes de captura, etiquetado denso que sale de operar, diversidad de entornos de LatAm y derechos limpios. El video crudo se comercia a $2 a $5 USD por hora; los datos especificados, a cerca de 100 veces ese precio."
- El modelo: "Contribución marginal de 75% por tarea. Breakeven de una celda entre 105 y 260 tareas al mes según la estructura. El prepago de paquetes convierte el capital de trabajo en negativo."
- Estado y siguiente paso: "No levantamos capital en esta etapa. La conversación de capital ocurre con datos de siniestralidad de 24 meses. Recibe el informe mensual: tareas ejecutadas, nivel de servicio, siniestralidad agregada y cupo restante."

**Componentes.** Botón **Recibir el informe mensual** (suscripción al segmento inversionista). Enlace **Leer el manual del operador** a `/pitch`.

**Notas.** Sin ronda abierta, sin valuación, sin term sheet. El pitch en `/pitch` se actualiza a la marca IAIdea Factory antes de publicar la landing (pendiente listado al final).

### Para partners y agentes

**Objetivo.** Capturar demanda agéntica sin publicitar una API que no opera.

**Copy propuesto.** "Seis llamadas: observar, transferir, representar, supervisar, obtener y acreditar. Cada una corre bajo un mandato con alcance y topes, abre una sesión con observaciones estructuradas y cierra con un paquete de evidencia con hash. La API y el servidor MCP se encienden sobre una operación probada. La lista de espera define el orden de acceso."

**Formulario.** Correo, nombre de la organización, qué agente o plataforma operas, qué primitiva necesitas primero. Sin documentación, sin sandbox, sin fecha.

### Newsletter

**Objetivo.** Un formulario que alimenta tres listas.

**Contenido.** Nombre: "Bitácora de la fábrica". Campos: correo y segmento (cliente, inversionista, partner). Doble opt-in. Cadencia mensual. Cada edición reporta tareas ejecutadas, nivel de servicio del mes, siniestralidad agregada, alcaldías activas y cupo restante.

**Copy del formulario.** "Un correo al mes con las cifras de la operación: tareas ejecutadas, nivel de servicio, siniestralidad y cupo. Sin promociones."

### Preguntas frecuentes

**Objetivo.** Cerrar objeciones legales y operativas con respuestas cortas. Cada respuesta enlaza a su sección.

1. **¿Cuándo empieza la beta?** "En 2027, en la Ciudad de México. No publicamos día. Si reservaste, te avisamos por correo con al menos 30 días de anticipación."
2. **¿Qué pasa si la beta no abre?** "Se reembolsa el total de tu paquete sin condiciones. Las reservas sin cargo no requieren ninguna acción."
3. **¿Cómo pido una tarea durante la beta?** "Desde el portal web con tu cuenta. Durante la beta también por correo, con el mismo registro y la misma evidencia."
4. **¿Qué es el mandato y por qué lo firmo?** "Es la autorización con la que actuamos por ti, con alcance enumerado y topes. La ley exige mandato para actuar a nombre de otro. Lo firmas una vez y cubre tus tareas dentro de ese alcance."
5. **¿Qué cubre la garantía?** "Nuestro incumplimiento: no ejecución, evidencia inválida o nivel de servicio roto. Reembolso más un múltiplo acotado del precio, con tope por tarea. No cubre daños consecuenciales."
6. **¿Cómo verifico la evidencia?** "Cada paquete lleva un hash encadenado. En el portal puedes comprobar que el paquete no cambió después de cerrarse."
7. **¿Manejan efectivo?** "No. Ningún operador recibe ni entrega dinero. Los pagos a terceros van por el canal digital de la plataforma."
8. **¿Hacen trámites que requieren notario?** "No como servicio propio. Acreditamos el hecho y preparamos el expediente; el notario o el actuario ponen el acto."
9. **¿Puedo comprar como persona física?** "Sí. El cobro para personas físicas abre cuando se complete la revisión legal de consumo; mientras tanto puedes reservar sin cargo."
10. **¿Cómo facturan?** "Factura CFDI en todo pedido, a empresa o a persona física con RFC. Sin RFC, factura a público en general."

### Pie legal

**Contenido.** "IAIdea Factory · Ciudad de México". Enlaces: aviso de privacidad, términos de la beta, términos de la garantía, contrato marco de mandato. Correo de contacto corporativo. Sin redes sociales en v1. Sin nombre de personas.

## Formularios y datos

La página captura cuatro tipos de registro. La tabla siguiente define las tablas mínimas en la base de datos:

| Tabla | Campos | Reglas |
|---|---|---|
| `suscriptores` | id, correo, segmento (cliente, inversionista, partner), confirmado (bool), fecha_alta, fecha_confirmacion, origen (`?a=` y `?ref=`) | Doble opt-in obligatorio. Baja con un clic desde cada correo |
| `reservas` | id, correo, tipo_cliente (empresa, persona_fisica), razon_social o nombre, rfc (opcional en etapa 1), paquete (10, 50, 100, 200, 1000), estado (reservada, convertida, cancelada, en_lista_de_espera), fecha | Una reserva descuenta del cupo. El paquete 1000 crea una solicitud de contrato, no una reserva |
| `pedidos` | id, reserva_id, monto, metodo (spei, tarjeta), referencia_pago, estado (pendiente, pagado, reembolsado), cfdi_folio, fecha | Solo en etapa 2. Un pedido pagado convierte la reserva |
| `lista_espera_api` | id, correo, organizacion, agente_o_plataforma, primitiva_prioritaria, fecha | Sin promesa de fecha |
| `cupo` | total (1000), reservado, pagado | El contador público muestra `total − reservado` |

**Flujo de reserva, etapa 1.** El visitante elige paquete, deja correo, tipo de cliente y nombre. Recibe un correo de confirmación con el resumen y el aviso de que no hay cargo. El cupo público baja. Una reserva sin confirmación de correo en 7 días se libera.

**Flujo de compra, etapa 2.** El visitante confirma la reserva o compra directo. Tarjeta: checkout de Stripe con el monto del paquete. SPEI: se muestra referencia y CLABE, y el pedido queda pendiente hasta la conciliación. Tras el pago: correo con confirmación, factura CFDI en un plazo definido por administración, y activación del paquete al inicio de la beta.

**Validaciones.** Correo con confirmación. RFC con formato válido cuando se capture. Un correo puede tener varias reservas. Sin captcha de terceros: usa un honeypot y límite de frecuencia por IP.

## Estados de la página

La página tiene cuatro estados globales, controlados por una sola variable de configuración:

| Estado | Cuándo | Qué cambia |
|---|---|---|
| `etapa_1` | Desde la publicación | Reservas sin cargo, newsletter, listas de espera. Sin checkout |
| `etapa_2_empresas` | Contrato marco, términos de garantía y entidad constituida listos | Checkout abierto para empresas. Personas físicas siguen en reserva |
| `etapa_2_completa` | Revisión legal de consumo completada | Checkout para todos |
| `beta_en_curso` | Primer despacho externo | El botón principal pasa a **Pedir una tarea**; el bloque de beta muestra tareas ejecutadas y nivel de servicio del mes |

El estado `cupo_agotado` se superpone a cualquiera de los anteriores cuando `reservado + pagado ≥ total`.

## SEO

La página es pública e indexable desde el primer día. Requisitos mínimos:

- Título: "IAIdea Factory — Acciones físicas verificables con garantía en CDMX". Descripción de menos de 160 caracteres con las palabras: inspección, entrega con acuse, firma, gestión, evidencia, garantía, Ciudad de México.
- Un solo H1 por página, igual al título del hero en modo cliente. Encabezados H2 para cada sección del mapa.
- URLs: `/` landing, `/pitch` manual del operador, `/terminos`, `/privacidad`, `/garantia`, `/mandato`. Sin parámetros en las URL canónicas; el selector de audiencia usa `?a=` y declara canónica la URL sin parámetro.
- `sitemap.xml` con las seis URL. `robots.txt` abierto.
- Datos estructurados JSON-LD: `Organization`, `Service` con `areaServed` en las tres alcaldías, y `FAQPage` con las diez preguntas.
- Open Graph y Twitter Card con imagen propia de 1200 × 630 píxeles y el título del hero.
- Rendimiento: menos de 100 KB de HTML, CSS y JavaScript propios, sin fuentes externas, sin frameworks. Imágenes en SVG o WebP.
- Idioma declarado `es-MX`.

Términos de búsqueda objetivo, en español: "inspección de inmueble con evidencia CDMX", "entrega de documentos con acuse CDMX", "supervisión de mantenimiento a distancia", "gestor con evidencia Ciudad de México", "acciones físicas para agentes de IA".

## Arquitectura técnica

La landing captura correos, reserva paquetes y cobra, así que no es un archivo estático puro. La tabla siguiente fija el stack:

| Capa | Herramienta | Razón |
|---|---|---|
| Front | HTML, CSS y JavaScript sin framework, desplegado en Vercel | Misma disciplina del pitch; carga rápida; nada que mantener |
| Datos | Supabase con las cinco tablas de la sección anterior y políticas de acceso por fila | Base del blueprint; el contador de cupo lee de aquí con una función pública de solo lectura |
| Funciones | Funciones serverless de Vercel para reservas, suscripciones y webhooks de pago | Sin servidor propio en la beta |
| Pagos | Stripe Checkout para tarjeta; SPEI por referencia con conciliación manual | En México las empresas pagan por SPEI; la tarjeta sirve a paquetes chicos y personas físicas |
| Factura | Emisión manual de CFDI durante la beta; automatizar con Facturama después de 50 pedidos | Volumen bajo al inicio |
| Correo | Resend para transaccional y newsletter, con doble opt-in | Segmentos sin plataforma pesada |
| Analítica | Plausible | Sin cookies de terceros |
| Dominio | `POR_DEFINIR`: verificar disponibilidad de iaideafactory.com y iaideafactory.mx | Marca nueva |

Variables de entorno esperadas: `SUPABASE_URL`, `SUPABASE_SERVICE_KEY`, `STRIPE_SECRET_KEY`, `STRIPE_WEBHOOK_SECRET`, `RESEND_API_KEY`, `ESTADO_PAGINA` con uno de los cuatro estados. Ninguna clave va en el HTML.

## Diseño visual

La landing no hereda la estética de terminal del pitch: el pitch es un manual para lectores técnicos; la landing vende a despachos, administradores y personas. Dirección: sobria y editorial, con mucho espacio, tipografía de sistema de alta legibilidad y la paleta del pitch como acento: verde para acciones y estados correctos, ámbar para cifras, rojo solo en fronteras. Tema claro por default, con tema oscuro disponible.

El bloque de sesión del pitch es el único elemento con estética de terminal, porque muestra el protocolo real. Toda ilustración es propia y en SVG. Sin fotos de stock, sin fotos de personas.

Antes de escribir código, quien construya presenta tres variantes del hero y del bloque de paquetes, y Pablo elige una. Ese es el mismo método con el que se decidió la estética del pitch.

## Orden de construcción

Construye en este orden. Cada paso tiene un entregable y un criterio de aceptación:

1. **Dominio y correo corporativo.** Entregable: dominio registrado y un buzón de contacto. Aceptación: el buzón recibe correo.
2. **Aviso de privacidad.** Entregable: texto revisado por abogado, publicado en `/privacidad`. Aceptación: cubre los tres roles y el newsletter. Bloquea la publicación.
3. **Base de datos.** Entregable: las cinco tablas con sus políticas. Aceptación: el contador de cupo se lee sin credenciales y ninguna tabla se escribe sin función servidor.
4. **Página estática completa.** Entregable: las 15 secciones con el copy de este documento, el selector de audiencia y los tres modos. Aceptación: la lista de verificación de la sección siguiente pasa completa en escritorio y en 375 píxeles de ancho.
5. **Formularios de etapa 1.** Entregable: newsletter con doble opt-in, reserva sin cargo, lista de espera de API y solicitud de contrato para el paquete Ancla. Aceptación: cada flujo envía su correo y escribe su registro; el cupo baja con cada reserva confirmada.
6. **SEO y rendimiento.** Entregable: metadatos, JSON-LD, sitemap, robots, Open Graph. Aceptación: menos de 100 KB propios y sin peticiones a terceros salvo Plausible y las funciones propias.
7. **Publicación de etapa 1.** Entregable: la página en el dominio con `ESTADO_PAGINA=etapa_1`. Aceptación: reserva de prueba completa de extremo a extremo.
8. **Pitch con la marca nueva.** Entregable: `pitch/index.html` con IAIdea Factory en lugar de PULPO, servido en `/pitch`. Aceptación: cero menciones de PULPO en el pitch.
9. **Checkout de etapa 2.** Entregable: Stripe Checkout, referencia SPEI, webhook que marca pedidos pagados y correo de confirmación. Aceptación: un pago de prueba en modo test convierte una reserva y envía el correo. No se activa sin los requisitos del estado `etapa_2_empresas`.
10. **Etapa 2 completa.** Entregable: cobro a personas físicas activado con los términos de consumo revisados. Aceptación: el abogado firma la revisión.

## Lista de verificación de aceptación

Antes de publicar cada etapa, comprueba:

- Contenido: cada cifra de la página está en este documento; ninguna sección tiene `POR_DEFINIR` visible; el copy pasa las reglas de la sección "Reglas de copy".
- Legal: no aparece ningún nombre de persona; no hay mención a efectivo, fe pública ni oficios como servicios propios; los cuatro documentos legales están enlazados y existen.
- Funcional: los tres modos de audiencia cambian hero, bloques y botones; el selector persiste y se refleja en `?a=`; el contador de cupo lee de la base; cada formulario escribe y envía correo; el estado global cambia con una sola variable.
- Accesibilidad: contraste AA en ambos temas, foco visible, formularios con etiquetas, texto alternativo en toda ilustración, navegación completa con teclado.
- SEO: un H1, metadatos, JSON-LD válido, sitemap y robots accesibles, canónica sin parámetros.
- Rendimiento: menos de 100 KB propios, sin fuentes externas, sin frameworks, sin scroll horizontal en 375 píxeles.
- Seguridad: ninguna clave en el HTML; escrituras solo por funciones servidor; honeypot y límite de frecuencia activos.

## Dependencias externas con dueño y fecha

La tabla siguiente cruza esta especificación con los pendientes legales de `docs/08-legal.md`:

| Ítem | Bloquea | Dueño | Cuándo |
|---|---|---|---|
| Aviso de privacidad por rol | Publicación de etapa 1 | abogado | Antes de publicar |
| Dominio y correo corporativo | Publicación de etapa 1 | Pablo | Antes de publicar |
| Confirmación de las tres alcaldías de la celda | Sección de cobertura | Pablo | Antes de publicar |
| Términos de la beta: reserva, vigencia, reembolso, cupo | Estado `etapa_2_empresas` | abogado | Antes de M4 |
| Contrato marco de mandato y términos de garantía | Estado `etapa_2_empresas` | abogado | Antes de M4, ya listado en `docs/08-legal.md` |
| Entidad legal constituida y cuenta bancaria para SPEI | Estado `etapa_2_empresas` | fiscalista y corporativo | Fase 0 |
| Revisión de consumo para personas físicas: términos de anticipo, cancelación y, si aplica, registro del contrato de adhesión | Estado `etapa_2_completa` | abogado | Antes de abrir el cobro a personas físicas |
| Actualización del pitch a la marca IAIdea Factory | Enlace a `/pitch` | quien construya | Paso 8 del orden de construcción |
| Instrumentación de Fase 0 para alimentar el newsletter | Primera edición del newsletter | Pablo | M0 |

## Pendientes fuera del alcance de la landing

Estos temas quedan registrados para no olvidarlos, y no bloquean la construcción:

- Tarea suelta para personas físicas, fuera de paquete. Se evalúa con datos de la beta.
- Versión en inglés de la sección de inversionistas. Se evalúa cuando exista demanda.
- Bloque de reclutamiento de operadores. Depende de la opinión laboral de `docs/08-legal.md`.
- Automatización de CFDI. Después de 50 pedidos.
- Segunda celda y lista de espera geográfica. Cuando la primera celda supere 70% de utilización durante dos meses.

## Métricas de la página

Durante la beta se miden cinco cosas:

- Reservas por semana, por tamaño de paquete y por tipo de cliente.
- Conversión de reserva a pago cuando abra el cobro.
- Suscriptores confirmados por segmento.
- Cupo restante frente a la capacidad real de la celda.
- Visitas por origen: enlace compartido con `?ref=`, búsqueda orgánica y directo.
