# Kitchen level props (draft)
Scale: 1 cell = 1 cm = 16 px. Transparent PNGs, alpha fully on or off, at most 16 colours, hard pixels, no drawn cast shadows.
Views: floor items are drawn straight top-down. Standing items are drawn front-on, seen from ~30 degrees above.

| File | Pixel size | Cells (cm) | Colours | View | Scene / role |
|---|---|---|---|---|---|
| kitchen_breakfast_toast_plate_table.png | 352x273 | 22x17 | 16 | front, slightly above | Opening: breakfast for girlfriend (on table) |
| kitchen_breakfast_toast_plate_floor.png | 352x352 | 22x22 | 15 | top-down | Opening: plate dropped on floor |
| kitchen_breakfast_coffee_mug.png | 144x160 | 9x10 | 13 | front, slightly above | Opening: breakfast |
| kitchen_crumb_fine_a..d.png | 4x4, 5x5, 6x6, 8x8 | 0.25-0.5 | 3-4 | top-down | Opening: collectibles |
| kitchen_bread_chunk_a..c.png | 32x30, 24x22, 28x27 | 1.4-2 | 11-13 | top-down | Opening: torn bread chunks, cover the hero can hide behind |
| kitchen_tv.png | 1280x1378 | 80x86 (incl. stand) | 16 | front, slightly above | Opening: TV news playing |
| kitchen_stove_breakfast.png | 1060x1286 | 60 cm body (pan handle overhangs ~6 cm) x 80 | 16 | front, slightly above | Opening: gas range with oven, egg frying |
| kitchen_basement_door.png | 1360x3200 | 85x200 (fills the whole canvas, no gap, not stretched); handle centre 1600 px (100 cm) from bottom | 14 | front | Kitchen exit -> next level (basement) |

The door is drawn in code (`/workspace/door_proc.py`) on an 8 px grid: 170x400 art pixels scaled up x8 with nearest-neighbour. It has flat wood blocks, an open door, a lit landing at the threshold, then treads that drop away (narrower, thinner, darker with each step, fading to near-black; only the treads show, no risers), and is fully opaque.

_preview.png: contact sheet on a beige background. Each sprite has a 16x16 px (1 cm) marker drawn at the same scale factor as the sprite (x4 for sprites up to 32 px, x1 up to 400 px, x0.25 for large ones).
