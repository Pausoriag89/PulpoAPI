# 04b — Unit economics: modelo base

> Estado: **CONGELADO como v0**. Documento de referencia. Complementa `04-economics.md` con la aritmética de breakeven y con el inventario de lo que falta medir. Toda cifra aquí es estimación de diseño salvo las marcadas como hecho: el modelo se recalibra con datos reales de Fase 0 y este documento se versiona a v1.

## Qué congela este documento

Congela la **estructura** del modelo: qué costos son fijos escalonados, cuáles variables, cómo se calcula el breakeven y qué métrica decide la viabilidad. La estructura sobrevive aunque cambien todos los números.

No congela los **valores**. Los parámetros son estimaciones para dimensionar el orden de magnitud y priorizar qué medir primero. La sección "Lo que falta por definir" lista cada uno con su dueño y su fecha.

## El modelo base

### Supuestos

La tabla siguiente contiene los parámetros del modelo v0:

| Parámetro | Valor v0 | Naturaleza |
|---|---|---|
| Fee blended por acción | $450 MXN | opinión — mezcla estimada de SKUs de Fase 1 |
| Costo del ejecutor semi-fijo | $14,800 MXN/mes | opinión — retainer + variable + equipo y telecom amortizados |
| Horas disponibles por ejecutor | 160 h/mes | hecho — 8 h × 20 días hábiles |
| Tiempo por acción, puerta a puerta | 2.0 h | opinión — incluye traslado |
| Techo de utilización multiplexada | 68% | opinión — heredado de `04-economics.md` (65–70%) |
| Aporte a fondo de garantía | 7.5% del fee | opinión — punto medio de la banda 5–10% |
| Comisión de pasarela | 3.6% + $3 | hecho — tarifa estándar de mercado |
| Traslado por acción | $50 MXN | opinión |
| Telemetría y datos por acción | $8 MXN | opinión |

### Estructura de costos

El ejecutor semi-fijo (decisión D17) es costo **escalonado**, no variable: contratas una persona completa o ninguna. Esa decisión define toda la forma del negocio.

Costo variable real por acción, con fee de $450:

```
garantía   $450 × 7.5%           = $33.75
pasarela   $450 × 3.6% + $3      = $19.20
traslado                          = $50.00
telemetría                        = $ 8.00
                                  ────────
                            total ≈ $111
```

Contribución marginal: **$339 por acción, el 75% del fee**. Cada acción por encima del breakeven aporta 75 centavos de cada peso a cubrir fijos y margen.

### Breakeven por configuración

La métrica que decide la viabilidad no es el volumen de breakeven, sino la **utilización requerida en el breakeven**. Si esa utilización supera el techo de 68%, la configuración no cierra sin importar cuánta demanda exista: no hay horas para servirla.

| Configuración | Breakeven | Por día hábil | Utilización requerida | Viabilidad |
|---|---|---|---|---|
| Fase 0 — 2 ejecutores, el fundador opera sin costo de caja | 105 acciones/mes | 5.2 | 65% | Ajustada. Fase 0 opera con pérdida por diseño: ~$18,000/mes con 50 acciones |
| Fase 1 — 3 ejecutores, el fundador como ops con costo sombra | 180 acciones/mes | 9 | 75% con 2.0 h · 64% con 1.7 h | Solo con ruteo denso |
| Estructura pagada — 4 ejecutores + ops contratado | 205–260 acciones/mes | 10–13 | 80% con fee $450 · 54% con fee $550 | Solo con fee ≥$500 o ruteo ≤1.7 h |
| Fase 2 — 16 ejecutores, 1,000 acciones/mes | ya rentable | 46 | 61–66% | EBITDA +$26,000 (6%) con fee $450 · +$71,000 (14%) con fee $500 |

Lectura corta: eres rentable en caja desde 105 a 180 acciones/mes mientras tú operes; rentable como empresa con nómina desde ~250 acciones/mes. En el gate de Fase 2 el margen es 6% o 14% según $50 de fee blended.

### La regla por ejecutor

Un ejecutor cubre su propio costo en **44 acciones/mes**, es decir 2.2 acciones por día hábil. A plena utilización rinde de 54 a 64 acciones según el ruteo, con contribución neta de $3,600 a $6,900/mes.

Usa esa cifra como control semanal: por debajo de 44 acciones por ejecutor, cada ejecutor adicional destruye valor.

### Chequeo del fondo de garantía

El accrual de 7.5% del fee cubre el costo esperado de garantía solo en el escenario bueno:

| Siniestralidad | Payout | Costo esperado | ¿Cubre el accrual de 7.5%? |
|---|---|---|---|
| 3% | 2x fee | 6.0% del ingreso | Sí |
| 5% | 2x fee | 10.0% del ingreso | No — sube el piso de precio |
| 5% | 3x fee | 15.0% del ingreso | No — sube el piso de precio |

