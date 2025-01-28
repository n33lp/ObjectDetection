# Object Detection using OpenCV

OpenCV provides robust methods for object detection using pre-trained models. It supports various object detection models by accepting their respective weight and config files. One can leverage OpenCV to obtain confidence thresholds and bounding box coordinates, which can then be used to plot bounding boxes and label detected objects efficiently. OpenCV also implements Non-maximum Suppression (NMS) to eliminate redundant overlapping detections, only retaining the highest confidence detection for each object.

## Getting Started

Before you begin, ensure you have the following files:
- **coco.names**: Contains the names of objects that the model can detect. The model outputs an integer corresponding to these names during detection.
- **frozen_inference_graph.pb**: This is the weights file, containing the tuned parameters of the model from training on a large dataset. To detect new objects, you would update these weights through retraining.
- **ssd_mobilenet_v3_large_coco_2020_01_14.pbtxt**: A config file for running the SSD MobileNet model through OpenCV. This file outlines necessary parameters for proper execution.

## Setup Environment
### For Windows:

1. **Open your command prompt** and navigate to your project directory:
    ```bash cd path\to\your\project```

2. **Install the virtual environment package** if it is not installed:
    ```bash pip install virtualenv```

3. **Create the virtual environment**:
    ```bash virtualenv venv```

4. **Activate the virtual environment**:
    ```bash .\venv\Scripts\activate```

### For macOS and Linux:

1. **Open your terminal** and navigate to your project directory:
    ```cd path/to/your/project```

2. **Install the virtual environment package** if it is not installed:
    ```pip install virtualenv```

3. **Create the virtual environment**:
    ```python3 -m venv venv```

4. **Activate the virtual environment**:
    ```source venv/bin/activate```

## Installing Dependencies

Once the virtual environment is activated, you can install the required packages from the `requirements.txt` file: ```pip install -r requirements.txt```  

## Run the Detection
# Navigate to the source folder and execute the main script to start object detection:
```python3 source/main_webcam.py```