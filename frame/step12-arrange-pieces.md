# 🧩 Baby Step 12 — Arrange Disconnected Parts as Puzzle Pieces

This step shows how to arrange disconnected mesh pieces so they interlock like puzzle pieces. This is ideal for assembling sculpture parts or preparing components for nesting and cutting.

### Step-by-step

1. **Start with separate parts**:
   - Use parts from Step 3 or any set of distinct mesh pieces.
   - Ensure they're clearly visible and not overlapping.

2. **Enter top orthographic view**:
   - Press `Numpad 7` for top view.
   - Press `Numpad 5` to switch to orthographic projection.

3. **Align flat side down**:
   - Select each part.
   - Rotate (`R X 90`) or use `Alt + R` to reset.
   - Use `S Z 0` in Edit Mode to flatten if needed.

4. **Snap pieces to a plane**:
   - Add a reference plane (`Shift + A` → Mesh → Plane).
   - Turn on **Snap** (`Shift + Tab`) and set to **Face**.
   - Move each part down to sit flush on the plane.

5. **Position like puzzle pieces**:
   - Move (`G`) and rotate (`R`) each part.
   - Leave 0.5 to 1 unit of space for cut tolerance.
   - Optionally add **empties** or **text labels** beside each part.

6. **Add interlocks manually (optional)**:
   - Use boolean objects like cylinders or notches.
   - Cut puzzle-like tabs or sockets using the Boolean modifier.

7. **Group parts**:
   - Select all → `Ctrl + G` to group.
   - Or parent to an empty (`Ctrl + P`).

8. **Export or print layout**:
   - Optionally convert to SVG (see Step 5).
   - Or render the layout for assembly instructions.