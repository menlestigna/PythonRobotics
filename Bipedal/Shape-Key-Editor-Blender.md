Anyone know how to do this in 2.5/2.6? I know I could do it back in 2.49 where all I had to do was go to Action Editor, click Add New, done. Someone please help me out on this so I can mix shapekeys together for the game engine. Thank you.
 
The action editor has object context, ie the keys there are paths from the object that is selected. The action is object.animation\_data.action. When you change an action in the action editor, this becomes the action for the selected object.
 
**Download File ➡ [https://eninlili.blogspot.com/?file=2A0P74](https://eninlili.blogspot.com/?file=2A0P74)**


 
The shape keys values are keyed onto the mesh or curve or data part of the object and that is what the shape key editor shows. The action
object.data.shapekeys.animation\_data.action
when you change an action here it goes onto the data part if it can have shape keys.
 
All that said, post an image of your dopesheet
EDIT:
Posted after ridix.
Another one is to use custom properties named after the shape keys on your object. Then use these to drive the shapes. You can then key them in the Action editor.
 
What the script does is adds custom properties to the object (object level properties, when keyed, show in the action editor) named after the shapekeys on the mesh. A driver relation is set up between the props and the shapes.
 
I am animating an action for a character I have made in Blender, and I have created mouth shape keys for lip-syncing. I want this action to have the character lip-syncing to some audio and have some body language, but I can't animate shape keys in the action editor (I can't create keyframes with the shape keys). Am I missing something here? How would I do this?
 
Terasology has an easy-to-edit shape format for blocks.While the block shape format is hand editable and one could write a block shape by hand,there is a great addon for the free, open source 3d editor Blenderwhich allows to easily create block shapes in a visual WYSIWYG environment and export them for use in Terasology.
 
A block shape in blender is a set of mesh objects corresponding to the various parts of the block shape.For each side and the center part of the block shape, a mesh object with the corresponding name can be present:Top, Bottom, Left, Right, Front, Back and Center.Additionally, extra mesh objects can be used to define the collision bounds for the block shape.

I'm very new to ARKit and SceneKit and 3D modelling/Blender 2.8, so bear with me, and apologies for the long detailed explanation, I just feel like I'm missing something simple and there aren't many guides online, that I can find, about how to do this.
 
I'm trying to build my own animoji/memoji with ARKit and Scenekit and I'm trying to export it to .dae/.scn and access all of the Blend shapes, to be able to modify them with ARFaceAnchor blend shapes.
 
I'm assuming I have to set up an SCNMorpher somewhere, to access the blend shapes. But if I can get some pointers as to how and where. Also if anyone knows how I can set up the morpher as an attribute in the node inspector, that would be great.
 
You need to add instance\_controllers to your Blender dae file so that SceneKit can correctly read the blend shapes. You can use this great tool to fix your file before importing it to SceneKit. Then, the shape keys appear in Xcode SceneKit editor and you can modify then in code with the SCNMorpher class.
 
The Shape Preset Selector is used to store and recall your custom Shapes. For example when you attempt to work with a fixed set of Standard Shapes, you can create Presets for each of your supported Shapes.
 
**Note:** Presets are stored globally (outside of the current Blend file), so all defined presets are available at any time in any project. Avastar is shipped with a few example presets (See the popup box in the image above)[/box]Shape Properties Section

- **Use Bind Pose:**Treat the current Restpose of the Rig as a Bind Pose. This is only used for modified Rigs (e.g. A-Posed Rigs).
- **Gender Selector:** Allows to switch the Rig between Female(Default) and Male. A rough estimate of the Avatar Height in SL is displayed besides the selector.

For experts: The bindpose feature is an improved and much more powerful replacement for the old Alter to Restpose feature. In easy words the Skeleton uses an edited custom Rig is, but it is internally treated as if it where in the original SL Restpose.
 
The section subpanel of the Avatar Shapes Editor contains the Shape Sliders. the sliders are organized almost identical to the Shape Editor in SL. The values assigned in SL match exactly with the slider values in Blender.
 
