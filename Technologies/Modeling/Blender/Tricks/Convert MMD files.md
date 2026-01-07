To convert [[MMD]] 3D models into different models with [[Blender]], it's mandatory the [MMD Tools — Blender Extensions](https://extensions.blender.org/add-ons/mmd-tools/).

After applying this extension in [[Blender]], you can paste your [[MMD]] file in [[Blender]], the file will be with all the correct textures applied.

Before exporting the [[MMD]] file in other file type, it's necessary to access the `Shading` tab
![[blender_shading.png]]

In shading tab, the [[MMD]] Base Text is connected with MMDShaderDev, if you export right now the file textures will be lost, then, it's necessary that you connect the following points:

MMD Base Tex.Color => Principled BSDF.Base Color
MMD Base Tex.Alpha => Principled BSDF.Alpha
Principled BSDF.Shader => Material Output.Surface