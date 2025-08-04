# 🧱 Baby Step 1 — Tessellate a Sphere Using Triangles and Squares

This step demonstrates how to create a tessellated sphere that combines triangles and squares to resemble a sculptural tile layout. The goal is to learn face selection, subdivision, face deletion, and smoothing.

## Step-by-step

1. **Delete the default cube**:
   - Open Blender → Press `X` → Confirm delete.

2. **Add a UV Sphere**:
   - Press `Shift + A` → Mesh → UV Sphere.
   - In the bottom-left corner panel (before clicking elsewhere), set:
     - Segments: `6`
     - Rings: `4`
   - This creates a low-resolution sphere with clear face divisions.

3. **Enter Edit Mode**:
   - Select the sphere → Press `Tab` to enter Edit Mode.

4. **Subdivide the mesh**:
   - Select all faces with `A`.
   - Right-click → Subdivide.
   - In the lower-left Subdivide panel, increase **Number of Cuts** to `1`.

5. **Select and delete triangles**:
   - Press `3` for Face Select mode.
   - Manually select alternating face rows to keep only square patterns.
   - Or, experiment with the Select → Checker Deselect option.
   - Press `Ctrl + I` to invert the selection.
   - Press `X` → Delete → Faces.

6. **Smooth and round the sphere**:
   - Go back to Object Mode (`Tab`).
   - Go to the **Modifiers tab** (wrench icon).
   - Add **Subdivision Surface Modifier**:
     - View Levels: `2`
   - Right-click the object → Shade Smooth.

7. **(Optional) Add more details**:
   - Apply modifier if needed.
   - You can also use Displace modifiers or sculpting tools.