# CNN Experiments on iCoSimal V3 Dataset

**MSE FTP Deep Learning - Mandatory Practical Work 01**

Deadline: Tuesday 14 April, 15:00

## Group Members
- Student 1: Marcos, Costa
- Student 2: Jose Pablo, Munoz
- Student 3: Artemii, Ponomarenko

## Overview

This project explores CNN architectures for animal image classification using the iCoSimal V3 dataset (30,000 images, 10 classes).

## Setup

### 1. Clone the repo
```bash
git clone https://github.com/marcosncosta1/DeepLearning_practical_1.git
cd DeepLearning_practical_1
```

### 2. Create virtual environment
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install torch torchvision matplotlib wandb tqdm numpy
```

### 4. Setup Weights & Biases
```bash
# Create free account at https://wandb.ai if you don't have one
wandb login
```
Follow the prompts to authenticate. All experiments will be logged to W&B automatically.

### 5. Download the dataset
Download iCoSimal V3 from the course link and extract to `data/`:

```
data/
├── train/
│   ├── cat/
│   ├── chicken/
│   ├── cow/
│   ├── dog/
│   ├── elephant/
│   ├── horse/
│   ├── rabbit/
│   ├── sheep/
│   ├── squirrel/
│   └── zebra/
└── validate/
    └── (same 10 classes)
```

## Run Experiments

```bash
jupyter notebook cnn_experiments.ipynb
```

Run cells in order. Start with `IMG_SIZE=64` for fast iteration.

## Experiments

### Mandatory
| # | Experiment | Objective |
|---|------------|-----------|
| A | CNN Depth | Compare shallow (1 conv) vs deep (5 conv) architectures |
| B | Hyperparameters | Tune learning rate and batch size |
| C | Fitting | Demonstrate overfitting and underfitting |
| D | Regularization | Test dropout and weight decay |
| E | Optimizers | Compare SGD, RMSprop, Adam |

### Optional (we chose these 4)
| # | Experiment | Objective |
|---|------------|-----------|
| F | Error Analysis | Identify common misclassifications |
| G | ResNet | Compare with pretrained ResNet |
| H | Data Augmentation | Improve generalization with transforms |
| - | W&B Monitoring | Track all experiments (integrated throughout) |

## W&B Dashboard

All experiments are automatically logged to Weights & Biases:
- View training curves in real-time
- Compare runs side-by-side
- Track hyperparameters and metrics

Dashboard: `https://wandb.ai/YOUR_USERNAME/icosimal-cnn`

## Project Structure

```
.
├── README.md
├── cnn_experiments.ipynb   # Main notebook
├── INSTRUCTIONS.txt        # Detailed guide
├── .gitignore
├── data/                   # Dataset (not in repo)
└── wandb/                  # W&B logs (auto-generated)
```

## Notes

- Mac users: Apple Silicon (M1/M2/M3) GPUs are supported via MPS
- If you get DataLoader errors, set `NUM_WORKERS = 0`
- Fill in "YOUR OBSERVATIONS HERE" sections before submitting

## Submission

- Format: PDF or .ipynb
- Include group member names
- Add W&B dashboard screenshots
