# Prototipos — Banco los Alpes

Colección de prototipos interactivos en HTML/CSS/JS plano, sin dependencias ni build.

## Estructura

```
.
├── index.html          # Portada con links a cada prototipo
├── tarjetapp/          # Prototipo 1: app de cliente (registro + home)
│   ├── index.html
│   └── README.md
└── comercio360/        # Prototipo 2: panel para comercios
    ├── index.html
    └── README.md
```

## Prototipos

| Carpeta | Producto | Pantallas |
|---------|----------|-----------|
| [`tarjetapp/`](tarjetapp/) | **TarjetApp** — onboarding y home de cliente | Splash · Registro 25% · Registro 50% · Identidad 75% · Home |
| [`comercio360/`](comercio360/) | **Comercio 360** — panel para comercios | Login · Dashboard · Reportes · Liquidez · Dispersión |

## Cómo usarlo

```bash
# Doble clic en index.html (portada con links a los dos prototipos)
open index.html

# O sirve la carpeta completa con un server local
python3 -m http.server 8000
# luego abre http://localhost:8000
```

Cada prototipo es autocontenido: puedes abrir directamente `tarjetapp/index.html` o `comercio360/index.html` sin necesidad de servidor.

## Compartir

```bash
git remote add origin git@github.com:<usuario>/<repo>.git
git push -u origin main
# o con GitHub CLI:
gh repo create banco-alpes-prototipos --public --source=. --push
```

## Características comunes

- **Frame de móvil en escritorio**, **pantalla completa en móvil** (responsive).
- **Dev nav** flotante (botones 1–5) para saltar entre pantallas sin completar el flujo.
- **Toasts** para acciones aún no implementadas.
- **Validación básica** en formularios.
- Variables CSS (`--primary`, `--bg`, etc.) al inicio de cada archivo para personalizar colores.

## Siguiente paso (si se quiere productizar)

Cada prototipo se traduce 1:1 a **React + Vite + Tailwind**: cada pantalla se vuelve un componente y los toasts se reemplazan por llamadas al backend.
