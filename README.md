📌 Working of the Code & Models
This code uses Mask R-CNN for object detection and instance segmentation on an input image.

1️⃣ Model Used: Mask R-CNN
Mask R-CNN is a deep learning model that detects objects and generates segmentation masks.
It extends Faster R-CNN by adding a mask prediction branch.
Trained on COCO dataset, which has 80 object classes.
2️⃣ Workflow of the Code
Loads the Pretrained Model

Downloads Mask R-CNN COCO weights (mask_rcnn_coco.h5).
Loads it in inference mode.
Takes User Input for Image Path

Reads the image using skimage.io.imread().
Runs Object Detection & Segmentation

Detects objects in the image using model.detect().
Returns bounding boxes, masks, class labels, and confidence scores.
Displays Detection Results

Draws bounding boxes and segmentation masks on detected objects.
Segments the Most Confident Object

Extracts the object with the highest confidence score.
Creates a white background for easy visualization.
Displays the Segmented Object

Shows both the original image and the segmented object.
3️⃣ How Mask R-CNN Works
Backbone (Feature Extraction)

Uses ResNet with Feature Pyramid Network (FPN) for feature extraction.
Region Proposal Network (RPN)

Proposes regions likely to contain objects.
ROI Align & Classification

Classifies objects in the proposed regions.
Refines bounding boxes.
Mask Generation

Generates pixel-wise segmentation masks.
4️⃣ Output
Detected objects with bounding boxes and masks.
Segmented version of the most confident object.
🚀 This can be applied to images, videos, and real-time applications!
