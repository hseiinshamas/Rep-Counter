```markdown
# Biceps Rep Counter

This project is a Python-based application that uses computer vision to count bicep curls (reps) in real-time. The system captures video frames from a camera, processes them to detect the movement of the user's arm, and counts the number of reps. The application uses a machine learning model to classify the movement as either "extended" or "contracted" to determine when a rep is completed.

## Features
- **Real-time rep counting**: The app counts bicep curls as you perform them, displaying the total count on the screen.
- **Camera integration**: Uses a camera feed to track the user's arm position.
- **Model training**: Train the system with custom "extended" and "contracted" arm positions for better accuracy.
- **GUI**: Built with Tkinter to provide a simple user interface for toggling the counting, training the model, and resetting the count.

## Requirements
- Python 3.x
- OpenCV
- PIL (Pillow)
- scikit-learn
- Tkinter (usually comes with Python)
- Camera device (webcam or external camera)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/biceps-rep-counter.git
   cd biceps-rep-counter
   ```

2. Install the required dependencies:
   ```bash
   pip install opencv-python Pillow scikit-learn
   ```

3. Ensure that you have a working camera connected to your system.

## Usage

1. Run the `main.py` script:
   ```bash
   python main.py
   ```

2. The app will open a window displaying the camera feed. You will see the following buttons:
   - **Toggle Counting**: Start or stop the rep counting.
   - **Extended**: Save an image of the arm in an extended position for training the model.
   - **Contracted**: Save an image of the arm in a contracted position for training the model.
   - **Train Model**: Train the model using the images captured for "extended" and "contracted" positions.
   - **Reset**: Reset the rep counter to zero.

3. The system will automatically start counting reps when the "Toggle Counting" button is pressed, detecting arm movements and updating the rep count on the screen.

## How It Works

- **Camera Feed**: The app captures frames from the camera in real-time.
- **Movement Detection**: The model classifies the arm position as either "extended" or "contracted" using a Linear Support Vector Classifier (SVC).
- **Rep Counting**: When both "extended" and "contracted" movements are detected in sequence, the rep counter is incremented.

## Model Training

- The model is trained using images of the user's arm in two distinct positions: "extended" and "contracted."
- The images are saved in separate directories (`1` for extended, `2` for contracted).
- After capturing enough training images, the user can train the model by pressing the "Train Model" button.

## Files
- `main.py`: Main script to run the application and interact with the camera feed.
- `model.py`: Contains the machine learning model and training logic using scikit-learn's `LinearSVC`.
- `camera.py`: Manages the camera feed and frame capture.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements
- OpenCV for computer vision tasks.
- scikit-learn for machine learning.
- Tkinter for the graphical user interface.

```

This `README.md` provides a clear explanation of your project, installation instructions, usage, and details about how it works. You can replace `yourusername` in the GitHub clone URL with your actual username.
