# contourToSurface
this is an example of class vtkVoxelContoursToSurfaceFilter
create surface from contours vtkVoxelContoursToSurfaceFilter is a filter that takes contours and produces surfaces. 
There are some restrictions for the contours: 
 The contours are input as vtkPolyData, with the contours being polys in the vtkPolyData. 
 The contours lie on XY planes - each contour has a constant Z 
 The contours are ordered in the polys of the vtkPolyData such that all contours on the first (lowest) XY plane are first, then continuing in order of increasing Z value. 
The X, Y and Z coordinates are all integer values. 
 The desired sampling of the contour data is 1x1x1 - Aspect can be used to control the aspect ratio in the output polygonal dataset. 
 This filter takes the contours and produces a structured points dataset of signed floating point number indicating distance from a contour. 
 A contouring filter is then applied to generate 3D surfaces from a stack of 2D contour distance slices. 
 This is done in a streaming fashion so as not to use to much memory.
