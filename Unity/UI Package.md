# Open Commissioning UI package

Package source: [https://github.com/OpenCommissioning/OC_Unity_UI.git](https://github.com/OpenCommissioning/OC_Unity_UI.git)

## 1. Install the package

1. Open **Window → Package Manager**
2. Install **Open Commissioning UI** from Git (`com.open-commissioning.ui`)
3. Confirm the package is listed under **Packages - SpiraTec AG**

![[AdobeExpressPhotos_906bd35fe0a94d83a7806c36ff0e6d56_CopyEdited.png]]
*Package Manager: Open Commissioning UI installed from the Git URL (`…/OC_Unity_UI.git#upm`).*

## 2. Add the UI prefabs to the scene

1. In the Project window, go to **Packages → Open Commissioning UI → Runtime → Prefabs**
2. Drag the required prefabs into the Hierarchy (at least **Interactions** and **Virtual Camera**; typically also **AppUI** / **Main Camera**)

![[Pasted image 20260717084456.png]]
*Prefab location under the package; Interactions and Virtual Camera in the scene Hierarchy.*

## 3. Make a geometry object interactive

1. Select the target geometry GameObject in the Hierarchy
2. In the Inspector, click **Add Component**
3. Search for **Interaction** and add the script

![[Pasted image 20260717115414.png]]
*Add Component → search “Interaction” on the Geometry object.*

4. Once added, also a **Box Collider** and an **Outline** component are added.

![[Pasted image 20260717115602.png]]
*Box Collider (trigger) + Interaction + Outline linked to the Interaction.*

6. Under **Interaction → Settings**, set **Mode** to **Selection, Hover** (or **Click** for 3D Buttons)

![[Pasted image 20260717115724.png]]
*Interaction Mode set to Selection, Hover.*

## 4. Register panel handlers

1. Select **DefaultPanels** under **Interactions / AppUI → PanelsManager**
2. Add the panel handler scripts your project needs (e.g. **Panel Handler Flexo Rf Tool Bay**)

![[Pasted image 20260717143614.png]]
*DefaultPanels with multiple Panel Handler scripts; Flexo Rf Tool Bay highlighted.*

3. Select **PanelsManager** and open the **Panel Manager** component
4. Extend the **Panel Handlers** list with **+** if you need extra slots

![[Pasted image 20260717144043.png]]
*Panel Manager list size and +/− controls to add handler slots.*

5. Right-click the **Panel Manager** header → **FindPanelsInChildren** to auto-fill the list from child handlers

![[Pasted image 20260717144146.png]]
*Context menu: FindPanelsInChildren fills the Panel Handlers list.*
