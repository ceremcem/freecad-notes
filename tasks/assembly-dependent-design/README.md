# Assembly Dependent Design

> a.k.a "[Modeling using assembly](https://github.com/realthunder/FreeCAD_assembly3/wiki/Modeling-using-Assembly)"

Workflow is as follows: 

1. You have a stock `Part` (eg. [3006 trimpot](./3006-trimpot.png)).
2. You need to make some arrangements to mount it in a place inside *Parent_part*: 
    1. Mark the appropriate pin holes on the `circuit board` (= Assembly Dependent Boolean Operation).
    2. Cut a round hole within the `front panel`, 
        1. Either with a *predefined cutting tool* within the assembled `Part`. (same as previous operation)
        2. Or a custom shape (*cutter*) which will be designed within the *Parent_part*. This *cutter* will use constraints from the assembled `Part` (= Assembly Dependent Part Design).
3. After making those operations, 
    1. Part can be moved, so the dependent operations should follow the changes (= Move Test)
    2. Part itself might be modified, so the results should track those changes. (= Modify Test)

# Example

In the following model, I'm going to cut the `circuit_board` with the *yellow part* (the device, I need its pins) and the `front_panel` with the newly created geometry inside Parent_part:

![Banner](./example.png)

Here is the origin of the model: [origin.zip](./origin.zip)

## Assembly Dependent Boolean Operation (A)

1. *Teleport* the desired geometries into the root of `Parent_part`:

    > Workaround: Currently a Subshape Binder goes into the active *Body*. So you need to create a temporary `Body` to attract the newly created Subshape Binder. 
  
   1. Create a temporary Body inside `Parent_part`. (This will be automatically marked as "Active Body")
   2. Click the desired geometry (`circuit_board`) + click the `Subshape Binder`.
   2. Click the desired geometry (`device`) + click the `Subshape Binder`.
   3. Verify: The subshape binders went inside the temporary Body within the `Parent_part`. 
   4. Cleanup:
       1. Select those subshape binders, move them outside the temporary Body (select, go to root., `T+D`) 
       2. Remove the temporary Body
3. Create a cut by using those objects (Select `circuit_board` and then the `device`, click to Part -> Cut tool.)
4. Verify that the result shape (Cut_A) is looking nice. 

## Assembly Dependent Part Design (B)

1. Create a Body in `Parent_part` (Rename it as "`cutting_tool`"). 
2. Click `front_panel`, click `Subshape Binder`
3. Click `device`, click `Subshape Binder`
4. Only move the `front_panel`'s, subshape binder outside the `cutting_tool (Body)` 
5. Click the subshape binder inside the `cutting_tool (Body)`, then click the front face of the `device`. 
6. Open Part Design WB, click the "Create A New Sketch" button. 
7. Create some external geometries based on the subshape binder 
8. Create your cutter tool geometry by using those external geometries
9. Close the sketch, 
10. Pad it appropriately.
11. Use `cutter_tool (Body)` and the Subshape Binder of `front_panel` to generate a `Cut`. 

## Move Test

1. Move your Part (the `trimpot`)
2. Verify that the cut shape follows the changes (after a Recompute). 

## Modify Test

1. Go to Part
2. Change some geometries which relate to the `Operation A` or `Operation B`. 
3. Verify that the cut shape follows the changes (after a Recompute).


# Screencasts

### Assembly Dependent Boolean Operation

![](./operation-a.mp4){preload=metadata}

### Assembly Dependent Boolean Operation, Move Test


![](./operation-a--move-test.mp4)


### Assembly Dependent Boolean Operation, Modify Test

![](./operation-a--modify-test.mp4)

[20210117T1531-operation-a-modify-test-is-successful.zip](./20210117T1531-operation-a-modify-test-is-successful.zip)


### Assembly Dependent Part Design + Move Test


![](./operation-b-and-move-test.mp4)


### Assembly Dependent Part Design, Modify + Move Test


![](./operation-b-modify-and-move.mp4)


# Version 

```
OS: Debian GNU/Linux 10 (buster)
Word size of OS: 64-bit
Word size of FreeCAD: 64-bit
Version: 0.19.26157 (Git)
Build type: Release
Branch: LinkStage3
Hash: d9d8c77520750e26e625782f89a899f9c7188efd
Python version: 3.7.3
Qt version: 5.11.3
Coin version: 4.0.0a
OCC version: 7.3.0
Locale: English/UnitedStates (en_US)
```

# Questions and answers

1. Is this workflow officially supported?
   1. [Yes](https://github.com/realthunder/FreeCAD_assembly3/issues/422#issuecomment-763219357) 
2. If yes, is when is the *Holding `Ctrl` button* (in your original tutorial) come into play? I can't figure out the necessity for that, what am I missing?
   1. Holding `Ctrl` button means "Create a copy beforehand and then move". However it doesn't work the way I would expect, so it's better not to use it anyway. (See [this](https://github.com/realthunder/FreeCAD_assembly3/issues/422#issuecomment-769260539)) 
4. Why can't I create external geometries within the Part Design WB based on Subshape's rectangular face but I could create based on the circular geometry? 
   1. Unknown at this time. 

# Related links 

1. Original (deprecated) HOWTO: https://github.com/ceremcem/fc-asm3-cut-window
2. Related issue: https://github.com/realthunder/FreeCAD_assembly3/issues/422
