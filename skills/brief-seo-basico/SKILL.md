---
name: brief-seo-basico
description: Genera un brief de contenido SEO listo para entregar a un redactor a partir de una keyword o tema. Usa este skill siempre que el usuario pida "hazme un brief", "brief para [keyword]", "brief de contenido", "qué estructura debería tener este artículo", o quiera convertir una keyword priorizada en instrucciones claras para escribir. También actívalo cuando el usuario comparta una keyword junto con URLs de competidores o data de SERP y quiera estructurar el contenido. El output es un documento de brief con meta, intención, objetivo, estructura por encabezados (H2/H3), enlaces internos sugeridos y recomendaciones de imágenes.
---

# Brief SEO Básico

Skill genérico para transformar una keyword en un brief que un redactor puede ejecutar sin contexto adicional. Pensado como punto de partida reutilizable: el usuario aporta la keyword (y opcionalmente el contexto de marca y los competidores), y el skill produce el brief estructurado.

## Cuándo usarlo

- El usuario tiene una keyword priorizada (por ejemplo, salida del skill de clustering) y quiere el brief.
- El usuario va a delegar la redacción y necesita instrucciones claras.
- El usuario quiere asegurar que el contenido cubra la intención y la estructura que rankea.

## Flujo de trabajo

1. **Confirma el input mínimo.** Necesitas: la keyword principal. Es útil (pero opcional): contexto de marca/cliente, audiencia, 2-3 URLs de competidores que rankean, y enlaces internos disponibles del sitio.

2. **Analiza la intención de búsqueda.** Determina si la keyword es informacional, comercial o transaccional, y qué espera ver el usuario que busca eso. Esto define el tipo de contenido (guía, comparativa, página de servicio, etc.).

3. **Analiza la SERP si hay datos.** Si el usuario aportó URLs de competidores o puedes buscarlas, identifica: el tipo de contenido que domina (artículo, listicle, página comercial), el rango de extensión, los subtemas que todos cubren (obligatorios) y los huecos (oportunidad de diferenciarse).

4. **Define meta y objetivo.** Propón un meta título (≤60 caracteres) y una meta descripción (≤155 caracteres) con la keyword. Escribe en una frase el objetivo del contenido y a quién va dirigido.

5. **Arma la estructura.** Propón los encabezados H2/H3 en orden lógico, cubriendo los subtemas obligatorios de la SERP más los huecos detectados. Para cada encabezado, una línea de indicación de qué cubrir (no escribas el contenido, solo la guía).

6. **Añade enlaces internos y CTAs.** Sugiere a qué páginas internas enlazar (si el usuario las aportó) y qué llamada a la acción cerrar según la intención.

7. **Recomienda imágenes.** Indica qué imágenes o gráficos reforzarían el contenido y dónde.

## Formato de salida

ALWAYS usa esta estructura exacta:

```
# Brief: [Keyword principal]

## Meta
- Keyword principal:
- Keywords secundarias:
- Meta título (≤60 car.):
- Meta descripción (≤155 car.):
- URL sugerida:

## Intención y objetivo
- Intención de búsqueda:
- Tipo de contenido:
- Objetivo del artículo:
- Audiencia:
- Extensión sugerida:

## Análisis de SERP
- Tipo de contenido que rankea:
- Subtemas obligatorios (todos los competidores los cubren):
- Huecos / oportunidad de diferenciación:

## Estructura (para el redactor)
### H1: [título propuesto]
### H2: [sección]
- Indicación de qué cubrir
### H2: [sección]
...

## Enlaces internos sugeridos
- [página] — anchor sugerido

## CTA
- [llamada a la acción según intención]

## Imágenes recomendadas
- [tipo de imagen] — [dónde ubicarla]
```

## Notas

- El brief guía, no redacta. No escribas el cuerpo del artículo dentro del brief salvo que el usuario lo pida explícitamente.
- Si no hay competidores ni acceso a SERP, construye la estructura desde la intención y dilo abiertamente.
- Mantén las indicaciones por sección concisas: el redactor necesita dirección, no un guion palabra por palabra.
- Si el usuario aporta una guía de marca, respeta su tono y vocabulario en las recomendaciones.
