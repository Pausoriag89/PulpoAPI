# 07 — Ruta crítica: de pequeño a escala

> Documento de proceso. Las fechas son relativas al mes 0 (arranque de Fase 0). Cada fase tiene criterios de avance Y de kill — se definen antes de empezar para que el resultado no los negocie.

## Fase 0 — Laboratorio sobre activos propios (M0–M3)

**Objetivo:** las 6 primitivas v0 ejecutándose con instrumentación total sobre demanda cautiva. Cero clientes externos, cero marketing, invisible.

- Entidad legal constituida (la que aísla el riesgo; ver `08-legal.md` y `09-gobernanza-ABIERTA.md`).
- 1 celda: 3 alcaldías CDMX alrededor de los activos propios (Domum + operación Airbnb Reforma).
- 2–3 ejecutores semi-fijos (prestadores de servicios con RFC, retainer parcial + variable — no gig puro: la rotación mata el activo de entrenamiento).
- SKUs v0: inspección con checklist (P1), entrega/recolección de llaves y documentos (P2), recepción de proveedor (P3), supervisión de mantenimiento/limpieza (P4), obtención de documentos simples (P5).
- Software v0: registro de mandatos, máquina de estados, paquete de evidencia con hash, app-guía del ejecutor (aunque sea PWA mínima). El router LLM puede ser humano-asistido en esta fase — lo que no puede faltar es el **dato**.
- Domum como primer agente comandante: sus decisiones disparan dispatches vía la API interna.

**Gate para Fase 1:** ≥150 acciones ejecutadas · SLA ≥90% · esquema de evidencia estable (2 semanas sin cambios) · costo real por acción conocido por SKU.
**Kill/pivot:** si tras 3 meses la varianza del mundo real impide estandarizar (SLA <75% sostenido con ejecutores entrenados), la tesis de determinismo falla → rediseñar antes de gastar en clientes.

## Fase 1 — Primer vertical externo: despachos legales (M4–M9)

**Objetivo:** ingresos externos reales y el endurecimiento de P2/P6 (custodia, identidad, acuse) que los verticales regulados comprarán después.

- 10–20 despachos pequeños/medianos en CDMX. Venta directa, silenciosa, sin marca pública fuerte (restricción 2028).
- Garantía formal v1 (reembolso + múltiplo acotado, tope por SKU) publicada en contrato.
- Partner notarial/actuarial para lo que exige fe pública (patrón partner-para-actos-licenciados).
- STR managers externos como extensión natural del vertical inmobiliario si hay capacidad ociosa.
- Dashboard de siniestralidad por primitiva desde la primera acción externa.

**Gate:** margen de contribución positivo por acción · SLA ≥95% · ≥3 clientes recurrentes con ≥20 acciones/mes · siniestralidad <3% por primitiva.
**Kill/pivot:** si el costo de adquisición de despachos supera 6 meses de su margen, el vertical externo #1 se sustituye (candidato siguiente: marketplaces de usados) sin tocar la operación.

## Fase 2 — Superficie agéntica encendida + multiplexeo (M10–M18)

**Objetivo:** pasar de operación con software a plataforma con operación.

- MCP server + REST API en beta privada: primeros agentes externos comandando acciones reales (los términos de RentAHuman/HumanInLoop informan el pricing agéntico).
- Router LLM en producción con allowlist completa y anti-estructuración automática.
- Vertical #3 (marketplaces de usados — ejercita la sesión viva) y retail execution como relleno de utilización (≤30% de horas de celda).
- Arquitectura de consentimiento para captura de video opt-in: primeros episodios del corpus formal.
- Segunda celda solo si la primera satura (>70% utilización sostenida 2 meses).

**Gate:** ≥1,000 acciones/mes · ≥5 agentes externos activos vía API o 2 integraciones B2B agénticas · utilización ≥55% · unit economics de `04-economics.md` validados o corregidos.

## Fase 3 — Lanzamiento visible (M18–M24, calendario 2028)

- Restricción BBVA levantada → marca pública, venta enterprise (seguros, verificaciones financieras), diáspora.
- Levantamiento de capital CON datos: siniestralidad de 24 meses, corpus en formatos estándar, demanda agéntica demostrada. (Levantar antes = vender barato la tesis sin la evidencia.)
- Decisión de gobernanza/estructura definitiva (ver `09-gobernanza-ABIERTA.md` — se decide aquí, no en Fase 0).
- Exploración formal de venta de cobertura de habilidades a labs de robótica.

## Reglas transversales de la ruta

1. Verticales antes que geografía; geografía solo por saturación.
2. Nada visible ni enterprise antes de 2028.
3. Todo mes sin cliente externo después de M6 es una alarma roja del patrón "expandir búsqueda en vez de actuar".
4. La API pública nunca se publicita antes de que la operación la respalde (lección RentAHuman).
