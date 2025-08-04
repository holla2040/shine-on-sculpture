# 🧮 Baby Step 11 — Flatten and Arrange Curve Shapes for Fabrication

This step guides you through preparing 3D curves or outlines for 2D fabrication (e.g., laser cutting or vinyl plotting) by flattening them and arranging them into a layout.

### Step-by-step

1. **Start with 3D curve objects**:
   - Use existing Bezier or NURBS curves.
   - These might be outlines, shapes, or wiring paths.

2. **Convert to 2D if needed**:
   - Select curve → In **Curve Properties**, set **2D** mode.
   - This ensures the curve lies flat on a plane.

3. **Align curves to front view**:
   - Go to front orthographic view (`Numpad 1` → `Numpad 5`).
   - Select the curves → `R` to rotate if necessary.

4. **Flatten all in Z-axis**:
   - Select all curves.
   - Press `S`, then `Z`, then `0` → Enter.
   - This squashes everything into a flat plane.

5. **Arrange for layout**:
   - Use `G` to move pieces around.
   - Use snapping (`Shift + Tab`) and enable **Increment** or **Vertex**.
   - Organize parts in a clean rectangle layout.

6. **Add bounding boxes (optional)**:
   - `Shift + A` → Mesh → Plane.
   - Resize to act as a cut bed or bounding frame.
   - Helps with spacing and scaling.

7. **Convert curves to mesh if needed**:
   - Right-click → Convert to Mesh from Curve.

8. **Export SVG or DXF**:
   - Use Blender's **Export SVG** plugin or external add-ons.
   - File → Export → SVG or DXF depending on your setup.

9. **Check output**:
   - Open exported file in Inkscape or CAD software to validate dimensions and layout.