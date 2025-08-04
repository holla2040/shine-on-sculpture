# 🧵 Baby Step 10 — Build a Curved Wire Structure Under a Surface

This step demonstrates how to create a network of curves under a surface, ideal for building supporting wires or internal frame structures for sculptural elements.

### Step-by-step

1. **Add a surface mesh**:
   - `Shift + A` → Mesh → Plane or UV Sphere.
   - Position or shape it to resemble the surface you want to support.

2. **Add a curve for support wire**:
   - `Shift + A` → Curve → Bezier.
   - Move it under the surface using `G Z`.

3. **Adjust curve shape**:
   - Enter Edit Mode (`Tab`) on the curve.
   - Move control points to follow the underside of the surface.
   - Use `E` to extrude additional supports.

4. **Convert to 3D and enable geometry**:
   - Select curve → go to **Curve Properties** tab.
   - Under **Geometry**, set **Depth** in the **Bevel** section (e.g., `0.01`) to give the curve thickness.

5. **Duplicate and distribute curves**:
   - In Object Mode, `Shift + D` to duplicate.
   - Use `G` and rotate (`R`) to align additional supports across surface.

6. **Optional: Add a lattice or wireframe modifier to the surface**:
   - Select the surface → Add **Wireframe Modifier**.
   - Creates an open lattice you can visually align with wires.

7. **Join support curves**:
   - Select all support curves → `Ctrl + J` to join.
   - They now behave as one object for editing.

8. **(Optional) Convert curves to mesh**:
   - For export or detailed editing: `Right-click` → Convert to → Mesh from Curve.

9. **Use for 3D printing or structural visualization**:
   - The curves now form a wire structure under your form.