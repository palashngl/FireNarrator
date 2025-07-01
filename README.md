# 🔥 FireNarrator: A Multimodal Fire Incident Reporting Framework

FireNarrator is a real-time multimodal fire understanding system that fuses visual (RGB image) and temporal sensor data to generate human-readable fire incident reports using large language models (LLMs). It combines deep vision classification (CNN), temporal severity estimation (Transformer), decision logic, and narrative generation via a fine-tuned FLAN-T5 model.

---

## 🧠 Core Components

1. **VisionInferNet**\
   A CNN-based fire classification model using Xception + SE attention, trained to detect fire types (e.g., building fire, forest fire).

2. **SensorFlameNet**\
   A Transformer-based model that performs temporal reasoning on multivariate sensor streams to estimate fire severity.

3. **Decision Engine**\
   Applies rule-based logic to decide safety actions based on class and severity.

4. **Structured-to-Text Generator**\
   A fine-tuned FLAN-T5 LLM that converts multimodal prompts into structured, fluent incident narratives.

---

## 📊 System Architecture



> 🔗 See [our paper](link-to-paper) for full methodology, equations, and experimental details.

---

## 🚀 Getting Started

### 🔧 Installation

```bash
git clone https://github.com/yourusername/FireNarrator.git
cd FireNarrator
pip install -r requirements.txt
```

Make sure to install:

- `tensorflow==2.15`
- `transformers`
- `scikit-learn`
- `pandas`, `matplotlib`
- `tqdm`, `sentencepiece`

---

## 📂 Dataset

The dataset includes:

- RGB fire images (`images/`)
- Aligned sensor readings (`sensor_data.csv`)
- Class and severity labels (`labels.csv`)

You can request the dataset via [dataset\_request.md](link-to-form).

---

## 🧪 Testing

You can test the FireNarrator pipeline using the provided notebook:

📄 [`FireNarrator.ipynb`](./FireNarrator.ipynb)

### Example:

1. Launch Jupyter:

```bash
jupyter notebook
```

2. Open `FireNarrator.ipynb`
3. Upload your test image and sensor CSV
4. Run all cells to view classification, severity score, and narrative output

---

## 📖 Citation

If you use FireNarrator in your research, please cite:

```bibtex
@inproceedings{ingle2025firenarrator,
  title={FireNarrator: A Multimodal Fire Incident Reporting Framework with Sensor Fusion and LLMs},
  author={Ingle, Palash Yuvraj and Amael, Joshua Tito and Kim, Young Gab},
  booktitle={Proceedings of the IEEE International Conference},
  year={2025}
}
```

---

## 🤝 Contributors

- [Palash Yuvraj Ingle](mailto\:palash@sejong.ac.kr)
- [Prof. Young Gab-Kim](mailto\:alwaysgabi@sejong.ac.kr)

---

## 📌 License

This project is licensed under the MIT License. See `LICENSE` for more details.

---

## 💡 Future Work

- Integrate real-time drone video stream input
- Expand dataset with real-world fire incidents
- Add multilingual report generation


