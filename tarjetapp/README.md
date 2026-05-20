# TarjetApp — Prototipo interactivo

Prototipo funcional de la app **TarjetApp** (Banco los Alpes) en un único archivo HTML.
Sin dependencias, sin build, sin instalación: se abre directo en cualquier navegador.

## Pantallas incluidas

1. **Splash / Bienvenida** — logo, "Crear Cuenta", login social.
2. **Registro paso 1 (25%)** — datos básicos (nombres, documento, email, teléfono, T&C).
3. **Registro paso 2 (50%)** — perfil legal (fechas, actividad, ingresos, gastos, dirección).
4. **Verificación de identidad (75%)** — captura de cédula y prueba de vida (simulada).
5. **Home (100%)** — saludo personalizado, saldo, productos y navegación inferior.

## Cómo usarlo

Abre `index.html` haciendo doble clic, o sirve la carpeta:

```bash
# Opción 1: doble clic
open index.html

# Opción 2: servidor local (opcional)
python3 -m http.server 8000
# luego abre http://localhost:8000
```

### Atajos del prototipo

- Botones **1–5** arriba a la derecha: salta entre pantallas sin completar el flujo.
- Los formularios validan campos requeridos antes de avanzar.
- El nombre escrito en el paso 1 aparece en el saludo de la pantalla Home.

## Estructura

```
tarjetapp-prototype/
├── index.html      # Todo el prototipo (HTML + CSS + JS)
└── README.md
```

Un solo archivo, fácil de compartir por correo, Drive o git.

## Compartir

```bash
git init
git add .
git commit -m "Initial prototype"
gh repo create tarjetapp-prototype --public --source=. --push
```

## Personalizar

- **Colores**: variables CSS al inicio de `<style>` (`--primary`, `--bg`, etc.).
- **Textos / labels**: edita directamente el HTML.
- **Lógica de navegación**: función `showScreen()` al final del `<script>`.
- **Validaciones**: handlers `form-step1` / `form-step2`.

## Siguiente paso (si se quiere productizar)

Migrar a **React + Vite + Tailwind** dividiendo cada pantalla en un componente y
conectando a un backend real. La estructura de pantallas y estilos se traduce 1:1.
