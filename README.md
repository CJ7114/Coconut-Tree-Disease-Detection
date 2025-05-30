# Coconut Tree Disease Detection

This project uses YOLOv5 to detect and classify various diseases in coconut trees. The model is designed to identify five different types of diseases:

1. Bud Root Dropping
2. Bud Rot
3. Gray Leaf Spot
4. Leaf Rot
5. Stem Bleeding

## Project Structure

```
coconutreedet/
├── yolov5/          # YOLOv5 implementation
├── data/            # Dataset directory (not included in repo)
│   ├── train/       # Training images
│   ├── val/         # Validation images
│   └── test/        # Test images
└── conum.yaml       # Dataset configuration file
```

## Setup

1. Clone the repository:
```bash
git clone https://github.com/[your-username]/coconutreedet.git
cd coconutreedet
```

2. Create a virtual environment and install dependencies:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Prepare your dataset:
   - Organize your images in the data directory
   - Update `conum.yaml` with your dataset path

## Training

To train the model:

```bash
python train.py --img 640 --batch 16 --epochs 100 --data conum.yaml --weights yolov5s.pt
```

## Inference

To run inference on new images:

```bash
python detect.py --source path/to/images --weights runs/train/exp/weights/best.pt
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- This project uses [YOLOv5](https://github.com/ultralytics/yolov5) by Ultralytics 