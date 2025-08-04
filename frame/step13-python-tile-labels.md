# 🐍 Baby Step 13 — Create and Label Flat Panels with Python

This step demonstrates how to use Blender's built-in Python scripting to automatically generate flat panels and label them. It is useful for automating repetitive modeling tasks or integrating procedural elements.

### Step-by-step

1. **Open the Scripting workspace**:
   - At the top of Blender, click **Scripting**.
   - You'll see the Text Editor and Python Console.

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
   - You'll see 6 flat planes with number labels appear.

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