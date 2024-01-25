
# YOLOv8 People Counting and Tracking

## Overview
This project utilizes YOLOv8, a state-of-the-art real-time object detection system, to count people entering a bus and track their movements. The goal is to provide an efficient and accurate solution for monitoring passenger traffic.

## Project Structure

### 1. Installation
Ensure you have the necessary dependencies installed by following the instructions in the `requirements.txt` file.

```bash
pip install -r requirements.txt
```

### 2. Data Preparation
Prepare your dataset or use pre-existing datasets containing bus footage for training and testing.

### 3. Model Training
Train the YOLOv8 model on your dataset to enable it to detect and track people entering the bus. Update configurations and hyperparameters as needed.

```bash
python train.py --data data.yaml --cfg yolov8-custom.cfg --weights '' --batch-size 16 --epochs 300 --device 0
```

### 4. Inference
Run the trained model on new bus footage to count and track people. Adjust confidence thresholds and other parameters for optimal results.

```bash
python detect.py --source <your_video_or_image_path> --weights <path_to_trained_weights> --conf 0.5
```

### 5. Results and Analysis
Evaluate the model's performance, analyze results, and fine-tune parameters if necessary. This may involve adjusting IOU thresholds, confidence levels, etc.

## Important Notes

- Ensure CUDA and cuDNN are properly configured for GPU acceleration.
- Customize the YOLOv8 configuration file (`yolov8-custom.cfg`) based on your specific requirements.
- Use the `--weights` flag in `detect.py` to load the trained weights for inference.

## Acknowledgments
This project builds upon the YOLOv8 architecture, and we extend our gratitude to the YOLO community for their contributions.

