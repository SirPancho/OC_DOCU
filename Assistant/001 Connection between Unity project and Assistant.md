

# General Scene configuration

![[create_project_object_in_scene.png]]

![[unity_tc_client_connection_settings.png]]

![[Pasted image 20260715132621.png]]

![[unity_console_confirmation_configuration_update.png]]

# Game objects hierarchy settings

In order to stablish the same hierarchy of function blocks in the TwinCAT project as in the Unity project it is necessary to check the Box *Is Name Sampler* in the inspection window of the parent game object in unity. If the checkbox is not active all the function blocks in Twincat will have the name of the parent as part of the name **Parent.Child_Element_FB**, this can lead to having FBs in TwinCAT with very large names and can cause problems when calling or instanciating the functions.

![[Pasted image 20260715132648.png]]

![[Pasted image 20260715132655.png]]

**View of the configuration xml for the creation of the function blocks in TwinCAT**

![[Project_configration_xml.png]]

![[Pasted image 20260715132713.png]]