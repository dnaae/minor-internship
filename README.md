# Minor Internship Project

## Description
Welcome aboard everyone (interested in quantitative breast cancer epigenetics)! This is where you will find scripts you need to handle single cell confocal microscopy data, in order to extract topographic cell features. 
The "FISH-QUANT pipeline" branch comprises 6 notebooks and is based on the FISH-QUANT v2 software. The "statistics" branch comprises 1 notebook dedicated in inferrential statistics. The original data is batches of 100 images treated under 8 different epigenetic modifiers- so 800 images in total. The pipeline aims to inform about the number of mRNA transcript aggregates (spots) and the number of transcription sites (aggregates in the cytoplasm) per image. This information is important to understand how transcription is regulated and how transcriptional bursting properties can be inferred. 

## Instructions
### FISH-QUANT pipeline branch
1. Upload your image data (tiff form) on google drive. <br />
2. Run the "channel splitting" script (on google colab), which splits the 4D channel (DAPI, smFISH, z planes, xy axis) into a DAPI and smFISH 3D image. <br />
3. Run the "segmentation" script, which uses a local threshold to extract nuclear and cellular masks for each cell image per treatment. <br />
4. Run the "spot detection" script, which results in maximum intensity areas (spots) and clusters (neighbouring aggregates) per cell (saved in csv). <br />
5. Run the "cell level results" script, which aligns masks, spots and clusters per image, calculates number of transcription sites and results in a field view of the cell with all aforementioned information depicted (output stored in npz). <br />
6. Run the "coordinates analysis" script, which computes topographic features about each cell. <br />
7. (Optionally) run the "synthetic data" script, which serves as benchmark for the pipeline. The user can determine the number of spots and clusters they want and check how the pipeline performs in identifying them.
### Statistics branch
Run the script on jupyter notebook and explore inferrential statistics tests and visualisations. 

## Acknowledgements
The pipeline uses packages from [GitHub Pages](https://github.com/fish-quant). 
