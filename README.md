# LLM Scam Detector
LLM-Based Scam Detector (Phishing Website Classification)

This project fine-tunes a LLaMA-3-8B model using LoRA on 18,000+ phishing website samples to perform real-time phishing detection with high accuracy.

## Features
- Fine-tuned LLaMA-3 model with LoRA achieving **98.85%** real-world accuracy
- Real-time detection using a scalable pipeline with **Selenium**, **MongoDB**, and **Dockerized microservices**
- Deployed with **NGINX reverse proxy** on **AWS EC2** for low-latency inference

## Tech Stack
- **LLM**: Meta LLaMA-3-8B, LoRA, Hugging Face Transformers
- **Backend**: FastAPI, Docker, NGINX, MongoDB
- **Deployment**: AWS EC2, containerized inference
- **Fine-tuning**: PyTorch, custom script using `scripts/fine_tune.py`

## Folder Structure
- `app/` – FastAPI backend
- `scripts/` – LoRA fine-tuning scripts
- `data/` – Sample phishing dataset
- `docker/` – Dockerfile for backend service
- `nginx/` – Reverse proxy configuration

## Getting Started

```bash
git clone https://github.com/your-username/llm-scam-detector.git
cd llm-scam-detector
docker build -t llm-scam-detector .
docker run -p 80:80 llm-scam-detector
