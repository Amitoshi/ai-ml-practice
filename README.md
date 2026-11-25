# AI / ML practice notebooks

These are beginner-level Google Colab notebooks from my AI and Machine Learning course at Freshers India, plus small AI and automation tools I built while learning.

The originals were scattered across a few Google accounts, because of Colab's free GPU limits. Many were still called "Untitled" and had half-finished cells. I've now gone through each one, worked out what I was trying to build, and rewritten it as a clean notebook that runs on its own: current library versions, public datasets, and no personal paths or keys. Each notebook's first cell names the original notebook it came from.

This is the **beginner** set. Medium and advanced AI projects aimed at real business use will be added as separate repos.

## How to run

Open a notebook on GitHub, then open it in Google Colab (File → Upload notebook, or the "Open in Colab" button if you have the extension). Use **Runtime → Change runtime type → GPU** for anything that trains a model. Notebooks that need an API key read it from Colab's **Secrets** panel (the 🔑 icon), so keys never go in the code.

## Contents

### `ml-basics/` — first steps
| Notebook | What it does |
|---|---|
| simple-linear-regression-cgpa-package | Predicts salary package from CGPA, and reports MAE, RMSE and R² |
| word2vec-embeddings-basics | Trains a tiny Word2Vec model and finds similar words |
| next-word-prediction-lstm | Next-word prediction: n-grams → padding → LSTM → generate |
| html-tag-autocomplete-first-try | Character-level LSTM that finishes an HTML tag |

### `deep-learning-text/` — text generation and language models
| Notebook | What it does |
|---|---|
| sonnet-bilstm-word-generator | Bidirectional LSTM trained on Shakespeare's sonnets that writes new lines |
| sonnet-lstm-train-val-callbacks | Same idea, with a validation split, EarlyStopping and ReduceLROnPlateau |
| sonnet-generator-from-phrase | Writes a sonnet from a starting phrase, with temperature sampling |
| alice-in-wonderland-text-generator | Text generator trained on *Alice in Wonderland*, using a tf.data pipeline |
| phileas-fogg-pytorch-transformer | A small Transformer language model built from scratch in PyTorch |
| fogg-attention-next-word-keras | Next-word model with a Keras self-attention block |
| faq-next-word-lstm / -early-stopping | Completes FAQ questions word by word |
| news-headline-generator-lstm | Generates news-style headlines |
| html-tag-autocomplete-char-lstm | Autocompletes HTML form tags |

### `computer-vision/`
| Notebook | What it does |
|---|---|
| blood-cell-classification-cnn | CNN that classifies 4 white blood cell types (Kaggle dataset), with a confusion matrix |
| cifar10-cnn-classifier | CNN on CIFAR-10: train, evaluate, predict |
| object-detection-pretrained-faster-rcnn | Detects objects with a pretrained Faster R-CNN and draws boxes |
| image-super-resolution-real-esrgan | 4x upscaling with Real-ESRGAN compared against a bicubic resize |
| text-to-image-imagen-pytorch-demo | A tiny text-to-image model trained on CIFAR-10 class captions |

### `ai-tools/` — small useful AI apps
| Notebook | What it does |
|---|---|
| document-qa-rag-chatbot | **Chat with your documents:** upload a PDF, DOCX or TXT file. It splits the text into chunks, builds embeddings (sentence-transformers), searches them with FAISS, answers with an open LLM and cites the sources. Gradio chat UI. |
| gemini-image-generation | Text-to-image with the Gemini API, with a Gradio UI |
| gpt2-quote-generator-finetune | Fine-tunes GPT-2 on quotes with a plain PyTorch training loop |
| whisper-audio-transcription | Speech to text with Whisper (Bengali or auto-detect) |
| text-to-speech-edge-tts | Text to speech in Bengali and other languages, with a Gradio app |
| real-estate-photo-enhancer | Fixes lighting and noise in property photos, with an optional upscale |
| realesrgan-image-upscaling / upscale-uploaded-image / upscale-gradio-app | Three ways to use Real-ESRGAN: a quick demo, upscaling your own image, and a web app |
| deepprivacy2-face-body-anonymization | Anonymises faces and bodies in photos for privacy |

### `automation/` — Python utilities
| Notebook | What it does |
|---|---|
| scrape-books-to-csv, scrape-listing-pages, scrape-multiple-pages | Polite scraping (robots.txt, delays) of practice sites into CSV |
| selenium-headless-scraper | Scrapes a JavaScript-rendered page with headless Chrome |
| drive-move-shared-docx | Uses the Google Drive API to collect shared DOCX files into a folder, with a dry run first |
| mp3-trimmer, compress-audio-ffmpeg | Trims and compresses audio with pydub and ffmpeg |
| video-to-vertical-short | Cuts a clip and crops it to 9:16 for Shorts or Reels |
| youtube-hd-download | yt-dlp downloader, only for videos you own or have permission to download |

### `data-collection/`
| Notebook | What it does |
|---|---|
| osm-business-finder | Lists businesses in any country or state from OpenStreetMap (name, category, address, website) and saves a CSV |
| school-list-open-data | Builds a list of schools in a city from open data |

These use open data only (OpenStreetMap / Overpass), with rate limits and no personal data.

## Note

The code was rewritten with the help of AI coding tools, the same way I work day to day, and I've checked what each notebook does. Some have not been re-run end to end since the rewrite. If you find something broken, please open an issue.
