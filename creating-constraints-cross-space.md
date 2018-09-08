# Description 

Creating external geometry constraints in cross space

# Preparation

Enable "Sync placement"

# Creating 

### Part Workbench
Add a Part (Part001) to the root (the yellow stairway icon)
Create all sub-shape binders (Binders) (may go to any active "Body"), move them into the Part001 (move between containers one by one to keep the Placement in sync (for now))
Click the appropriate face of any Binder, use Sketcher->Flat Face, close
Drag and drop the Sketch001 into the Part001
Double click the Sketch001 to edit
Use "External Geometry" tool to teleport constraints from outside geometry through the Binder(s)
Draw the projection for your desired geometry, close 
"Extrude" the sketch (under Part WB) (possibly you may want to use "symmetric" option if this will be used as a virtual cutter) 
Drag and drop the Extrude001 into the Part001 container
Move the Part001 into the Assembly container (one by one, again)
(Use the "Extrude001" as cutter and not the Part001, if it would be used as a cutter)

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
