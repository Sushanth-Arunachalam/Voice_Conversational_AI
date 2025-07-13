# Voice_Conversational_AI


# 🎙️ Voice Agentic AI Assistant (Hackathon Project)

This project is a voice-enabled, Retrieval-Augmented Generation (RAG) assistant for internal document Q&A, built using:

- Browser-based voice recording
- LLMs (OpenAI GPT-3.5)
- RAG over internal documents (via FAISS)
- Text-to-Speech (gTTS)
- Python + Google Colab (simulated REST API)

---

## Setup Instructions

1. **Run in Google Colab (Recommended)**  
   Open the `.ipynb` file in Colab. All installations and setups are handled there.

2. **Install dependencies (auto in Colab):**
   ```
   pip install -U langchain langchain-openai langchain-community openai faiss-cpu gtts pydub speechrecognition tenacity
   ```

3. **Upload your internal document**  
   When prompted, upload your CSV (e.g., `HackathonInternalKnowledgeBase.csv`).

4. **Talk to the assistant**  
   - The notebook will prompt you to speak.
   - It records, transcribes, retrieves relevant info using RAG, responds using GPT, and speaks back.

---

## Sample Conversation Logs

```
User (via voice): "What internal tool do we use for reporting?"
Assistant: "According to the internal knowledge base, the team uses 'InsightTrack' for all internal reporting."
```

```
User: "Tell me what our migration plan was in Q2."
Assistant: "In Q2, the plan included a phased rollout of SalesOps, with compliance checks completed in stage 2."
```

---

## API Simulation

While no REST API is deployed, the notebook includes function equivalents:

| Endpoint | Simulated Function |
|----------|--------------------|
| `POST /transcribe` | `transcribe_audio_file()` |
| `POST /chat` | `chat_with_llm()` |
| `POST /speak` | `speak_text()` |
| `POST /converse` | Full voice → GPT → voice pipeline |
| `POST /upload_rag_docs` | Upload + embed CSV into FAISS vectorstore |

---

## .env (Use Placeholder Values)

See `.env` file for structure. Do **not** commit real keys.

---

## File Structure

```
├── Voice_Agentic_AI_Colab_With_Conversion.ipynb
├── HackathonInternalKnowledgeBase.csv
├── README.md
├── .env
├── architecture.mmd (optional)
└── api_contract.pdf (optional)
```

---

## Theme Alignment: CRE + AI Agents

This assistant mimics a real-world **internal knowledge agent** for commercial real estate orgs:
- Use case: Ask internal questions hands-free
- Built-in: Document-aware RAG, voice accessibility, memory

---

## Submission Ready
Voice input via mic
RAG document retrieval
GPT-powered assistant
Text-to-speech output
Conversation memory
Notebook-only deploy (lightweight)

---

##  Notes


This prototype is fully working in Colab and satisfies all major requirements — we hope it demonstrates creative use of AI Agents in a commercial real estate context.

---
