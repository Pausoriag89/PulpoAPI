# 03 — Las 6 primitivas (base fundacional)

Todo lo ejecutable por PULPO es una configuración parametrizada de seis primitivas. No existe "tarea en texto libre". Un vertical nuevo = plantillas nuevas de parámetros + template de evidencia; nunca primitivas nuevas sin decisión explícita de framework.

## Región operativa v1 (dentro de la cual viven las 6)

percibir + actuar · custodia hasta documento/objeto (nunca dinero) · mandato simple (nunca notarial in-house) · ejecutor generalista (nunca oficio licenciado) · latencia programada o mismo día · sesgo a recurrente.

## Catálogo

### P1 — OBSERVAR
Documentar el estado de un bien, espacio o situación contra checklist estructurado.
- **Parámetros:** objetivo, esquema de checklist, nivel de detalle, ¿sesión viva?
- **Evidencia:** fotos georreferenciadas + timestamp + esquema de datos llenado + hash del paquete.
- **Consume:** inmobiliario (inspección, acta entrada/salida), seguros (siniestro, riesgo), marketplaces (usados), legal (estado de hechos para preparación), retail (anaquel).
- **Robot-readiness:** la primera absorbible (cámaras, drones); diseñar el esquema para que la fuente de captura sea intercambiable.

### P2 — TRANSFERIR
Mover documento u objeto con identidad verificada en ambos extremos y cadena de custodia.
- **Parámetros:** ítem, origen/destino, verificación de identidad requerida, ventana.
- **Evidencia:** cadena de custodia (quién tocó qué cuándo) + acuse firmado + identidad verificada.
- **Consume:** legal (contratos, notificaciones extrajudiciales), inmobiliario (llaves, documentos), fintech futuro (contratos de crédito), diáspora.
- **Frontera:** interpelación judicial = actuario; efectivo/valores = excluido.

### P3 — REPRESENTAR
Presencia física bajo mandato: fila, turno, ventanilla, recepción de un tercero.
- **Parámetros:** lugar, gestión permitida (enumerada), tope de decisión, duración máxima.
- **Evidencia:** mandato vigente verificado + registro de gestión + resultado documentado.
- **Consume:** trámites (actas, constancias), inmobiliario (recibir proveedor), boletos/turnos.
- **Robot-readiness:** la última — la presencia con efectos jurídicos exigirá humano por años.

### P4 — SUPERVISAR
Observar a un tercero ejecutando un servicio y validar contra criterio de conformidad.
- **Parámetros:** servicio supervisado, checklist de conformidad, autoridad ante desviación (enumerada), ¿sesión viva?
- **Evidencia:** sesión + checklist + veredicto conforme/no-conforme + registro de desviaciones.
- **Consume:** inmobiliario (el plomero, la limpieza STR), diáspora (reparación en casa de los padres), construcción ligera.
- **Regla dura:** el generalista supervisa el oficio, jamás lo ejecuta (línea D4).

### P5 — OBTENER
Conseguir un documento, constancia u objeto emitido/vendido por un tercero.
- **Parámetros:** ítem, emisor, requisitos, tope de gasto (pago SIEMPRE por canal digital de la plataforma, nunca efectivo del ejecutor).
- **Evidencia:** comprobante de emisión/compra + custodia hasta entrega.
- **Consume:** trámites, farmacia no controlada, compras específicas, legal (copias certificadas).

### P6 — ACREDITAR
Recolectar firmas y consentimientos con verificación de identidad presencial.
- **Parámetros:** documento, firmantes, nivel de verificación, testigos requeridos.
- **Evidencia:** identidad verificada + firma + registro audiovisual bajo consentimiento + timestamp.
- **Consume:** legal, fintech futuro (KYC presencial), inmobiliario (contratos de renta).
- **Frontera:** fe pública = notario partner. PULPO acredita el hecho; el fedatario da la fe.

## Por qué 6 y no N

1. **Garantía precificable:** la siniestralidad se acumula por primitiva a través de todos los verticales. Seis distribuciones densas > doscientas anémicas.
2. **Entrenamiento y sustitución del ejecutor:** seis SOPs dominables por un generalista en días; onboarding barato, calidad homogénea, red intercambiable.
3. **Catálogo de habilidades robot-ready:** cada primitiva se descompone en sub-habilidades físicas (desplazarse, identificar, manipular, fotografiar, esperar, entregar, firmar-testificar). Ese árbol primitiva→sub-habilidad es el esqueleto del corpus de datos (ver `06-datos-moat.md`): los compradores de datos robóticos pagan por cobertura especificada de un catálogo de habilidades, no por horas de video.
4. **Superficie API estable:** `observar()`, `transferir()`, `representar()`, `supervisar()`, `obtener()`, `acreditar()` — un agente aprende seis llamadas y accede a todos los verticales. El contrato no cambia cuando el actuador deje de ser humano.

## Contrato actuator-agnostic (decisión congelada)

Toda primitiva se especifica contra la interfaz `Actuador` (capacidades: desplazamiento, manipulación, captura, interacción verbal, espera), no contra "persona". `ActuadorHumano` es el driver v1. `ActuadorRobot` es un driver vN que se conecta al mismo contrato. Razón: la migración a RoboLaborForce debe ser un cambio de driver, no una refundación.
