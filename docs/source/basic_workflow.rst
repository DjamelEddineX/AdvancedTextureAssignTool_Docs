Basic Workflow
=============

This tutorial covers the standard workflow for using ATA to assign textures to materials.

Preparing Your Textures
---------------------
For best results, name your textures using standard naming conventions:

* ``MaterialName_Albedo.png`` or ``MaterialName_BaseColor.png`` for color textures
* ``MaterialName_Normal.png`` for normal maps
* ``MaterialName_Metallic.png`` for metallic maps
* ``MaterialName_Roughness.png`` for roughness maps
* etc.

Step 1: Open the Tool
-------------------
Navigate to Tools > Advanced Texture Assign Tool > Window to open the main interface.

Step 2: Add Materials
-------------------
There are several ways to add materials to the tool:

* Select objects in your scene and click "Get Materials" to add all materials from the selection
* Drag and drop materials directly from your Project window into the tool
* Use "Batch Assign" to process all materials in a folder

Step 3: Set Texture Source
------------------------
Click the folder icon next to the Texture Folder field and select the folder containing your textures.

Step 4: Configure Options
-----------------------
Set your desired processing options:

* Enable "Fix Normal Maps" to automatically mark normal maps correctly
* Enable "Create ORM Map" if you need ORM maps
* Enable "Smart Combination Detection" to detect special texture formats

Step 5: Process Materials
-----------------------
Click "Assign Textures" to process all materials in the list.

The tool will:
1. Scan your texture folder for matching textures
2. Process and convert textures as needed
3. Assign textures to the correct shader properties
4. Configure material settings appropriately

Step 6: Review Results
--------------------
After processing, your materials should have all textures properly assigned. You can:

* Use "Revert Selected" to undo changes to specific materials
* Use "Revert All" to undo all changes
* Use "Clear Textures" to remove all textures from materials

Dealing with Special Cases
------------------------
* **Roughness vs. Smoothness**: If you have roughness maps but your shader uses smoothness, ATA will automatically convert them
* **Alpha Textures**: If you have separate opacity maps, ATA can combine them with your color textures
* **Combined Maps**: For special formats like ORM or HDRP Mask Maps, enable the corresponding options