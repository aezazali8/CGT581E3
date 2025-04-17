Parametric Light Cover  README
This repository contains the Grasshopper definition and STL files for two parametric light cover models designed for 3D printing. The models are generated in Rhino using Grasshopper, with adjustable parameters to explore variations in curvature, segmentation, and texture.



How to Modify Parameters
Open the .gh file in Grasshopper and use the sliders provided in the definition to control the model's geometry.

1. Vertical Resolution (Number of Layers)
Slider Name: Number of Layers

Default Value: 150

Description: Controls how many circular cross-sections are stacked along the Z-axis. Higher values lead to smoother curvature; lower values create faster but coarser designs.

2. Circle Radius Range (Profile Curve)
Slider Names: Base Radius and Radius Multiplier

Default Values: 40 (base), 20 (multiplier)

Description: Adjusts the minimum and maximum radius of each horizontal slice. The result is a bulging or pinching effect toward the center.

3. Mathematical Function (Sine or Cosine)
Component: Math > Trig > Sine or Cosine

How to Change: Replace the sine function with cosine (or vice versa) to alter the side profile from convex to concave or symmetric forms.

4. Number of Segments per Circle
Slider Name: Number of Segments

Default Values: 30 (Model 1), 50 (Model 2)

Description: Determines how many line segments each circular layer has. Higher values produce smoother curves; lower values make the design more faceted.

5. Offset Depth (Extrusion Control)
Slider Name: Offset Amount

Default Value: 5

Description: Controls how far each curve segment is offset before forming the final surface. This gives the lamp its thickness and texture pattern.

6. Height of the Lamp
Indirectly Controlled By: Number of Layers + Z Step

Description: The product of total layers and the Z-step defines overall height. You can adjust the Z-step inside the Series component (Step Size).

How to Export for 3D Printing
Use the Bake function in Grasshopper once your model is finalized.

In Rhino, select the baked geometry and use Mesh > Mesh From NURBS Object if needed.

Export as .stl using File > Export Selected, and select STL (Stereolithography).

Make sure your final geometry is a closed mesh suitable for FDM 3D printing. You can check this in Rhino using the Check command.

