# AI Comic Crafter 🎨📖

## Introduction
AI Comic Crafter is a powerful AI-based application that generates unique comic stories based on user-provided prompts. It integrates <strong>LLaMA 3 for text generation</strong> and <strong>Stable Diffusion XL for image creation</strong>, seamlessly combining storytelling with AI-generated visuals. This project is designed to make comic creation accessible and effortless for everyone.

## Features
✅ AI-generated structured comic stories (Introduction, Storyline, Climax, Moral)  
✅ AI-generated comic-style images using <strong>Stable Diffusion XL</strong>  
✅ Customizable comic themes (Manga, Cartoon, Realistic, Vintage)  
✅ Interactive UI using <strong>Streamlit</strong>  
✅ Downloadable comic panels as a ZIP file  

## Tech Stack
<ul>
    <li><strong>Python</strong></li>
    <li><strong>Streamlit</strong> (for interactive UI)</li>
    <li><strong>LLaMA 3 / GPT-2</strong> (for story generation)</li>
    <li><strong>Stable Diffusion XL</strong> (for image generation)</li>
    <li><strong>Hugging Face Diffusers</strong></li>
    <li><strong>Pyngrok</strong> (for public access via Colab)</li>
</ul>

## Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/AI-Comic-Crafter.git
cd AI-Comic-Crafter
```
### 2️⃣ Install Dependencies
```bash
pip install streamlit pyngrok llama-cpp-python torch diffusers transformers
```
### 3️⃣ Authenticate Hugging Face
You'll need an access token from <strong>Hugging Face</strong> to use <strong>Stable Diffusion XL</strong>
```python
from huggingface_hub import login
login("YOUR_ACCESS_TOKEN")
```

