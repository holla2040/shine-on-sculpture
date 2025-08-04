# 🔧 Baby Step 6 — Engrave Labels into Mesh with a Boolean Modifier

This step teaches you to engrave text into the surface of an object using the Boolean modifier. This is ideal for embossing or engraving part numbers or decorative text directly into geometry.

### Step-by-step

1. **Add your base mesh**:
   - Example: `Shift + A` → Mesh → Cube.

2. **Add a Text object**:
   - `Shift + A` → Text.
   - Rotate it upright: `R X 90`, press Enter.
   - Move it over the cube using `G`.

3. **Edit the text**:
   - With text selected, press `Tab` to enter edit mode.
   - Change the label (e.g. "A1" or "Part 3").
   - Press `Tab` again to exit text edit mode.

4. **Convert the text to a mesh**:
   - Right-click → Convert to → Mesh from Curve.

5. **Add thickness with Solidify (optional)**:
   - Modifier tab → Add **Solidify Modifier**.
   - Set Thickness to `0.01`–`0.03`.

6. **Position text partially inside cube**:
   - Use top or front view (`Numpad 7` or `1`).
   - Move the text slightly into the surface of the cube.

7. **Apply the Boolean modifier**:
   - Select the cube.
   - Go to Modifiers tab → Add Modifier → Boolean.
   - Set **Operation** to **Difference**.
   - Click **Object**, then choose the text mesh.
   - **Note**: Blender 4.5+ includes a new **Manifold** solver option that's faster and more reliable than the default Float solver. Try it if you encounter issues.

8. **Apply the modifier**:
   - Click the ▼ drop-down on the Boolean modifier → Apply.
   - You can now delete the text mesh — the engraved mark remains.

9. **Smooth shading (optional)**:
   - Right-click → Shade Smooth.

10. **Export or print-ready**:
   - You now have a mesh with real engraved geometry.