# Description 

Creating external geometry constraints in cross space

# Preparation

Enable "Sync placement"

# Creating 

### Part Workbench
Add a `Part` to the root (the yellow stairway icon)
Create all sub-shape binders (Binders), move into the PartBody 
Click the appropriate face of any Binder, use Sketcher->Flat Face, close
Drag and drop the Sketch into the Part
Double click the Sketch to edit
Use "External Geometry" tool to teleport constraints from outside geometry through the Binder(s)
Draw the projection for your desired geometry, close 
"Extrude" the sketch (possibly you may want to use "symmetric" option if this will be used as a virtual cutter) 
Drag and drop the `Extrude` into the `Part` container
Move the `Part` into the Assembly container

### PartDesign Workbench
Add a Body to the root (the blue stairway icon)
Drag and drop the Body into the Assembly container (or you'll get Cyclic Dependency error in the end)
Double click the Body to activate it 
Single click any object to create a sub-shape binder for that, and click "sub-shape binder" button. Binders will go into the Body automatically.
Make visible and click the appropriate face of any binder, click Sketch to create a sketch
Use "External Geometry" tool to teleport the remote constraints
Draw the projection of your desired geometry, close 
Select the Sketch (it should be already selected), click Pad to generate the solid
Switch to Assembly3 WB, move or set some constraints to locate.

# Updating 
double click PartBody/Extrude/Sketch
arrange the visibility for the binders
edit the projection

# Using 

Create a sub-shape binder of PartBody/Extrude (not PartBody itself) within the upper Assembly container 
Use this Binder as Tool for a Cut operation
