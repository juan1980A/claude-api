# Curso de Claude API — Platzi

Repositorio de código del **Curso de Claude API de Platzi**.

## ¿De qué trata este proyecto?

A lo largo del curso construyes aplicaciones reales sobre la API de Anthropic
(Claude), empezando por una primera llamada al modelo y terminando con una app
web que reúne varios proyectos en un solo lugar.

Los temas que se cubren:

- Primeras llamadas a la API y manejo del array de `messages`.
- Conversaciones multi-turn, gestión de contexto y control de tokens.
- Streaming de respuestas en tiempo real y un chatbot de terminal.
- Inputs multimedia (imágenes y PDFs) y outputs estructurados con JSON.
- Prompt engineering aplicado a extracción de datos.
- Tool use: definir herramientas, manejar `tool_result` y construir un loop
  agéntico (razonar → actuar → observar).
- Manejo de errores y seguridad en agentes.
- Optimización de costos con prompt caching y procesamiento masivo con Batch API.
- Frontend + hub de proyectos con FastAPI.

Cada clase está implementada en **dos rutas equivalentes**:

- `python/` — versión en Python (ruta principal, `fastapi` + `anthropic`).
- `typescript/` — versión en TypeScript (ruta alternativa, Node + `@anthropic-ai/sdk`).

La rama `main` contiene la app final desplegable de la clase 16.

## Requisitos

- Python 3.11+ (o Node.js 20+ si sigues la ruta TypeScript).
- Una API key de Anthropic.

Copia la plantilla y rellena tu key:

```bash
cp .env.example .env
```

El código lee las variables del entorno pero no carga el `.env` por sí solo,
así que expórtalas antes de ejecutar los ejemplos:

```bash
set -a && source .env && set +a
# o directamente:
export ANTHROPIC_API_KEY="tu_api_key"
```

## Cómo ejecutar la app de `main` (clase 16)

Python (es una app FastAPI, se sirve con `uvicorn`):

```bash
cd python/clase-16
uvicorn --app-dir final main:app --reload
```

TypeScript (desde la raíz del repositorio):

```bash
cd typescript && npm install && npm run clase:16:final
```

## Listado de ramas

Cada clase tiene dos checkpoints: `-inicio` (punto de partida) y `-final`
(solución completa y comentada).

| Clase | Tema | Ramas |
| --- | --- | --- |
| 01 | Quickstart: tu primera llamada a Claude API | `clase-01-inicio` · `clase-01-final` |
| 02 | Conversaciones multi-turn: el array de `messages` | `clase-02-inicio` · `clase-02-final` |
| 03 | Estrategias de gestión de contexto y tokens | `clase-03-inicio` · `clase-03-final` |
| 04 | Streaming de respuestas en tiempo real | `clase-04-inicio` · `clase-04-final` |
| 05 | Construye el chatbot con interfaz de terminal | `clase-05-inicio` · `clase-05-final` |
| 06 | Inputs multimedia: imágenes y documentos PDF | `clase-06-inicio` · `clase-06-final` |
| 07 | Outputs estructurados con JSON mode | `clase-07-inicio` · `clase-07-final` |
| 08 | Prompt engineering para extracción de datos | `clase-08-inicio` · `clase-08-final` |
| 09 | Tool use: cómo Claude llama funciones externas | `clase-09-inicio` · `clase-09-final` |
| 10 | Definir herramientas y manejar `tool_result` | `clase-10-inicio` · `clase-10-final` |
| 11 | Loop agéntico: razonar → actuar → observar | `clase-11-inicio` · `clase-11-final` |
| 12 | Manejo de errores y seguridad en agentes | `clase-12-inicio` · `clase-12-final` |
| 13 | Prompt caching: reduce costos hasta un 90% | `clase-13-inicio` · `clase-13-final` |
| 14 | Batch API para procesar miles de requests | `clase-14-inicio` · `clase-14-final` |
| 16 | Frontend + hub de proyectos con FastAPI | `clase-16-inicio` · `clase-16-final` |

Otras ramas:

- `main` — app final del curso (clase 16) y este índice.

## Navegación del curso

```bash
git checkout clase-05-inicio   # empezar la clase 5 desde cero
git checkout clase-05-final    # ver la solución de la clase 5
```
