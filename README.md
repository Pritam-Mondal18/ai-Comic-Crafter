# AI Comic Crafter 🎨📖

## Introduction
AI Comic Crafter is a powerful AI-based application that generates unique comic stories based on user-provided prompts. It integrates <strong>LLaMA 3 for text generation</strong> and <strong>Stable Diffusion XL for image creation</strong>, seamlessly combining storytelling with AI-generated visuals. This project is designed to make comic creation accessible and effortless for everyone.

## Problem Description

The objective of ComicCrafter AI is to develop an application capable of generating a comic book-style short story based on a user-provided prompt. The application should generate a story split into four parts: introduction, storyline, climax, and moral. The project will be executed in four distinct phases:

## Phase 1: LLM Story Generation
<ol><ul><li>Develop a module that generates a coherent story using LLMs based on the user’s prompt.</li><li>he story is divided into four parts: introduction, storyline, climax, and moral.</li></ul></ol>

## Phase 2: Image Generation
<ol><ul><li>Develop a module that generates images corresponding to each story part using AI-based image generation tools like Stable Diffusion.</li><li>Ensure that the images are coherent with the story.</li></ul></ol>

## Phase 3: Merging Story and Images
<ol><ul><li>Create a system to merge the generated text and images into a cohesive comic book format.</li><li>Ensure proper alignment and formatting of the text and images.</li></ul></ol>
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
### 4️⃣ Run the Application
```bash
streamlit run app.py
```
If running on <strong> Google Colab</strong>, use <strong> pyngrok </strong> to expose the app:
```python
!ngrok authtoken YOUR_ACCESS_TOKEN
from pyngrok import ngrok
import os
os.system("streamlit run app.py &")
public_url = ngrok.connect(8501)
print(f"Streamlit app is live at: {public_url}")
```
## How to Use
<ol> <li>1️⃣Enter your story elements (or let AI generate them for you).</li> <li>2️⃣Select a <strong>genre</strong> and <strong>comic style</strong>.</li> <li>3️⃣Click <strong>"Generate Story with AI"</strong> to auto-generate text.</li> <li>4️⃣Click <strong>"Generate Comic"</strong> to create AI-generated comic panels.</li> <li>5️⃣Download the comic as a ZIP file.</li> </ol>

## Example Output

### 📝 <strong>Story Example:</strong>

<pre>Title: The Cyber Hero<br/>Introduction: In a futuristic city, a hacker discovers a government conspiracy.<br/>Storyline: He builds an AI-powered suit and fights for justice.<br/>Climax: A thrilling showdown against the corrupt cyber-police.<br/>Moral: Technology must be used for good, not oppression. </pre>

🖼️ <strong>Generated Comic Panels:</strong>

<img src="comic_panel_1.png" alt="Sample Comic Panel">

## Building the Architecture
<p>The <strong>AI Comic Crafter</strong> follows a modular approach:</p> <ul> <li><strong>User Input Module</strong> – Collects user input (custom text or AI-generated story elements).</li> <li><strong>LLM-Based Story Generation</strong> – Uses <strong>LLaMA 3 / GPT-2</strong> to generate structured comic stories.</li> <li><strong>Image Generation Module</strong> – Uses <strong>Stable Diffusion XL</strong> to create images corresponding to the story panels.</li> <li><strong>Rendering & Display Module</strong> – Displays the generated comic story and images in <strong>Streamlit</strong> UI.</li> <li><strong>Download Module</strong> – Allows users to download the generated comic as a ZIP file.</li> </ul>

## Challenges Faced
<ul> <li><strong>Computational Constraints</strong> – Running <strong>Stable Diffusion XL</strong> without a dedicated GPU is slow. Solutions include cloud-based inference.</li> <li><strong>Story & Image Alignment</strong> – Ensuring AI-generated images match the context of the story is a challenge.</li> <li><strong>Fine-Tuning LLaMA 3</strong> – Adapting LLaMA 3 for structured comic storytelling requires iterative fine-tuning.</li> <li><strong>Real-Time Processing</strong> – Achieving low-latency text and image generation for an interactive experience.</li> </ul>

## Contributing
🚀 We welcome contributions! Feel free to fork the repo, submit pull requests, and enhance the project.
## License
📜 This project is licensed under the <strong>MIT License</strong>.

