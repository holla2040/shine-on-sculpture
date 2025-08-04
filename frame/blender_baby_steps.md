# Blender Baby Steps: Independent Tutorials for Sculpture Projects

Each tutorial below is **fully self-contained**, designed for a **Blender novice**, and written using Blender 4.5 LTS+. These tutorials do **not depend on each other** and can be followed in any order. Each one demonstrates a single concept to help you build and understand sculpture components.

---

## 🐍 Baby Step 13 — Create and Label Flat Panels with Python

This step demonstrates how to use Blender’s built-in Python scripting to automatically generate flat panels and label them. It is useful for automating repetitive modeling tasks or integrating procedural elements.

### Step-by-step

1. **Open the Scripting workspace**:
   - At the top of Blender, click **Scripting**.
   - You’ll see the Text Editor and Python Console.

2. **Create a new script**:
   - In the Text Editor, click **New**.
   - Copy and paste the code below:

   ```python
   import bpy

   # Create 6 labeled flat panels in a grid
   for i in range(6):
       bpy.ops.mesh.primitive_plane_add(size=1, location=(i * 1.5, 0, 0))
       panel = bpy.context.active_object
       panel.name = f"Panel_{i+1}"

       # Add label as text
       bpy.ops.object.text_add(location=(i * 1.5, 0, 0.01))
       text = bpy.context.active_object
       text.data.body = f"{i+1}"
       text.scale = (0.3, 0.3, 0.3)

       # Convert text to mesh (optional)
       bpy.ops.object.convert(target='MESH')

       # Parent text to panel
       text.parent = panel
   ```

3. **Run the script**:
   - Click the **Run Script** button or press `Alt + P`.
   - You’ll see 6 flat planes with number labels appear.

4. **Adjust spacing or layout**:
   - Modify the `location=(i * 1.5, 0, 0)` line to space in X, Y, or Z.

5. **Save your script**:
   - Click **Text** → Save As and give your script a name like `label_panels.py`.

6. **Use script on future projects**:
   - Load your saved script anytime.
   - Run it to generate labeled parts quickly.

7. **(Optional) Add export function**:
   - Automate export via:
   ```python
   bpy.ops.export_scene.obj(filepath="/tmp/labeled_panels.obj")
   ```

---
## 🧩 Baby Step 12 — Arrange Disconnected Parts as Puzzle Pieces

This step shows how to arrange disconnected mesh pieces so they interlock like puzzle pieces. This is ideal for assembling sculpture parts or preparing components for nesting and cutting.

### Step-by-step

1. **Start with separate parts**:
   - Use parts from Step 3 or any set of distinct mesh pieces.
   - Ensure they’re clearly visible and not overlapping.

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

---
## 🧮 Baby Step 11 — Flatten and Arrange Curve Shapes for Fabrication

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
   - Use Blender’s **Export SVG** plugin or external add-ons.
   - File → Export → SVG or DXF depending on your setup.

9. **Check output**:
   - Open exported file in Inkscape or CAD software to validate dimensions and layout.

---
## 🧵 Baby Step 10 — Build a Curved Wire Structure Under a Surface

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

---
## 🪟 Baby Step 9 — Add Spacing Between Tessellated Panels

This step demonstrates how to space apart previously joined or tessellated panels. It’s helpful for exploded views, printing separations, or physically cutting/scoring designs.

### Step-by-step

1. **Start with multiple flat panels**:
   - Use the separated cube faces from Step 3 or create multiple flat meshes.

2. **Select a panel in Object Mode**:
   - Right-click to select a panel.
   - Use `G` to move it slightly on the X, Y, or Z axis.

3. **Set precise spacing**:
   - Press `N` to open the **Sidebar**.
   - In the **Item** tab, set specific `Location` values.
   - For example: spread panels by `0.1` or `0.2` units on the X axis.

4. **Distribute with snapping (optional)**:
   - Enable snapping (`Shift + Tab`).
   - Use **Increment** or **Vertex** snapping.
   - Hold `Ctrl` while dragging to snap in precise increments.

5. **Use Array Modifier for grid layout (optional)**:
   - Add Array Modifier to one panel.
   - Set X/Y offsets for spacing.
   - Apply modifier to generate multiple spaced copies.

6. **Visual alignment aid**:
   - Add a reference plane or empty as origin.
   - Align all panels relative to this using snapping or coordinates.

7. **Use Explode layout for presentation (optional)**:
   - Select all panels → `Alt + G` to reset location.
   - Use `G` + axis to slide each panel away in a radial or linear direction.

8. **Group spaced parts**:
   - Select all → `Ctrl + G` to group.
   - Use collections or parenting to keep layout manageable.

---
## 📏 Baby Step 8 — Measure the Length of a Curve

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
   - Blender doesn’t show curve length by default.
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

---
## 🧪 Baby Step 7 — Simulate Layer Lines with Sliced Geometry

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
   - **Note**: In Blender 4.5+, try the **Manifold** solver for cleaner results.

6. **Apply and clean up**:
   - Apply the Boolean modifier.
   - Delete the slicing object (planes).

7. **Check the result**:
   - You’ll see horizontal divisions or slices across the object.
   - These mimic layer lines.

8. **Style further (optional)**:
   - Add solidify modifier for plate thickness.
   - Color layers differently using Material Slots.

