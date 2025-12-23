# AudioScene
AudioScene – Image to Audio Description System Built an assistive AI system that generates accurate image captions using pretrained vision–language models and converts them into natural speech for accessibility applications. It is designed to help visually impaired users understand visual scenes using image captioning and text-to-speech technology.

## 🔹 Features
- User image upload
- High-quality image captions using pretrained BLIP
- Natural audio narration (Text-to-Speech)
- Runs entirely in Google Colab

  ## 🧠 Models and Techniques Explored in This Project

### 🔹 Custom Image Captioning Model (Experimental Phase)

As part of the learning and experimentation phase, this project initially implemented a custom image captioning model based on classical deep learning architectures. The model followed an encoder–decoder framework consisting of:

- A Convolutional Neural Network (CNN) encoder to extract visual features from images.
- A Recurrent Neural Network (GRU-based) decoder to generate captions word by word.
- An attention mechanism to improve alignment between image regions and generated words.

This phase helped in understanding the complete captioning pipeline, including sequence modeling and attention-based learning.

---

### 🔹 Bahdanau Attention Mechanism

The custom model incorporated **Bahdanau Attention**, an additive attention mechanism that allows the decoder to dynamically focus on different spatial regions of the image while generating each word in the caption.

Key advantages of using Bahdanau Attention include:
- Improved context awareness during caption generation
- Better alignment between visual features and textual output
- Enhanced interpretability compared to plain encoder–decoder models

This attention-based approach demonstrated meaningful learning but required extensive training and large-scale data to achieve high-quality captions.

---

### 🔹 Limitations Observed

While the attention-based model successfully generated captions, the results were limited by:
- Restricted training time
- Limited computational resources
- The complexity of learning both visual semantics and natural language from scratch

As a result, captions lacked fluency and detailed contextual understanding when compared to large pretrained models.

---

### 🔹 Transition to Pretrained Vision–Language Model (BLIP)

To overcome these limitations and ensure reliable performance for an assistive application, the project transitioned to using **BLIP (Bootstrapping Language–Image Pretraining)**, a state-of-the-art pretrained vision–language model.

BLIP has been trained on large-scale image–text datasets, enabling it to generate accurate, context-aware, and fluent captions without task-specific training. This significantly improved caption quality and made the system suitable for real-world usage.

---

### 🔹 Summary of Approach

This project adopts a **hybrid development strategy**:
- Custom model with Bahdanau Attention for conceptual understanding and experimentation
- Pretrained BLIP model for production-level caption accuracy and robustness

This combination balances theoretical learning with practical performance, aligning well with accessibility-focused applications such as AudioScene.

## 🔹 Technologies Used
- Python
- PyTorch
- Transformers (BLIP)
- gTTS (Text-to-Speech)
- Google Colab

## 🔹 How It Works
1. User uploads an image
2. The system generates a descriptive caption
3. The caption is converted into speech
4. Audio output is played to the user

## 🔹 How to Run (Colab)
1. Open the notebook in Google Colab
2. Install dependencies
3. Upload an image
4. Listen to the generated audio description

## 🔹 Use Cases
- Assistive technology for visually impaired users
- Accessibility-focused AI applications
- Computer vision + audio projects

## 🔹 Future Enhancements
- Distance and obstacle detection
- Real-time camera input
- Multi-language audio support

## 👩‍💻 Author
Vidhyalakshmi Subramanian
