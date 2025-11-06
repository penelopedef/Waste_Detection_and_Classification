## Waste Detection and Classification
#### Researcher - Penelope DeFreitas
#### Purpose - This repository was completed as a graded project in partial fulfillment of the requirements for the postgraduate studies

## Background
The increasing volume of waste production in urban environments poses significant challenges for municipal waste management systems. 
With landfills nearing capacity and recycling rates lagging behind production, there is a critical need for innovative solutions to 
promote efficient waste sorting and recycling. While specific statistics may vary depending on the region and context, globally, urban 
areas generate substantial waste, with projections indicating a steady increase in waste production over the coming years. For instance, 
according to the World Bank, urban waste generation is expected to rise from 2.01 billion tonnes in 2016 to 3.40 billion tonnes by 2050 
(World Health Organization, 2024). Toronto's economy produces around 2.1 million tons of solid waste annually, with projections increasing 
to 2.5 million tons by 2030 if current trends persist (Circle Economy, 2022).

The motivation behind WasteWise Toronto is to leverage advanced machine learning and data science techniques to improve sorting accuracy,
thus enhancing recycling efforts and reducing the overall environmental footprint of urban waste management. 

## About the Dataset
- A mixed Waste dataset was used for this project. It comprised 6,884 images images 416x416 colour images in 11 classes. The training images were 4800, testing images were ¬1000 and validation images were ¬1000 in quantity. The classes in the dataset included: 'cans', 'tins', 'metal_trays_plates_pans','cardboard', 'styrofoam container', 'envelope', 'paper', 'carton', 'plastic', 'organics', 'general'
- ¬2100 were recyclables, ¬2100 organics, ¬2100 general

The following pre-processing steps was applied to each image:
- Auto-orientation of pixel data (with EXIF[Exchangeable Image File Format]-orientation stripping)
- Resize to 416x416 (Stretch)
N.B - EXIF-orientation stripping involves analyzing the orientation information stored in the EXIF metadata and rotating or flipping the image data accordingly to ensure that it is displayed correctly.

The following augmentation was applied to create 3 versions of each source image:
- 50% probability of horizontal flip
- 50% probability of vertical flip
- Equal probability of one of the following 90-degree rotations: none, clockwise, counter-clockwise, upside-down
- Random shear of between -15° to +15° horizontally and -15° to +15° vertically
- Reference Provided by a Roboflow user License: CC BY 4.0

Blue Bin:Recyclables
- Metals ('cans', 'tins', 'metal_trays_plates_pans'): https://www.kaggle.com/datasets/sumn2u/garbage-classification-v2?select=metal
- Cardboard boxes: https://universe.roboflow.com/dataset-t7hz7/cardboard-eupc8/dataset/3
- Styrofoam containers : https://universe.roboflow.com/namseoul-qobk6/styrofoam-qt1kt/dataset/1 Envelopes: https://universe.roboflow.com/mateo-ojeda/envelope-c6750/dataset/1 - Paper: https://universe.roboflow.com/natalie-perrochon-yqnhb/recycling-try-2/dataset/16
- Carton juice and milk boxes: https://app.roboflow.com/waste-z6zen/carton-xuife/1
- Plastic bottles: https://universe.roboflow.com/betul-rt4lp/plastic-bottle-cuwtu/dataset/1

Green Bin: Organics (fruits, vegetables, scraps from plates and garbage dumps, rotting foods) https://universe.roboflow.com/patata-man-y8maj/bio-waste/browse?queryText=&pageSize=50&startingIndex=0&browseQuery=true https://universe.roboflow.com/search?q=organic%20waste

Black Bin: General waste
- mugs: https://universe.roboflow.com/gsa-team/mugs-vhjth
- broken plates: https://app.roboflow.com/waste-z6zen/general-1/1
- cigarettes: https://universe.roboflow.com/universitadellacalabria-icrla/cigarettebuttdetection-tlhei
- Masks and gloves: https://universe.roboflow.com/sultana-almasoud/our_gp2
