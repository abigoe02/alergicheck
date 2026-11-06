---
version: 1
slug: "prototipo-8-index-html"
primary_target: "prototipo-8/index.html"
related_targets: []
---

# Prototipo 8 · Pantalla de la máquina

Scope: prototipo-8/index.html. Mode: Operate (kiosk-style task screen shown on a phone for interviews). Build: code-led.

Audience/job: student in front of a vending machine marks the allergens they avoid and picks a safe snack, then buys it by typing the slot code on the machine keypad.

States: reposo, catálogo sin filtro, catálogo filtrado (apto / trazas / no apto tachado / sin ficha), ficha (apto, trazas, no apto, pendiente), solicitud enviada, aviso de inactividad.

## Direction contract
THESIS: The grid IS the machine: 4 shelves × 3 slots (A–D, 1–3) in physical order, never re-sorted; filtering re-lights the shelves instead of hiding products. Refuses the e-commerce list with search and sort.
OWN-WORLD: Inherited AlergiCheck world from index.html and Figma S8: cream ground #f7f4ef, white slot cards, coffee brand #7a4a35, Inter, slot-code chips in near-black, green/amber/red verdict pills with icon + text.
STORY: The student sees what the machine holds, taps what they avoid, sees at once which slots are safe, opens one to confirm, and learns the code to press.
FIRST VIEWPORT: Reposo: brand + machine location top; large question headline; allergen icon row; ghosted shelf preview; full-width coffee "Toca para empezar" at thumb height.
FORM: Figma S8 composition pinned by the user (pinned brief, no roll). seed: none (unavailable)
Signature interaction: on filter change each slot re-lights in shelf order (short stagger): safe slots gain a green ring, unsafe ones dim and their name is struck through.
FINISH: unreviewed and undocumented is unfinished; this build ends with the finish review, the verdict, DESIGN.md, and every shipping raster carrying its provenance
