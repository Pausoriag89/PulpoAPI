# 08 — Restricciones legales congeladas y fronteras

> Referencia. Cada regla lleva su razón. Nada de esta lista se relaja sin opinión legal formal por escrito.

## R1 — Cero efectivo, cero valores (congelada desde el día 0)

Hecho: recibir recursos para entregarlos en otro lugar cae textualmente en la definición de transmisor de dinero (Art. 81-A Bis LGOAAC). Operar sin registro CNBV: prisión de 3 a 15 años + multa hasta 100,000 días de salario mínimo. **El registro se dispara por actividad, no por monto** — ningún tope por transacción exenta. La LFPIORPI agrega acumulación en ventanas de 6 meses (anti-estructuración).
Consecuencia de diseño: P5 (OBTENER) paga siempre por canal digital de la plataforma; el ejecutor jamás toca dinero del cliente. Flujos de efectivo del mundo real se rutean a corresponsales bancarios licenciados si algún día se ofrecen — como partners, jamás in-house.

## R2 — Garantía sí, seguro no

Hecho: cubrir riesgo de terceros cobrando prima requiere institución autorizada (LISF/CNSF). Garantizar el cumplimiento propio sin prima separada es derecho mercantil ordinario.
Reglas: (a) la garantía cubre solo incumplimiento propio, con tope; (b) jamás se cobra "prima" separada del fee; (c) daño consecuencial se transfiere a aseguradora tercera cuando la siniesralidad propia lo haga suscribible; (d) plataforma-como-mandataria es la estructura que permite (a) sin ser fianza — garantizar el desempeño de un tercero siendo mero intermediario sí sería fianza.

## R3 — Cadena de autoridad: mandato siempre

Hecho: actuar a nombre de otro exige mandato. Carta poder simple basta para trámites administrativos; actos patrimoniales exigen poder notarial. Un agente de IA no tiene personalidad jurídica: no puede otorgar ni recibir mandato.
Diseño: humano principal → mandato de alcance enumerado y topes → plataforma (mandataria) → ejecutor. El agente es canal de instrucción dentro de un mandato preexistente. Sin mandato vigente: la acción no se despacha, sin excepciones. Mandatos permanentes con alcance/topes ("presupuesto de autonomía") para clientes recurrentes y, a futuro, dispositivos.

## R4 — Fronteras con profesiones licenciadas

- Fe de hechos → notario. Interpelación/notificación judicial → actuario. Ajuste de siniestros → ajustador registrado CNSF. Oficios (plomería, electricidad) → técnicos; el generalista supervisa, no ejecuta.
- Patrón único: PULPO produce el expediente perfecto y la logística; el licenciado pone el acto. Partners, nunca in-house.

## R5 — Laboral

Hecho: la reforma LFT de plataformas digitales está vigente (IMSS/INFONAVIT obligatorios sobre umbral de ingreso; 1M+ afiliados a inicios de 2026). El arbitraje laboral gig ya no existe como supuesto económico.
Diseño Fase 0–1: pocos ejecutores semi-fijos, prestadores de servicios profesionales con RFC, retainer + variable. Pendiente obligatorio antes de escalar supply (M6): opinión formal de abogado laboral sobre la estructura. Riesgo reconocido: la relación semi-fija con SOP y supervisión se parece a subordinación; no se escala el supply sin esa opinión.

## R6 — Privacidad y datos

- LFPDPPP: la plataforma es responsable del tratamiento; avisos de privacidad por rol (cliente, ejecutor, terceros captados).
- Congelado: observación estructurada por default; video/audio crudo solo por elevación con consentimiento; interiores de vivienda solo con elevación explícita del principal; anonimización de terceros antes de que un episodio entre al corpus.
- Política de retención del log la define consejo legal (trazabilidad total = evidencia total, también en contra).

## R7 — Restricción del fundador (estructural, hasta 2028)

Cero involucramiento operativo visible, cero venta enterprise a jugadores del ecosistema financiero, cero marca pública fuerte antes del levantamiento de la restricción BBVA. La estructura societaria de Fase 0 debe reflejarlo (tenencia y operación formal). Es restricción de calendario, no de diseño — el diseño ya la incorpora (Fases 0–2 invisibles).

## Pendientes legales (diferidos con dueño)

| Ítem | Cuándo | Dueño |
|---|---|---|
| Opinión laboral formal (estructura de ejecutores) | antes de M6 | abogado laboral |
| Política de retención de logs y evidencia | antes de primera acción externa (M4) | abogado |
| Contrato marco de mandato + t&c de garantía | antes de M4 | abogado |
| Estructura societaria definitiva y aislamiento de riesgo | Fase 0 (constitución) | fiscalista + corporativo |
| Revisión de umbrales LFPIORPI aplicables a custodia/traslado de bienes | antes de M4 | abogado PLD |
