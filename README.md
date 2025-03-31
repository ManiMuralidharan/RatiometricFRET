# RatiometricFRET
RatiometricFRETMatlabbased
This MATLAB code for a Multi-Frame Ratio Viewer GUI.

1. Save the Code as a MATLAB Function:

Open MATLAB.
Create a new script (File > New > Script).
Copy and paste the entire code into the script.
Save the script as MultiFrameRatioViewer_new.m. Make sure the filename matches the function name.
2. Run the Function:

In the MATLAB command window, type:
Matlab

MultiFrameRatioViewer_new
Press Enter. This will launch the Multi-Frame Ratio Viewer GUI.
3. Understanding the GUI:

Load Numerator Button:
Click this button to select a multi-frame TIFF file that will be used as the numerator in the ratio calculation.
Load Denominator Button:
Click this button to select a multi-frame TIFF file that will be used as the denominator in the ratio calculation.
Save as TIFF Button:
Click this button to save the currently displayed ratio image as a TIFF file.
Frame Slider:
This slider allows you to navigate through the frames of the loaded TIFF files.
The displayed ratio image will update based on the selected frame.
Frame Label:
Displays the current frame number and the total number of frames.
Min Ratio Slider:
Sets the minimum ratio value to be displayed. Values below this threshold are clamped to this value.
Max Ratio Slider:
Sets the maximum ratio value to be displayed. Values above this threshold are clamped to this value.
Min Intensity Slider:
sets the minimum intensity of the displayed image.
Max Intensity Slider:
sets the maximum intensity of the displayed image.
Colormap Dropdown:
Allows you to select a colormap for the displayed ratio image.
Axes:
Displays the calculated ratio image.
4. Step-by-Step Usage:

Load Numerator and Denominator Images:
Click the "Load Numerator" button and select the numerator TIFF file.
Click the "Load Denominator" button and select the denominator TIFF file.
The first frame of the calculated ratio image will be displayed in the axes.
Navigate Frames:
Use the frame slider to navigate through the frames of the loaded TIFF files.
The displayed ratio image will update as you move the slider.
Adjust Ratio and Intensity Limits:
Use the "Min Ratio" and "Max Ratio" sliders to adjust the range of ratio values displayed.
Use the "Min Intensity" and "Max Intensity" sliders to adjust the intensity range of the displayed image.
Select Colormap:
Use the colormap dropdown to select a colormap for the displayed image.
Save Ratio Image:
Click the "Save as TIFF" button to save the currently displayed ratio image as a TIFF file.
Close the GUI:
Close the figure window when you are finished.
Key Code Details:

GUI Creation: The code uses figure and uicontrol to create the GUI elements.
Image Loading: The loadNumerator and loadDenominator functions use uigetfile to select TIFF files and loadMultiFrameTIFF to load the image data.
Ratio Calculation: The processFrame function calculates the ratio image by dividing the numerator image by the denominator image. It also handles division by zero and applies the ratio limits.
Image Display: The imshow function is used to display the ratio image in the axes.
Colormap Selection: The colormap function is used to set the colormap of the displayed image.
Slider Callbacks: The updateFrame and updateDisplay functions are called when the sliders or dropdowns are adjusted, updating the displayed image.
Saving TIFF: The saveAsTIFF function saves the current ratio image as a TIFF file using imwrite.
Multi-frame Tiff loading Function: The function loadMultiFrameTIFF loads all frames of the tiff file into a 3 dimensional matrix.
Error Prevention: The code includes checks to prevent errors caused by empty image data or division by zero.
Important Notes:

Image Processing Toolbox: This code relies on the MATLAB Image Processing Toolbox for functions like imfinfo, imread, and imshow.
TIFF File Format: Make sure your TIFF files are compatible with MATLAB's imread function.
Ratio Calculation: The ratio calculation assumes that the numerator and denominator images are aligned and have the same dimensions.
Slider Limits: The ratio and intensity sliders have predefined limits. You can adjust these limits in the code if needed.
File Permissions: Make sure MATLAB has the necessary read/write permissions for the files and folders you are working with.
