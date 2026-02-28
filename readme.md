# 🧠 Multilingual Handwritten OCR System

Arabic 🇸🇦 | French 🇫🇷 | English 🇬🇧

## 📌 Project Idea

This project extracts handwritten text from images in:

* Arabic 

* French 

* English 

The system automatically:

- Detects the language of the image 

- Chooses the correct OCR model 

- Extracts the text 

- Sends the result to a local LLM (via Ollama) 

- Cleans the output and returns only the final answers 

The goal is to build a simple but smart OCR pipeline without training models from scratch.

## 🏗️ How The System Works

🔹 Step 1 – Image Input

User uploads an image (handwritten page).

🔹 Step 2 – Language Detection

We run a lightweight OCR first, then detect the language from extracted text.

🔹 Step 3 – Language-Based OCR

Depending on detected language:

Arabic → Arabic OCR model

French → French OCR model

English → English OCR model

🔹 Step 4 – LLM Cleaning (Ollama)

The extracted text is sent to a multilingual LLM (like qwen2.5).

The LLM removes:

_ Questions 

_ Instructions 

_ Noise 

_ Extra words 

And returns only:
✔ Clean final text  
✔ Answers only  

## 🖥️ Simple Interface

The interface is intentionally minimal.

## 🎨 UI Components

📷 Image Input (Upload button)

▶ Process Button

📄 Text View (Shows final extracted result)

**🔄 Full Pipeline Flow**

User Upload Image  
        ↓  
Light OCR (language detection)  
        ↓  
Select OCR Model  
        ↓  
Extract Text  
        ↓  
Send to Ollama  
        ↓  
Return Clean Final Text  
        ↓  
Display in Text View  

That’s it.  
No complexity.