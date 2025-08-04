# 🪟 Baby Step 9 — Add Spacing Between Tessellated Panels

This step demonstrates how to space apart previously joined or tessellated panels. It's helpful for exploded views, printing separations, or physically cutting/scoring designs.

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