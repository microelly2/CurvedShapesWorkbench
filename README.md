# Curved Shapes
FreeCAD Workbench for creating 3D shapes from 2D curves
  
## Installation

- go in your personal FreeCAD folder ( usually ~/.FreeCAD on Linux )
- cd Mod ( or create this folder if it doesn't exist )
- git clone https://github.com/chbergmann/CurvedShapesWorkbench.git
- start FreeCAD

"Curved Shapes" workbench should now show up in the workbench dropdown list.
  
## Tools
### ![](./Resources/icons/curvedArray.svg) Curved Array
Creates an array and resizes the items in the bounds of one or more hull curves.
In this example, the orange base shape is rescaled in the bounds of the red and violet hullcurves. The curves do not have to be connected.  
The hullcurves should lie on or parralel to the XY- XZ- or YZ- plane.  

![WingExample](Examples/WingExample.png)

##### Parameters
- Base: The object to make an array from
- Hullcurves: List of one or more bounding curves        
- Axis: Direction axis of the Base shape
- Items: Nr. of array items
- OffsetStart: Offset of the first part in Axis direction
- OffsetEnd: Offset of the last part from the end in opposite Axis direction
- Twist: Applies a rotation around Axis to the array items. 
- Surface: make a surface over the array items
- Solid: make a solid if Base is a closed shape

##### Resolve a CurvedArray item to a compound of single objects
Go to the Part workbench. In the Part menu, select Compound -> Explode compound  

### ![](./Resources/icons/curvedSegment.svg) Curved Segment
Interpolates between two 2D curves.
 
![CurvedSegment](Examples/CurvedSegment.jpg)
![CurvedSegment2](Examples/CurvedSegment2.jpg)

##### Parameters
- Shape1: The first object of the segment
- Shape2: The last object of the segment
- Hullcurves: List of one or more bounding curves (optional)       
- NormalShape1: Direction axis of Shape1 (auto computed)
- NormalShape2: Direction axis of Shape2 (auto computed)
- Items: Nr. of items between the segments
- makeSurface: make a surface over the array items
- makeSolid: make a solid if Base is a closed shape
- InterpolationPoints: Unequal edges will be splitted into this number of points

### ![](./Resources/icons/CornerShape.svg) Interpolated Middle
Interpolates a 2D shape into the middle between two 2D curves. The base shapes can be connected to a shape with a sharp corner.

![InterpolatedMiddle2](Examples/InterpolatedMiddle2.jpg)
![InterpolatedMiddle](Examples/InterpolatedMiddle.jpg)
 
##### Parameters
- Shape1: The first object of the segment
- Shape2: The last object of the segment     
- NormalShape1: Direction axis of Shape1 (auto computed)
- NormalShape2: Direction axis of Shape2 (auto computed)
- makeSurface: connect Sape1 and Shape 2 with the interpolated middle
- makeSolid: make a solid if Shape1 and Shape2 are closed shapes
- InterpolationPoints: Unequal edges will be splitted into this number of points

### ![](./Resources/icons/Horten_HIX.svg) Horten H IX
This is an example design for testing and presentation of this workbench.  
It is a python script that creates the shape of the [Horten H IX](https://de.wikipedia.org/wiki/Horten_H_IX), a stealth fighter that has been build in Germany in 1944.

## Discussion
[https://forum.freecadweb.org/viewtopic.php?f=8&t=36989](https://forum.freecadweb.org/viewtopic.php?f=8&t=36989)
