# 🤖 Agentic AI Hiring Assistant

## 📌 Overview
This project is an intelligent AI Hiring Assistant designed to evaluate resumes against job descriptions using structured reasoning and transparency.  
It simulates how a real hiring analyst evaluates candidates by checking skills, evidence, relevance and gaps rather than simple keyword matching.

The system uses a hybrid approach:
- Rule-based evaluation for consistency
- Optional LLM reasoning for deeper understanding

It generates:
- Skill match score
- Project quality score
- Risk flags
- Evidence summary
- Final hiring verdict

---

## 🏗️ System Architecture

### Step 1: Input Processing
Resume and job description are provided as text input.

### Step 2: Parsing Layer
Extracts:
- Skills  
- Projects  
- Experience  
- Job requirements  

### Step 3: Skill Normalization
Maps similar skills into standard form to improve matching accuracy.

Example:
```
react.js → REACT_JS  
restful api → REST_API  
context api basic → CONTEXT_API  
```

### Step 4: Evidence Detection
Checks whether skills appear:
- Only in skills section (weak)
- Inside projects (strong)
- With context (medium/strong)

### Step 5: Scoring Engine
Calculates:
- Skill match score  
- Project quality score  
- Risk penalties  

Final verdict:
```
Shortlist | Review | Reject
```

### Step 6: Optional LLM Reasoning
Used only when deeper reasoning is required:
- Ambiguous skill context  
- Weak confidence score  
- Explanation generation  

---

## ⚙️ Tech Stack
- Python  
- FastAPI  
- NLP  
- LLM API (Groq – Llama/Mixtral)  
- Modular agent pipeline  

---

## ▶️ Run Project
```
git clone https://github.com/yourusername/ai-hiring-agent.git
cd ai-hiring-agent
pip install -r requirements.txt
uvicorn app.main:app --reload
```

Open:
```
http://127.0.0.1:8000/docs
```

---

## 📊 Output
The system generates structured evaluation including:
- Resume analysis  
- Skill match score  
- Risk flags  
- Final hiring verdict  

---
## Structure
<img width="800" height="596" alt="image" src="https://github.com/user-attachments/assets/fa0a62b4-a202-4e2d-b712-686538adf2ed" />

## ⚠️ Limitations
- Accuracy is iterative  
- Resume parsing depends on text format  
- LLM reasoning limited due to API constraints  
- Built for logic demonstration, not full production  

---

## 🚀 Future Improvements

- Better semantic matching  
- Interview question generator  
- Dashboard UI  
- Cloud deployment  
- Multi-resume processing  

---

## 👨‍💻 Author
Jignesh Thacker  
AI/ML & Generative AI Enthusiast  
GitHub: https://github.com/Jignesh03
<img width="1494" height="730" alt="Screenshot 2026-01-27 230136" src="https://github.com/user-attachments/assets/0e625c25-bf4d-49ce-b562-e18dc1e3021a" />
<img width="1388" height="570" alt="Screenshot 2026-01-27 231143" src="https://github.com/user-attachments/assets/883b6c1b-e468-493e-b10b-ef5ce340d054" />
