# image-filter
Image Edge Detection using Custom Filters
This project demonstrates basic image filtering techniques using custom-designed kernels to highlight horizontal, vertical, and diagonal edges in a grayscale image.

📂 Requirements
Make sure you have the following Python libraries installed:

pip install opencv-python numpy matplotlib pandas
📸 Input Image
Ensure that you have an image named filter.jpg in the same directory as the script. The image will be loaded in grayscale mode.

🧠 Filtering Logic
We define three custom convolution kernels to detect edges in different directions:

1. Horizontal Kernel
horizontal_kernel = np.array([
    [-1, -1, -1],
    [-10, -10, -10],
    [ 1,  1,  1]
])
2. Vertical Kernel
vertical_kernel = np.array([
    [-1, -10,  1],
    [-10, -10, 10],
    [-1, -10,  1]
])
3. Diagonal Kernel
diagonal_kernel = np.array([
    [-10, -1, -1],
    [ 1, -10, -1],
    [ 1,  1, -10]
])
These kernels are applied using cv2.filter2D() which performs a 2D convolution.

🖼️ Output
The output consists of four subplots:

Original Image

Horizontal Edge Filtered Image

Vertical Edge Filtered Image

Diagonal Edge Filtered Image

Each image is displayed using matplotlib.

