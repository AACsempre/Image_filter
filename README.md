# Image_filter
Computer vision to remove corrupted images from a large amount of frames.
It is required to produce a clean Timelapse, for instance, following the evolution of a construction work.

Frames to be removed include empty images, corrupted images, and images taken at night or in a dark environment, when operations are halted.

## crop.ipynb
Crops all frames in a folder.
It might be useful if there is a permanent area of interest in all the pictures.
The area is defined in terms of pixels, referring to the top left corner.

## rename.ipynb
Rename all the files in a folder in an incremental measure.
This step is required when using the entire set of frames to create a videolapse through ffmpeg software.

## ocv_cluster.ipynb
Creates clusters within the entire set of images, in order to identify images that should be filtered out of the timelapse.
Different features are obtained from each image file into a dataframe - Python OpenCV library is used.
A kmeans clustering algorithm classifies each picture into a specific cluster - Python sklearn library is used.

## sep_folders.ipynb
After the clustering classification, every file can be relocated to a specific folder.
A visual inspection can easily identify which folders are of interest.