El kill de Fase 1 (siniestralidad <3% por primitiva) coincide con la frontera económica del accrual. Esa coincidencia no es casual y conviene mantenerla al fijar el múltiplo de payout por SKU.

## Dos correcciones que este modelo produce sobre `04-economics.md`

Ambas quedan como PROPUESTA. No modifican `04-economics.md` hasta tu decisión explícita.

1. **La banda "costo ejecutor 40–55% del fee" solo se cumple con acciones de 1.7 h o menos.** Con 2.0 h y 68% de utilización, el ejecutor consume el 61% del fee, fuera de la banda declarada. El documento asume densidad de ruteo sin decirlo. Corrige la banda a 45–60% o condiciónala de forma explícita al tiempo por acción.

2. **El gate de utilización de Fase 2 (≥55%) queda por debajo del breakeven (61%).** Puedes aprobar tu propio gate perdiendo dinero. Sube el gate a ≥60–65%, o añade "EBITDA ≥ 0" como condición paralela.

## Lo que falta por definir

### Ranking de sensibilidad

Mide primero lo que más mueve el resultado. La tabla siguiente ordena las incógnitas por su impacto sobre la utilización requerida en el breakeven, con la configuración de 4 ejecutores:

| # | Incógnita | Rango probado | Swing en utilización | Efecto |
|---|---|---|---|---|
| 1 | Fee blended | $350 a $550 | 45 puntos | Con $350 el breakeven exige 109% de utilización: imposible a cualquier volumen |
| 2 | Tiempo por acción | 1.5 h a 2.5 h | 40 puntos | No cambia el breakeven en acciones; cambia si cabe en la capacidad |
| 3 | Costo del ejecutor | $12,000 a $19,500 | 28 puntos | El extremo alto es el escenario donde la opinión laboral obliga a IMSS e INFONAVIT |
| 4 | Overhead mensual | $18,000 a $45,000 | 25 puntos | |
| 5 | Traslado por acción | $30 a $90 | 15 puntos | Proxy de la densidad de la celda |
| 6 | Accrual de garantía | 5% a 15% | 11 puntos | El extremo alto corresponde a siniestralidad 5% con payout 3x |

Distinción que conviene retener: el fee y el costo mueven **cuántas** acciones necesitas; el tiempo por acción y el techo de utilización mueven **si esas acciones caben** en las horas que compraste. Son dos fallas distintas y se corrigen con palancas distintas.

**Escenario adverso compuesto.** Si se combinan opinión laboral desfavorable ($19,500 por ejecutor), ruteo lento (2.3 h) y fee bajo ($400), el breakeven sube a 360 acciones/mes con 129% de utilización requerida. La estructura pagada dejaría de necesitar cuatro ejecutores y pasaría a necesitar ocho, con el volumen proporcional. Este escenario no invalida la tesis; define el orden en que debes cerrar las incógnitas.

### A. Costos

| Ítem | Por qué importa | Cómo se resuelve | Cuándo |
|---|---|---|---|
| Costo real del ejecutor, con el veredicto laboral | Incógnita #3. Si la relación semi-fija se considera subordinación, el costo sube ~30% y el breakeven por ejecutor pasa de 44 a ~57 acciones | Opinión laboral formal (ya listada en `08-legal.md`) y luego renegociar la estructura de retainer | Antes de M6 |
| Tiempo real puerta a puerta **por primitiva** | Incógnita #2. El blended de 2.0 h oculta que P1 y P4 duran más que P2 | Instrumentar tiempo por fase de la sesión desde la primera acción de Fase 0 | M0 |
| Costo de traslado real por celda | Incógnita #5. Depende del modo de transporte, la hora y la densidad | Registrar traslado real por acción, separado del tiempo de ejecución | M0 |
| Composición del overhead | Incógnita #4. Hoy es un número único sin desglose | Desglosar software, hosting, herramientas, contabilidad y seguros | M3 |
| Costo de verificación de evidencia | El muestreo humano de `05-arquitectura.md` no está costeado | Definir el porcentaje de muestreo y medir minutos por paquete verificado | M3 |
| Costo de re-ejecución | Una acción repetida por causa propia consume capacidad sin generar fee, y no siempre dispara garantía | Registrar re-ejecuciones como categoría propia desde Fase 0 | M0 |
| Costo del router LLM por acción | Marginal hoy, pero entra al piso de precio en Fase 2 | Medir tokens por clasificación cuando el router entre a producción | M10 |

### B. Ingreso y precio

