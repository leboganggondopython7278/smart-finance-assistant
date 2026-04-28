# 📓 Developer's Diary – Budget Buddy Smart Finance Assistant

# 📓 Developer's Diary — Budget Buddy Smart Finance Assistant

**Student:** Lebogang Nyasha Gondo
**Unit:** ISYS2001 — Introduction to Business Programming
**Project:** Budget Buddy — Smart Finance Assistant
**Repository:** Final-Programming-Project-budget-buddy-lebogang
**Due Date:** Friday 22 May 2026
**AI Tools Used:** Claude (Anthropic), ChatGPT (OpenAI), Google Gemini

---

## 🎯 Project Summary

I am building Budget Buddy  a Smart Finance Assistant that 
allows users to upload a CSV file of their expenses, analyse 
their spending patterns, and receive personalised financial 
advice through a chatbot interface.

---

## 🗓️ Week 3 — Project Planning & Foundation

**Date:** March 2026
**AI Tools Used:** Google Gemini

**What I did this week:**
- Reviewed the full project specification and assessment rubric
- Decided on Budget Buddy theme
- Set up the Developer's Diary structure
- Identified how each lab ticket connects to the final project

**AI Use this week:**
Used Google Gemini to help understand the project brief, 
clarify what RAG and Agent Tools mean, and plan the 
diary structure.

---

## 🗓️ Week 4 — Loops & Multiple Transactions

**Date:** 17 March 2026
**AI Tools Used:** ChatGPT (OpenAI) and Google Gemini

**Goal:**
Add loops to handle multiple expenses in one session.

**Artifact:**
```python
while True:
    expense_input = input("[CELESTI] Expense amount (or 'done'): $")
    if expense_input.lower() == 'done':
        break
    try:
        amount = float(expense_input)
        expenses.append(amount)
        total_spent += amount
    except ValueError:
        print("CELESTI says: Invalid amount!")
```

**Context:**
I was trying to build a loop that collects multiple 
expenses and stops when the user types done.

**Reflection:**

What worked:
Before this week I froze when I saw code and did not 
know where to start. Breaking the problem into smaller 
pieces helped me understand each part separately before 
putting it all together. I found it helpful to think of 
the loop like a cashier scanning items — they keep going 
until the customer says they are finished.

What did not work:
ChatGPT code sometimes had indentation errors and did 
not run properly the first time. I used Gemini to cross 
check the code which helped me find the mistakes. I 
learned not to rely on one AI tool alone.

What I learned:
While loops keep running when you do not know how many 
times to repeat. For loops are better when you know the 
exact number. Storing expenses in lists instead of one 
variable made it possible to analyse, search and 
summarise all transactions.

**GitHub Commit:**
Week 4 - Added loop-powered CELESTI Finance Tracker 
with input validation and interactive menu

---

## 🗓️ Week 5 — Functions & Modular Design

**Date:** 19 March 2026
**AI Tools Used:** ChatGPT (OpenAI) and Google Gemini

**Goal:**
Learn how to break code into functions and use the 
pyinputplus library for better input validation.

**Artifact:**
```python
import pyinputplus as pyip

def get_number(prompt):
    return pyip.inputFloat(prompt)

def perform_calculation(operation, num1, num2):
    if operation == "1":
        return add(num1, num2)
    elif operation == "2":
        return subtract(num1, num2)
```

**Context:**
I was trying to break a calculator into separate 
functions where each function has one job, and replace 
manual input validation with pyinputplus.

**Reflection:**

What worked:
Three analogies helped me understand functions — the 
restaurant where each staff member has one role, the 
recipe written once and used many times, and the SAP 
module testing where you test each part separately 
before combining.

What did not work:
Seeing the full code all at once caused confusion. 
Working through one blank at a time with hints was 
much more effective.

What I learned:
Six keywords are the foundation of functions — def 
creates them, return sends answers back, print shows 
output, input collects user input, float converts text 
to numbers, and if/elif checks conditions.

**GitHub Commit:**
Week 5 - Added modular calculator with pyinputplus 
for better input validation

---

## 🗓️ Week 8 — Setup & AI Integration ⭐

**Date:** 29 April 2026
**AI Tools Used:** Copilot

**Artifact:**
```python
# Install all required libraries
!pip install gradio pandas hands-on-ai -q

import pandas as pd
import os

# Configure AI connection
os.environ['HANDS_ON_AI_SERVER'] = 'https://ollama.serveur.au'
os.environ['HANDS_ON_AI_MODEL'] = 'llama3.2'
os.environ['HANDS_ON_AI_API_KEY'] = 'isys2001-assignment-key'

print("✅ Budget Buddy AI configured successfully!")
```

**Context:**
I set up the Budget Buddy repository from the template 
and installed all required libraries including 
hands-on-ai, gradio and pandas in Google Colab.

**Reflection:**

What worked:
Library installation worked after removing the # symbol 
that was blocking the install command. Copilot explained 
that # mutes a line of code which is why the original 
starter code was not installing anything.

What did not work:
The university AI server at ollama.serveur.au returned 
connection errors on first attempts. Also replaced 
getpass popup with hardcoded API key for simplicity.

What I learned:
A # symbol comments out code making Python ignore that 
line completely. The os.environ dictionary stores 
environment settings that other programs can read — 
like storing the server address and password for the 
AI connection. I also learned to use multiple AI tools 
together — Copilot identified issues that other tools 
missed.

**GitHub Commit:**
Week 8 - Set up Budget Buddy repository and installed 
required libraries

---

## 🗓️ Week 9 — Chatbot Personality ⭐

**Date:** (to be completed)
**AI Tools Used:** Claude (Anthropic)

**Goal:**
Build the finance-oriented chatbot personality 
using hands-on-ai.

**Artifact:** (to be completed)

**Context:** (to be completed)

**Reflection:** (to be completed)

**GitHub Commit:** (to be completed)

---

## 🗓️ Week 10 — RAG Component ⭐

**Date:** (to be completed)
**AI Tools Used:** Claude (Anthropic)

**Goal:**
Implement RAG so the chatbot reads the user's 
CSV expense file before answering.

**Artifact:** (to be completed)

**Context:** (to be completed)

**Reflection:** (to be completed)

**GitHub Commit:** (to be completed)

---

## 🗓️ Week 11 — Agent Tool ⭐

**Date:** (to be completed)
**AI Tools Used:** Claude (Anthropic)

**Goal:**
Build and register a custom budget calculator 
tool the chatbot can call automatically.

**Artifact:** (to be completed)

**Context:** (to be completed)

**Reflection:** (to be completed)

**GitHub Commit:** (to be completed)

---

## 🗓️ Week 12 — Gradio UI & Full Integration ⭐

**Date:** (to be completed)
**AI Tools Used:** Claude (Anthropic)

**Goal:**
Build the Gradio interface and connect Chat, RAG 
and Agent Tool together into one working app.

**Artifact:** (to be completed)

**Context:** (to be completed)

**Reflection:** (to be completed)

**GitHub Commit:** (to be completed)

---

## 🗓️ Week 13 — Final Testing & Submission

**Date:** Due Friday 22 May 2026

**Final Checklist:**
- [ ] Colab Notebook complete with all 6 steps
- [ ] Chat component working
- [ ] RAG component working
- [ ] Agent Tool working
- [ ] Gradio UI working and polished
- [ ] Testing Section complete
- [ ] README.md updated
- [ ] Developer's Diary complete for Weeks 8-12
- [ ] GitHub has 1 commit per week Weeks 8-12
- [ ] kevin-blasiak-curtin added as collaborator
- [ ] ZIP file prepared for submission
