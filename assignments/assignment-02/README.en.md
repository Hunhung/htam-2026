# 2026.11.22 Pegboard Accessory 3D Printing Record How Things Are Made

[中文](README.md) | [English](README.en.md)

[File inventory](source-inventory.csv)

[Bilingual HTML page (online)](https://hunhung.github.io/htam-2026/assignments/assignment-02/print-20261122-bilingual-review.html) · [Original Chinese TXT](source/record-original.txt)

## Background and assignment requirements

This is the second assignment for How Things Are Made: design and 3D print an accessory for a specific object on the laboratory pegboard. This record follows my selection of pliers, measurement, sketching, modeling, printing, and installation test.

- Choose a physical object and use its measurements to design the accessory.

- Refer to the supplied pegboard mounting geometry and consider FDM printing.

- Mount the printed accessory on the pegboard and check its fit and use.

## 1. Choosing the object and measuring it

I chose pliers as the object for my design. In fact, I found four different types of pliers here, with only the heads differing. I wanted to design a pegboard accessory that supports the pivot. For stability and safety, I also added a fence at the top, around the plier head, so the pliers could be taken out conveniently while also keeping the lab safe. I measured the length and widest part of the head, the distance from the bottom of the pivot to the tip of the head, and the thickness of the pliers. These measurements helped me design a hook and fence of a suitable size.

![Choosing pliers in the lab](images/object-choice-1.jpg)

![Different pliers and measuring tools](images/object-choice-2.jpg)

![Measurement record 1](images/measure-1.jpg)

![Measurement record 2](images/measure-2.jpg)

![Measurement record 3](images/measure-3.jpg)

![Measurement record 4](images/measure-4.jpg)

![Measurement record 5](images/measure-5.jpg)

## 2. Sketching the structure

After analyzing the requirements, I drew a rough sketch. The design is very simple: it adds a fence at the top of a common hook, but I think this can provide an effective safeguard. The accessory consists of two parts, a hook and a fence, which I will explain further in the modeling and printing stages.

![Sketch of the hook and upper fence](images/sketch-1.jpg)

![Position of the pliers in the holder](images/sketch-2.jpg)

## 3. Modeling in Fusion and the one-piece design

This time I tried modeling in Fusion. SketchUp is the modeling software I am most familiar with, but I wanted to try some new tools. Fusion's keyboard shortcuts and mouse controls are a little different from SU, so it was still a bit of a challenge for me, haha. I originally modeled everything as one piece. Later, during printing, I found it difficult to choose an ideal orientation for good strength. It also needed a lot of support, and the print quality was not ideal.

![The one-piece model in Fusion](images/fusion-model.jpg)

![Adjusting the geometry in Fusion](images/fusion-adjustment.jpg)

## 4. The first print and its problems

Halfway through the first print, the tree supports had already developed problems, so I paused the print. I do not know whether it was related to the material, but the printed model had stringing and was not very strong. I also found that my first model was too small, so I adjusted the model file again.

![Slicing and supports for the first version](images/slice-first.jpg)

![Checking supports and unsupported areas in the first version](images/slice-check.jpg)

![First print process 2](images/first-print-2.jpg)

![Result of the first print 1](images/failed-part-1.jpg)

![Result of the first print 3](images/failed-part-3.jpg)

![Result of the first print 5](images/failed-part-5.jpg)

<details>

<summary>More photographs of the first print (7)</summary>



![First print process 1](images/first-print-1.jpg)

![First print process 3](images/first-print-3.jpg)

![First print process 4](images/first-print-4.jpg)

![First print process 5](images/first-print-5.jpg)

![Result of the first print 2](images/failed-part-2.jpg)

![Result of the first print 4](images/failed-part-4.jpg)

![Additional record of the first printed part](images/failed-part-extra.jpg)

</details>

## 5. Splitting the parts and designing the joint

I recalculated the required dimensions and enlarged the model. I also reconsidered how the whole hook would carry the load, and finally decided to split the model into two components: the hook and the fence. The hook had originally been printed upright, which would make the result relatively weaker, so I laid it flat instead. I designed a simple mortise-and-tenon joint between the hook and the fence. To allow for printing error and possible wear, I left a clearance of 0.15 mm per side in the X direction and 0.20 mm per side in the Y direction, so the printed parts could be assembled easily while remaining fairly stable.

![The pin-and-hole connection between the fence and post](images/joint.jpg)

## 6. Slicing and the second print

For printing, I first exported the two finished model parts as STL files and placed them in one Bambu Studio project. I adjusted their orientation and selected the corresponding printer model. The first time, I forgot to select the correct model, so I had to slice it again. Because the H2D has two nozzles, the left or right nozzle can also be selected as needed. After selecting the settings, slicing, checking the supports, and exporting the sliced plate as a .gcode.3mf file, the print was ready to start. During printing, I could check the required time and filament weight, and then just wait patiently~

![Selecting the corresponding printer model](images/printer-selection.jpg)

![Slicing the two parts in their separate orientations](images/slice-two-parts.jpg)

![Printer record from the second print](images/second-print.jpg)

## 7. The finished parts and installation test

To remove the finished parts from the printer, I took out the build plate and gently flexed it to release the 3D-printed parts from the bottom. This made it easy to remove them intact. I mounted the accessory on the pegboard for testing, and the overall fit was quite good. At the joint, however, further tests with different clearances, finishing methods, and filaments might lead to a better fit. This will certainly require several rounds of physical testing.

![The hook mounted on the pegboard](images/finished-1.jpg)

![The assembled hook and fence without the pliers](images/finished-4.jpg)

![Front view with the pliers in place](images/finished-2.jpg)

![Another view with the pliers in place](images/finished-3.jpg)

## Downloads

| File | Contents |
| --- | --- |
| [Final fence STL](models/01-fence.stl) | Separate fence part |
| [Final post and hook STL](models/02-post-hook.stl) | Separate post, backplate, and hook part |
| [First one-piece model STL](models/first-version.stl) | Reference for comparing the first version |
| [Dimensioned PDF drawing for review](downloads/cad-review-a.pdf) | Four sheets: assembly, part views, and connection section |
| [2D DXF drawing for review](downloads/cad-review-a.dxf) | Editable 2D linework |
| [Original Word record](source/print-diary-original.docx) | The original document supplied by the author |
| [Original Chinese TXT](source/record-original.txt) | The complete original Chinese record |
| [Chinese TXT with corrected clearances](source/record-corrected.txt) | The confirmed pin-and-hole clearance correction |
| [Source asset inventory](source-inventory.csv) | Mapping of all 32 photographs to their source files |

The dimensioned drawings are the earlier review version, generated from the final print STL files. They have not been confirmed as native associative Fusion drawings. The latest native Fusion model and corresponding final slicing files will be added after version checking.
