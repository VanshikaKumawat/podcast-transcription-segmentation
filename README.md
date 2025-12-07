# podcast-transcription-segmentation
End-to-end system for podcast audio cleaning, Whisper transcription, topic segmentation, keyword extraction, and interactive transcript navigation — using AMI audio as dataset. Includes preprocessing, ASR, NLP modeling, visualization, and UI.

🎧 Podcast Transcription, Segmentation & HR-Interview Summarization Pipeline

This project implements an end-to-end Audio → Segmentation → ASR → Summarization system designed for:

Podcast processing

HR interview analysis

Meeting & conversation summarization

Speaker-wise transcript generation

Segment-level insights & metrics

It uses AMI Meeting Corpus as the primary dataset and integrates state-of-the-art ASR models, NLP pipelines, and deep-learning based segmentation.

🚀 Project Features
🔊 1. Audio Preprocessing

Standardizes sampling rate (16kHz)

Denoising, normalization

Works with long audio files (1–2 hours)

✂️ 2. Audio Segmentation

Silence-based segmentation

Energy-based segmentation

Optional VAD-based (Voice Activity Detection)

Handles noisy interviews and long meetings

🗣️ 3. Automatic Speech Recognition (ASR)

Supports multiple ASR backends:

Whisper Large-V3 / Medium / Small

NeMo CTC models

Wav2Vec2-based models

Outputs:

Full transcript

Timestamped transcript

Segment-wise transcript

🧑‍🤝‍🧑 4. Speaker Diarization (Optional)

pyannote.audio diarization

Outputs speaker-annotated transcript:
(SPEAKER A: … | SPEAKER B: …)

📝 5. Summarization Pipeline

Generates:

Overall summary

Segment-wise summaries

Speaker-wise summaries

Key topics

Keywords

Q&A extraction

Sentiment & emotion analysis

📊 6. HR Interview–Specific Analytics

Candidate performance indicators

Interviewer-candidate talk ratio

Question complexity extraction

Behavioral signal insights

STAR method summary (Situation–Task–Action–Result)

🗂️ Dataset Used (AMI Meeting Corpus)

Example loaded files:

ES2002a.Mix-Lapel.wav  
ES2002b.Mix-Lapel.wav  
ES2002c.Mix-Lapel.wav  
ES2002d.Mix-Lapel.wav  


Why AMI?

High-quality multi-speaker meetings

Long-form conversational structure (similar to HR interviews)

Fully transcribed

⚙️ Tech Stack
Component	Technology
Language	Python 3.10+
ASR	OpenAI Whisper, Wav2Vec2
Segmentation	PyDub, WebRTC VAD
Diarization	pyannote.audio
Summarization	Transformers / GPT models
Visualization	Matplotlib, Plotly
Data Storage	JSON, CSV, TXT
🧩 Pipeline Architecture
Audio Input (.wav)
        ↓
Segmentation (silence / VAD)
        ↓
ASR Transcription
        ↓
(Optional) Diarization
        ↓
NLP Processing (Summaries, Topics, Q&A)
        ↓
Outputs → JSON, TXT, CSV

📁 Folder Structure (Recommended)
project-root/
│
├── data/
│   ├── raw_audio/
│   │   ├── ES2002a.Mix-Lapel.wav
│   │   ├── ...
│   ├── segments/
│   ├── transcripts/
│   └── summaries/
│
├── notebooks/
│   ├── 01_audio_loading.ipynb
│   ├── 02_segmentation.ipynb
│   ├── 03_asr_transcription.ipynb
│   ├── 04_summarization.ipynb
│   └── 05_hr_interview_analysis.ipynb
│
├── src/
│   ├── preprocessing/
│   │   └── audio_preprocess.py
│   ├── segmentation/
│   │   └── vad_segmentation.py
│   ├── asr/
│   │   └── whisper_transcriber.py
│   ├── summarization/
│   │   └── summary_pipeline.py
│   ├── hr_analysis/
│   │   └── interview_metrics.py
│   └── utils.py
│
├── models/
│   └── (Saved ASR models, diarization models)
│
├── README.md
├── requirements.txt
└── main.py

▶️ How to Run

Install dependencies:
pip install -r requirements.txt


Run entire pipeline:
python main.py --audio data/raw_audio/ES2002a.Mix-Lapel.wav


Outputs stored in:

/data/transcripts  
/data/summaries  
/data/segments  

📌 Project Outcomes
End-to-end HR interview analysis system
Long-form audio handling + segmentation
Accurate transcripts

High-quality summarization

Useful analytics for recruiters

Ready for deployment in HR tech tools

🏗️ Future Improvements

Real-time segmentation & ASR

UI dashboard

Fine-tuned ASR for HR interviews

Large-Scale multi-speaker diarization

📜 License

MIT License (customize if needed)

✅ 2. GitHub Folder Structure (Short Form)
📦 Podcast-HR-Interview-Analysis
 ┣ 📂 data
 ┣ 📂 notebooks
 ┣ 📂 src
 ┣ 📂 models
 ┣ 📜 README.md
 ┣ 📜 requirements.txt
 ┗ 📜 main.py


🚀 3. Steps to Push Code to GitHub
Step 1 – Initialize repo
git init
git branch -M main

Step 2 – Add remote GitHub repo
git remote add origin https://github.com/VanshikaKumawat/podcast-transcription-segmentation.git

Step 3 – Add files
git add .

Step 4 – Commit
git commit -m "Initial commit: audio pipeline project"

Step 5 – Push
git push -u origin main
