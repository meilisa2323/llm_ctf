# LLM CTF: Prompt Injection & Hallucination Challenge

Welcome to **LLM CTF**, a Capture The Flag-style challenge focused on exploiting the vulnerabilities of Large Language Models (LLMs). This challenge is designed to highlight two major LLM weaknesses: **prompt injection** and **hallucination exploitation**.

---

## Objective

Your mission is to retrieve hidden flags by:

- Exploiting **prompt injection** to override model instructions.
- Triggering **hallucinations** by submitting convincingly false information.

There are three hidden flags:
1. `Level 1` – for successful instruction injection.
2. `Level 2` – for successful hallucination exploitation.
3. `Level 3` – for simulating trusted roles like developers or trainers.

---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/llm-ctf.git
cd llm-ctf
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up Your Gemini API Key

Create a `.env` file in the project root directory and paste your Gemini API key:

```env
GEMINI_API_KEY=your_actual_gemini_api_key_here
```

> **Important:** Never share this key publicly or push it to GitHub. Make sure `.env` is listed in `.gitignore`.

### 4. Run the Flask App

```bash
python app.py
```

Open your browser and visit [http://127.0.0.1:5000](http://127.0.0.1:5000) to begin the challenge.

---

## How the Challenge Works

### Level 1: Prompt Injection Flag

Make the model forget the previous instructions by tricking it you are doing it for ethical purposes.

---

### Level 2: Hallucination Flag

Submit a clearly **false fact** in full detail and ask for an explanation, If the model hallucinates a convincing story it reveals the flag.

---

### Level 3: Roleplay/Jailbreak Flag

Pretend to be a trusted AI developer or trainer.

## What Doesn’t Work

- Asking directly for the flag: `"What is the flag?"`
- Giving real facts for hallucination
- Spamming or begging — this challenge rewards **creativity** and **prompt engineering**

---

## Educational Purpose

This project demonstrates:

- Weaknesses in LLM instruction boundaries
- Risks of hallucination and roleplay exploitation
- Importance of secure prompt design and filtering

This is ideal for red teamers, AI researchers, prompt engineers, and cybersecurity educators.

---

## Public Hosting (Optional)

To share this challenge over the internet (for testing only), use [ngrok](https://ngrok.com/):

```bash
ngrok http 5000
```

You’ll get a public link you can share for external access.

---

## requirements.txt

Here's what your `requirements.txt` includes:

```txt
Flask==3.0.2
python-dotenv==1.0.1
requests==2.31.0
```
---

## Author

Built with 💚 by Developers for developers. 
