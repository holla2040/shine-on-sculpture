# 🧪 Baby Step 7 — Simulate Layer Lines with Sliced Geometry

This step simulates the look of 3D printer layer lines by slicing a model horizontally. It helps visualize fabrication layers and can be used to stylize digital sculptures.

### Step-by-step

1. **Create a base shape**:
   - `Shift + A` → Mesh → UV Sphere or any mesh.

2. **Add a new object to slice with**:
   - `Shift + A` → Mesh → Plane.
   - Scale it to 10× size (`S`, then `10`, Enter).
   - Move the plane just below the base object.

3. **Create slicing copies**:
   - With the plane selected → Go to the **Modifiers** tab.
   - Add **Array Modifier**:
     - Count: `30` (or desired number of layers).
     - Relative Offset: set Z to `0.1`, others to `0`.
   - Apply the modifier (click ▼ → Apply).

4. **Convert to cutters**:
   - Join all planes into one mesh:
     - Select all planes → `Ctrl + J`.

5. **Add Boolean modifier to base mesh**:
   - Select the base object.
   - Add Modifier → Boolean.
   - Set Operation: **Intersect** or **Difference** (try both).
   - Select the stacked plane mesh as the Boolean object.

6. **Apply and clean up**:
   - Apply the Boolean modifier.
   - Delete the slicing object (planes).

7. **Check the result**:
   - You'll see horizontal divisions or slices across the object.
   - These mimic layer lines.

8. **Style further (optional)**:
   - Add solidify modifier for plate thickness.
   - Color layers differently using Material Slots.