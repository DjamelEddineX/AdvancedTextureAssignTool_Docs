Features
========

Advanced Texture Assign Tool offers numerous features that streamline texture assignment in Unity:

Automatic Texture Matching
-------------------------
ATA automatically matches textures to materials by analyzing filenames. If your material is named "WoodFloor" and you have textures like "WoodFloor_Albedo.png" or "WoodFloor_Normal.png", the tool will find and assign them correctly.

Smart Map Processing
------------------

Roughness Inversion
^^^^^^^^^^^^^^^^^^
If your workflow requires a smoothness map (like Unity Standard) but you only have a roughness map, ATA automatically inverts the roughness texture to create a smoothness map.

Metallic-Smoothness Packing
^^^^^^^^^^^^^^^^^^^^^^^^^^
ATA combines metallic and smoothness into a single texture channel if your shader requires it (for example, Unity Standard and HDRP).

HDRP Mask Maps
^^^^^^^^^^^^^
Automatically creates HDRP Mask Maps with metallic (R), ambient occlusion (G), detail mask (B), and smoothness (A) channels properly packed together.

ORM Maps
^^^^^^^
Creates glTF-compatible ORM maps combining ambient occlusion (R), roughness (G), and metallic (B) channels.

Alpha Handling
------------
Can merge a separate alpha (opacity) map into your color texture for transparent materials, and automatically configures the material's blend mode.

Normal Map Fixing
---------------
Detects and marks normal maps properly so Unity recognizes them as such, and enables normal mapping on your materials.

Multiple Pipeline Support
-----------------------
Supports all major Unity rendering pipelines:

* Built-in Render Pipeline
* Universal Render Pipeline (URP)
* High Definition Render Pipeline (HDRP)
* Custom shaders (with standard property naming)

Batch Processing
--------------
Process multiple materials at once, either from your current selection or by picking a folder containing materials.

Custom Rules
----------
Add your own keywords through the Settings window to match specific naming conventions in your textures.

Revert Capability
---------------
Made a mistake? Easily revert to original textures with one click.