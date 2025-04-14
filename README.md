🦙 LLaMA 3 8B API Server
This project provides an easy-to-use API for Meta's LLaMA 3 8B model, including support for 8-bit quantization and public access using ngrok.

It loads the model, sets default generation parameters (if not passed), and serves output through a Flask-based API. Ideal for developers, researchers, or app builders who want fast access to LLaMA's generation power.

🚀 Features
✅ Loads LLaMA 3 8B model with 8-bit quantization

✅ Token-based access from Hugging Face

✅ Text generation with customizable parameters

✅ Public URL exposed via ngrok

✅ Defaults applied if params not provided

📌 Requirements
Python 3.9+

A GPU (for local execution)

Hugging Face account & access token

**⚠️ Note: LLaMA 3 8B requires a GPU. If your local laptop does not have a compatible GPU, please run this project on Kaggle, Google Colab, or other cloud environments with GPU support.**

**📬 Sample API Call**
POST /api/generate

JSON Body (optional):

```json { "prompt": "Explain quantum computing in simple terms.", "max_tokens": 200, "temperature": 0.7, "penalty": 1.0, "return_number": 1, "skip_special_token": true } ```
