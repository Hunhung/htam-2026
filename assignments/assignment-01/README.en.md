# 2026.11.16 How Things Are Made · Assignment 1 · 3D Scanning Record

[中文](README.md) | [English](README.en.md)

[File inventory](source-inventory.csv)

[Bilingual HTML file](scan-20261116-bilingual-review.html) · [Original Chinese TXT](source/record-original.txt)

## Background and assignment requirements

This is the first assignment for How Things Are Made, titled Digital Bodies: Scan, Mix & Modify. The following records my scanning, initial alignment attempts and model export on November 16, 2026.

- Combine at least one 3D scan with another 3D model.
- Clean and repair the mesh in preparation for 3D printing; physical printing is not required for this assignment.
- Document scanning, editing, the associated digital files, and the problems and reflections from the process.

## 1. Connecting the scanner and choosing a software version

When connecting Revo Scan, I ran into a connection problem. After trying to connect it to the laptop through USB and Type-C, I found that the problem was the app version. The scanner I was using in the Fab Lab was a POP2, but I had downloaded an incompatible version, Revo Scan 6. After downloading Revo Scan 5, I connected successfully.

![Scanner setup](images/setup.jpg)

![Connecting to the laptop (3)](images/device-view.jpg)

![Connecting to the laptop (4)](images/cables.jpg)

![Connecting to the laptop (11)](images/connection.jpg)

![Connecting to the laptop (8)](images/software-download.jpg)

![Connecting to the laptop (7)](images/version.jpg)

## 2. Unstable scanner performance

Unfortunately, the scanner seems to have started having problems around noon today. It was very unstable during scanning, and the final results were disappointing. Today, it could not scan smooth surfaces consistently. The scanned surfaces looked like muddy ground: all the detail was lost, and there were also surface discontinuities and shifts. At the point-cloud stage, the number of captured points was clearly insufficient, and the result after one-click processing was pretty disgusting too.

![Scanner setup (12)](images/scan-setup-2.jpg)

![Scanner setup (13)](images/scan-setup-3.jpg)

## 3. Scanning the plaster model and the mouse

I tried scanning a small plaster model in the lab, but the facial detail was extremely poor: it was barely recognizable as a human face. I then chose my mouse as the scanning subject. Its surface was originally smooth and curved, but the scanned result looked like a toad. I first placed the mouse upright on the turntable and scanned its upper part, then turned it bottom-side up and scanned the underside. Both scans contained errors and missing detail. My original plan was to align the scans of the top and bottom to obtain one complete model, but because of the problems with detail and accuracy, I did not get a satisfactory result in the end.

![Lost facial detail](images/face.jpg)

![Failed plaster scan (1)](images/plaster-side.jpg)

![Failed plaster scan (2)](images/plaster-front.jpg)

![Misaligned plaster scan](images/offset.jpg)

![Uneven mouse point cloud](images/mouse-cloud.jpg)

![Uneven mouse model (1)](images/mouse.jpg)

![Uneven mouse model (3)](images/mouse-other.jpg)

## 4. Trying to align the mouse scans

During alignment, I tried selecting matching points, but the model accuracy was low and there was some misalignment. The alignment result was not as good as I had imagined.

![Aligning the scans (1)](images/alignment.jpg)

![Aligning the scans (2)](images/alignment-alt.jpg)

## 5. Connecting Revo Scan on a phone

I also tried Revo Scan on a phone, but there were connection problems. I suspected poor contact in the connection; in any case, it would not stay connected reliably. Considering that the scanner was malfunctioning, I did not continue trying.

![Scanner setup (9)](images/mobile-revo.jpg)

## 6. Switching to RealityScan and a different object

In the end, I decided to try RealityScan on a phone to take photographs and generate a 3D model. The instructions in the mobile RealityScan app stated that it was better suited to scanning food, plush objects or natural surfaces, and less suited to smooth, flat surfaces. My guess here was that analyzing 3D data from photographs could not locate points as precisely as a scanner using structured light and lasers, so the resulting model surfaces were also rougher. However, the advantage of this app was that its textures were beautiful: they could accurately display the materials and details of the objects in the photographs through texture maps. As a result, the final output was at least visually attractive. The actual model, however, still needed further refinement. This is also why I eventually changed the object I was scanning and chose a plush toy: its surface was more uneven.

