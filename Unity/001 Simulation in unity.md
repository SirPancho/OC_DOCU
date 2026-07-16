
# Set up of the unity project

1. Create a new Unity project
2. Select the rendering Engine **URP**
3. Install dependencies for the Unity project
	1. Copy the dependencies from the GitHub repository *OpenCommissioning/OC_Unity_Core*
	2. Open the manifest.json of the project *../Unity_Project/Packages/manifest.json*
	3. Paste the dependencies into the manifest file
	4. Copy the link for the unity package of OC also from the GitHub repository
	5. Paste the link into the manifest file
	6. Save the changes in the file and close

![[Pasted image 20260715132002.png]]

4. Apply default layers for the simulation
	1. Go to the OpenCommissioning Tab
	2. Settings
	3. Apply Default layers
5. Go to project settings
	1. Player
	2. Check the box *run in background*

![[Project settings player configuration.png]]

# Create the project configuration for OC

1. Create a game object with the name **Project**
![[Project_gameobject_as_parent_of_OC_simulation.png]]
2. In the *Inspector window* add the **Tc Ads Client** element
![[InspectorWindow_Project_TcAdsClient.png]]