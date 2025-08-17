Texture Types
============

ATA recognizes and processes the following texture types based on their filenames:

Base Color / Albedo
------------------
**Keywords**: albedo, basecolor, diffuse, color, base_color, base color

The main color texture for your material. In physically-based rendering, this represents diffuse reflection without any lighting information.

Normal Maps
----------
**Keywords**: normal, norm, nrm, normalmap, normal map

Normal maps provide surface detail by encoding direction information. ATA automatically marks these as normal maps in Unity and enables normal mapping on your materials.

Metallic
-------
**Keywords**: metallic, metal, metalness

Defines which parts of the surface are metallic (white) versus non-metallic (black). Used in physically-based rendering for reflection calculations.

Roughness
--------
**Keywords**: roughness, rough

Defines the microsurface detail of the material. Rough surfaces (white) scatter reflected light, while smooth surfaces (black) have clearer reflections. ATA automatically inverts this to create smoothness maps when needed.

Smoothness
---------
**Keywords**: smoothness, smooth

The inverse of roughness. Smooth surfaces (white) have clear reflections, while rough surfaces (black) scatter reflected light.

Ambient Occlusion
---------------
**Keywords**: ao, ambientocclusion, ambient_occlusion, occlusion

Represents how exposed each point on the surface is to ambient lighting. Used to add depth to crevices and joints.

Emission
-------
**Keywords**: emission, emissive, glow

Defines areas that emit light. ATA automatically enables emission on your materials when this texture is detected.

Height / Parallax
---------------
**Keywords**: height, displacement, parallax

Used for parallax mapping to create the illusion of depth on flat surfaces.

Alpha / Opacity
-------------
**Keywords**: opacity, transparency, alpha

Defines transparent areas of your material. ATA can combine this with your base color texture and set up the material for transparency.

Detail Mask
---------
**Keywords**: mask, detail_mask, detailmask

Controls where detail maps are applied on your material's surface.

Combined Formats
--------------
ATA also recognizes special combined texture formats:

* **Metallic-Roughness**: metallic[_-]?roughness, metal[_-]?rough, etc.
* **ORM Maps**: \\borm\\b, \\bmro\\b, occlusion[_-]?roughness[_-]?metallic
* **HDRP Mask Maps**: maskmap, mask[_-]?map
* **Albedo-Alpha**: albedo[_-]?alpha, basecolor[_-]?alpha, etc.
* **Specular-Gloss**: spec[_-]?gloss, specular[_-]?gloss

Adding Custom Keywords
--------------------
You can add your own custom keywords through the Settings window (Tools > Advanced Texture Assign Tool > Settings).