![Phone scan of the mouse (2)](images/phone-mouse.jpg)

![Phone scan of the mouse (4)](images/phone-mouse-alt.jpg)

![Phone capture (1)](images/phone-start.jpg)

![Phone capture (2)](images/capture.jpg)

## 7. Capture lighting and point-cloud checks

When using RealityScan, I first selected Object Mode. I placed the object on a flat surface and took photographs from all directions through continuous manual or automatic capture. One thing to pay attention to here is that the photographs need to be continuous, clear and complete; otherwise, a large amount of Unconnected content will appear later. In the point cloud generated after my first 72 photographs, I noticed many gaps in the darker areas. I tried adding lighting and taking more photographs, which filled in some of the darker areas. Ultimately, though, I thought I should have prepared a complete lighting setup from the beginning to make sure that every side of the object could be captured properly. In the darker areas I tried to fill in, the added lighting created unnatural transitions between light and dark. This is something I think I did not do well enough this time.

![Phone capture (3)](images/phone-generation.jpg)

![Phone capture (4)](images/cloud.jpg)

![Phone capture (6)](images/phone-cloudprogress.jpg)

![Phone capture (7)](images/unconnected.jpg)

## 8. Model generation, export and untextured comparison

Finally, after checking the point cloud four or five times, I generated the model. In the generation options, I chose Water-tight Mesh, so that the result would be a complete model, with areas lacking detail filled in intelligently by the algorithm. To get a better result, I also chose higher quality and 8K textures. The result had a very good visual appearance in terms of its materials, while the untextured mesh did still have some rough surfaces and details. I will continue modifying and improving it.

![Phone capture (5)](images/settings.jpg)

![Phone capture (8)](images/phone-completed.jpg)

![Textured result](images/result.jpg)

![Untextured mesh](images/white.jpg)

## 9. Tidying up the model and adding a base in Blender

I imported the scanned model into Blender and made some simple adjustments by hand. I removed unwanted parts, adjusted the size, and tried to make the surface a little smoother. The result looked tidier than the original export, but the surface was still rough and some details were missing.

I then added a simple rectangular base, adjusted the positions, and combined the scan with the base to make a small display piece. Finally, I saved the Blender project and exported the model as an STL file.

Below are previews of the model before and after editing, and the combined result.

| Original scan | After cleanup and scaling |
| --- | --- |
| ![Original scanned mesh](images/model-raw.jpg) | ![Cleaned mesh](images/model-clean.jpg) |

| Separate simplified base | Combined display piece |
| --- | --- |
| ![Independent rectangular base](images/model-base.jpg) | ![Combined piece, oblique view](images/model-final-iso.jpg) |

| Front | Back | Top |
| --- | --- | --- |
| ![Front](images/model-final-front.jpg) | ![Back](images/model-final-back.jpg) | ![Top](images/model-final-top.jpg) |

## Downloads

| File | Contents |
| --- | --- |
| [Final combined STL (ZIP)](downloads/display-piece.zip) | STL of the model combined with its base |
| [Cleaned body STL (ZIP)](downloads/clean-model.zip) | Scaled body mesh |
| [Separate simplified base STL](models/processed/02_plinth_base.stl) | A separate simple rectangular base |
| [Original RealityScan export (ZIP)](downloads/realityscan-original.zip) | Rei.obj, Rei.mtl and two original 8K texture maps; keep together after extraction |
| [POP2 scan 03 (ZIP)](downloads/pop2-scan-03.zip) / [scan 04 (ZIP)](downloads/pop2-scan-04.zip) | Two original PLY scan exports |
| [Blender combination project (ZIP)](downloads/blender-project.zip) | Saved Blender project; see the STL download above for the final exported model |
| [Original Word diary](source/scan-diary-original.docx) | Source of the complete Chinese diary |
| [Original material inventory](source-inventory.csv) | Inventory of the original scan materials |

The original photographs, videos and Revo Scan project are kept locally. Scan outputs and model files can be downloaded above.
