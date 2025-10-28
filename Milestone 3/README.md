### CodGenie -Intelligent code explainer and generator system

An intelligent code explainer and generator system built with Streamlit, JWT Authentication, and state-of-the-art AI models.  
This application empowers developers, students, and coders to **understand, generate, and improve code** instantly — all in one secure interface.


### Features

## Authentication System
- Secure **JWT-based login and registration**
- Roles: `Admin`, `Developer`, `General User`, and `Student`
- Passwords stored securely using **bcrypt hashing**

## AI-Powered Code Intelligence
- **Code Explanation:** Understand complex code instantly
- **Code Generation:** Generate optimized code snippets from natural language prompts
- **Multi-language Support:** Python, JavaScript, Java, SQL, C++
- Utilizes **Gemma**, **DeepSeek**, and **CodeBERT** models

###  Tech Stack
| Layer | Technology |
|-------|-------------|
| Frontend | Streamlit |
| Backend | Python + SQLite |
| Authentication | JWT |
| Model Inference | Transformers (Gemma, DeepSeek, CodeBERT) |
| Deployment | Ngrok (for Colab or local) |

---

##  Architecture Overview

+----------------------------+
| User Interface |
| (Streamlit Frontend) |
+------------+---------------+
|
v
+----------------------------+
| Authentication Layer (JWT) |
| - Login / Register |
| - Token Validation |
+------------+---------------+
|
v
+----------------------------+
| AI Model Layer |
| - Gemma 2B for Python |
| - DeepSeek Coder 1.3B |
| - CodeBERT for embeddings |
+------------+---------------+
|
v
+----------------------------+
| SQLite Database |
| - User Info (Email, Role) |
| - Encrypted Passwords |
+----------------------------+


##  Installation & Setup


If you are using Google Colab, use Ngrok to expose the app:

from pyngrok import ngrok
public_url = ngrok.connect(8501)
print(public_url)

 Default Credentials
Role	Email	Password
Admin	admin@ai	Admin123!
Directory Structure
AI-Code-Assistant/
│
├── integrated_app.py           # Main Streamlit application
├── integrated_app.db           # SQLite database (auto-created)
├── requirements.txt            # Dependencies
├── README.md                   # Project documentation
└── assets/                     # (Optional) Images, logo, screenshots

**How It Works**

User Authentication:
Users register and log in securely using JWT tokens.

Code Explanation:
Paste your code → select language → get detailed explanation powered by AI.

Code Generation:
Describe what you need → AI generates clean, executable code.

Role-based Features:
Different roles for better user segregation and model optimization.

👩‍💻 Team Members
Name	Role	Contribution
[Ashreen Fathima and Piyushmani tiwari]Frontend & JWT Integration	Streamlit UI, Authentication Flow
[Yashs]	AI Model Integration	Model fine-tuning and testing (full stack)
[Rajveer]	Backend Developer	Database and API Integration
[]	Documentation	README, Testing, and Maintenance

