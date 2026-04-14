# CNN Experiments on iCoSimal V3 Dataset

**MSE FTP Deep Learning - Mandatory Practical Work 01**

Deadline: Tuesday 14 April, 15:00

## Group Members

- Student 1: Marcos, Costa
- Student 2: Jose Pablo, Muñoz
- Student 3: Artemii, Ponomarenko

## Experiments

### Mandatory

| Experiment      | Objective                                                                  |
| --------------- | -------------------------------------------------------------------------- |
| CNN Depth       | Compare shallow (1 conv) vs medium (3 conv) vs deep (5 conv) architectures |
| Hyperparameters | Tune learning rate and batch size                                          |
| Fitting         | Demonstrate overfitting and underfitting                                   |
| Optimizers      | Compare SGD, RMSprop, Adam, SGD + Momentum                                 |
| Regularization  | Test dropout and weight decay                                              |

### Optional (we chose these 4)

| Experiment        | Objective                                     |
| ----------------- | --------------------------------------------- |
| Data Augmentation | Improve generalization with transforms        |
| Error Analysis    | Identify common misclassifications            |
| ResNet            | Compare with pretrained ResNet                |
| W&B Monitoring    | Track all experiments (integrated throughout) |

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

### 5. Run Experiments

```bash
jupyter notebook cnn_experiments.ipynb
```
