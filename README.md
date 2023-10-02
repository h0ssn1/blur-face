
# Blured Face in personal images

I have implemented a code that detects faces using haarcascade_frontalface and blurs the face of the user in the image.

My own Image :)

## Screenshots

![App Screenshot](https://drive.google.com/file/d/1xBfvr6unwme_pxLq-pdJRCxn59YlMaKZ/view?usp=sharing)

## Documentation

The blur function takes an input image (img) and a kernel size factor (k). It calculates the height (h) and width (w) of the image, and then determines the kernel size (kh, kw) by dividing the height and width by the factor. If the calculated kernel size is even, it subtracts 1 to make it odd. Finally, it applies Gaussian blur to the image using the calculated kernel size and sigmaX=0, and returns the blurred image.

The pixelate_face function takes an input image (image) and the number of blocks (blocks) for pixelation. It divides the image into blocks x blocks regions by computing the x and y steps based on the width and height of the image. It then loops over these regions and for each region, it extracts the corresponding ROI (Region of Interest) from the image. It calculates the mean RGB values of the ROI and draws a rectangle with the mean RGB values over the ROI in the original image. This process effectively pixelates the face regions in the image. Finally, it returns the pixelated image.

The code defines a variable factor which represents the kernel size factor for blurring.

It reads an image using cv2.imread from the specified file path.

The image is converted to grayscale using cv2.cvtColor to simplify face detection.

The Haar cascade classifier (haarcascade_frontalface_default.xml) is loaded using cv2.CascadeClassifier.

The detectMultiScale function is used to detect faces in the grayscale image. It takes the grayscale image, a scale factor of 1.5, and a minimum number of neighbors of 5 as parameters. The function returns a list of rectangles representing the detected faces in the image.

For each detected face, the corresponding region is extracted from the original image using array slicing (image[y:y + h, x:x + w]). The blur and pixelate_face functions are then applied to the extracted face region to blur and pixelate it.

Finally, the modified image is displayed using cv2_imshow.


![Logo](https://qph.cf2.quoracdn.net/main-qimg-28cadbd02699c25a88e5c78d73c7babc)
![Logo](https://editor.analyticsvidhya.com/uploads/95103cv.png)


## Roadmap

-Phase 1: Setting Up the Project
   Create a new GitHub repository for the project.
   Initialize the repository with a README file.
   Clone the repository to your local machine.
   Set up the project structure and file organization.
-Phase 2: Dependencies and Environment Setup
   Identify and list the necessary dependencies for the  code.
   Create a virtual environment for the project.
   Install the required dependencies (OpenCV, NumPy) in  the virtual environment.
-Phase 3: Face Detection and Pixelation Functions
   Implement the blur function to perform image blurring.
   Implement the pixelate_face function to pixelate the  face regions.
   Test the functions individually to ensure they are working correctly.

## Authors

- [Hosein Madadi](https://www.github.com/h0ssn1)

