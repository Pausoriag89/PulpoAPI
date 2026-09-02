# PULPO — capa de actuación física para agentes de IA

> Marca: **IAIdea Factory** (D25, 2026-09). PULPO permanece como codename interno de este repo y no aparece en superficies públicas.

Repo privado de diseño y registro del proyecto. Estado: **blueprint — pre-build**.

## La idea en tres niveles de zoom

**Nivel 1 — una frase.**
API que permite a un agente de IA ejecutar acciones físicas verificables en el mundo real a través de humanos despachados, con evidencia estructurada, garantía por acción y trazabilidad total — diseñada para que el actuador humano sea sustituible por robots sin cambiar el contrato.

**Nivel 2 — un párrafo.**
Los agentes de IA ya piensan, planean y pagan, pero no tienen cuerpo. Todo lo que requiere presencia física — inspeccionar, entregar, recoger, esperar, supervisar, firmar — hoy es un muro para cualquier sistema autónomo. PULPO expone ese mundo físico como una API: seis primitivas de acción estandarizadas, ejecutadas por una red de operadores generalistas entrenados, con telemetría en vivo (visión, audio, estado), mandato legal del usuario final, allowlist determinista de lo permitido y garantía sobre el cumplimiento. Empezamos en CDMX sirviendo demanda real de hoy (administración de propiedades, despachos legales) para acumular el activo que nadie más tiene: datos operativos estructurados de cómo los humanos ejecutan acciones físicas — el corpus que entrena a la siguiente generación de actuadores, que ya no serán humanos.

**Nivel 3 — el documento completo.**
Leer en orden: `docs/01` a `docs/09`.

## Punto focal (el pitch en una tesis)

Hoy las acciones físicas las hacen humanos. Si instrumentamos y mapeamos **cómo** las hacen, ese registro vale en tres niveles: (1) el servicio en sí (ingreso presente), (2) el proceso pulido y estandarizado (margen creciente), (3) el dato de ejecución (el insumo que la robótica necesita y no tiene). Human-out-of-the-loop empieza forzosamente como human-in-the-loop, varias generaciones. Quien opere ese loop durante los años previos al despliegue masivo de robots en LatAm llega al big bang siendo dueño del catálogo de habilidades, de la demanda y de los datos. Migración planeada: empresa de servicios apificados para agentes → RoboLaborForce as a Service.

## Estructura del repo

| Ruta | Contenido | Naturaleza |
|---|---|---|
| `docs/01-tesis.md` | Idea, problema, a quién sirve | Referencia |
| `docs/02-timing.md` | Por qué en 2 años y por qué empezar hoy | Referencia |
| `docs/03-primitivas.md` | Las 6 primitivas SKU — base fundacional | Referencia |
| `docs/04-economics.md` | Unit economics, multiplexeo, garantía | Referencia |
| `docs/04b-unit-economics.md` | Modelo de breakeven v0 y qué falta medir | Referencia |
| `docs/05-arquitectura.md` | Capas, vigía, mandatos, protocolo de sesión | Referencia |
| `docs/06-datos-moat.md` | Los 3 niveles del dato y la migración a robots | Referencia |
| `docs/07-ruta-critica.md` | Fases 0–3, hitos, criterios kill/scale | Proceso |
| `docs/08-legal.md` | Restricciones congeladas y fronteras | Referencia |
| `docs/09-gobernanza-ABIERTA.md` | Estructura accionaria — **decisión abierta** | Proceso |
| `decisiones/registro.md` | Log de decisiones con su razón | Proceso |
| `pitch/` | HTML interactivo del pitch | Output |
| `landing/` | Especificación de ejecución de la landing de IAIdea Factory | Output |

## Reglas del repo

1. Toda decisión congelada se registra en `decisiones/registro.md` **con su razón**. La razón es lo que sobrevive al olvido.
2. Hechos separados de opinión en todos los documentos. Lo no verificable se etiqueta como opinión.
3. Referencia (estable, se lee) y proceso (operativo, se ejecuta) no se mezclan en un mismo documento.
4. Lo diferido se nombra como diferido, no se olvida.
