# prompt-based-ABSA-project
Gated Hybrid ABSA Model

DeBERTa-v3 + Gemma-2B with Learnable Gated Fusion

A hybrid deep learning architecture for Aspect-Based Sentiment Analysis (ABSA) that combines contextual encoding with large language model reasoning using an adaptive gated fusion mechanism.

📌 Overview

This project integrates:

🤖 DeBERTa-v3-base – Contextual representation learning

🧠 Gemma-2B (8-bit, frozen) – Prompt-based semantic reasoning

🔀 Learnable Gated Fusion – Adaptive feature balancing

📊 Evaluation with Accuracy & Macro F1-score

The model dynamically decides whether to prioritize contextual or semantic signals depending on the input sentence and aspect.

🏗️ Architecture
Input: Sentence + Aspect
        │
        ├── DeBERTa-v3 (Context Encoder)
        │
        ├── Gemma-2B (Prompt-based Reasoning)
        │
        └── Learnable Gated Fusion
                    │
             Classification Layer
                    │
              Sentiment Output

🚀 Features

Hybrid Transformer + LLM architecture

Memory-efficient 8-bit quantization

Stratified dataset splitting

Custom PyTorch Dataset class

Evaluation using Scikit-learn metrics

Modular and research-friendly implementation

📂 Project Structure
├── Untitled13.ipynb        # Training & evaluation notebook
├── dataset.csv             # Input dataset
├── README.md               # Documentation

⚙️ Installation

Clone the repository:

git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name


Install dependencies:

pip install torch transformers accelerate bitsandbytes
pip install pandas scikit-learn

📊 Dataset Format

The dataset must contain the following columns:

sentence	aspect	label

Example:

The food was delicious but service was slow, food, positive
The food was delicious but service was slow, service, negative


Label Encoding:

0 → Negative  
1 → Neutral  
2 → Positive

🧠 Training

Run the notebook:

Untitled13.ipynb


Or convert to script and run:

python train.py

📈 Evaluation Metrics

Accuracy

Macro F1-score

Classification Report

🔍 Inference Example
predict_sentiment(
    "The battery life is amazing but the display is dull",
    "battery",
    model
)


Output:

positive

🖥️ Requirements

Recommended:

Python 3.9+

GPU (T4 / A100 preferred)

Minimum 12GB VRAM (for 8-bit LLM)

📌 Applications

Product review sentiment analysis

Restaurant feedback mining

E-commerce opinion tracking

Social media monitoring

📜 License

This project is for academic and research purposes.

👩‍💻 Author

Yamini Morasa
