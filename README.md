# FairyTale RAG – A Multimodal Retrieval-Augmented Generation System

**Project ID:** T18_mlse_project  

---

## Team Members
- **Priyanshi Saini** – SID: 202418002  
- **Anandita Saolapurkar** – SID: 202418005  
- **Bhavin Gurnani** – SID: 202418018  

---

## Project Overview

**FairyTale RAG** is a multimodal Retrieval-Augmented Generation (RAG) system that learns the **style, tone, and visual aesthetics of classic fairy tales** from a small illustrated storybook dataset and generates entirely new stories and illustrations in the same style.

The system can:
- Generate a new fairy tale story from any input image  
- Generate storybook-style illustrations from a new text story  
- Convert a complete story into a sequence of coherent images, enabling automatic picture book creation  
- Generalize to unseen stories while preserving the gentle, classic fairy tale style  

This project combines vision-language models, vector similarity search, and generative models into a unified multimodal pipeline.

---

## Key Features

- Custom dataset from **15 illustrated pages** of classic fairy tales  
  (*Little Red Riding Hood* and *Snow White*)
- Multimodal vector database using **CLIP + FAISS**
- Image → Story generation with Retrieval-Augmented Generation
- Text → Image generation with consistent visual style
- Story → Image Sequence generation for picture book creation
- Works on completely unseen stories (e.g., a new kitten fairy tale)

---


## System Architecture

Children's Storybook  
(15 images + corresponding texts)  
|  
v  
CLIP Encoder (Image and Text Embeddings)  
|  
v  
FAISS Vector Database  
Similarity search to find the most relevant book page  
|  
+------------------+------------------+  
|                  |                  |  
v                  v                  v  
Image Input     Text Input     Story Sequence Input  
|  
v  
Retrieval using CLIP and FAISS  
|  
v  
Prompt Augmentation  
|  
v  
BLIP Image to Text Story Generation  
|  
v  
Stable Diffusion Text to Image Generation  
|  
v  
Generated Story, Image, or Image Sequence  

---

## Models Used

CLIP  
Used to generate joint image and text embeddings for multimodal retrieval  

FAISS  
Used for fast similarity search over embedding vectors  

BLIP (fine tuned)  
Used for image to text story generation with retrieved context  

Stable Diffusion (fine tuned)  
Used for text to image generation while preserving storybook visual style  

---

## Project Structure

T18_mlse_project/  
|  
|-- README.md              Project documentation  
|-- requirements.txt       Python dependencies  
|-- final_code.ipynb       Complete runnable notebook  
|  
|-- images/                Original storybook illustrations (15 images)  
|-- output_images/         Generated images from demo runs  
|  
|-- .gitignore  

---

## How to Run the Project

Step 1: Clone the Repository

git clone <repository-url>  
cd T18_mlse_project  

Step 2: Install Dependencies

pip install -r requirements.txt  

Step 3: Run the Notebook

Open and execute the notebook file:  
final_code.ipynb  

The notebook contains the following steps:
- Dataset loading and preprocessing  
- Image and text embedding creation  
- FAISS index building for retrieval  
- Retrieval augmented prompt construction  
- Image to text story generation  
- Text to image generation  
- End to end multimodal demos  

---

## Example Capabilities

Image to Story  
Input: A random image  
Output: A brand new fairy tale written in classic storybook style  

Text to Image  
Input: A short fairy tale paragraph  
Output: A matching illustrated scene  

Story to Image Sequence  
Input: A complete story  
Output: Multiple illustrations forming a picture book  

---

## Applications

Automated children’s book creation  
Creative storytelling tools  
Multimodal retrieval augmented generation research  
Educational content generation  
AI assisted illustration pipelines  

---

## Notes

The dataset is intentionally small to demonstrate few shot multimodal learning  
Retrieval ensures stylistic consistency even for unseen inputs  
The system is designed as an end to end multimodal RAG pipeline  

---

## Acknowledgements

This project was developed as part of a Machine Learning and Deep Learning coursework submission  
The focus of the project is on practical applications of multimodal generative AI and retrieval augmented systems  

---
