# TalentScout-AI Hiring Assistant Chatbot 

## Project Overview
The **Hiring Assistant Chatbot** (TalentScout AI) is an AI-powered virtual interviewer designed to streamline technical hiring processes. This chatbot conducts structured interviews, evaluates candidate responses, and provides a hiring probability score based on their technical proficiency. It integrates AI-powered question generation, authentication, and database management.

## Features
- Interactive AI-driven interview process
- Secure user authentication (Signup/Login)
- Dynamic technical question generation based on roles and skills
- Real-time validation of user inputs (name, email, phone, etc.)
- MongoDB integration for storing candidate details securely
- Gauge chart visualization for hiring probability
- Streamlit-based responsive UI with a professional design

---

## Installation Instructions
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- MongoDB (running on `localhost:27017` or update the URI in `data_handler.py`)

### Step 1: Clone the Repository
```sh
 git clone https://github.com/Jagdeesh-P/TalentScout-AI-Recruitment-Assistant.git
```

### Step 2: Install Dependencies
```sh
 pip install -r requirements.txt
```

### Step 3: Run the Application
```sh
 streamlit run app.py
```

---

## Usage Guide
The chatbot follows a structured hiring workflow. Below is the flowchart depicting the interaction process:

```
+----------------------+        +----------------------+        +----------------------+        +----------------------+
|  User Signup/Login   | ---->  |   Start Interview    | ---->  |  Answer Questions    | ---->  |   Get Evaluation     |
+----------------------+        +----------------------+        +----------------------+        +----------------------+
```

### Step-by-Step Process:
1. **Login/Signup**: Users must first log in or create an account.
2. **Start Interview**: The chatbot greets users and collects their personal and technical details.
3. **Answer Technical Questions**: AI dynamically generates domain-specific questions based on skills and experience.
4. **Get Evaluation**: At the end, the chatbot calculates a hiring probability score and provides feedback.

---

## Technical Details
### Libraries Used
- **Streamlit**: UI framework
- **Streamlit-Chat**: Chat UI components
- **Google Generative AI (Gemini-2.0-Flash)**: AI-powered interview assistant
- **Plotly**: Data visualization (hiring probability gauge)
- **Pymongo**: MongoDB database management
- **Python-Dotenv**: Secure API key storage

### Architecture
The system architecture follows a modular structure:

```
+------------+         +------------+         +------------+         +------------+
|  Frontend  | ---->   |  Backend   | ---->   |   AI API   | ---->   |  Database  |
+------------+         +------------+         +------------+         +------------+
```

- **Frontend**: Streamlit UI for chat interactions
- **Backend**: Python (handling authentication, validation, AI-driven responses)
- **Database**: MongoDB for storing candidate data securely
- **AI Model**: Gemini API for natural language processing

---

## Prompt Design
The chatbot formulates questions dynamically based on job roles and skills.

**Example Prompt for AI Question Generation:**
```text
Generate 5 technical interview questions on {technology} for a {roles} screening with {years} of experience.
The questions should be challenging but answerable in 2-3 lines, focused on practical knowledge and real-world applications.
```

**Example Prompt for Hiring Probability Calculation:**
```text
Evaluate the candidate based on their provided responses.
Complete data is provided
Return only a hiring probability percentage between 0 and 100%.
```

---

## Challenges & Solutions
### Challenge 1: AI-Generated Questions Were Too Generic
**Solution:** Enhanced prompt engineering to generate role-specific and experience-level-adjusted questions.

### Challenge 2: Secure Input Handling
**Solution:** Implemented regex-based validation and input sanitization to prevent injections.

### Challenge 3: Storing Candidate Data Securely
**Solution:** Used MongoDB instead of local storage, ensuring data integrity and privacy.

### Challenge 4: Maintaining UI Responsiveness
**Solution:** Custom CSS and optimized Streamlit elements for a better user experience.

---

## Screenshots & Visuals
*(Add UI screenshots, architecture diagrams, and chat flow images here.)*

---

## Future Enhancements
- Expand AI training for improved response evaluation
- Multi-language support for global hiring
- Admin dashboard for HR teams to manage candidates
- Voice-based interaction for better accessibility

---

## Contributors
- **Jagdeesh P** – Project Lead & Developer

For any queries, contact: [jagdeeshpersonal@gmail.com]

---

## License
MIT License (or specify your license)

---

*Happy Hiring!*

