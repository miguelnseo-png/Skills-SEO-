---
name: keyword-clustering-basico
description: Agrupa y prioriza una lista de keywords por intención de búsqueda y las mapea a páginas del sitio. Usa este skill siempre que el usuario suba o pegue una lista de keywords (desde un export de Google Search Console, de Ahrefs, o escritas a mano) y quiera organizarlas, clusterizarlas por intención, priorizarlas por oportunidad, o decidir qué páginas crear u optimizar. También actívalo cuando el usuario diga "clusteriza estas keywords", "agrupa por intención", "qué páginas debería crear", "prioriza estas keywords" o "mapea keywords a páginas". El output es una tabla clara (y opcionalmente un CSV) con cada keyword etiquetada por intención, prioridad y página destino.
---

# Keyword Clustering Básico

Skill genérico para convertir una lista cruda de keywords en una estrategia de páginas accionable. Pensado como punto de partida: funciona solo con una lista de keywords, sin depender de herramientas de pago. Si hay datos de volumen y dificultad (de Ahrefs o GSC), se usan para afinar la priorización; si no los hay, se estima la oportunidad con el razonamiento sobre intención y competencia.

## Cuándo usarlo

- El usuario pega o adjunta una lista de keywords.
- El usuario tiene un export de GSC con las queries por las que ya aparece el sitio.
- El usuario pregunta qué páginas crear u optimizar a partir de un conjunto de términos.

## Flujo de trabajo

Sigue estos pasos en orden:

1. **Reúne el input.** Identifica la fuente: lista pegada, CSV de GSC (columnas típicas: query, clicks, impressions, position) o export de Ahrefs (keyword, volume, KD). Si hay columnas de volumen o posición, consérvalas para la priorización.

2. **Clasifica cada keyword por intención de búsqueda.** Usa estas cuatro categorías:
   - **Informacional** — el usuario busca aprender (ej: "qué es", "cómo funciona", "guía de"). Suele mapear a blog/contenido TOFU.
   - **Comercial** — el usuario investiga antes de decidir (ej: "mejor", "vs", "comparativa", "reseña"). Mapea a comparativas, listicles, páginas de categoría.
   - **Transaccional** — el usuario quiere actuar/comprar/contratar (ej: "comprar", "precio", "cerca de mí", marca + servicio). Mapea a páginas de producto, servicio o landing.
   - **Navegacional** — el usuario busca una marca o sitio específico. Rara vez es prioridad de contenido nuevo.

3. **Agrupa en clusters temáticos.** Junta keywords que un solo artículo o página podría cubrir. Una página bien hecha rankea para un cluster, no para una sola keyword.

4. **Asigna prioridad.** Usa esta lógica:
   - Alta — intención clara (transaccional o comercial), oportunidad realista (volumen razonable + competencia abordable, o ya rankeando en posiciones 4-20 según GSC).
   - Media — buena intención pero más competida, o volumen menor.
   - Baja — informacional de soporte, volumen muy bajo, o muy competida sin autoridad suficiente.
   - Regla práctica: los "low-hanging fruits" son keywords donde el sitio ya aparece en página 2 (posición 11-20 en GSC) — pequeñas mejoras on-page las suben rápido. Priorízalas siempre.

5. **Mapea cada cluster a una página.** Para cada cluster define:
   - Keyword principal (la de mayor intención/oportunidad del grupo).
   - Tipo de página (servicio, producto, categoría, blog, landing local).
   - Acción: **crear nueva** u **optimizar existente**.

## Formato de salida

Presenta SIEMPRE una tabla con estas columnas:

| Keyword | Intención | Cluster | Volumen* | Prioridad | Página destino | Acción |

(*Volumen solo si está disponible en el input. Si no, omite la columna o márcala como "sin dato".)

Debajo de la tabla, añade un resumen breve en prosa: cuántos clusters salieron, cuáles son los 3 quick wins más claros, y qué páginas nuevas valdría la pena crear primero.

Si el usuario lo pide, genera además un CSV descargable con las mismas columnas.

## Notas

- No inventes volúmenes ni KD. Si no hay datos, dilo y prioriza por intención y razonamiento de competencia.
- La intención manda sobre el volumen: una keyword transaccional de 50 búsquedas/mes suele valer más que una informacional de 2.000.
- Mantén los clusters accionables: si un cluster tiene 30 keywords muy distintas, probablemente son varios clusters.
