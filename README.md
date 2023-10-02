#!/bin/bash

# Create README file
cat <<EOF > README.md
# Image Face Pixelation

This repository contains code that applies pixelation and blurring effects to faces detected in an image using OpenCV. The code utilizes the Haar cascade classifier for face detection and provides functions for blurring and pixelating the face regions.

## Prerequisites

- Python 3.x
- OpenCV
- NumPy

## Installation

1. Clone the repository:

   \`\`\`shell
   git clone https://github.com/your-username/your-repo.git
   \`\`\`

2. Install the required dependencies:

   \`\`\`shell
   pip install opencv-python numpy
   \`\`\`

3. Download the Haar cascade classifier file (\`haarcascade_frontalface_default.xml\`) and place it in the same directory as the code file. You can find the file in the OpenCV GitHub repository: [haarcascade_frontalface_default.xml](https://github.com/opencv/opencv/blob/master/data/haarcascades/haarcascade_frontalface_default.xml)

## Usage

1. Modify the code file to specify the input image file path:

   \`\`\`python
   image = cv2.imread('path/to/your/image.jpg')
   \`\`\`

2. Run the code:

   \`\`\`shell
   python your_code_file.py
   \`\`\`

   The code will detect faces in the image, pixelate the face regions, and display the modified image.

## Customization

- Kernel Size Factor: Adjust the \`factor\` variable to change the kernel size for blurring. Higher values result in stronger blurring effects.

- Number of Blocks: The \`blocks\` parameter in the \`pixelate_face\` function determines the number of blocks used for pixelation. Increasing the value will result in smaller pixelated regions.

## License

This project is licensed under the [MIT License](LICENSE).

Feel free to use and modify the code according to your needs.

## Acknowledgements

The face detection and pixelation techniques utilized in this code are based on the OpenCV library. Special thanks to the OpenCV community for their contributions.

If you find this code useful, please consider giving a star to this repository.
EOF

echo "README file generated successfully!"
