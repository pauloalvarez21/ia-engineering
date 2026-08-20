# ia-engineering

Aplicación Python que utiliza LangChain y OpenAI (vía OpenRouter) para generar resúmenes y datos interesantes a partir de información de texto.

## Características

- **Generación de resúmenes**: Toma un bloque de texto y genera un resumen conciso.
- **Extracción de datos interesantes**: Identifica y lista hechos destacados del tema proporcionado.
- **Integración con OpenRouter**: Utiliza el modelo `openrouter/free` a través de la API de OpenRouter para procesar el texto.
- **Prompt Template**: Emplea plantillas parametrizables de LangChain para estructurar las solicitudes al modelo de IA.

## Tecnologías

- **Python 3.14+**
- **LangChain**: Framework para desarrollo de aplicaciones con modelos de lenguaje.
- **LangChain-OpenAI**: Integración con modelos de OpenAI y compatibles.
- **python-dotenv**: Gestión de variables de entorno.

## Estructura del proyecto

```
├── main.py                  # Punto de entrada principal
├── pyproject.toml           # Configuración del proyecto y dependencias
├── src/
│   └── langchain/
│       └── __init__.py      # Módulo principal
├── .env                     # Variables de entorno (no incluido en git)
├── .gitignore               # Archivos ignorados por git
└── .python-version          # Versión de Python requerida
```

## Configuración

### Requisitos previos

- Python 3.14 o superior
- [uv](https://docs.astral.sh/uv/) (gestor de paquetes)

### Instalación

```bash
# Instalar dependencias
uv sync

# Crear archivo .env con tu API key
echo "OPENAI_API_KEY=tu-api-key-aqui" > .env
```

### Variables de entorno

| Variable | Descripción |
|----------|-------------|
| `OPENAI_API_KEY` | Tu API key de OpenRouter o OpenAI |

## Uso

```bash
# Ejecutar la aplicación
uv run main.py
```

La aplicación procesará el texto de ejemplo (biografía de Elon Musk) y generará:
1. Un resumen breve del contenido.
2. Dos hechos interesantes sobre el tema.

## Ejemplo de salida esperada

```
**Resumen:**
Elon Musk es un empresario y CEO de Tesla y SpaceX, reconocido como la persona más rica del mundo desde 2025...

**Hechos interesantes:**
1. Musk fue el mayor donante en las elecciones presidenciales de EE.UU. de 2024...
2. En junio de 2026, se convirtió brevemente en el primer billonario en dólares estadounidenses...
```

## Desarrollo

El proyecto incluye herramientas de formateo de código:

```bash
# Formatear código con Black
uv run black .

# Ordenar imports con isort
uv run isort .
```

## Licencia

Este proyecto es privado.
