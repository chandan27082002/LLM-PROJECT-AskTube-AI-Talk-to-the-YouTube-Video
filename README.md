# LLM-PROJECT-AskTube-AI-Talk-to-the-YouTube-Video

# 🎥 AskTube AI — Talk to the YouTube Video

AskTube AI is a powerful voice-enabled, multilingual web application that allows users to **ask questions**, **generate summaries**, and **create quizzes** based on any YouTube video with English or Hindi captions. Built with NVIDIA AI, LangChain, and Streamlit, it's designed for effortless understanding of video content.

---
![AskTube Banner](https://raw.githubusercontent.com/chandan27082002/LLM-PROJECT-AskTube-AI-Talk-to-the-YouTube-Video/main/image.png)
## 🌟 Features

- 🔗 **YouTube Transcript Extraction**
- ❓ **Ask Questions** about the video using AI
- 📄 **Summarize** the entire video into bullet points
- 🧠 **Generate Topics & MCQs** for learning and testing
- 🗣️ **Voice Input** using your microphone
- 🔊 **Text-to-Speech** responses (with audio download)
- 🌐 **Multilingual Support** (English, Hindi, Bengali, Tamil, Telugu, Marathi, Gujarati)

---

## 🔧 Technologies Used

| Component | Technology |
|----------|-------------|
| **Frontend & UI** | Streamlit |
| **Transcript Extraction** | `youtube_transcript_api` |
| **Translation** | `deep_translator` |
| **Embeddings & Vector Store** | LangChain + FAISS + NVIDIA Embeddings |
| **LLM** | `ChatNVIDIA` (NVIDIA AI models like Mixtral, LLaMA3) |
| **Text-to-Speech** | gTTS (Google Text-to-Speech) |
| **Voice Input** | `speech_recognition` |
| **Text Splitting** | `RecursiveCharacterTextSplitter` from LangChain |

---

## 🚀 How It Works

1. **User inputs a YouTube video link**
2. **Transcript** is fetched:
   - tries English
3. **Transcript is embedded** using NVIDIA QA model
4. Based on the user action:
   - Ask question → relevant transcript chunks are retrieved → sent to NVIDIA LLM → response generated
   - Summarize → text split → summarized in chunks → merged into final bullet points
   - Quiz → topics and MCQs are generated using AI
5. If desired, the answer is:
   - Translated to another language
   - Converted to speech using gTTS
   - Downloaded as an MP3

