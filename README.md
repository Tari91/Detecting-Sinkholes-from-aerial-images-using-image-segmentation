This project demonstrates how to detect **sinkholes** from aerial imagery using **semantic segmentation** with a U-Net deep learning model. It generates synthetic data for training, performs segmentation using PyTorch, and exports results to an **Excel report with visual mask comparisons**.

---

## 📸 Sample Output

| Original Image | Ground Truth Mask | Predicted Mask |
|----------------|-------------------|----------------|
| ![img](https://via.placeholder.com/64) | ![gt](https://via.placeholder.com/64) | ![pred](https://via.placeholder.com/64) |

---

## 🚀 **Features**

✅ Synthetic aerial image generation  
✅ U-Net segmentation with PyTorch  
✅ Pixel-wise IoU evaluation  
✅ Excel report with embedded mask previews  
✅ Easily extendable to real aerial/satellite datasets  

---

## 🔧 Installation

```bash
pip install torch torchvision matplotlib pandas openpyxl scikit-learn
📁 Project Structure
bash
Copy
Edit
.
├── sinkhole_segmentation.py      # Main training & evaluation script
├── exported_masks/               # Saved mask images (GT and Prediction)
├── sinkhole_results.xlsx         # Final report with visuals
└── README.md
🧠 Model: U-Net Architecture
The U-Net model is a symmetric encoder-decoder architecture ideal for segmentation tasks, especially with limited training data.

css
Copy
Edit
Input --> [Encoder] --> Bottleneck --> [Decoder] --> Output (Mask)
It uses skip connections to preserve spatial information for precise segmentation.

🧪 How to Use
bash
Copy
Edit
python sinkhole_segmentation.py
After training, results will be saved as:

bash
Copy
Edit
sinkhole_results.xlsx
exported_masks/
├── gt_0.png
├── pred_0.png
...
📊 Excel Report Format
Image ID	GT Pixels	Predicted Pixels	IoU Score	GT Mask	Prediction Mask
0	612	580	0.8912	✅ Img	✅ Img

🔬 Evaluation Metric
IoU (Intersection over Union): Measures overlap between predicted and ground truth masks.

Binary Cross Entropy: Used as the training loss function.

🌱 Future Improvements
 Integrate real aerial/satellite datasets (e.g., UAV or Sentinel-2)

 Add data augmentation and noise simulation

 Build a lightweight web interface with Gradio/Streamlit

 Deploy to Hugging Face Spaces or Google Colab

👤 Author
Tarinabo williamtarinabo@gmail.com
