
# 3D Breast Cells Image Segmentation 

This project focuses on developing an automated process to generate masks from 2D slices of 3D breast cell images, aiming to assist in medical image analysis and cancer research.

Tools Used:

    Python 
    OpenCV
    Scikit-Image
    NumPy
    Matplotlib
    TiffFile
    Fiji


Techiniques Used:

    Thresholding
    Noise Reduction
    Morphological Operations
    Segmentation
    Image Conversion
    Visualization Techniques
    TIFF Handling

Non-Local Means Denoising:

Uses a noise reduction technique that averages the values of pixels based on the similarity of small patches around them, preserving important features like edges while removing noise.

Adaptive Thresholding:

Dynamically adjusts the threshold value based on the local mean intensity of image slices to effectively separate foreground (cellular structures) from the background.

Distance Transform:

Computes the minimum distance from each pixel to the nearest background pixel, which is crucial for the watershed algorithm to identify the centers of cells.

Watershed Segmentation:

Applies the watershed algorithm using the distance transform as the landscape, where local maxima serve as flood sources, effectively segmenting touching or overlapping cells.

Bilateral Filtering on Masks:

Employs a bilateral filter on the segmentation masks to smooth them while retaining edge boundaries, thereby reducing noise without blurring the edges of the cells.

Morphological Operations: 
Erosion and Small Hole Removal:

Uses erosion to refine the mask by removing small pixels from the boundaries of detected regions, enhancing the accuracy of cell boundaries.
Removes small holes in the mask to ensure complete and continuous segmentation of cells without any interruptions.

Visualization Using XOR Operations:

Implements XOR operations to visually compare and contrast the differences between the original, enhanced, and segmented images, providing insight into the effectiveness of the processing steps.



To run the code, 
Update the Image Path, Images Folder and Mask Folder path and run the cells.