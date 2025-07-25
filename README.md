# Face Recognition System

A real-time face recognition system built with Python, OpenCV, and dlib. This project can detect faces in video streams and compare them against known face encodings.

## Features

- Real-time face detection and recognition
- Video stream processing (webcam support)
- Face encoding generation and storage
- High-accuracy face matching using dlib
- Cross-platform compatibility

## Prerequisites

- Python 3.8+ (recommended for best compatibility with dlib)
- OpenCV
- dlib
- face_recognition library
- numpy

## Installation

### 1. Clone the repository
```bash
git clone <repository-url>
cd "Face Recog"
```

### 2. Set up Python environment
For best compatibility with dlib, it's recommended to use Python 3.8:

#### Using pyenv (recommended):
```bash
# Install pyenv if not already installed
sudo pacman -S pyenv

# Install Python 3.8
pyenv install 3.8.18

# Set local Python version
pyenv local 3.8.18

# Create virtual environment
python -m venv venv
source venv/bin/activate
```

#### Alternative: Use system Python
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install --upgrade pip
pip install dlib
pip install face-recognition
pip install opencv-python
pip install numpy
```

## Usage

1. **Run the main application:**
   ```bash
   python main.py
   ```

2. **Add known faces:**
   - Place face images in a `known_faces` directory
   - The system will automatically encode and store them

3. **Real-time recognition:**
   - The application will access your webcam
   - Detected faces will be compared against known faces
   - Results will be displayed in real-time

## Project Structure

```
Face Recog/
├── main.py              # Main application file
├── known_faces/         # Directory for known face images
├── venv/               # Virtual environment
├── README.md           # This file
└── LICENSE             # MIT License
```

## Configuration

- **Camera index**: Modify the camera index in `main.py` if using a different camera
- **Face detection model**: The system uses dlib's CNN face detection model
- **Recognition tolerance**: Adjust the tolerance value for face matching accuracy

## Troubleshooting

### Common Issues:

1. **dlib installation fails:**
   - Ensure you have the required system dependencies
   - Try installing with conda: `conda install -c conda-forge dlib`

2. **Camera access issues:**
   - Check camera permissions
   - Verify camera is not being used by another application

3. **Performance issues:**
   - Reduce video resolution
   - Lower the number of known faces
   - Use GPU acceleration if available

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [dlib](http://dlib.net/) - Machine learning library
- [face_recognition](https://github.com/ageitgey/face_recognition) - Face recognition library
- [OpenCV](https://opencv.org/) - Computer vision library

## Support

If you encounter any issues or have questions, please open an issue on the project repository. 