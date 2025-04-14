# 🦙 LLaMA 3 8B API Server

This project provides a lightweight, easy-to-use API for **Meta's LLaMA 3 8B** language model with support for **8-bit quantization** and **public access via ngrok**.

It handles everything — from loading the model and applying default generation parameters (if not provided) to serving outputs through a **Flask-based API**. Perfect for developers, researchers, and app builders who want fast, programmatic access to LLaMA's powerful text generation.

---

## 🚀 Features

- ✅ Loads LLaMA 3 8B model with 8-bit quantization
- ✅ Hugging Face token-based authentication
- ✅ Text generation with customizable or default parameters
- ✅ Public API access via ngrok tunnel
- ✅ Auto-fallback to default values if no parameters are passed

---

## 📌 Requirements

- Python 3.9+
- A compatible GPU (for local usage)
- Hugging Face account and access token

> ⚠️ **Important:** LLaMA 3 8B requires a GPU.  
> If your local machine does not have one, we recommend running the project on platforms like:
> - [Kaggle](https://kaggle.com)
> - [Google Colab](https://colab.research.google.com)
> - Any cloud provider with GPU access

---

## 📬 Sample API Call

**Endpoint:** `POST /api/generate`

**Example Request Body:**

```json
{
  "inputs": "Explain quantum computing in simple terms.",
  "max_tokens": 200,
  "do_sample_set":true,
  "temperature_score": 0.7,
  "penalty": 1.0,
  "return_number": 1,
  "skip_special_token": true
}
 ```

## 🌐 Deployment Options

| Platform     | Supported | Notes                         |
|--------------|-----------|-------------------------------|
| ✅ Local GPU | ✔️        | Recommended for best speed    |
| ✅ Kaggle    | ✔️        | No setup required, free GPU   |
| ✅ Colab     | ✔️        | Ideal for prototyping         |

## 🧠 Credits

- [Meta AI](https://ai.meta.com/) for **LLaMA 3**
- [Hugging Face Transformers](https://huggingface.co/docs/transformers/index) for model loading and inference
- [bitsandbytes](https://github.com/TimDettmers/bitsandbytes) for 8-bit model quantization
- [pyngrok](https://github.com/alexdlaird/pyngrok) for public API tunneling via ngrok

