# **Cartoonify Image and Video Project 🎨✨**

## **Project Overview**
The purpose of this project is to transform an image or video into a cartoon-like representation and allow users to download the cartoonized output. This is achieved through various image-processing techniques, including edge detection, smoothing, and masking, using OpenCV and Python libraries.


https://github.com/user-attachments/assets/debe8a91-8719-48b9-ba46-fc0462269031


---

## **Features**
1. **Cartoonize Image**: Converts an uploaded image into a cartoon-style image by applying:
   - Grayscale conversion.
   - Edge detection.
   - Bilateral filtering for smooth colors.
   - Masking to combine edges and smooth colors.
2. **Cartoonize Video**: Processes each frame of an uploaded video to apply a cartoon effect and combines them into a new video.
3. **Download Output**: Both cartoonized images and videos can be downloaded directly from the application.

---

## **Steps for Image Cartoonization**
### **Step 1**: Import Required Libraries
- **CV2**: For image processing.
- **easygui**: For file selection dialog.
- **NumPy**: To handle arrays for pixel values.
- **ImageIO**: For reading and saving files.
- **Matplotlib**: For visualizing transformations.
- **OS**: For file path handling.

### **Step 2**: Select Image
- A file box is displayed using `easygui` to choose an image.

### **Step 3**: Read and Store the Image
- Images are read as NumPy arrays using `cv2.imread()` for processing.

### **Step 4**: Grayscale Transformation
- Convert the image to grayscale using `cv2.cvtColor()` with the `BGR2GRAY` flag.

### **Step 5**: Smoothening the Grayscale Image
- Apply `cv2.medianBlur()` for a blur effect to smoothen the image.

### **Step 6**: Edge Detection
- Use adaptive thresholding to highlight edges in the image.

### **Step 7**: Create a Smoothened Mask
- Apply `cv2.bilateralFilter()` to create a smoothened and color-enhanced version of the image.

### **Step 8**: Combine Edge and Smooth Mask
- Combine the edges and smooth mask using `cv2.bitwise_and()` to produce the cartoon effect.

---

## **Steps for Video Cartoonization**
1. **Upload Video**: A video file is selected for processing.
2. **Process Each Frame**: Each frame of the video is cartoonized using the same steps as the image cartoonization process.
3. **Combine Frames**: All processed frames are combined into a cartoonized video.
4. **Download**: The cartoonized video is made available for download.

---

## **User Interface**
The application is built with **Streamlit**:
- **Upload Option**: Allows users to upload images (`.jpg`, `.png`) and videos (`.mp4`, `.avi`).
- **Preview Option**: Displays both the original and cartoonized versions.
- **Download Button**: Enables downloading of cartoonized outputs.

---

## **How to Use**
1. **Upload Image or Video**: Click on the "Choose File" button to upload a file.
2. **View Cartoonized Output**: View the cartoon effect applied to your uploaded image or video.
3. **Download**: Click the "Download" button to save the cartoonized output to your device.

---

## **Technologies Used**
- **OpenCV**: For image and video processing.
- **NumPy**: For handling numerical computations.
- **Streamlit**: For creating a user-friendly interface.
- **Matplotlib**: For plotting image transformations.

---

## **How to Run Locally**
1. Clone the repository:
   ```bash
   git clone https://github.com/apekshachandak1/Image-or-video-into-cartonize-effect-.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Image-or-video-into-cartonize-effect-
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Run the application:
   ```bash
   streamlit run app.py
   ```
5. Open the local Streamlit URL in a browser to use the application.

---

## **Future Enhancements**
- Adding additional cartoon styles.
- Improving processing speed for large videos.
- Extending the application for real-time webcam video processing.
