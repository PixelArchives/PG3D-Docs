# Editor Crashing
Here are listed the reasons why editor may crash.

## LightingData
After decompiling, editor will crash when importing assets. (occured on Unity 5.3-2017.3)

Try going to folder with game scenes, and then moving all folders with lighting data outside Assets folder.  
After that editor should be aple to load unless there is other issue.  

Usaly there is 2 lighting data files for each map:
- Baked..?
- Light Probes
  
The one that is crashing the editor is Baked one, they even look different.

Baked one has a lot of strange data.

Light Probes has strage data too, but what makes them different is that Light Probes has positions:  
`{x: -0.70710677, y: -0.70710677, z: 0}`

The reason why im saying this, is because you would like to use them.  
They contain original probe positions, and is useful if you want to recover them in scene.
