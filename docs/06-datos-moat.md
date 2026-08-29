# 06 — Datos, moat y la migración a RoboLaborForce

## Los tres niveles de valor de la misma ejecución

Cada acción física ejecutada por un humano instrumentado produce valor tres veces:

1. **El servicio** — el fee de hoy. Paga la operación.
2. **El proceso** — cada ejecución afina el SOP: dónde falla el mundo real, qué evidencia convence, qué pasos se automatizan. El margen crece con el volumen sin subir precio.
3. **El dato** — el episodio estructurado (contexto → pasos → observaciones → desviaciones → resultado) entra al corpus. Este es el activo de la década.

## Corrección crítica a la tesis del moat (verificada)

La tesis original era "cientos de miles de horas de grabación". **El mercado ya refutó esa versión.** Hecho (estado del mercado de datos para physical AI, 2026):

- Existe un **glut** de video egocéntrico crudo: se comercia a $2–5 USD/hora, por debajo de su costo de producción ($5–20/hora). Los equipos de robótica descartan ~90% del footage masivo por redundante o irrelevante; "en una hora de video encontramos 2–3 segmentos útiles".
- Lo que sí pagan los labs, a ~100x el precio del commodity: datos **especificados antes de capturarse** — catálogo de habilidades con metas de cobertura explícitas, diversidad de entornos sobre volumen (32 entornos × 50 demostraciones supera volúmenes masivos de lo mismo), modos de falla representados, alineación de sensores, derechos limpios, formatos estándar (LeRobot, RLDS, MCAP).
- El co-entrenamiento video-humano + teleoperación supera a robot-only por 34–228%. El dato humano bien especificado sí es insumo real — cuando está curado.

**Reformulación congelada del moat:** no somos una cámara que graba trabajo; somos una **fundición de datos de habilidades físicas**: especificación antes de captura (el SOP de cada primitiva ES la especificación), etiquetado denso gratis (checklist, desviaciones, resultado y siniestro se registran para operar, no como costo extra de labeling), diversidad LatAm que ningún dataset gringo cubre (entornos, objetos, informalidad, infraestructura), y derechos limpios por arquitectura de consentimiento desde el día uno. El subproducto de operar bien es exactamente el dataset que el mercado paga caro; el subproducto de solo grabar es el commodity de $2/hora.

## Arquitectura de consentimiento (condición de venta del dato)

- Telemetría estructurada: cubierta por los términos de servicio de operación.
- Video/audio de ejecución: **opt-in pagado del ejecutor** (retribución extra por episodio grabado) + consentimiento del cliente por SKU + zonas de privacidad (interiores de vivienda: solo con elevación explícita del principal).
- Anonimización de terceros en cuadro antes de que un episodio entre al corpus vendible.
- Derechos: cesión explícita y trazable por episodio. Un corpus sin derechos limpios no es vendible a ningún lab serio — el consentimiento no es compliance, es empaque del producto.

## La migración: servicios apificados → RoboLaborForce as a Service

Tesis: human-out-of-the-loop empieza forzosamente como human-in-the-loop, varias generaciones, mejorando órdenes de magnitud. La secuencia:

| Etapa | Actuador | Qué acumulamos |
|---|---|---|
| 1 (hoy) | Humano con SOP + telemetría | Demanda, SOPs, siniestralidad, corpus |
| 2 | Humano asistido (el agente corrige en sesión) | Descomposición fina de habilidades |
| 3 | Híbrido: robot en primitivas absorbibles (OBSERVAR primero), humano en el resto | Datos de handoff humano↔robot — los más escasos del mundo |
| 4 | Flotilla robótica propia/asociada; humanos en excepciones y fe presencial | El cliente ya es nuestro; el robot es un cambio de driver |

La interfaz `Actuador` (ver `05-arquitectura.md`) es lo que hace esto un cambio de driver y no una refundación. En la etapa 4 el modelo de negocio del que habla la tesis original ("el humano invertirá en sus robots y sus habilidades en vez de trabajar") se sirve desde aquí: PULPO opera la demanda, el estándar y la certificación de habilidades; los dueños de robots conectan capacidad como hoy un ejecutor conecta su tiempo.

Opinión honesta sobre la ventana LatAm: el costo laboral mexicano retrasa la adopción robótica local años respecto a EE.UU. — eso alarga la etapa 1–2 (más tiempo para acumular) y retrasa la 3–4 (el pago del corpus llega después). Es una ventaja de acumulación y un riesgo de paciencia de capital a la vez. Se registra la paradoja sin resolverla; la resuelven los datos de Fase 1–2.

## Qué NO haremos con los datos

- No vender datos de clientes ni episodios identificables. Se vende cobertura de habilidades, no vidas ajenas.
- No capturar en interiores sin elevación explícita.
- No prometer "anonimizado" donde técnicamente no lo es.
La primera venta de datos que viole la confianza operativa mata el negocio de servicios que financia todo. Orden de prioridad congelado: servicio > proceso > dato.
