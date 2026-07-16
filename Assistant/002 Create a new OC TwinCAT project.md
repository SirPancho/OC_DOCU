
![[OC_Assistant_MainWindow.png]]

1. Open the **OC Assistant**
2. click the button *create*
3. Select the path for the twincat project
4. click *OK*

![[OC_TC_Project_created_with_assistant.png]]

When the assistant finishes the creation of the project, it will automatically open the TwinCAT Engineering IDE with the created solution. Inside the solution will be only a PLC project

![[Initial OC TwinCAT project created.png]]

## Configuration the Real-Time settings in TwinCAT for running in a PC

## Synchronize Unity project tree with TwinCAT project tree

Before synchronizeing both projects it is required that the OC Assistant is running and connected to the OC TwinCAT solution.

The TwinCAT runtime has to be in STOP and the Unity project has to be in EDITOR mode

1. Select the *Project* object
2. In the *Tc Ads Client* component click the button **Create Configuration**. This will create a *.xml* file with the hierarchy of stations and devices from Unity

![[Button_create_TC_project_configuration_xml.png]]

![[Unity_project_tree.png]]

3. Click the button **Update TwinCAT Project** to start the synchronization

![[Button_Update_TC_project.png]]

In the Twincat project will appear a structure of folders and function blocks similar to the hierarchy in Unity

![[TwinCAT_project_tree.png]]