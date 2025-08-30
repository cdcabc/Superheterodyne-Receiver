We order all the boards thru JLC. As of today (3/27/2025), the only thing that JLC needs is a Gerber and drill file zipped together. The Gerber file contains different CAMtastic files for the layers that you choose, while the drill file is used to tell the fab machine where to drill holes (if you want to learn more about CAMtastic files, just Google around and read up about the entire fabrication process.)

Every PCB project (.PrjPCB) contains different files, such as schematics, the PCB itself, and potentially other small things. One of these files is the “Output Job File”, which contains what PCB information is exported. If you are working on an older project that you’ve inherited, there are probably multiple output job files that have been created. However, if you are working on a project from scratch, you will need to make one for the project.


![[Pasted image 20250830133106.png]]
Figure 1: Creating a new “Output Job File”_

![[Pasted image 20250830133122.png]]
_Figure 2: Fresh “Output Job File”_

Like I said earlier, all JLC really cares about are the Gerber and drill files (there are ‘better’ files, such as ODB++, but JLC doesn’t currently support anything besides Gerber.) To export these files, we want to add new outputs under the “Fabrication Outputs” section. To do this, just click the “+” icon under “Fabrication Outputs”, click the “Gerber” and “NC Drill” options, and then just click the name of your PCB document (don’t click “[PCB Document]”). Once you’ve added these outputs, we will need to configure them, which can be done by right-clicking the individual output and clicking the “Configure” option at the bottom of the menu.

![[Pasted image 20250830133134.png]]
_Figure 3: “Configure” options for Gerber output_

The first configuration menu is for the Gerber output (_Figure 3_). Here, I usually select the units to be inches and the decimal range to be .01 mils (this honestly might be a little overkill, as there is no shot JLC can actually guarantee a .01 mil tolerance. To put .01 mils into perspective, this is the same as roughly 250 nm.) We also want the filename to reflect each individual layer, so the “FileName.Extension” option should be set to “filename.*” and not “*.gbr”. When it comes to the “Layers to plot” section, there are only a few important layers: all the copper layers (“Copper Layers”), the silkscreen layers (“Silkscreen”), the solder mask layers (“Solder Mask”), and the board boundary (“Keep-Out Layer”). Some mechanical layers can be included, as they could contain useful info for JLC, but they aren’t usually needed (the only time a mechanical layer is required is when the board outline is included on a mechanical layer, rather than the keep-out layer). There are also some advanced settings, so I will just post a screenshot below (_Figure 4_) of the settings I use and you can copy those if you want.

![[Pasted image 20250830133145.png]]

_Figure 4: “Advanced” options for the Gerber configuration menu_

![[Pasted image 20250830133154.png]]

Figure 5: “Configure” options for the NC Drill file_

The drill file configuration options are a little simpler. Just copy what I have above (_Figure 5_) and you should be good. Honestly, the default options are probably fine.

After this is all done, we can export the outputs. To do this, you have to click the “Folder Structure” option under the “Output Containers” section on the right-hand side of the output job file. Once this is highlighted, you can add individual outputs to this container by clicking the “Enabled” option to the very right of each output.

![[Pasted image 20250830133210.png]]

_Figure 6: Prepping outputs for exporting (“Enabled” option is circled)_

Now that the outputs have a path, we can export them. To export, just click “Generate content” under “Folder Structure”. The outputs will go to wherever the local path is that you set (by default, the output path is ‘C:\Users\Public\Public Documents\Altium\[projectName]’). I’m not sure what decides the next folder that the outputs are saved in (I think it is whatever license you are using?), but the outputs will be saved in a folder at the end of this path named either “Project Outputs for [projectName]” or “Project Outputs for Free Documents”. Anyways - the folder at the end of the path should look like it does below (_Figure 7_).

![[Pasted image 20250830133220.png]]

_Figure 7: Gerber and drill files exported_

Next, just zip the Gerber and drill files into one folder and give them a name that will help you understand what they actually are (I usually just do “[projectName] Gerber and drill”). Ta-da: you now have your zipped outputs.

The second half of the process is actually adding the board to the JLC cart. To do this, you will need to sign into the JLC account and click the “Order Now” option (or something like that) wherever you see it. An ordering webpage should pop up (_Figure 8)._

![[Pasted image 20250830133227.png]]

_Figure 8: Snippet of the ordering webpage_

As of now, the file upload button says “Add gerber file”, but what we actually want to add is the zipped folder that contains both the Gerber and drill files. So yeah, just click the button and click the .zip, not the actual Gerber folder. After you do this, the page will load a little bit, and JLC will be able to autofill some of the easier board options, such as “Layers” and “Dimensions”. I’m going to walk you through all the actual options, what each one means, and what we usually choose. There will also be a screenshot at the bottom that contains all the info that I used for my most recent order.