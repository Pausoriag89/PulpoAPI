# 01 — Tesis

## El problema

Un agente de IA puede razonar, buscar, escribir, pagar y coordinar. No puede tocar. Cada vez que una cadena autónoma llega a un paso físico — verificar que el departamento quedó bien después del plomero, entregar un contrato con acuse, recoger una constancia, esperar un turno, mirar un auto usado antes de comprarlo — la cadena se rompe y regresa a un humano coordinando por WhatsApp. El mundo físico es el último syscall sin implementar.

Los intentos existentes (2026) fallaron por diseño, no por timing:

- **Human API** (EE.UU., $65M de fondos cripto): en realidad es una empresa de datos de entrenamiento (audio, captura visual). "Human Action" es roadmap, no operación.
- **RentAHuman** (EE.UU., indie): marketplace con API y MCP. Resolvió matching y pagos; no resolvió ejecución. Evidencia: tareas con 30 aplicantes y cero cumplimiento; ~70 agentes conectados tras seis meses. Un marketplace best-effort no es consumible por un agente.
- **HumanInLoop** (Filipinas): el único con operación real — porque es un BPO preexistente (iSuporta) con API encima. Valida la secuencia: operación primero, superficie agéntica después. Techo geográfico: no ejecuta en LatAm.

Lo que un agente necesita y nadie ofrece: **determinismo de ejecución**. Pides la acción → se ejecuta con SLA → o falla explícito con reembolso automático. Eso es una operación con garantía, no un tablón de anuncios.

## La solución

Una capa de actuación física con cinco propiedades que ningún jugador combina:

1. **Catálogo cerrado de 6 primitivas** (ver `03-primitivas.md`) — no texto libre. Todo lo ejecutable es una configuración parametrizada de OBSERVAR, TRANSFERIR, REPRESENTAR, SUPERVISAR, OBTENER, ACREDITAR.
2. **Protocolo de sesión con telemetría en vivo** — el agente no postea y espera: comanda, percibe (observación estructurada; video crudo solo bajo elevación) y corrige a mitad de tarea. El humano opera como periférico estandarizado: actuador y sensor.
3. **Cadena de autoridad legal** — mandato del usuario final (humano) con alcance enumerado y topes; el agente es solo canal de instrucción. Registro de mandatos como activo central.
4. **Legalidad por allowlist determinista** — un LLM enruta hacia el catálogo; nunca autoriza. La máquina de estados determinista autoriza. Detección de estructuración por agregación sobre el log.
5. **Garantía por SKU** — respondemos por nuestro propio cumplimiento como mandatarios (reembolso + múltiplo acotado del fee). Precificada con siniestralidad propia por primitiva.

## A quién sirve, en orden

1. **Fase 0 — agentes propios:** Domum (administración de propiedades) y la operación Airbnb propia. Demanda cautiva, cero ciclo de venta, laboratorio del protocolo.
2. **Fase 1 — compradores humanos de acciones verificables:** despachos legales (entregas con acuse, firmas, obtención de documentos), administradores de propiedades y STR. Compran el servicio hoy con presupuesto existente; son el simulador de la demanda agéntica.
3. **Fase 2 — agentes de terceros vía API/MCP:** cuando la autoridad de gasto agéntico llegue a LatAm, la superficie ya existe sobre una operación probada.
4. **Fase 3 — plataformas y dispositivos:** OEMs de inteligencia ambiental y robots de casa; el trigger deja de ser una persona y pasa a ser un sensor.

## Lo que NO somos (fronteras de identidad)

- No somos gig marketplace: no subastamos tareas, despachamos con SLA y respondemos por el resultado.
- No somos mensajería: la entrega es un caso particular de TRANSFERIR con cadena de custodia e identidad; el producto es la evidencia, no el traslado.
- No movemos dinero ni valores (ver `08-legal.md`).
- No ejecutamos oficios licenciados ni actos que exigen fe pública: los ruteamos a partners (notarios, actuarios, técnicos certificados) y entregamos el expediente perfecto.
- No vendemos "humanos": vendemos acciones físicas verificadas. El ejecutor es sustituible por diseño — esa sustituibilidad es la tesis de largo plazo.
