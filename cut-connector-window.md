# Cut Connector Window 

Instructions to cut the `panel` according to `connector`:

0. Preparation (skip if you have these components drawn already):

  * Draw a pcb (label: `pcb`)
  * Draw a connector (label: `connector`)
  * Draw a front panel (label: `panel`)
  

1. Select the `connector` face 
2. Go to `Sketcher` workbench, click "Create a new sketch" button

![image](https://user-images.githubusercontent.com/6639874/43920382-76b50f7c-9c21-11e8-818c-2fffbfb128b9.png)

3. Go to `Part` workbench, extrude the socket window (preferably select the "symmetric" checkbox) (label this `panel-cut`)

4. Put `connector` and `panel-cut` into a Asm3 container. (label this `socket-part`)

5. Select `panel-cut`, go to `Part Design`, click "sub-shape binder"

6. Select `panel` and `Binder`, go to `Part` workbench, click "cut". (label this cut as `panel-part`)

7. Select `panel-cut` and make it invisible

8. Create new Asm3 container, select `pcb`, `socket-part` and `panel-part` and drop into this Asm3 container. 
