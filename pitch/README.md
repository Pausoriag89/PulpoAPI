# Pitch interactivo

`index.html` — el blueprint explicado a distintos niveles de complejidad, como manual del operador (estética terminal). Abrir directo en cualquier navegador; no requiere servidor.

Spec cumplida (acordada antes de construir):

- Un solo archivo HTML autocontenido, sin dependencias externas (cero requests de red).
- Tema oscuro por default, toggle dark/light en barra sticky superior, slider de tamaño de texto 0.75x–1.25x (preferencias persistidas en localStorage).
- Navegación por niveles de zoom: `--nivel=` frase → párrafo → tesis completa → apéndices (primitivas, economics, arquitectura, ruta crítica).
- Audiencias conmutables: `--audiencia=` inversionista · cliente (despacho/administrador) · partner técnico/agéntico — mismo contenido base, énfasis y CTAs re-encuadrados.
- Fuente de contenido: `docs/01`–`07`. El pitch nunca contradice el registro de decisiones (D01–D20); hecho y opinión conservan sus etiquetas; la restricción del fundador se menciona abstraída (sin nombrar al empleador).
- Respeta `prefers-reduced-motion`, imprime expandido (todos los niveles), sin scroll horizontal de página en móvil.

El chart de multiplexeo es ilustrativo y está marcado como opinión; sus curvas se sustituyen con datos reales de Fase 0.
