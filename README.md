# T18_mlse_project

## Team Members
- [Priyanshi Saini] - SID: 202418002
- [Anandita Saolapurkar] - SID: 202418005
- [Bhavin Gurnani] - SID: 202418018

## Project Title: FairyTale RAG – A Multimodal Retrieval-Augmented Generation System

### Overview
We built an intelligent AI that "remembers" classic fairy tales from a children's storybook (Little Red Riding Hood + Snow White) and can:
- Take any new image → generate a brand-new story in the exact same gentle, classic style
- Take any new story → generate beautiful illustrations that look like they came from the same book
- Turn a full story into a sequence of matching images (perfect for creating new picture books!)

This is a **multimodal RAG** system combining retrieval (CLIP + FAISS), image-to-text (fine-tuned BLIP), and text-to-image (fine-tuned Stable Diffusion).

### Key Features
- Custom dataset from 15 illustrated pages of classic fairy tales
- Multimodal vector database for fast similarity search
- Image → Story generation with RAG context
- Text → Image and Story → Image Sequence generation
- Works on completely unseen stories (e.g., a new kitten fairy tale)

### Architecture
