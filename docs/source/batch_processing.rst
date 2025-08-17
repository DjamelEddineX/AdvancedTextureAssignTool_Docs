Batch Processing
==============

ATA offers powerful batch processing capabilities to handle multiple materials at once.

Method 1: Processing Selected Materials
-------------------------------------
1. Select multiple objects in your scene that use different materials
2. Open ATA (Tools > Advanced Texture Assign Tool > Window)
3. Click "Get Materials" to add all materials from selected objects
4. Set your texture folder and processing options
5. Click "Assign Textures"

All materials will be processed in sequence, with progress displayed in the Unity Editor.

Method 2: Batch Processing From Folders
-------------------------------------
For processing many materials without having to select objects in your scene:

1. Organize your materials in a folder
2. Organize your textures in another folder (ideally with naming that matches your materials)
3. Open ATA (Tools > Advanced Texture Assign Tool > Window)
4. Click "Batch Assign"
5. Select your materials folder when prompted
6. Select your textures folder when prompted

ATA will process all materials in the folder, attempting to match them with textures based on name.

Tips for Efficient Batch Processing
---------------------------------
* **Consistent Naming**: Use consistent naming conventions for both materials and textures
* **Folder Organization**: Keep related textures in the same folder as their materials
* **Check Console**: Enable "Verbose Logging" to see detailed information about the batch process
* **Start Small**: Test with a few materials first before processing your entire project

Working with Material Variants
----------------------------
If you have multiple variants of the same material:

1. Ensure each variant has a unique name
2. Name your textures with the specific variant name
3. Use batch processing to set up all variants at once

For example, if you have "Wood_Dark" and "Wood_Light" materials, name your textures "Wood_Dark_Albedo" and "Wood_Light_Albedo" accordingly.