---
## 🔧 Baby Step 6 — Engrave Labels into Mesh with a Boolean Modifier

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
   - Change the label (e.g. “A1” or “Part 3”).
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

---
## 🧰 Baby Step 5 — Flatten and Export Surfaces as SVG

This step shows you how to unwrap a 3D surface and export it as an SVG file. This is especially useful for preparing components for laser cutting or vector-based fabrication.

### Step-by-step

1. **Start with a flat surface or panel**:
   - Example: Select a cube face object you created in a previous step.

2. **Enter Edit Mode**:
   - Select the object → `Tab` to enter Edit Mode.
   - Select all (`A`).

3. **Unwrap the surface**:
   - Press `U` → **Project from View** (for current camera angle projection).
   - This flattens the selected geometry into UV space.

4. **Switch to the UV Editing workspace**:
   - From the top tab, choose **UV Editing**.
   - You’ll see:
     - Left: UV Editor window with the 2D layout.
     - Right: 3D viewport.

5. **Check alignment and scaling**:
   - Ensure the object is facing front before unwrap (`Numpad 1`).
   - If not flat, use View → Align View → Align to Active Face.

6. **Install Export to SVG add-on**:
   - Edit → Preferences → Add-ons.
   - Search for `UV Export` or install external plugin like **UV → Export SVG**.

7. **Export the UV layout as SVG**:
   - In UV Editor, click UV → Export UV Layout.
   - Choose `.svg` format if supported.
   - Set size and fill settings (usually black stroke, no fill).
   - Save to your desired location.

8. **Open in vector tools**:
   - Open exported SVG in Inkscape, Illustrator, etc. for further layout, labels, or CAM prep.

---
## 🔤 Baby Step 4 — Add Number Labels to Objects Using Text

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

---
## 🧊 Baby Step 3 — Break a Cube Into Separate Flat Panels

This step teaches you how to split the faces of a cube into separate flat mesh objects. This is useful for preparing components that will later be spaced or labeled individually.

### Step-by-step

1. **Add a cube**:
   - `Shift + A` → Mesh → Cube.

2. **Enter Edit Mode**:
   - Select the cube and press `Tab`.
   - Press `3` to activate Face Select mode.

3. **Separate each face**:
   - Select one face at a time.
   - Press `P` → **Selection**.
   - Repeat until all 6 faces are separated into their own objects.

4. **Return to Object Mode**:
   - Press `Tab`.
   - You now have 6 separate panels in the same location.

5. **Move and inspect**:
   - Select each panel.
   - Press `G` to move it away slightly to inspect.
   - Use `R` to rotate them for exploded views.

6. **Rename panels for organization**:
   - Open the **Outliner** panel.
   - Rename each panel (e.g. "Top", "Front", "Left").

7. **Group or parent if needed**:
   - Select all → `Ctrl + G` to create a group.
   - Or `Ctrl + P` to parent them under an empty object.

---
## 📚 Table of Contents

1. [Tessellate a Sphere Using Triangles and Squares](#-baby-step-1--tessellate-a-sphere-using-triangles-and-squares)
2. [Create a Hollow Wire Mesh Sphere](#-baby-step-2--create-a-hollow-wire-mesh-sphere)
3. [Break a Cube Into Separate Flat Panels](#-baby-step-3--break-a-cube-into-separate-flat-panels)
4. [Add Number Labels to Objects Using Text](#-baby-step-4--add-number-labels-to-objects-using-text)
5. [Flatten and Export Surfaces as SVG](#-baby-step-5--flatten-and-export-surfaces-as-svg)
6. [Engrave Labels into Mesh with a Boolean Modifier](#-baby-step-6--engrave-labels-into-mesh-with-a-boolean-modifier)
7. [Simulate Layer Lines with Sliced Geometry](#-baby-step-7--simulate-layer-lines-with-sliced-geometry)
8. [Measure the Length of a Curve](#-baby-step-8--measure-the-length-of-a-curve)
9. [Add Spacing Between Tessellated Panels](#-baby-step-9--add-spacing-between-tessellated-panels)
10. [Build a Curved Wire Structure Under a Surface](#-baby-step-10--build-a-curved-wire-structure-under-a-surface)
11. [Flatten and Arrange Curve Shapes for Fabrication](#-baby-step-11--flatten-and-arrange-curve-shapes-for-fabrication)
12. [Arrange Disconnected Parts as Puzzle Pieces](#-baby-step-12--arrange-disconnected-parts-as-puzzle-pieces)
13. [Create and Label Flat Panels with Python](#-baby-step-13--create-and-label-flat-panels-with-python)

---

## 🧱 Baby Step 1 — Tessellate a Sphere Using Triangles and Squares

This step demonstrates how to create a tessellated sphere that combines triangles and squares to resemble a sculptural tile layout. The goal is to learn face selection, subdivision, face deletion, and smoothing.

### Step-by-step

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

---

(Expanded content for each baby step continues below.)

## 🔷 Baby Step 2 — Create a Hollow Wire Mesh Sphere

This step shows how to convert a standard UV sphere into a hollow mesh structure using the Wireframe modifier. This is ideal for creating sculpture components with open geometry.

### Step-by-step

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

---
