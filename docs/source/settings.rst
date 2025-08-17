Settings
========

ATA provides various settings to customize its behavior according to your workflow:

Processing Options
----------------

Fix Normal Maps
^^^^^^^^^^^^^
When enabled, ATA will automatically mark textures identified as normal maps with the correct import settings in Unity.

Preserve Original Textures
^^^^^^^^^^^^^^^^^^^^^^^^
Keep the original textures after processing. When disabled, temporary processed textures will be deleted.

Create ORM Map
^^^^^^^^^^^^
Generate glTF-style ORM maps (Occlusion-Roughness-Metallic) when possible.

Smart Combination Detection
^^^^^^^^^^^^^^^^^^^^^^^^
Use advanced pattern matching to detect combined texture formats from filenames.

Delete Processed Textures
^^^^^^^^^^^^^^^^^^^^^^
Remove temporary processed textures after they're used. Helps keep your project clean.

Verbose Logging
^^^^^^^^^^^^^
Show detailed logs in the console about the texture processing steps.

Advanced Options
--------------

Combine Alpha with Diffuse
^^^^^^^^^^^^^^^^^^^^^^^
Merge separate alpha/opacity textures into base color textures for materials that need transparency.

Invert Roughness
^^^^^^^^^^^^^
Automatically convert roughness textures to smoothness by inverting their values. Essential for Unity's Standard shader which uses smoothness.

Pack Metalness/Roughness
^^^^^^^^^^^^^^^^^^^^^
Combine metallic and smoothness/roughness textures into single maps using the correct channels.

Create HDRP Mask Map
^^^^^^^^^^^^^^^^^
Generate HDRP-compatible mask maps that combine metallic, ambient occlusion, detail mask, and smoothness.

Use Alpha As Mask
^^^^^^^^^^^^^^^
When a standalone alpha texture is found but no mask texture, use the alpha texture as a mask.

Visualize Metallic Maps
^^^^^^^^^^^^^^^^^^^^
Make metallic maps more visually apparent by applying their values to all RGB channels instead of just the R channel.

Custom Keyword Mappings
--------------------
You can define your own keywords for texture identification through the Settings window (Tools > Advanced Texture Assign Tool > Settings). This allows you to match your studio's specific naming conventions.

Each mapping consists of:

* **Keyword**: The term to look for in texture filenames
* **Shader Property**: The Unity shader property to assign matching textures to