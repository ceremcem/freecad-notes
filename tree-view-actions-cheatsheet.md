# TreeView Actions

![treeview actions context menu](https://user-images.githubusercontent.com/1207888/62813097-95ab3200-bb3b-11e9-8e2c-c939cff3e691.png)

# Cheatsheet

* **Sync view**: 
  * Description: Auto switch to the 3D view containing the selected item.
  * Shortcut: `T, 1`
  * When to disable: 
    * If a module (eg. TechDraw) wants you to to select an object in the tree view and then press a button (eg. TechDraw's "Insert multiple linked views of drawable object(s)" button), you *might* want to disable. **However there is a tip**: First select the object you want to "Insert its linked view", then click `Ctrl` key, then click your TechDraw instance. Last selection will switch to TechDraw view, so you can click "Insert multiple linked views..." button without disabling this feature. 

* **Sync selection**:
  * Description: Auto expand tree item when the corresponding object is selected in 3D view.
  * Shortcut: `T, 2`
  * When to disable: 
    * While fixing multiple broken `Element`s: 
      * `1.` Disable *Sync selection*
      * `2.` Click on the erroneous `Element`
      * `3.` A yellow "shadow" will appear in 3D view 
      * `4.` Make a good guess of relevant geometry and click to select it. 
      * `5.` Hover on your `Element` 
      * `6.` Type `T, D` and then "Click" to update element link. 
      * `>` Go to step 2 until there is no broken `Element` left. 
      * `7.` Enable *Sync selection*

* **Sync placement**:
  * Description: Auto adjust placement on drag and drop objects across coordinate systems.
  * Shortcut: `T, 3`
  * When to disable: 
    * Disable if you encounter an interference with a container object that implements its own placement management.
* **Pre-selection**:
  * Description: Pre-select the object in 3D view when mouse over the tree item.
  * Shortcut: `T, 4`
  * How to use: 
    * Hover an object on tree view. 
    * See the object is highlighted with yellow color and brought to the front in the 3D view so you can easily locate the object.
  * When to disable: 
    * `Pre-selection` may cause slow down when dealing with very large model. When graphics memory is not enough, the slowdown will be very noticable.
    
* **Record Selection**:
  * Description: Record selection in tree view in order to go back/forward using navigation button.
  * Shortcut: `T, 5`
  * How to use:
    * `1.` Switch to `Assembly 3` Workbench 
    * `2.` Use the navigation buttons ([<- ->](https://user-images.githubusercontent.com/6639874/62826720-ffbde880-bbc8-11e9-8a7a-a4a22799c46c.png)) to switch back and forth between your last selections. 
  * When to disable: 
    * Can be temporarily disabled to make the last selection as an anchor to jump back, while ignoring any follow up selection.
