# Car and People Counter

Car and People Counter is a Python application that uses the YOLO (You Only Look Once) object detection model to count cars in a video stream and count people in a mall moving up and down on an escalator. The application detects cars and people in the video, tracks them, and provides real-time counting within specified regions.

## Features

- Real-time car detection and counting.
- Real-time people detection and counting on an escalator.
- Modern-looking rectangles and text overlays.
- Region-based counting (e.g., counting cars moving up and down or people on an escalator).

## Requirements

To run this application, you'll need the following dependencies:

- Python 3.x
- OpenCV
- Numpy
- YOLO pre-trained model weights (e.g., yolov8l.pt)
- cvzone
- sort (Simple Online and Realtime Tracking algorithm)
- Montserrat-Bold.ttf (for modern text rendering)

You can install most of these dependencies using pip:

```bash
pip install opencv-python numpy cvzone
```

You can download the YOLO pre-trained model weights from [YOLO website](https://pjreddie.com/darknet/yolo/).

## Folder Structure

- `car_counter/`: Contains the car counting application.
- `people_counter/`: Contains the people counting application for the escalator.

## Usage

### Car Counter

1. Clone this repository:

```bash
git clone https://github.com/your-username/car-and-people-counter.git
cd car-and-people-counter
```

2. Place your YOLO pre-trained model weights (`yolov8l.pt`) in the project directory.

3. Create a mask image named `mask.png` to define the region of interest (ROI) for car counting.

4. Create a graphics image named `graphics.png` for modern overlays (optional).

5. Run the car counter:

```bash
python car_counter.py
```

The car counter application will open a video stream and display the car counting results in real-time. You can customize the regions of interest, fonts, and other parameters within the code.

### People Counter

1. Navigate to the `people_counter/` folder:

```bash
cd people_counter
```

2. Place your YOLO pre-trained model weights (`yolov8l.pt`) in the `people_counter/` folder.

3. Create a mask image named `mask.png` to define the region of interest (ROI) for people counting.

4. Create a graphics image named `graphics.png` for modern overlays (optional).

5. Run the people counter for the escalator:

```bash
python people_counter.py
```

The people counter application will open a video stream and display the people counting results in real-time as they move up and down on the escalator. You can customize the regions of interest, fonts, and other parameters within the code.

## Configuration

You can customize the following parameters in the respective `.py` files (`car_counter.py` and `people_counter.py`):

- Video source (e.g., a video file or camera stream).
- YOLO model weights file path (`YOLO_WEIGHTS`).
- Class names for object detection (`CLASS_NAMES`).
- Region of interest limits (e.g., `limitsUp` and `limitsDown` for the escalator).
- Font file for modern text rendering (`font`).


*Note: This project is inspired by Murtaza's Workshop object detection tutorial.*

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


## Acknowledgments

*Note: This project is inspired by Murtaza's Workshop object detection tutorial.*

- This project uses the YOLO object detection model, courtesy of Joseph Redmon and Ali Farhadi. [YOLO website](https://pjreddie.com/darknet/yolo/)
- The SORT (Simple Online and Realtime Tracking) algorithm is used for object tracking. [SORT GitHub](https://github.com/abewley/sort)

```

Feel free to replace `your-username` with your actual GitHub username when sharing this on your GitHub repository. This updated README includes information about both the car counter and the people counter applications, with separate usage instructions for each.
```
