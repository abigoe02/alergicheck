# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Estudiantes universitarios (UPC, Lima) con alergias o restricciones alimentarias que compran snacks en las máquinas expendedoras del campus. Están de pie frente a la máquina, con poco tiempo entre clases, y necesitan saber rápido y con confianza si un snack es seguro para ellos. En esta etapa, los usuarios reales del prototipo son los entrevistados de una validación de Design Thinking: lo usan en el celular del equipo mientras piensan en voz alta (técnica LOUD).

## Product Purpose

AlergiCheck ayuda a decidir qué snack comprar según tus alergias. Hay dos soluciones en validación:

- **Prototipo A (app móvil, `index.html`):** el estudiante registra sus alergias, le toma una foto al snack y la IA (Gemini vía Supabase) dice si es apto.
- **Prototipo 8 (pantalla en la máquina, `prototipo-8/`):** la máquina muestra todos sus productos; el estudiante toca los alérgenos que evita y los productos aptos se iluminan mientras los no aptos se atenúan y se tachan.

El éxito es que el entrevistado encuentre un snack seguro sin ayuda y confíe en el veredicto.

## Operating Context

- Máquinas de distintos proveedores (Vendomática, entre otros); cada una tiene sus propios códigos de ranura (A1, B2…). El código de barras del empaque no se puede escanear porque el producto está detrás del vidrio.
- La pantalla de la máquina es compartida: vuelve al inicio sola tras 30 s sin uso y no guarda el perfil de nadie.
- Las fichas de alérgenos las verifica la cafetería; un producto nuevo puede no tener ficha todavía.
- Entrega del curso: entrevista grabada en un solo video por integrante, mostrando ambos prototipos.

## Capabilities and Constraints

- Sitio estático en GitHub Pages (repo `abigoe02/alergicheck`); sin build ni framework.
- 14 alérgenos de referencia: lácteos, gluten, huevo, maní, frutos secos, soya, pescado, mariscos, moluscos, ajonjolí, mostaza, apio, sulfitos, altramuz.
- Estados de veredicto: Apto, Puede contener trazas, No apto, Sin ficha / no reconocido.
- El prototipo B usa `catalogo.json`: fichas de prueba de la cafetería Jacinto & Cornelia (UPC San Isidro), armadas con etiquetas y la carta; deben confirmarse con la cafetería. La información nutricional del prototipo B son valores de ejemplo.

## Brand Commitments

- Nombre AlergiCheck, en español peruano, tuteo.
- Identidad ya definida en Figma ("AlergiCheck · Prototipos S7 y S8") y en `index.html`: fondo crema, café como color de marca, Inter, verde/ámbar/rojo para estados.

## Evidence on Hand

- Diseños de Figma S7 v2 (app) y S8 (máquina, 6 pantallas: Reposo, Catálogo, Catálogo filtrado, Ficha apta, Ficha pendiente, Solicitud enviada).
- No hay testimonios, métricas ni catálogo real; no inventarlos.

## Product Principles

1. El veredicto nunca depende solo del color: siempre lleva texto e ícono.
2. Ante la duda, precaución: sin ficha o con trazas nunca se muestra como apto.
3. Rápido frente a la máquina: decidir en segundos, sin registrarse.
4. Privacidad en pantallas compartidas: nada persiste entre usuarios.
