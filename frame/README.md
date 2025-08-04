# Blender Baby Steps: Independent Tutorials for Sculpture Projects

## 📝 Project Summary

This repository contains a series of **independent, self-contained Blender tutorials** designed for a true beginner creating physical sculptures. 
Each tutorial walks through a small, concrete Blender modeling task — such as flattening a mesh to SVG, 
engraving labels, simulating print layers, or scripting geometry with Python.

These baby steps are intended to help build components for a **physical sculpture project** with fabrication-ready outputs for laser cutting, wire bending, and assembly. Each step can be run standalone. 
There is no dependency between steps — they are meant to be **learn-by-example snapshots** covering key Blender techniques for sculpture fabrication.

This documentation was developed collaboratively using ChatGPT and refined iteratively to ensure:
- Realistic beginner workflows using Blender 4.5 LTS or later
- Clean, linear instructions for each operation
- Reusable, versioned Markdown files with one step per file

The repository structure includes:
- A top-level `README.md` with this project summary and Table of Contents
- A `blender_baby_steps/` folder with individual `.md` files for each tutorial step

Each tutorial can be printed, tracked, or edited individually to suit the needs of your sculpture fabrication or design workflow.

---

## 🎨 Sculpture Workflow Concept

Based on exploration with ChatGPT, this project supports a complete workflow for creating physical sculptures from 3D designs:

1. **3D Surface Design**: Start with any 3D shape in Blender (e.g., a blanket draped over a chair)
2. **Tessellation**: Break the surface into discrete flat squares and triangles with controllable sizing
3. **Wire Mesh Support**: Generate curved wire structures underneath following layer lines (like 3D printer layers)
4. **Fabrication Outputs**: Export everything for physical construction:
   - SVG files for laser cutting flat panels
   - Wire lengths and projection patterns for bending
   - Assembly guides with numbered pieces

## 🔧 Workflow Overview

The conversation with ChatGPT revealed several key capabilities needed for sculpture fabrication:

### Surface Processing
- **Tessellation Control**: Specify maximum size of squares and triangles
- **Planar Flattening**: Ensure tessellated pieces are truly flat (not curved like "Pringles")
- **Edge Splitting**: Separate pieces so they're individual elements with controllable spacing
- **Smart Labeling**: Etch ID numbers on pieces for assembly reference

### Wire Mesh Generation
- **Layer Line Approach**: Create wire mesh following 3D printer-style layer lines with specific spacing
- **Curve Preservation**: Maintain smooth curves rather than angular segments
- **Length Calculation**: Get exact wire lengths for cutting before bending
- **Projection Mapping**: Project wire patterns downward for manual bending guides

### Automation & Export
- **Python Scripting**: Automate the entire export process with a single script
- **SVG Generation**: Export flat pieces arranged for efficient laser cutting
- **Assembly Documentation**: Generate visual guides showing piece placement
- **Batch Processing**: Handle hundreds of pieces with automatic numbering

## 🏭 Fabrication Pipeline

The complete workflow from 3D design to physical sculpture:

1. **Design Phase**
   - Create or import 3D surface in Blender
   - Test with simple shapes (parabola/dome recommended for beginners)

2. **Surface Preparation**
   - Apply tessellation with size constraints
   - Flatten any curved faces to true planes
   - Split into individual objects
   - Scale down slightly for spacing/tolerances

3. **Wire Frame Creation**
   - Generate layer lines at specified intervals
   - Convert to curves with proper thickness
   - Calculate lengths for material preparation
   - Create projection layouts

4. **Export & Fabrication**
   - Run Python script to export all components
   - Laser cut numbered flat pieces
   - Project and bend wires to shape
   - Weld wire frame structure

5. **Assembly**
   - Use numbered pieces as 3D puzzle
   - Reference assembly guide/map
   - Weld pieces to wire frame in order

---


Each tutorial below is **fully self-contained**, designed for a **Blender novice**, and written using Blender 4.5 LTS+.

## 📚 Table of Contents

- [Tessellate a Sphere Using Triangles and Squares](step01-tessellate-sphere.md)
- [Create a Hollow Wire Mesh Sphere](step02-wire-mesh-sphere.md)
- [Break a Cube Into Separate Flat Panels](step03-separate-cube-panels.md)
- [Add Number Labels to Objects Using Text](step04-text-labels.md)
- [Flatten and Export Surfaces as SVG](step05-export-svg.md)
- [Engrave Labels into Mesh with a Boolean Modifier](step06-boolean-engrave.md)
- [Simulate Layer Lines with Sliced Geometry](step07-layer-lines.md)
- [Measure the Length of a Curve](step08-measure-curve.md)
- [Add Spacing Between Tessellated Panels](step09-tile-spacing.md)
- [Build a Curved Wire Structure Under a Surface](step10-curve-under-surface.md)
- [Flatten and Arrange Curve Shapes for Fabrication](step11-flatten-curves.md)
- [Arrange Disconnected Parts as Puzzle Pieces](step12-arrange-pieces.md)
- [Create and Label Flat Panels with Python](step13-python-tile-labels.md)