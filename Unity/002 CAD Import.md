
The CAD files to be used in the unity project must be in *.fbx*  or *.obj* format, if the construction files are developed in other CAD environment, they need to be converted first either in the CAD Software of with additional Software tools like **Pixys**, **Blender**, etc.

1. Move the *.fbx || .obj* files to the project under the folder Assets/CAD data
2. Create a new folder *Assets/Prefabs* to store the Prefabs required in the project
3. Drag the CAD file into the project scene
4. Create a new Prefab from the CAD file added to the Scene

## Definition of the Geometry hierarchy inside a game object

For an easy organization of simulation objects, it is always recommended to rearrange the 3D meshes of the imported CAD file, in this way it is better to identify all the corresponding sub elements of an object.

1. From the imported CAD geometry create a new prefab
	1. Select the object in the project tree
	2. Go to Prefab
	3. Select Unpack all
	4. Drag the Geometry from the Project tree into the Prefabs folder
2. Edit the Prefab of the geometry
3. In the Project tree create new sub elements
	1. Geometry
	2. Transport
	3. MA_Drive
4. Move all the geometry elements under the Geometry element

![[Pasted image 20260715132047.png]]
