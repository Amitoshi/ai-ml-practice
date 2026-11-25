# AI / ML practice notebooks

My Google Colab notebooks from the AI and Machine Learning course at Freshers India, plus small AI tools I built afterwards. I ran them across a few Google accounts because of Colab's free GPU limits, and I've now gathered them in one place.

These are learning notebooks, not production code. Some follow course exercises closely, and some are my own experiments. Most notebooks still include their outputs (training logs, accuracy, sample predictions), so you can see what happened without running them.

## ML coursework (`ml-coursework/`)

| Notebook | What it does | Stack |
|---|---|---|
| `blood-cell-classification-cnn` | Classifies blood cell images by type with a CNN, plus confusion matrix and report | TensorFlow / Keras, OpenCV, scikit-learn, seaborn |
| `cifar10-image-classifier` | Image classification on CIFAR-10 | TensorFlow / Keras |
| `sonnet-text-generator-lstm` / `-v1` / `sonnet-predict` | Trains an LSTM on Shakespeare's sonnets and generates new lines | TensorFlow |
| `alice-text-generation`, `phileas-fogg-text-model` | The same text-generation idea on other books | TensorFlow, PyTorch |
| `lstm-next-word-prediction`, `next-word-prediction` | Predicts the next word from a short text | TensorFlow, scikit-learn |
| `news-headline-generator` | Bidirectional LSTM text model with dropout, from a news-headline exercise | TensorFlow / Keras |
| `faq-chatbot-tensorflow` | Next-word model trained on a course FAQ text (CampusX exercise) | TensorFlow |
| `html-tag-guesser` | Small sequence model that guesses HTML tags | TensorFlow |
| `simple-linear-regression` | First regression model | scikit-learn, pandas |
| `word2vec-qna-test` | Word similarity test with word2vec | gensim |
| `gpt2-fine-tuning` | Fine-tunes GPT-2 on a small custom dataset | Hugging Face Transformers, PyTorch |
| `imagen-pytorch-experiment` | Tries out a text-to-image model | imagen-pytorch |

## AI tools (`ai-tools/`)

| Notebook | What it does | Stack |
|---|---|---|
| `docx-pdf-rag-chatbot` | Upload a DOCX or PDF and ask questions about it. Splits the text into chunks, embeds them, finds the closest chunks and answers from them. Gradio UI. | sentence-transformers, FAISS, Transformers, Gradio |
| `gemini-image-generation` | Generates images through the Gemini API. The key comes from Colab secrets. | google-genai |
| `whisper-audio-transcription` | Speech to text | OpenAI Whisper |
| `text-to-voice-edge-tts` | Text to speech | edge-tts |
| `image-upscaler-realesrgan` | Upscales low-resolution images | Real-ESRGAN |
| `real-estate-photo-enhancer-gradio` | Upload a property photo and it improves contrast, brightness and sharpness and removes noise. Gradio web UI. | Real-ESRGAN, OpenCV, Gradio |

## Run them

Open any notebook on GitHub, then click **Open in Colab** (or use File → Upload notebook in Colab). Use a GPU runtime for the training notebooks. For the Gemini notebook, add your own `GEMINI_API_KEY` in Colab's Secrets panel.

## What's next

I'm now bringing this into my main work: AI features inside WordPress, such as a site assistant that uses retrieval over a site's own content (the same idea as the RAG notebook above).
