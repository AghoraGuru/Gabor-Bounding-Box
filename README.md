# 📷 Image Text Line Detection and Bounding Box Creation

This script processes an input image, applies Gabor filters to detect text lines, and creates bounding boxes around the detected text lines. The resulting modified image is saved with the bounding boxes, and bounding box coordinates are stored in a JSON file.

## 🛠️ Installation

1. Make sure you have Python installed on your system.
2. Install the required packages by running:
   
```py
pip install opencv-python
```

## 🚀 Usage

1. Replace `img_path` with the path to the image you want to process.
2. Adjust the Gabor filter parameters in the `cv2.getGaborKernel` function to fine-tune the text line detection.
3. Tweak the parameters in the `cv2.HoughLinesP` function for line detection.
4. Run the script:

```py
python bounding_box.py
```

## 🔍 Script Explanation

The script follows these steps:

1. Load the image using OpenCV.
2. Create a Gabor filter bank using `cv2.getGaborKernel`.
3. Apply Gabor filters to the image and store the filtered images.
4. Detect edges using the Canny edge detector.
5. Use Hough Transform to detect lines.
6. Group lines based on y-coordinates to form text lines.
7. Create a new folder to save the modified image and boxed text lines.
8. Iterate through grouped lines, draw bounding boxes, and save boxed images.
9. Store bounding box coordinates in a dictionary and save as JSON.
10. Save the modified image with bounding boxes.

## 🤝 Help me out with Filter Parameters

Do let me know if you found a better parameter for any filter being used; it would mean a lot!
