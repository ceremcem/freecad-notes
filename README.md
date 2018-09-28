# FreeCAD Notes 

## Assembly 3

* [Asm3 Constraints and «Natural» Links](https://www.dropbox.com/s/k40drc9rlkflrjs/Asm3_contr_et_liaisons_courantes_En.pdf?dl=0)
* [Assembly3 Builder Scripts](https://github.com/ceremcem/build-freecad-asm3)

## Deeper Knowledge 

* [Understanding the `Element` concept](https://github.com/realthunder/FreeCAD_assembly3/issues/61)
* [Understanding the Cyclic dependency errors](https://github.com/realthunder/FreeCAD_assembly3/issues/74)
* [Race condition between Asm3 const. and Sketcher Ext. const](https://github.com/realthunder/FreeCAD_assembly3/issues/102#issuecomment-425258495)


## Miscellaneous 

* Prevent TechDraw position jump: [Use "LockPosition=true"](https://forum.freecadweb.org/viewtopic.php?style=10&t=29853)
* Importing DXF files: [Enable importer in Preferences](https://github.com/realthunder/FreeCAD_assembly3/issues/85#issuecomment-420690833)
* Subshape not found: [1](https://forum.freecadweb.org/viewtopic.php?t=23746), [Follow the best practices](https://forum.freecadweb.org/viewtopic.php?f=3&t=15432&start=40#p143978)

## Ongoing

Periodically check those and add to this HOWTO when they are ready:

* [Hitting escape key while editing in a Sketch](https://forum.freecadweb.org/viewtopic.php?f=10&t=30759)
* [Disabling Sketch constraints](https://forum.freecadweb.org/viewtopic.php?p=256171#p256171)
* [Sync operation Placement with its Base object](https://forum.freecadweb.org/viewtopic.php?f=8&t=30859) 
* [Embed Python code into FreeCAD document](https://forum.freecadweb.org/viewtopic.php?f=3&t=30731)
* [Dxf to Drill file conversion](https://forum.freecadweb.org/viewtopic.php?f=3&t=31176)

## TODO 

Followings will be tested by me and then merged into the appropriate sections of this HOWTO:

* [Slice part with plane](https://open-shelf.appspot.com/FreeCAD/en-US/34.html), [Part Slice](https://www.freecadweb.org/wiki/Part_Slice)
* [Make 3D from 2D drawings](https://forum.freecadweb.org/viewtopic.php?t=8121)
* Multiple Holes, [image](https://user-images.githubusercontent.com/6639874/44943027-5589ee00-adc7-11e8-95d8-29288d94fb86.png), [Link](https://forum.freecadweb.org/viewtopic.php?f=3&t=30625) 

## Complementary Tasks 

* Printing DXF `1:1`: 
  * TechDraw -> Export
  * LibreCAD -> Open -> Select drawing -> Print Preview -> select `1:1` -> Print

## By Task 

| Task &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;| Screenshot/Screencast | Link &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;| 
| ---- | --------------------- | ---- |
| Using External Geometry | ![image](https://user-images.githubusercontent.com/6639874/45157889-08ed4b00-b1eb-11e8-9f4a-95cf49c88730.png) | [Link](https://www.freecadweb.org/wiki/Sketcher_External)
| Measure Distance Center to Center | ![measurement-center-to-center](https://user-images.githubusercontent.com/6639874/44947330-467d5d00-ae14-11e8-8255-0a95f35e25cb.gif) | [Link](https://forum.freecadweb.org/viewtopic.php?p=253824#p253821) |
| Customize WB Toolbar | ![customize workbench bars](https://user-images.githubusercontent.com/6639874/45043088-ee916100-b074-11e8-9fed-7737c07aaea0.gif) | ---
| Using filename as parameter source | ![image](https://forum.freecadweb.org/download/file.php?id=66816) | [Link](https://forum.freecadweb.org/viewtopic.php?f=3&t=30720&p=254625#p254653) |
| Projection Constraints | ![image](https://user-images.githubusercontent.com/6639874/45158649-4a7ef580-b1ed-11e8-903f-17ed828b88fd.gif) | [Link](https://github.com/realthunder/FreeCAD_assembly3/issues/63#issuecomment-419207737)
| Generating 2D drawing from an object | ... | ...
| Create radius on a plate vertex | ![image](https://forum.freecadweb.org/download/file.php?id=67148) | [Link](https://forum.freecadweb.org/viewtopic.php?f=3&t=30851)
| Part slice | ![image](https://www.freecadweb.org/wiki/images/thumb/a/a9/Part_Slice_Demo.png/600px-Part_Slice_Demo.png) | TODO
| Pause recalculations while working in spreadsheet | ... | [spreadsheet -> right click -> Skip recomputes](https://forum.freecadweb.org/viewtopic.php?f=3&t=31005)
| Set tolerance on cut | ![image](https://forum.freecadweb.org/download/file.php?id=67322) | [Part/3D Offset*](https://forum.freecadweb.org/viewtopic.php?f=3&t=30922&p=257265#p256250) or [OpenScad/IncreaseTolerance](https://forum.freecadweb.org/viewtopic.php?p=257177#p257133)
| Resizing DXF logo | ... | [Draft/Scale](https://forum.freecadweb.org/viewtopic.php?p=257164#p257164)
| Iterating through cells | ... | [Link](https://forum.freecadweb.org/viewtopic.php?f=22&t=31053)

# By Task (Asm3)
| Task &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;| Screenshot/Screencast | Link &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;| 
| ---- | --------------------- | ---- | 
| Resetting orientation which is ruined by `Move Part` tool (![image](https://user-images.githubusercontent.com/6639874/44947919-2736fd80-ae1d-11e8-9f9e-16c64a89788a.png)) | ![image](https://user-images.githubusercontent.com/6639874/44947955-af1d0780-ae1d-11e8-934e-d1ec0a26e711.png) | [Link](https://github.com/realthunder/FreeCAD_assembly3/issues/21#issuecomment-411357888) |
| Moving an object inside sub-container | ![movement-inside-container](https://user-images.githubusercontent.com/6639874/44950966-b9f88c00-ae5f-11e8-8a64-10172af06c23.gif) | [Link](https://github.com/realthunder/FreeCAD_assembly3/issues/28#issuecomment-412379339)
| Center to Plane Constraint | ![center-to-plane-example](https://user-images.githubusercontent.com/6639874/45145556-93bd4e00-b1c9-11e8-8094-44c3a11767ee.gif) | [Link](https://github.com/realthunder/FreeCAD_assembly3/issues/51#issuecomment-419013856)
| Replacing Parts | ![image](https://github.com/realthunder/FreeCAD_assembly3/wiki/images/replace-part.gif) | [Link](https://github.com/realthunder/FreeCAD_assembly3/issues/61)
| Modeling using assembly | ![image](https://user-images.githubusercontent.com/6639874/45268003-2df9ec00-b47f-11e8-894e-92f6214c3713.gif) | [Link](https://github.com/ceremcem/fc-asm3-cut-window) 
| Centering distinct planes | ... | [Link](https://github.com/realthunder/FreeCAD_assembly3/issues/53#issuecomment-419249913)
| Assembly Based Dimensions | ![dynamic-measurement-success](https://user-images.githubusercontent.com/6639874/45010978-d7248a80-b018-11e8-8f1d-60874426036b.gif) | [Link](https://forum.freecadweb.org/viewtopic.php?f=3&t=30676)
| Fixing broken binder | ![fixing-broken-binder](https://user-images.githubusercontent.com/6639874/45266593-ff234c00-b465-11e8-992d-6bd9150d7c5c.gif) | Select both `Binder` and the `Part` and click `Sub-shape Binder`
| Fixing broken elements | ... | [Link](https://github.com/realthunder/FreeCAD_assembly3/issues/140)
| Find relations for a part | ![image](https://user-images.githubusercontent.com/6639874/45596665-1f07c200-b9c8-11e8-8f1c-a8dccff0bcc1.png) | Click part + use the "`Find Relations`" button
| Quick move/create link | ... | [Link](https://github.com/realthunder/FreeCAD_assembly3/issues/103)
