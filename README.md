# Voice-Activated-AI-Assistant
### Project Description: Voice-Activated AI Assistant

**Overview**: A Google Colab-based voice assistant for home appliance repair (AC, fridge, oven, washing machine). It transcribes user speech, matches issues to repair services, generates responses, and converts them to speech.

**Features**:  
- Voice input/output via microphone or audio upload (WAV/MP3).  
- Service matching using NLP and embeddings.  
- Contextual responses via mock Grok chain.  
- Downloadable audio files.  

**Technologies**:  
- **Platform**: Google Colab (Python 3.11, June 2, 2025).  
- **Speech**: Deepgram SDK (v3.5.0) for STT/TTS, PyDub (v0.25.1).  
- **NLP**: Sentence-Transformers (v2.6.1, `all-MiniLM-L6-v2`), LangChain (v0.2.12).  
- **Core**: NumPy (v1.25.2), PyTorch (v2.2.0), Requests (v2.32.3), timm (v0.9.16), fsspec (v2025.3.2).  
- **Frontend**: IPython, google.Colab, JavaScript for audio recording.  

**Workflow**:  
1. User says, e.g., “My fridge is leaking water.”  
2. Deepgram transcribes audio.  
3. Sentence-Transformers matches to Fridge Repair.  
4. Mock Grok chain responds: “Sounds like a blocked defrost drain. Want a technician?”  
5. Deepgram converts to speech, plays, and offers downloads.  

**Challenges Overcome**:  
- Fixed `numpy.char` and `TimmWrapperConfig` errors.  
- Resolved Colab dependency conflicts (`spacy`, `gcsfs`).  
- Bypassed Ollama/`phi4` issues with mock Grok chain.  

**Future Scope**:  
- Add Ollama with `llama3.2:1b`.  
- Support multilingual responses.  
- Integrate repair scheduling APIs.  

**Notes**: It uses mock Grok due to an invalid `XAI_API_KEY`. Reset Colab runtime before running. If the Deepgram API key expires, it may need to be replaced.
