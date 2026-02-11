# 📖Personal Troubleshooting Handbook

This repository serves as a record for the issues that I ran into whilst tinkering and learning Pytorch - I personally play a guitar thus I used guitar analogy to aid my learning.

## 🎸 The "Amp" Analogy: Tuning the Model
Deep learning models are like high-end guitar amplifiers. To get the best "tone" (accuracy), you have to tweak specific "knobs" within the code.

* **Gain (Learning Rate):** Controlled via `optim.Adam(..., lr=0.001)`. If too high, the model "screams" (loss fluctuates); if too low, it's too quiet to learn.
* **Buffer (Batch Size):** Managed in the `DataLoader`. Higher values utilize more of the **NVIDIA RTX 2080 Super's 8GB VRAM** for faster training.
* **Rehearsal (Epochs):** The number of times the model sees the training set. Over-rehearsing can lead to **Overfitting** (memorizing instead of understanding).

## 🛠️ Environment Configuration
This project is optimized for **Python 3.11**. Due to library stability, newer versions (like 3.14) may not be compatible with current PyTorch wheels.

**Installation for GPU Acceleration (CUDA 12.1):**
```bash
pip3 install torch torchvision torchaudio --index-url [https://download.pytorch.org/whl/cu121](https://download.pytorch.org/whl/cu121)
```

## 📄 Troubleshooting
See my `pytorch_Troubleshoot-Manual.txt` for the specific errors I ran into and their fixes.
