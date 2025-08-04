# 🔷 Baby Step 2 — Create a Hollow Wire Mesh Sphere

This step shows how to convert a standard UV sphere into a hollow mesh structure using the Wireframe modifier. This is ideal for creating sculpture components with open geometry.

## Step-by-step

1. **Start with a clean scene**:
   - File → New → General.
   - Delete the default cube (`X`).

2. **Add a UV Sphere**:
   - `Shift + A` → Mesh → UV Sphere.
   - Accept the default settings (32 segments, 16 rings).

3. **Apply the Wireframe modifier**:
   - Select the sphere.
   - Go to the Modifier tab (wrench icon).
   - Click **Add Modifier** → **Wireframe**.

4. **Adjust thickness**:
   - Set **Thickness** to `0.03` (or experiment with values).
   - Leave other settings at default.

5. **(Optional) Add a Subdivision Surface modifier**:
   - Add another modifier: **Subdivision Surface**.
   - Move it below Wireframe in the stack.
   - Increase View to `2` or `3` for smoothness.

6. **Apply modifiers**:
   - Apply both modifiers if you need final geometry (click ▼ on each modifier → Apply).

7. **Shade Smooth**:
   - Right-click the object → Shade Smooth.

8. **Export or duplicate**:
   - Now you have a geometric mesh suitable for wire sculptures or printing.