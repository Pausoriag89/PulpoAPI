# 05 — Arquitectura

## Capas por robustez (mapa de realidad)

**Núcleo robusto / autónomo (backbone — se construye primero):**
- Catálogo de primitivas y SKUs (datos propios, lógica determinista).
- Registro de mandatos: quién autorizó qué alcance, topes, vigencia, revocación, evidencia de identidad. **El activo legal central.**
- Máquina de estados de la acción: `solicitada → validada → despachada → en_sesión → evidencia_entregada → verificada → cerrada | fallida → garantía`. Única autoridad de ejecución.
- Cadena de evidencia: paquete por acción (geo, timestamps, media, checklist, firmas) con hash encadenado — trazabilidad absoluta y a prueba de edición.
- Motor de garantía: reglas determinísticas de disparo de reembolso.

**Frágil / mantenimiento perpetuo (se administra, nunca se promete como autónomo):**
- Supply humano: vetting, entrenamiento, rotación, calidad.
- Streaming de sesión en vivo (red celular, batería, cobertura).
- Integraciones con partners licenciados.

**Errores irreversibles (human-gated siempre):**
- Todo lo que toca dinero del cliente (cobro sí, custodia jamás).
- Firma de mandatos y su alcance.
- Pago de garantías arriba de umbral.
- Alta de un SKU nuevo al catálogo.

## El vigía: router, nunca juez (decisión congelada)

Frontera de confianza: la descripción de tarea que llega por API es **input hostil** (escrita por un agente, que la escribió a partir de un usuario, potencialmente adversarial). El componente que la come no puede tener poder de actuar.

- LLM clasifica la solicitud contra el catálogo → emite `sku_id + parámetros` o `no_clasificable`.
- `no_clasificable` → rechazo o compuerta humana. Nunca "probablemente legal".
- La autorización real es determinista: ¿mandato vigente? ¿alcance cubre este SKU? ¿tope respetado? ¿agregación en ventana de 6 meses bajo umbral? — todo contra tablas.
- Anti-estructuración: agregación sobre el log por principal, por destino y por patrón; alertas determinísticas.

Razón: allowlist convierte un problema infinito (¿es ilegal?) en uno finito (¿es exactamente esto?). La garantía solo es precificable sobre el espacio finito.

## Protocolo de sesión (el diferenciador técnico)

```
dispatch(sku, params, mandato_id)
  → sesión_abierta(actuador_asignado, eta)
  → stream de observaciones ESTRUCTURADAS (default)
     · elevación a video/audio crudo solo bajo permiso explícito del SKU + consentimiento
  → comandos de corrección del agente (dentro del alcance del SKU, enumerados)
  → paquete_de_evidencia(hash)
  → verificación (automática por esquema + muestreo humano)
  → cierre | garantía
```

Privacidad congelada: observación estructurada por default; video crudo por elevación. Retención definida por consejo legal (la trazabilidad absoluta también es evidencia en contra — la política de retención es decisión legal, no técnica).

## Interfaz Actuador (la decisión que habilita RoboLaborForce)

```python
class Actuador(Protocol):
    capacidades: set[Capacidad]  # desplazarse, manipular, capturar, interactuar, esperar
    def ejecutar(self, paso: PasoSOP, sesion: Sesion) -> Observacion: ...
```
`ActuadorHumano` (v1): app del ejecutor — SOP paso a paso, captura guiada, telemetría. `ActuadorRobot` (vN): mismo contrato. Los SOPs se escriben contra pasos atómicos ejecutables por cualquiera de los dos. Cada ejecución humana instrumentada es, por diseño, un episodio etiquetado del corpus (ver `06-datos-moat.md`).

## Stack (alineado al stack del fundador)

Python 3.12+ · Pydantic v2 · SQLAlchemy 2.x/Alembic sobre Supabase (Postgres + pgvector; acceso vía SQLAlchemy, regla anti-lock-in) · httpx · pytest con tests golden sobre la lógica core (máquina de estados, motor de garantía, agregación anti-estructuración) · VPS + systemd · app ejecutor: por decidir (diferido — mejora con datos de Fase 0; candidato: PWA antes que nativa) · superficie agéntica: MCP server + REST, latente hasta Fase 2 · UI clientes: Lovable.

Contención: el LLM router corre aislado, sin credenciales de escritura; solo emite clasificaciones que la máquina de estados valida. Ningún componente que come input externo escribe directo a mandatos, pagos o catálogo.
