# AI Image Recognition Dashboard - README

## Project Overview
This project analyzes an image and identifies what object it contains, using ResNet50 (a pre-trained deep learning model). The result is displayed in a clean visual dashboard showing the image, top 5 predictions, final answer, and model information.

## Output Screenshot

<img width="1364" height="669" alt="image" src="https://github.com/user-attachments/assets/cb4ec04a-8d3f-4d94-b492-28f5db437c72" />

## Features
- Uses a pre-trained ResNet50 model (trained on the ImageNet dataset, 1000 classes)
- Analyzes any image and returns the top 5 possible predictions with confidence percentages
- Clean, dark-themed dashboard (built with matplotlib) showing:
  - Input image
  - Top 5 predictions bar chart
  - Final prediction card
  - Model information card

## Requirements
The following libraries are needed:
```
torch
torchvision
pillow
matplotlib
```

To install:
```
pip install torch torchvision pillow matplotlib
```

## How to Run
1. Name your image `image.jpg`
2. Place it in the same folder as `project_4_fixed.py`
3. Run the file name in terminal
```
python project_4_fixed.p
```
4. The top 5 predictions will print in the terminal, and a dashboard window will open.

## How It Works
1. The image is loaded and preprocessed into the format required by ResNet50
2. The model analyzes the image and produces probabilities across 1000 classes
3. The softmax function converts these probabilities into percentages
4. The top 5 highest-confidence classes are selected
5. Everything is displayed visually in a dashboard (built using GridSpec layout so no elements overlap)

## Notes
- Confidence scores may appear low if the image contains multiple visually similar classes (e.g., different car types) — this is normal, not a bug.
- If `image.jpg` is not found, the script will show an error and stop.