| Ítem | Por qué importa | Cómo se resuelve | Cuándo |
|---|---|---|---|
| Precio de lista **por SKU** | Incógnita #1, la de mayor impacto. Hoy existe una banda de $180 a $900 y un blended supuesto | Fijar precio por SKU con el piso de precio de `04-economics.md` y el benchmark de alternativas del mercado | M3 |
| Mix real de SKUs | El blended de $450 depende de una mezcla que nadie ha medido | Medir la distribución real de acciones por SKU en Fase 0 y Fase 1 | M6 |
| Viabilidad del piso de $180 | Una acción suelta con traslado difícilmente baja de ~$250–300 de costo real | Reservar el piso de $180 para acción recurrente en suscripción y fijar un piso distinto para one-shot | M3 |
| Modelo de suscripción | `04-economics.md` menciona "N acciones/mes" sin modelarlo. Cambia el CAC amortizado y vuelve predecible la utilización | Modelar la suscripción como reserva de capacidad, no como descuento por volumen | M6 |
| Elasticidad por vertical | Define el techo de precio antes de perder al cliente | Probar dos niveles de precio con despachos comparables en Fase 1 | M9 |
| Pricing agéntico | Diferido en D20. Define si un agente paga igual, más o menos que un humano | Decidir con los datos de las primeras integraciones de Fase 2 | M10 |

### C. Operación

| Ítem | Por qué importa | Cómo se resuelve | Cuándo |
|---|---|---|---|
| Utilización real alcanzable | El techo de 68% es opinión heredada, no medición | Medir utilización semanal por ejecutor desde la primera semana | M0 |
| Curva de aprendizaje | El tiempo por acción de las primeras 50 ejecuciones no representa el estado estable | Reportar tiempo por acción en cohortes de 25 ejecuciones | M3 |
| Densidad mínima de celda | Determina cuántas acciones por kilómetro cuadrado sostienen un ruteo de 1.7 h | Cruzar geolocalización de acciones contra tiempo de traslado | M6 |
| Ramp-up de un ejecutor nuevo | Define el costo hundido por ejecutor y la penalización de la rotación | Medir semanas hasta productividad plena del segundo y tercer ejecutor | M6 |
| Estacionalidad real por vertical | Las curvas complementarias del pitch son ilustrativas | Registrar demanda por hora y por día durante 3 meses con dos verticales activos | M9 |
| Costo de adquisición de cliente | El gate de Fase 1 exige CAC menor a 6 meses de margen, sin número de referencia | Registrar horas de venta y conversión por despacho contactado | M4 |

### D. Garantía

| Ítem | Por qué importa | Cómo se resuelve | Cuándo |
|---|---|---|---|
| Siniestralidad por primitiva | Es el dato que no se puede comprar y que sostiene la garantía | Registrar todo incumplimiento por SKU desde la primera acción, incluidas las de Fase 0 | M0 |
| Múltiplo de payout por SKU | Con 5% de siniestralidad y 3x, el costo esperado triplica el accrual | Fijar el múltiplo por SKU una vez exista siniestralidad de 6 meses | M9 |
| Reserva inicial del fondo | Antes de acumular accrual no hay fondo, y la garantía ya es exigible en contrato | Definir la reserva de arranque en meses de siniestro esperado, con la primera acción externa | Antes de M4 |
| Tope de acumulación del fondo | Sin tope, el accrual inmoviliza capital indefinidamente contra CETES | Definir el fondo como porcentaje del ingreso anualizado, con excedente liberable | M12 |

### E. Capital y caja

| Ítem | Por qué importa | Cómo se resuelve | Cuándo |
|---|---|---|---|
| **Capital de trabajo** | Ausente del modelo y de todo el repo. Si el despacho paga a 30 días y el ejecutor cobra quincenal, con 250 acciones/mes inmovilizas ~$112,500; a 60 días, ~$225,000. Supera la caja estimada para llegar al breakeven | Fijar términos de cobro en el contrato marco y modelar el ciclo de conversión de efectivo | Antes de M4 |
| Caja total hasta breakeven | La estimación de $100,000 a $160,000 excluye CAPEX de software, constitución y legal | Presupuestar Fase 0 completa con los pendientes de `08-legal.md` costeados | M0 |
| Costo de constitución y legal inicial | `08-legal.md` lista cinco pendientes con dueño, ninguno con monto | Cotizar los cinco y añadir la columna de costo | M0 |

## Reproducibilidad

El modelo es aritmética simple y cabe en una hoja de cálculo. Sus cinco ecuaciones:

```
costo_variable   = fee × (garantía + pasarela%) + pasarela_fijo + traslado + telemetría
contribución     = fee − costo_variable
costos_fijos     = ejecutores × costo_ejecutor + overhead
breakeven        = costos_fijos ÷ contribución
utilización_req  = (breakeven × horas_por_acción) ÷ (ejecutores × 160)
```

Regla de decisión: si `utilización_req` supera el techo medido, la configuración no cierra y debes mover fee, tiempo por acción o número de ejecutores antes de buscar más demanda.
