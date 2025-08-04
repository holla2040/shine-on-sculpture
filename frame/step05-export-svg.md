# 🧰 Baby Step 5 — Flatten and Export Surfaces as SVG

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
   - You'll see:
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