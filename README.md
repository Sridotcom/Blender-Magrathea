# Blender-Magrathea - 3D Planet Builder
Completed by: Srivishal Sudharsan <br>
Mentored By: Dr. David Rice (Post Doctoral Researcher at The Open University of Israel)

## What does Blender-Magrathea do?
Blender-Magrathea is a useful resource for researchers to visualize planets in a scientifically accurate manner, and present them to the public. <br>

Given the internal properties of a planet (namely the radii, phases of matter, and densities of its N layers) Blender-Magrathea will automatically create a cross-sectional 3D model of the planet. <br>

The layers of the planets are textured according to the type of material (ice, water, iron, silicon, etc.) They can also be colored by [density](https://github.com/Sridotcom/Blender-Magrathea/blob/bfc01bba2d67828b14456e416e70073423a341d3/Density.py), to better understand how different phases of matter or materials can affect planet density. <br>

The code currently supports [Magrathea](https://github.com/DavidRRice/Magrathea) output files, which take in the mass of the various layers of a planet (core, mantle, hydrosphere, and atmosphere) and return the pressure, temperature, density, and phase of the planet at various radii. Example outputs of planets modelled by phase and density are shown below.


| Phase model                            | Density model                            |
| ----------------------------------- | ----------------------------------- |
| ![phase](planet443%235.png) | ![density](https://github.com/Sridotcom/Blender-Magrathea/assets/66920443/7f6bd83e-fc86-4901-9853-8f26ac6a374c)(width="200" height="100") |


## Step by Step Instructions
1. Download Blender: https://www.blender.org/download/
2. Once Open - under New File press General
3. In the top bar select Scripting
4. At the top of the new pop-up window select New - this will create a new Text window
5. Copy and paste code from Blender_Code.py into this new text window
6. Grab the file path of the Magrathea output file. Instructions to do that are here: https://www.sony.com/electronics/support/articles/00015251
7. On line 17 Replace text inside of the file_name variable (only replace the text in between the quotation marks) with the file path of the desired Magrathea output file
8. Press the Run Script button at the top right of the Text/Code window
9. In the top bar press "Layout"
10. In the top right (Viewport Shading options) select the 3rd sphere which should look like a sphere that is partially shaded in 
11. The interior of the planet should be complete now!


## How to change how a material looks
If you don't like the way a layer looks then select it in the "Layout" tab. Click on the sphere that you want to change and it will be outlined in yellow. Alternatively, you can select a sphere via the 'Scene Collecction" section in the top right. Once a sphere is selected, click on the "Shading" tab in the top toolbar. On the bottom window ensure that "Use Nodes" is checked. Now you should see the Node Setup (bottom window) for the selected material (top window). Each box represents a node and they each code for an aspect of the material. 

If you want to alter the way the material looks you can simply click on a factor in one of the nodes such as Roughness, Sheen, Scale, etc, and enter a new number. It will get updated in the top window. To make more drastic changes you can also add new nodes via the "Add" button in the top left of the bottom window. This video provides a good introduction to nodes and how to alter materials using them: https://www.youtube.com/watch?v=moKFSMJwpmE&ab_channel=GrantAbbitt. This link gives an overview on what each node does: https://docs.blender.org/manual/en/latest/render/shader_nodes/index.html.

The above steps will show you how to change nodes manually (it will not save if you run the program again). If you would like to change a material programmatically (permanent) then press the "Scripting" tab in the top toolbar. Scroll down to lines 144 - 428. Each block of code here is coding for a different material in the "Shading" tab. To alter a specific material, scroll down till you find the block of code with the title of the desired material. Altering the nodes now varies a lot with what your trying to do but the existing code should give some sort of direction. To create new nodes use the nodes.new(Node Name) function. The Node Name can be found by searching up "Desired Node Blender Python name". To make more changes, reference Stack Overflow and Blender Artists, which both are very helpful for altering nodes.

If you have any questions or problems with the code please feel free to reach out via email at Srivishal123@gmail.com or david.rice@unlv.edu!
