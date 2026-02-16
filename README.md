# MLPR Lab 5 – Face Detection and Colour-Based Clustering

## Aim

The aim of this lab is to:
- Detect faces in an image using Haar Cascade classifiers.
- Extract colour information from detected face regions.
- Convert colour data to HSV colour space.
- Perform clustering using K-Means to analyse patterns in hue and saturation values.
- Visualise clustering results to identify meaningful groupings.

---

##  Methodology

### Face Detection

We used OpenCV’s Haar Cascade Classifier to detect faces in the image.

- The image was first converted to grayscale.
- Haar cascade classifier was applied using `detectMultiScale()`.
- Bounding boxes were drawn around detected faces.

**Libraries used:**
- OpenCV
- NumPy
- Matplotlib

---

### Colour Space Conversion

For each detected face:

- The face region was extracted.
- Converted from BGR to HSV colour space.
- Mean Hue and Saturation values were computed.

HSV colour space was chosen because:
- Hue represents colour type.
- Saturation represents colour intensity.
- It separates brightness from colour information.

---

### Feature Extraction

For every detected face:

- Extracted mean Hue
- Extracted mean Saturation
- Stored values in a feature array

This resulted in a 2D feature space:
