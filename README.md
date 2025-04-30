# my_lvcaiquexian_01

The dataset is too large to be uploaded directly to GitHub. It has been uploaded to Baidu Netdisk instead:

- Download link: [Click to access Baidu Netdisk](https://pan.baidu.com/s/1yReEiaqf6Yty2FdqNmkQvA)  
- Extraction code: 8y3g

Please download and extract the dataset before using it according to the project instructions.

---

# my_lvcaquexian_01

## 📦 Dataset

The training dataset is too large to be uploaded directly to GitHub. It has been uploaded to Baidu Netdisk instead:

- **Download link**: [Click to access Baidu Netdisk](https://pan.baidu.com/s/1yReEiaqf6Yty2FdqNmkQvA)
- **Extraction code**: `8y3g`

After downloading, extract the dataset and place it in the `datasets/` folder of this project.

---

## 🧠 my_lvcaquexian_01 Training Guide

This project uses the **YOLOv11** model for training on a custom dataset. Follow these steps to set up and train the model:

### 1. Environment Setup

Make sure you are using Python ≥ 3.8, and create a virtual environment (optional but recommended):

```bash
python -m venv yolov11-env
source yolov11-env/bin/activate  # On Windows: yolov11-env\Scripts\activate
```

Install all required dependencies:

```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing, install Ultralytics YOLO manually:

```bash
pip install ultralytics
```

---

### 2. Dataset Placement

After downloading the dataset from Baidu Netdisk, extract and place it in:

```bash
datasets/my_dataset/
```

Make sure the folder includes images and labels in YOLO format, and you have a corresponding `data.yaml` file pointing to it.

---

### 3. Training Command

Use the following command to train the model:

```bash
python train.py --img 640 --batch 16 --epochs 300 --data data.yaml --cfg yolov11.yaml --weights '' --name yolov11_exp
```

Explanation of key parameters:

- `--img`: image resolution (e.g., 640)
- `--batch`: batch size (e.g., 16)
- `--epochs`: number of epochs (e.g., 300)
- `--data`: path to your `data.yaml`
- `--cfg`: model architecture file (e.g., yolov11.yaml)
- `--weights`: set to `''` to train from scratch
- `--name`: experiment name, will be used for saving logs and results

---

### 4. Results and Checkpoints

After training:

- All outputs (model weights, training logs, results) will be saved in:
  ```bash
  runs/train/yolov11_exp/
  ```
- Best weights can be found at:
  ```
  runs/train/yolov11_exp/weights/best.pt
  ```

You can use these weights later for validation or inference.



