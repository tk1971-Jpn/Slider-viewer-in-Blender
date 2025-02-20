### This script is designed to display MPR images in JPEG format, created from DICOM data, within Blender using sliders.  

<img width="612" alt="slider" src="https://github.com/user-attachments/assets/874d13d7-40a9-4622-86c1-c06f8d79a9e9" />

**Note:** Please prepare MPR images in JPEG format from DICOM data in advance using [tk1971-Jpn/DICOM-to-JPEG](https://github.com/tk1971-Jpn/DICOM-to-JPEG).

**Note:**  When using a Windows PC, a SyntaxError (unicode error) related to the path can be resolved by adding `r` at the beginning of the path.  
`NG` path = "C:\Users\myname\Documents\file.txt"  
`OK` path = r"C:\Users\myname\Documents\file.txt"  

1. Launch Blender
2. Select the Scripting mode and click the "New Text" button (the icon with two overlapping documents) to enable the creation of a new script.
3. Select the appropriate script, copy it, and paste it into Blender's text data-block.
4. Assign the values obtained from running the `DICOM to JPEG` script to the following variables.

- `pixel_pitch`: The second value of "pixel pitch"  
- `pixel`: The third value of "size of 3D array" 
- `ax_slide_number`: The value of "Number of files"  
- `ax_slide_distance`: The value of "slice distance" 

5. Assign the directory of the folder where the MPR images are stored (containing subfolders named A, C, and S) to `folder_path`.
6. When you run the script, an "Image Slider" tab will appear in the sidebar of the 3D viewport, allowing you to move the sliders to display the desired image in each direction.
