# 📏 Baby Step 8 — Measure the Length of a Curve

This step shows you how to measure the length of a curve object accurately in Blender, which is useful when fabricating materials to length (e.g., wire or tubing).

### Step-by-step

1. **Add a Bezier curve**:
   - `Shift + A` → Curve → Bezier.

2. **Enter Edit Mode**:
   - Select the curve and press `Tab`.
   - Select and move the control points (`G`) to shape the curve.
   - Use `E` to extrude additional segments.

3. **Convert to 3D if needed**:
   - In the **Properties Panel**, under the **Curve** tab:
     - Enable **3D** under the **Shape** section.

4. **Enable curve length display**:
   - Blender doesn't show curve length by default.
   - Open the **Sidebar (N key)** in the viewport.
   - Under the **Item** tab, Blender will only show length for mesh objects, not native curves.

5. **Convert curve to mesh temporarily**:
   - Select the curve → `Alt + C` or Right-click → Convert to Mesh.

6. **Enable edge length display**:
   - Go to Overlays (top-right corner of viewport).
   - Enable **Edge Length** under **Measurement**.
   - Enter Edit Mode and select all edges.
   - Total length is the sum of all segments shown.

7. **Use Exact Edit add-on (optional)**:
   - Edit → Preferences → Add-ons.
   - Enable **Add Mesh: Extra Objects** or **MeasureIt**.
   - These add-ons provide tools for accurate length calculation and onscreen dimensions.

8. **Undo mesh conversion if needed**:
   - If you want to preserve the original curve, duplicate it first (`Shift + D`).