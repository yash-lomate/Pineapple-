# Pineapple-
A team project for excellence

Our entry for the **IEEE AI Hackathon 2026 – Multimodal LLM Challenge** 

## The problem
A high school teacher often teaches more than 100 students across several classes. They do not have time to check if each student really understands the work, or to give each student practice on their own weak topics. Also, a good grade does not always mean real understanding.

## What we are building
A tool for **high school teachers and students** that runs fully on our own machine, with open-weight AI models. No student data goes to the cloud.

It works **alongside the school's LMS** (Google Classroom or Canvas). It does not replace the LMS. The LMS keeps assignments and official grades. Our tool shows what each student actually understands.

## How it works (first version)
1. The teacher uploads course notes, an answer key and a rubric.
2. The student uploads their work, for example a photo of handwritten math or physics.
3. The AI checks the work against the rubric and gives a **draft grade with feedback**. The teacher approves or changes it. The AI never gives a final grade alone.
4. The student does a short **viva**: 2–3 questions about their own work, answered by voice. The AI marks each topic as *solid*, *partial* or *missing*.

## Later, if we have time
- **Practice worksheets** made for each student's weak topics
- **Video** answers: the student records a short clip explaining their solution
- **Code**: small Python programs for practice problems, such as a physics simulation
- **Class view** for teachers and a **progress page** for parents
- **Doubts chat** that answers only from the teacher's materials, and says so when the answer is not there

## Modalities
| Input | Where we use it |
|---|---|
| Image | Photos of handwritten student work |
| Text | Teacher notes, rubric and answer key, used as the knowledge base |
| Audio | Voice answers in the viva |
| Video | Short "explain your solution" clips (later) |
| Code | Generated practice code (later) |

## Technology
- **AI model:** Gemma 4 12B, one open-weight model that takes text, image, audio and video
- **Run locally with:** Ollama or llama.cpp
- **Backend:** Python, with LangGraph for the AI steps and RAG over the teacher's materials
- **Interface:** a website for now (it may become a desktop app). It should also work on a phone.