FairyTale RAG – A Multimodal Retrieval-Augmented Generation System
Project ID: T18_mlse_project
Team Members
Priyanshi Saini – SID: 202418002
Anandita Saolapurkar – SID: 202418005
Bhavin Gurnani – SID: 202418018
Project Overview
FairyTale RAG is a multimodal Retrieval-Augmented Generation (RAG) system that learns the style, tone, and visual aesthetics of classic fairy tales from a small illustrated storybook dataset and generates entirely new stories and illustrations in the same style.
The system can:
Generate a new fairy tale story from any input image
Generate storybook-style illustrations from a new text story
Convert a complete story into a sequence of coherent images, enabling automatic picture book creation
Generalize to unseen stories while preserving the gentle, classic fairy tale style
This project combines vision-language models, vector similarity search, and generative models into a unified multimodal pipeline.
Key Features
Custom dataset created from 15 illustrated pages of classic fairy tales
(Little Red Riding Hood and Snow White)
Multimodal vector database using CLIP + FAISS for fast similarity retrieval
Image → Story generation using Retrieval-Augmented Generation
Text → Image generation with consistent visual style
Story → Image Sequence generation for end-to-end picture book creation
Works on completely unseen inputs (e.g., a new kitten fairy tale)
System Architecture
                 Children's Storybook
            (15 images + corresponding texts)
                           │
                           ▼
            CLIP Encoder (Image & Text Embeddings)
                           │
                           ▼
                 FAISS Vector Database
            (Similarity search: relevant book page)
                           │
        ┌──────────────────┼──────────────────┐
        ▼                  ▼                  ▼
   Image Input          Text Input       Story Sequence
        │                  │                  │
        ▼                  ▼                  ▼
   Retrieval (CLIP + FAISS) → Prompt Augmentation
                           │
                           ▼
            BLIP (Image-to-Text Story Generation)
                           │
                           ▼
        Stable Diffusion (Text-to-Image Generation)
                           │
                           ▼
        Generated Story / Image / Image Sequence
Models Used
CLIP
Used to generate joint image-text embeddings for retrieval
FAISS
Efficient similarity search over multimodal embeddings
BLIP (fine-tuned)
Image-to-text model used for story generation with retrieved context
Stable Diffusion (fine-tuned)
Text-to-image generation maintaining storybook visual style
Project Structure
T18_mlse_project/
│
├── README.md              # Project documentation
├── requirements.txt       # Python dependencies
├── final_code.ipynb       # Complete runnable project notebook
│
├── images/                # Original storybook illustrations (15 images)
│
├── output_images/         # Generated images from demo runs
│
└── .gitignore             # Git ignore rules
How to Run the Project
1. Clone the Repository
git clone <repository-url>
cd T18_mlse_project
2. Install Dependencies
pip install -r requirements.txt
3. Run the Notebook
Open and execute the notebook:
final_code.ipynb
The notebook contains:
Dataset loading
Embedding creation
FAISS index building
Retrieval logic
Image-to-text generation
Text-to-image generation
End-to-end demos
Example Capabilities
Image → Story
Input: A random image
Output: A brand-new fairy tale written in classic storybook style
Text → Image
Input: A short fairy tale paragraph
Output: A matching illustrated scene
Story → Image Sequence
Input: Full story
Output: Multiple illustrations forming a picture book
Applications
Automated children’s book creation
Creative storytelling tools
Multimodal RAG research
Educational content generation
AI-assisted illustration pipelines
Notes
The dataset is intentionally small to demonstrate few-shot multimodal learning
Retrieval ensures stylistic consistency even for unseen stories
Designed as an end-to-end multimodal RAG pipeline
Acknowledgements
This project was developed as part of a Machine Learning / Deep Learning coursework submission, focusing on practical applications of multimodal generative AI and retrieval-augmented systems.
