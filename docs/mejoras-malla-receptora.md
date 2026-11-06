# Mejoras de la malla receptora · cuadro "Nuevas ideas"

Cada prototipo recibió **solo sus propias ideas** de la hoja `Malla_Receptora_AlergiCheck.xlsx`.

## Prototipo A · App móvil (`index.html`)

| # | Idea de la malla | Dónde quedó | Cómo mostrarlo en la entrevista |
|---|---|---|---|
| A1 | Fuente y fecha en cada resultado, con acceso a la etiqueta original | Resultado → recuadro **Fuente** (cafetería, IA, Open Food Facts o demo), fecha de revisión y botón **Ver etiqueta original** (abre la foto tomada o la foto del empaque) | Escanea un snack y baja hasta el final de la hoja |
| A2 | Escaneo asistido: guía de encuadre, aviso de reflejo y alternativas si falla | Cámara: guía "Que el nombre quede dentro del marco"; el aviso cambia a amarillo si detecta **reflejo** u **oscuridad**. Botón **Buscar** (abajo a la derecha): búsqueda por nombre en las fichas de la cafetería y **código de barras** (con la cámara en Android/Chrome o escribiendo los números en iPhone; los datos salen de Open Food Facts). Si no se reconoce, el resultado ofrece **Buscar por nombre o código** | Apunta a la vitrina con reflejo; toca **Buscar** y escribe "empanada pollo" |
| A3 | Sección "¿Cómo funciona el escaneo?" con nivel de certeza | Enlace bajo el botón de escanear en Inicio, botón **?** en la cámara y en cada resultado. Cada resultado muestra **Certeza alta / media / baja** | Toca "¿Cómo funciona el escaneo?" en Inicio |
| A4 | Ejemplos para los alérgenos menos conocidos y explicación visible de trazas | Perfil: moluscos, ajonjolí, mostaza, apio, sulfitos y altramuz muestran un ejemplo junto al nombre ("Sulfitos · fruta seca, vinagre"). La tarjeta de trazas explica qué son, sin tener que tocar el ícono | Primera pantalla |
| A5 | Confirmación visual al guardar el perfil | Al tocar **Guardar** aparece "¡Listo, guardamos tu perfil!" con el número de alergias | Guarda el perfil |
| A6 | Ampliar la lista de alérgenos manteniendo buscador y "Otra alergia" | Perfil agrupado en **Los más comunes** (8), **Otros de declaración obligatoria** (6) y **Otras alergias** con atajos (maíz, cacao, fresa, kiwi, durazno, tartrazina) + buscador + "Otra alergia" | Primera pantalla |
| A7 | Información nutricional opcional en la ficha | Desplegable **Información nutricional (por 100 g)** en el resultado, cuando hay datos: productos leídos por código de barras (Open Food Facts) y modo demo. Las fichas de la IA no la traen todavía (ver nota) | Busca el código 7622210449283 |
| A8 | Paleta alternativa más juvenil sin perder el semáforo | Perfil → **Apariencia: Cálida / Juvenil** (morado). Verde, ámbar y rojo no cambian | Cambia la apariencia y vuelve a escanear |

**Nota A7:** para que la IA (Gemini) también devuelva información nutricional hay que pedirle el campo `nutricion` en la función `reconocer` de Supabase (`{"calorias", "grasas", "grasas_saturadas", "azucares", "sodio"}`, por 100 g). La app ya lo muestra si llega.

## Prototipo B · Pantalla informativa (`prototipo-8/index.html`)

Ahora usa el catálogo real de la cafetería (`catalogo.json`, Jacinto & Cornelia · UPC San Isidro) en lugar de los 12 productos inventados.

| # | Idea de la malla | Dónde quedó | Cómo mostrarlo en la entrevista |
|---|---|---|---|
| B1 | Buscador de productos y categorías | Catálogo: buscador y categorías **Sándwiches, Empanadas y salados, Pasteles y postres, Snacks, Ensaladas y bowls, Bebidas** | Escribe "yogurt" o toca **Snacks** |
| B2 | Fotos reales y marca de cada producto | Cada tarjeta y ficha muestra la **marca** (Nancy Natur, Sufrut, Pituquita o la cafetería). Las **fotos** se agregan en `prototipo-8/fotos/` (ver su LEEME); mientras no haya foto se dibuja un ícono del tipo de producto | — (faltan las fotos) |
| B3 | "¿Qué evitas?" como primer paso, comunes primero, sin desplazarse | Tras "Toca para empezar" aparece **¿Qué evitas?** con los 8 alérgenos más comunes, sin desplazarse, y "Ver 6 alérgenos más". En el catálogo, la barra de abajo resume lo que evitas y tiene **Cambiar** (ya no hay que deslizar filtros) | Desde el inicio |
| B4 | Íconos y letras más grandes y con más contraste | Textos de 13–17 px como mínimo en tarjetas, dos columnas en vez de tres, íconos y etiquetas de estado más grandes, grises más oscuros | — |
| B5 | Detalle de cada alérgeno y qué significa "trazas" en lenguaje simple | Ficha: cada alérgeno con ejemplos ("Lácteos · leche, queso, mantequilla, yogurt") y recuadro **¿Qué significa "puede contener"?**. En el catálogo, enlace **¿Qué son las trazas?** | Marca lácteos y abre unos Palitos de Yuca con Ajonjolí |
| B6 | QR para cargar las alergias guardadas en la app (simulado) | En "¿Qué evitas?": **¿Usas la app AlergiCheck?** muestra un QR; **Simular escaneo desde la app** carga lácteos y gluten y lo confirma | Paso "¿Qué evitas?" |
| B7 | El mismo catálogo en versión web para revisarlo desde casa | En el inicio hay un QR **Revísalo desde tu celular** que abre `prototipo-8/?web`: sin cuenta regresiva ni pantalla de reposo | Escanéalo con el celular |
| B8 | Información nutricional opcional | Ficha: desplegable **Información nutricional (por 100 g)** con octógonos de advertencia. Son **valores de ejemplo**, rotulados así, porque la cafetería no publica su tabla | Abre cualquier producto |

Se mantiene la vuelta al inicio tras 30 s sin uso y el borrado de filtros entre personas.
