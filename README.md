# Face Recognition Project

-> Overview
This project implements a real-time face recognition system using Python, OpenCV, and the face_recognition library. The system is designed to recognize faces from a pre-trained dataset of images and identify individuals in a live video feed from a webcam. It serves as an educational example of computer vision and machine learning applications in facial recognition technology.


-> Features
Real-time Face Detection: Utilizes OpenCV and the face_recognition library to detect faces in live video streams.
Face Encoding and Comparison: Encodes facial features from training images and compares them against detected faces in real-time.
Multi-face Recognition: Capable of detecting and identifying multiple faces simultaneously in the video feed.
Unknown Person Handling: Labels unrecognized faces as "Unknown Person" to handle cases where the face doesn't match any trained individuals.
Interactive Video Display: Displays the video feed with bounding boxes around detected faces and overlaid names.
Simple Training Dataset: Uses a collection of images stored in the images/ directory for training the recognition model.

-> Technologies Used
Python: Core programming language.
OpenCV (cv2): For image processing and video capture.
NumPy: For numerical operations and array handling.
face_recognition: A powerful library built on dlib for face detection and recognition.
Installation
Prerequisites
Python 3.7 or higher
Webcam (for real-time recognition)

-> Dependencies
Install the required libraries using pip:

Note: The face_recognition library requires additional system dependencies. On Windows, you may need to install Visual Studio Build Tools. Refer to the face_recognition documentation for detailed installation instructions.

Usage

-> Prepare Training Images:
Place images of individuals you want to recognize in the images/ folder.
Name the image files with the person's name (e.g., john.jpg, jane.png).
The system currently includes sample images of soccer players: Lewandowski, Messi, Neymar, Pedri, and Raphinha.

Run the Notebook:

Open face.ipynb in Jupyter Notebook or JupyterLab.
Execute the cells in order to train the model and start the recognition process.
Real-time Recognition:

The final cell opens your webcam and starts real-time face recognition.
Detected faces will be highlighted with red rectangles.
Recognized individuals will have their names displayed above the bounding box.
Unrecognized faces will be labeled as "Unknown Person".
Press 'q' to stop the video feed and exit the program.
How It Works
Training Phase:

The system loads all images from the images/ directory.
For each image, it detects the face location and encodes the facial features into a numerical representation.
These encodings are stored as the "trained" data for comparison.
Recognition Phase:

The webcam captures video frames continuously.
Each frame is processed to detect faces and encode their features.
The encoded features are compared against the trained encodings using face distance calculations.
The closest match (smallest distance) determines the recognized person.
A threshold is implicitly used through the compare_faces function to determine if a match is valid.
Display:

Bounding boxes are drawn around detected faces.
Names are overlaid on the video feed for recognized individuals.
Project Structure
Limitations and Considerations
Training Dataset Size: The current implementation uses only 5 training images. For better accuracy, a larger and more diverse dataset is recommended.
Lighting and Angle Variations: The system's performance may vary with different lighting conditions, face angles, and occlusions.
Processing Speed: Real-time processing depends on hardware capabilities. Face recognition can be computationally intensive.
Privacy Concerns: Facial recognition technology raises important privacy and ethical considerations. Use responsibly and in compliance with applicable laws.
Single Face per Image: The training assumes one face per image. Multiple faces in training images may cause issues.
Future Improvements
Implement face registration functionality to add new faces dynamically.
Add confidence scores for recognition results.
Integrate with databases for larger-scale face storage and retrieval.
Optimize performance for mobile or edge devices.
Add age, gender, or emotion detection features.
Implement face tracking across video frames for smoother recognition.
Contributing
Contributions to improve the project are welcome! Please:

Fork the repository.
Create a feature branch.
Make your changes.
Test thoroughly.
Submit a pull request with a clear description of the changes.
License
This project is open-source and available under the MIT License. Feel free to use, modify, and distribute the code.

Acknowledgments
This project uses the face_recognition library by Adam Geitgey.
Sample images are of public figures (soccer players) for demonstration purposes.
Disclaimer
This face recognition system is for educational and demonstrative purposes only. It may not be suitable for production use without further testing, optimization, and consideration of accuracy, bias, and privacy implications. Always respect individuals' privacy and comply with relevant data protection regulations when implementing facial recognition technology.
