# Exno.7 – Prompt Engineering



---

## Aim:

To develop a **prompt-based application** tailored to personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

---

## Algorithm:

1. Define the Problem:
Identify a real-world task to be solved using prompt engineering. For this exercise, the task is to organize daily tasks effectively.

2. Design a Simple Prompt:
Create a basic prompt to list tasks.

Example:
“Help me list the tasks I need to complete today.”

3. Test the Simple Prompt:
Execute the prompt and review the output. Adjust wording if necessary to make it more detailed.

4. Design an Intermediate Prompt:
Create a prompt that organizes tasks based on priority and time.

Example:
“Help me organize my tasks for today by priority and assign time slots for each task.”

5. Test the Intermediate Prompt:
Execute and review the output. Refine to include categories such as urgent, important, and optional.

6. Design an Advanced Prompt:
Enhance the prompt to include reminders, dependencies, and estimated time.

Example:
“Help me create a structured daily plan with task descriptions, deadlines, dependencies, estimated durations, and reminders.”

7. Test the Advanced Prompt:
Execute and review how it schedules tasks with realistic timelines and suggestions.

8. Evaluate and Improve:
Review the results, incorporate feedback, and iterate for better clarity, structure, and relevance.
---

## Python Code:

```python
# Daily Task Organizer using ChatGPT

import openai

# Set API Key
openai.api_key = "your_openai_api_key"

# Function to query ChatGPT
def ask_chatgpt(prompt):
    try:
        response = openai.ChatCompletion.create(
            model="gpt-4",
            messages=[{"role": "user", "content": prompt}]
        )
        return response.choices[0].message.content
    except Exception as e:
        return f"Error: {e}"

# Step 1: Basic Prompt - Simple Task List
prompt1 = "List 5 tasks I should complete today for productivity."
print("=== Basic Prompt ===")
print(ask_chatgpt(prompt1), "\n")

# Step 2: Intermediate Prompt - With Priorities
prompt2 = "Organize my daily tasks into High, Medium, and Low priority categories."
print("=== Intermediate Prompt ===")
print(ask_chatgpt(prompt2), "\n")

# Step 3: Advanced Prompt - With Time Allocation and Motivation
prompt3 = ("Create a structured daily plan for my tasks with estimated time allocations, "
           "short breaks, and a motivational quote at the end.")
print("=== Advanced Prompt ===")
print(ask_chatgpt(prompt3))
```

---

## Sample Output:

```
Simple Prompt:
“List the tasks I need to complete today.”
Output:

Finish Python assignment

Prepare for the math test

Grocery shopping

Call friend for group project discussion

Read 2 chapters from programming book

Intermediate Prompt:
“Organize today’s tasks by priority and assign time slots.”
Output:

Finish Python assignment – High Priority – 10:00 AM to 12:00 PM

Prepare for math test – High Priority – 1:00 PM to 3:00 PM

Grocery shopping – Medium Priority – 4:00 PM to 5:00 PM

Call friend for group project discussion – Medium Priority – 5:30 PM to 6:00 PM

Read 2 chapters from programming book – Low Priority – 7:00 PM to 8:00 PM

Advanced Prompt:
“Create a structured daily plan with task details, priorities, dependencies, estimated times, and reminders.”
Output:

Task	Priority	Start Time	Duration	Dependencies	Reminder
Finish Python assignment	High	10:00 AM	2 hours	None	9:45 AM
Prepare for math test	High	1:00 PM	2 hours	Python assignment must be completed first	12:45 PM
Grocery shopping	Medium	4:00 PM	1 hour	None	3:45 PM
Call friend for project discussion	Medium	5:30 PM	30 mins	None	5:15 PM
Read programming book	Low	7:00 PM	1 hour	None	6:45 PM
```

---

## Result:

The prompt-based application was executed successfully. Starting from a basic prompt to organize daily tasks, the process evolved into a more structured and efficient plan using progressively advanced prompts. The application demonstrated how creativity, problem-solving, and clear communication with large language models like ChatGPT can yield practical solutions for personal productivity.

---
