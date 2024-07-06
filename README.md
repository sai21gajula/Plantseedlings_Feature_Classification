# Plantseedlings_Feature_Classification

## Project Overview

This project focuses on classifying plant seedlings using various pre-processing and feature extraction techniques on low-resolution images to improve the classification accuracy of a Convolutional Neural Network (CNN) model. The primary goal is to identify plant seedlings and classify weed species accurately to aid in agricultural applications.

## Dataset

The dataset used in this project is the Plant Seedlings Classification dataset obtained from Kaggle. It consists of 4,750 RGB images of plant seedlings belonging to 12 different species, including 3 plant species and 9 weed species.

- **Plant Species:**
  - Sugar Beat (255 images)
  - Common Wheat (253 images)
  - Maize (257 images)

- **Weed Species:**
  - Sugar beet (463 images)
  - Black-grass (309 images)
  - Charlock (452 images)
  - Cleavers (335 images)
  - Common Chickweed (759 images)
  - Fat Hen (538 images)
  - Loose Silky-bent (762 images)
  - Scentless Mayweed (607 images)
  - Shepherds Purse (274 images)
  - Small-flowered Cranesbill (27 images)

## Pre-processing Techniques

The following pre-processing techniques were applied to improve image quality and enhance features for better classification:

1. **Label Encoding**: Converts categorical labels into numerical format.
2. **Image Sharpening using Gaussian Filter**: Enhances edges and minute details.
3. **Image Noise Reduction using Gaussian Blur**: Reduces noise while preserving edges.
4. **Geometric Transformations**: Adjusts the spatial configuration of the image.
5. **Colour Pixel Transformation (RGB to HSV)**: Converts RGB images to HSV for better color distinction.
6. **K-means Image Clustering**: Segments images to highlight important features.
7. **HSV Mask on K-means Enhanced Image**: Masks and extracts significant image regions based on HSV color space.
8. **Canny Edge Detection**: Detects edges for structural information.

## CNN Model Specifications

The CNN model used in this project consists of six convolutional layers with the following configuration:

- **Convolutional Layers**: 64, 128, 128, 256, 256 filters
- **Kernel Size**: 3x3
- **Activation Function**: ReLU
- **Dense Layers**: Two layers with 256 filters each, ReLU activation
- **MaxPool Layer**: 2x2 filter size
- **Optimizer**: Adam

The model was trained on 70% of the dataset, with 15% used for validation and 15% for testing.

## Results and Analysis

Various combinations of pre-processing techniques were tested to evaluate their impact on classification accuracy. The combinations and their respective accuracies are:

1. **Model without Pre-processing**: 
   - Training Accuracy: 87.21%
   - Testing Accuracy: 85.97%

2. **Model with Image Segmentation**:
   - Training Accuracy: 88.8%
   - Testing Accuracy: 88.08%

3. **Model with K-means Clustering**:
   - Training Accuracy: 96.45%
   - Testing Accuracy: 90.46%

4. **Model with HSV Mask on K-means**:
   - Training Accuracy: 99.41%
   - Testing Accuracy: 96.717%

The best results were achieved using a combination of K-means clustering and HSV mask, resulting in a training accuracy of 99.41% and testing accuracy of 96.717%.

## Conclusion

This project demonstrates the effectiveness of using advanced pre-processing and feature extraction techniques to enhance the performance of a CNN model for plant seedling classification. The combination of K-means clustering and HSV masking significantly improves classification accuracy, providing a reliable method for distinguishing between similar-looking plant species.

## References

- Muthukrishnan R and Radha M “Edge Detection Techniques for Image Segmentation” International Journal of Computer Science & Information Technology (IJCSIT) Vol 3 No 6, 2011.
- Valliammal N & Geethalakshmi S. “Plant Leaf Segmentation Using Non Linear K-means Clustering.” International Journal of Computer Science Issues. 9, 2012.
- Lawrence C. N, Moataz A, Mohammed A Z “Recent advances in image processing techniques for automated leaf pest and disease recognition – A review” Information Processing in Agriculture, 2021.
- Monishanker H, Ananya S, Habibullah B “Plant Disease Detection by Image Processing: A Literature Review” SDRP Journal of Food Science & Technology, 2019.
- Rzanny M, Seeland M, Wäldchen J, Mäder P “Acquiring and pre-processing leaf images for automated plant identification: Understanding the tradeoff between effort and information gain” Plant Methods, 2017.

For more detailed information, please refer to the provided Jupyter notebook and documentation.

---

This README provides a detailed overview of the project, including dataset details, pre-processing techniques, model specifications, results, and conclusions. Let me know if you need any additional information or modifications.
