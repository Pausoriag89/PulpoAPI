# 04 — Economics

> Cifras marcadas como opinión son estimaciones de diseño para dimensionar; se sustituyen con datos reales de Fase 0. Regla no negociable: todo capital parqueado se compara contra CETES.

## La unidad económica: la hora-ejecutor en celda

El costo del negocio es la hora del ejecutor dentro de una celda de densidad (zona geográfica atendible sin tiempo muerto de traslado excesivo). El ingreso es el fee por acción. Todo lo demás es amortización.

**Multiplexeo (la economía de escala real).** Un vertical solo tiene demanda picuda: inmobiliario en horario hábil con picos de fin de mes; legal en vencimientos; retail en horario comercial; siniestros aleatorios; diáspora en fines de semana. Curvas complementarias sobre la misma celda. Opinión: utilización mono-vertical ~30–40%; multiplexada ~65–70% → el costo efectivo por acción cae cerca de la mitad. Ese delta es simultáneamente el margen y el fondeo de la garantía. Es la economía del cloud aplicada a trabajo físico: demanda heterogénea sobre capacidad compartida.

**Corolario congelado:** expandir verticales antes que geografía. 3 alcaldías con 8 verticales > 8 ciudades con 1 vertical.

## Estructura de ingreso por acción (opinión, para modelar)

| Componente | Rango estimado |
|---|---|
| Fee por acción (según primitiva y latencia) | $180–$900 MXN |
| Costo ejecutor (hora prorrateada + traslado) | 40–55% del fee |
| Aporte a fondo de garantía | 5–10% del fee |
| Plataforma/overhead prorrateado | 10–15% del fee |
| Margen de contribución objetivo | 25–35% |

Piso de precio por SKU: `costo_ejecutor + siniestralidad_esperada + (reserva_garantía × tasa CETES de costo de oportunidad) + overhead`. Un SKU que no cubre ese piso sale del catálogo — la garantía no se subsidia, se precifica.

## Los tres pisos de ingreso (secuencia temporal)

1. **Servicio (M0+):** fee por acción. Paga la operación desde el día uno. Techo: lineal con horas.
2. **Proceso (M9+):** SOPs optimizados con datos → menos re-ejecuciones, menos siniestros, rutas y bundling mejores → el margen crece sin subir precio. También habilita productos de suscripción (N acciones/mes por propiedad/despacho) con mejor economía de adquisición.
3. **Datos (M18+):** el corpus estructurado de ejecución física (ver `06-datos-moat.md`). No es ingreso principal en la ventana 0–18m; es la opción de mayor convexidad después. No se modela como ingreso base — se modela como opción gratis que la operación paga.

## Fondo de garantía

- Cubre: incumplimiento propio (no-ejecución, evidencia inválida, SLA roto) → reembolso + múltiplo acotado del fee (opinión: 1–3x, tope duro por SKU).
- NO cubre: daño consecuencial. Eso se transfiere a aseguradora tercera cuando exista siniestralidad de 12+ meses por SKU (nuestros datos son lo que la vuelve suscribible — activo, no gasto).
- La reserva vive en instrumentos líquidos; su costo de oportunidad (CETES) entra al piso de precio de cada SKU.

## CAPEX y estructura

Asset-light deliberado: sin flotilla, sin locales de cara al público en fase experimental. CAPEX real: instrumentación del ejecutor (smartphone + arnés de captura si aplica), software propio, vetting/entrenamiento (~costo hundido por ejecutor que la rotación gig convierte en la métrica a vigilar — razón para el modelo de ejecutor semi-fijo, ver `07-ruta-critica.md`).

## Métricas norte

1. Utilización de celda (%h facturables / h disponibles).
2. Tasa de cumplimiento SLA por SKU (norte: ≥97%).
3. Siniestralidad por primitiva (garantías pagadas / acciones).
4. Costo de adquisición por acción recurrente vs one-shot.
5. Margen de contribución por acción, después de garantía.
6. Retención de ejecutores a 90 días (proxy de calidad del supply).
