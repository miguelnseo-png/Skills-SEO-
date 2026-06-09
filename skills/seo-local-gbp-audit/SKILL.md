---
name: seo-local-gbp-audit
description: "comparativa de estatus del seo local del cliente"
---

Genera documentos profesionales en .docx de auditoría y propuesta SEO para Google Business Profile (GBP). USAR ESTA SKILL cuando el usuario mencione:  seo-local-gbp-audit, ficha de Google, Google Business Profile, GBP, auditoría de competidores, propuesta de valor para cliente sin ficha, posicionamiento local, SEO local, Google Maps, comparativa de fichas, o cuando quiera analizar cómo está un negocio vs sus competidores en Google.
Produce DOS tipos de documentos según el caso: - MODO A — Cliente SIN ficha de Google: genera propuesta de valor + comparativa con competidores de la categoría. - MODO B — Cliente CON ficha de Google: genera auditoría comparativa completa con puntos fuertes, debilidades,
oportunidades, análisis FODA, tabla maestra de comparación y plan de acción priorizado.
Siempre en formato .docx, con paleta de colores adaptable al cliente, plan de acción incluido en el documento. Usar también cuando el usuario diga "hazme el informe GBP", "compara la ficha de mi cliente",  "propuesta para cliente sin Google", o cualquier combinación de cliente + Google + competidores.SEO Local — Google Business Profile Audit
Descripción general
Esta skill produce documentos .docx profesionales de SEO local para Google Business Profile en dos modos:
ModoCondiciónDocumento generadoA — Propuesta de ValorCliente NO tiene ficha GBPPropuesta + comparativa vs competidores de la categoríaB — Auditoría ComparativaCliente SÍ tiene ficha GBPAuditoría completa con FODA, tabla maestra, plan de acción

PASO 1 — Detectar el Modo correcto
Antes de pedir datos, determinar si el cliente tiene o no tiene ficha de Google verificada.

Si ya se mencionó en la conversación → proceder directamente al formulario del modo correspondiente.
Si no está claro → preguntar: "¿Tu cliente ya tiene una ficha de Google Business Profile creada y verificada?"


PASO 2 — Solicitar los datos (Formularios)
Si los datos no están en la conversación, pedirlos usando el formulario correspondiente.
No inventar ni asumir datos que el usuario no haya dado.
Formulario MODO A — Cliente sin ficha GBP
DATOS DEL CLIENTE:
- Nombre del negocio
- Categoría / rubro
- Ciudad y zona geográfica
- Palabra clave principal objetivo (ej: "academia de oratoria Maracay")
- ¿Cuántos competidores aproximados aparecen en Google Maps para esa palabra clave?
  (Pocos 1-3 / Moderados 4-10 / Muchos 11-20 / Saturado 20+)
- Colores corporativos del cliente (si los tiene) o paleta preferida

DATOS DE COMPETIDORES (los que aparezcan en GBP para la keyword):
Por cada competidor relevante:
  - Nombre y categoría
  - N° de reseñas y puntuación
  - ¿Tiene fotos? ¿Cuántas aprox.?
  - ¿Publica Posts?
  - ¿Tiene descripción?
  - ¿Tiene servicios listados?
  - Datos activos: horario / teléfono / web / redes sociales
Formulario MODO B — Cliente con ficha GBP
DATOS DEL CLIENTE:
- Nombre del negocio y categoría
- Ciudad y zona geográfica
- Palabra(s) clave principal(es) objetivo
- URL o nombre exacto de su ficha en Google Maps
- ¿Ficha verificada? (Sí / No)
- N° de reseñas y puntuación actual
- ¿Responde las reseñas? (Sí / No)
- N° de fotos cargadas y tipo (producto / instalaciones / gráficas)
- ¿Publica Google Posts? (frecuencia)
- ¿Tiene servicios/productos listados? (Sí / No)
- ¿Tiene descripción redactada? (Sí / No — ¿incluye la keyword?)
- Datos activos: horario / teléfono / web / redes sociales
- Posición actual en resultados para cada keyword objetivo
- Colores corporativos del cliente o paleta preferida

POR CADA COMPETIDOR (idealmente 3-5):
  - Nombre y categoría
  - URL o nombre en Google Maps
  - ¿Ficha verificada?
  - N° de reseñas y puntuación
  - ¿Responden reseñas?
  - N° de fotos y tipo
  - ¿Publica Posts?
  - ¿Servicios listados?
  - ¿Descripción redactada? ¿Incluye keyword?
  - Datos activos: horario / teléfono / web / redes
  - Posición en resultados (si se conoce)

PASO 3 — Definir la paleta de colores
Antes de generar el .docx, definir la paleta basada en los colores del cliente:
javascript// Paleta base (adaptar con los colores del cliente)
const DARK    = "[color oscuro principal]";   // ej: azul marino, verde oscuro
const MID     = "[color medio]";              // ej: azul medio, verde medio  
const LIGHT   = "[color claro de fondo]";     // ej: azul claro, verde claro
const ACCENT  = "[color de acento]";          // ej: naranja, dorado, rojo
const WHITE   = "FFFFFF";
const GRAY    = "F5F7FA";
const DARK_TX = "1A1A2E";