The green dots (icons) on the right side of the sliders appear when the slider value has been changed from its default value. Click on these green dots to reset the corresponding Slider Value to its default (Then also the icon disappears)
 
In general, the Shape Editor also works when the rig has been edited (when the Armature was modified in edit mode). However the Shape Sliders behave slightly different for bones which have been edited. Especially when sliders not only scale bones but also translate them (like for example the eye distance slider or the Shoulder distance slider) then as soon as the bones are edited, they only can be rotated and scaled. Any translation component is then suppressed!
 
Assume you have edited the Shoulder Bones and separated them a bit (see image). This means the Shoulder bones (actually mShoulderLeft and mShoulderRight to be precise) are now treated differently. Hence we have marked all sliders which directly move the Shoulders with a red background color (see below).
 
One pretty obscure feature of the SL appearance slider system is that it distinguishes between bones with edited joints and bones without edited joints. As soon as a joint is edited (for example when a bone is moved out of place in Armature edit mode), all sliders which directly affect the bone no longer apply bone translations to the bone.
 
By default the Avatar Shape Editor is enabled. This allows you to test the behavior of your meshes in regard to the Avatar Mesh shape sliders in SL, before the meshes are even exported. However, sometimes a rig becomes so complicated and the creator decides that the usage of the Avatar Shape Editor is actually not wanted. In this case Avastar allows you to disable the Avatar Shape editor by unchecking the check mark in the header of the Appearance panel.
 
**Important:** When you want to disable the Avatar Shape editor, then it is best to set the white Human Shape mode first (see above). This makes sure that your rig matches the neutral skeleton. While this is not strictly necessary we still recommend that you enable the white Human shape prior to disabling the Shape Editor. Then you can be sure that if you ever want to enable the Shape editor again, you will not suffer from unexpected deformations of the skeleton.
 
This function makes all slider changes permanent for the active (and selected) Custom Mesh. Take care: This function deletes all Shape keys (should you have defined Some) and the Mesh gets permanently and irreversible changed!
 
The Mesh deformer (not an Avastar feature) is an old development that came about a couple of years ago, but the project has never gone public in Second Life. However we keep basic support for the Mesh deformer available, because other compatible online worlds might possibly support the Mesh deformer.
 
HI, Im retargeting a Unity asset store asset to something else. I need to thin it down by moving some vertices. Its not a straight shape but a turn. How can I move the vertices but keep the shape? UV needs to stay intact too
 
the problem is most likely that you created this in blender as a small piece, made uvs for channel 0 & 1 and then duplicated the piece with an array
now you have 7 duplicates where alle the UVs are stacked upon each other, because they are all copies of the first geometry and this is fine for your uv channel that handles your textures, since you want them to be on top of each other, so every piece looks exactly as the first one
the problem is the second uv channel, lightmaps need to have a unique uv space and should not overlap (there are cases where you can get away with it, but usually its a nono)
 
second, you apply the array modifier in blender and open the uv editor, go to uv channel 2 and unwrap them again.
depending on wether the geometrie is merged or not you now have either 7 uv chunks layed out or one long uv chunk
 
okay, i thought you created the asset, but if it was created by someone else, most likely the modifiers are already applied, the only way you could still have not applied modifiers is when you opened a .blend file, all other imported formats do not have any modifiers
you can check that under the modifier tab (screenshot), there you can also apply them
 
instead of writing every step, look at this video how to open the uv editor,
usually it would be better to take some time and learn the basic functions of any software you want to use, there are a lot of tutorials that cover the basic layout and how to navigate in the programm
 
now select the object
on the second screenshot you can see the selected tab on the right side and below that you should have a list under UV MAPS
there you need to select the second uv channel
go into edit mode (tab) and select every vertice (a), then press u and select unwrap
this should make a new unwrap for uv channel 2
 
I fixed it by using the Knife project tool instead. So I didnt move the vertices. INstead I used the wall without window. Created a plane of same size as window and then cut out the window hole. This does not answer my question about UV its rather a work arouind. So if someone know how to retarget the UV i would like to know. Thanks
 
You can try some of the basic 3D modelling software for this purpose, if you go direc