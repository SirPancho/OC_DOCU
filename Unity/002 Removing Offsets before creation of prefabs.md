Original mesh with offset from origin and still with position as (0,0,0)

![[imported_mesh_with_offset_from_origin.png]]

1. Create an empty object in the main Scene palced at the origin of the scene

![[create_temprary_game_object.png]]

2. Manually move the game object to the desired origin of the meshes to reorganize. Rotate the origin of the game object if needed in order to align properly the origin with the meshes.

![[Recentering_the_temporary_gameobject.png]]

3. Create a child object in the temporary game object with the name of the *prefab* (will be useful in later steps) and an additional child object *geometry* for allocating the meshes.

![[create_child_game_objects_in_the_temporary_game_object.png]]

4. Select the desired meshes and drag them to the *geometry* child object

![[add_meshes_to_the_geometry_child_object.png]]

5. Verify that the child object with the *prefab* name has a position (0,0,0). Prefabs need to have a null point as origin. Then drag the *prefab* object to the **prefab folder** in the project window.

![[drag_the_game_object_into_prefabs_folder.png]]

6. Open the prefab object directly from the prefab folder and verify that the meshes do not have any offset.  If the prefab looks correct close the prefab editor.

![[origin_of_a_prefab.png]]

7. In the main scene drag the prefab element out of the temporary game object into the main scene level. (Basically out of the temporary parent) This will make unity to recalculate the offset for the whole *prefab* but not for the meshes. 

![[drag_out_the_prefab_from_the_temporary_object.png]]

8. Delete the empty temporary game object from the main scene.