// Si el cliente no tiene colores definidos, usar la paleta institucional por defecto:
// DARK="0D2B4E" (navy) / MID="1565C0" (azul) / LIGHT="E3F0FF" / ACCENT="E65100"

PASO 4 — Generar el documento
Leer primero el SKILL.md de docx antes de escribir cualquier código:
/mnt/skills/public/docx/SKILL.md
Estructura MODO A — Propuesta de Valor

Banner de portada — nombre del negocio, tipo de documento, keyword objetivo
Frase de gancho — párrafo introductorio contextualizado al rubro
Estadísticas clave — tabla de 3 tarjetas (competidores en zona / dato del sector / potencial Top 3)
¿Qué es una ficha GBP optimizada? — explicación breve y accesible
Tabla comparativa — cliente (sin ficha) vs competidores principales (con colores semáforo)
Beneficios concretos para el negocio — 6 bullets con negrita + descripción
Sección especial del sector — datos o ventajas específicas del rubro (salud, educación, industria, etc.)
¿Qué incluye la optimización? — lista de entregables
Plan de acción — tabla con acciones, plazos e impacto esperado
Bloque CTA de cierre — llamado a la acción con urgencia contextualizada
Pie de página — documento preparado para [nombre del cliente]

Estructura MODO B — Auditoría Comparativa

Banner de portada — nombre, tipo auditoría, keyword objetivo, fecha
Resumen ejecutivo — diagnóstico de 2 párrafos + 4 tarjetas KPI
Tabla comparativa maestra — todos los factores vs todos los competidores (✅/⚠️/❌)
Puntos fuertes — lo que el cliente ya hace bien (bullets con negrita)
Puntos de mejora — debilidades críticas con análisis por cada una (H3 + párrafo explicativo)
Análisis FODA — tabla 2x2 (Fortalezas / Debilidades / Oportunidades / Amenazas)
Oportunidades por prioridad — tabla con columnas: Prioridad / Oportunidad / Por qué importa
Plan de acción — tabla numerada con: Acción / Plazo / Impacto esperado
Conclusión y diagnóstico final — proyección de resultados con optimización
Pie de página — documento preparado para [nombre del cliente]


PASO 5 — Reglas de construcción del .docx
Semáforo de evaluación (Modo B)

✅ verde claro → cumple correctamente
⚠️ amarillo → cumple parcialmente
❌ rojo claro → ausente o incorrecto

Prioridades del plan de acción

🔴 Alta → impacto directo en posicionamiento, acción inmediata
🟠 Media → mejora significativa, primera o segunda semana
🟡 Normal → optimización continua, mes 1-2

Tablas obligatorias en Modo B

Tabla maestra comparativa — filas = factores GBP, columnas = cliente + competidores
Tabla FODA — cuadrante 2x2 con shading por sección
Tabla de oportunidades — 3 columnas: prioridad / oportunidad / por qué importa
Tabla plan de acción — 4 columnas: # / acción / plazo / impacto

Sección especial por sector (Modo A)
Adaptar la sección 7 según el rubro del cliente:

Salud → Panel de conocimiento médico, atributos de accesibilidad, búsquedas de alta intención
Educación → Búsquedas por programa, reseñas de exalumnos, Google Posts de resultados
Industria/B2B → Fotos de stock y galpón, distribución nacional, categorías técnicas
Retail/Comercio → Horarios especiales, productos listados, ofertas por Posts
Gastronomía → Menú en GBP, fotos de platos, reservas y horarios pico
Servicios profesionales → Credenciales visibles, caso de uso de reseñas, atributos de servicio


PASO 6 — Validación y entrega
bash# Siempre validar antes de presentar
python /mnt/skills/public/docx/scripts/office/validate.py /mnt/user-data/outputs/[nombre].docx
Nombre del archivo de salida:

Modo A: [NombreCliente]_Propuesta_GBP.docx
Modo B: [NombreCliente]_Auditoria_GBP_Competitiva.docx

Usar present_files para entregar el documento al usuario.

Referencia rápida — Checklist de factores GBP evaluados (Modo B)
#FactorImpacto SEO1Ficha verificadaMuy alto2Palabra clave en nombre del negocioMuy alto3Categoría principal correctaMuy alto4Descripción redactadaAlto5Keyword en la descripciónAlto6Servicios/productos listadosAlto7N° de reseñasMuy alto8Responde reseñasMedio9Puntuación promedioAlto10N° de fotosAlto11Fotos del establecimientoAlto12Fotos del producto/servicioMedio-Alto13Google Posts publicadosMedio14Horario cargadoAlto15Teléfono activoAlto16Sitio web vinculadoAlto17Redes sociales vinculadasMedio18Posición en resultados por keywordDiagnóstico

Notas importantes

Nunca inventar datos — si falta información, marcarla como "a verificar" en el documento
Siempre contextualizar — el tono y los ejemplos deben ser específicos del rubro y la ciudad del cliente
El plan de acción siempre incluido — no es un documento separado, va dentro del mismo .docx
La paleta es adaptable — si el cliente tiene colores definidos, usarlos; si no, usar la paleta institucional navy/azul/naranja
Datos parciales son válidos — con la información disponible se genera el documento y se señalan los campos pendientes de verificación