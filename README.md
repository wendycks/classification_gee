# Land Cover Classification Using Google Earth Engine

## Overview
This README provides instructions for running the `classification_land` script, which performs land cover classification on Landsat 8 imagery over Nanaimo (Vancuover Island), BC, Canada, using Google Earth Engine (GEE). It includes steps for image selection, training a classifier, and validating classification accuracy.

## Getting Started
- Ensure you have access to Google Earth Engine (GEE).
- Open the `classification_land` script within the GEE Code Editor.

## Step-by-Step Instructions

### Step 1: Image Selection
The script starts by selecting a cloud-free Landsat image of Nanaimo from the summer of 2020.
It filters images based on the least cloud cover and specific date ranges to ensure quality and relevance.

### Step 2: Merging Class Names
The script merges various predefined land cover classes such as water, forest, urban, barren, and grass into a single class collection for subsequent analysis.

### Step 3: Creating Training Data
Training data is generated by selecting relevant spectral bands.
The script samples these bands within the defined regions of interest that correspond to the merged class names.

### Step 4: Training the Classifier
A Random Forest classifier is trained using the specified bands and the prepared training data.
The training involves adjusting parameters to optimize classification performance.

### Step 5: Running the Classification
The trained classifier is applied to classify each pixel of the image into one of the land cover categories.

### Step 6: Displaying Classification
The classification result is added to the map in the GEE Code Editor.
Different land cover classes are displayed using a distinct color palette for visual evaluation.

### Step 7: Validation of Classification
Validation data is prepared similarly to training data but from separate regions to ensure unbiased accuracy assessment.
The script calculates an error matrix and overall accuracy to evaluate the performance of the classification.

### Step 8: Review and Analysis
Review the classification and validation results displayed in the GEE Code Editor.
Analyze the error matrix and overall accuracy to assess the effectiveness of the classification.

## Additional Notes
It is recommended to review and adjust the regions of interest or classification parameters based on specific project needs or geographical variations within the study area.
For detailed explanations and adjustments of script parameters, refer to the embedded comments within the `classification_land` script.

## License
This project is open source and available under the MIT License.
