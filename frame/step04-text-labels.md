# 🔤 Baby Step 4 — Add Number Labels to Objects Using Text

This step explains how to add visible number labels using text objects in Blender. This is useful for marking parts before exporting or fabricating.

### Step-by-step

1. **Create a base object**:
   - Add a Cube (`Shift + A` → Mesh → Cube).

2. **Add a Text object**:
   - `Shift + A` → Text.
   - The text will appear flat on the X-Y plane.

3. **Rotate and position**:
   - With the text selected:
     - Press `R X 90` and Enter to rotate it upright.
     - Use `G` to move it onto a visible cube face.
     - Press `S` to scale it smaller.

4. **Edit the text**:
   - Press `Tab` while the text is selected to enter text edit mode.
   - Delete existing characters and type your label (e.g. `01`).
   - Press `Tab` again to exit edit mode.

5. **Convert to mesh**:
   - With the text selected, right-click → Convert to → Mesh from Curve.

6. **Add Solidify modifier (optional)**:
   - Adds thickness for 3D printing or Boolean operations.
   - Go to Modifiers tab → Add **Solidify** → Thickness ~ `0.01`.

7. **Align and position**:
   - Use snapping (`Shift + Tab`) or `G` and `R` to position label flush on surface.
   - Use wireframe or orthographic view (`Numpad 5`) for precision.

8. **(Optional) Parent label to part**:
   - Select text → `Shift` + select cube → `Ctrl + P` → Object.