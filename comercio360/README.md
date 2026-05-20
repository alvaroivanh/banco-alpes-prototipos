# Comercio 360 — Prototipo interactivo

Prototipo funcional de la app **Comercio 360** (panel para comercios) en un único archivo HTML.
Sin dependencias, sin build, sin instalación.

## Pantallas incluidas

1. **Login** — NIT + password (con toggle de visibilidad), login social Google/Apple/Facebook.
2. **Dashboard** — Ventas del mes, gráfica de tendencia y top de productos.
3. **Reportes y Descargas** — selección de período y tipo, generador de reportes y descargas PDF/CSV.
4. **Solicitar Liquidez** — adelanto de ventas con animación de procesamiento.
5. **Dispersión de Fondos** — dispersión estándar (8 días, 0%) vs rápida (<24h, 3.5%).

## Cómo usarlo

```bash
open index.html
# o servidor local:
python3 -m http.server 8000
```

### Atajos del prototipo

- Botones **1–5** arriba a la derecha: salta entre pantallas sin login.
- La barra inferior navega entre Dashboard / Reportes / Financiación / Dispersión.
- El formulario de login valida campos antes de avanzar.
- "Solicitar Adelanto" simula el flujo de procesamiento (~1.2s) y muestra toast.
- En Dispersión, cada botón muestra el monto neto calculado con la tasa correspondiente.

## Personalizar

- **Colores**: variables CSS al inicio de `<style>` (`--primary`, `--bg`, etc.).
- **Datos mostrados**: edita directamente el HTML (saldos, productos, reportes).
- **Lógica de tasas**: handler `[data-dispersion]` al final del `<script>`.
