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

```json { "inputs": "Explain quantum computing in simple terms.", "max_tokens": 200, "do_sample_set":true "temperature_score": 0.7, "penalty": 1.0, "return_number": 1, "skip_special_token": true } ```

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

