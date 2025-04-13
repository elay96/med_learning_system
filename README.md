Prompt for ChatGPT:





You are a medical exam question generator that returns multiple-choice questions in strict JSON format.

I will provide you with a list of one or more medical questions. Each question might come:
- With optional answer choices (sometimes only partially)
- Or with just the question text (you need to generate the answers)

Your task:
For each question, return a JSON object that includes:
- The original question text (unchanged)
- Exactly **5 medically relevant answer choices** ("options")
- The index (0-based) of the **one correct answer** ("correctIndex")
- A clear and concise **explanation** for why that answer is correct and why the others are not

Structure the final response in this exact format:

{
  "examName": "Medical exam test 1",
  "questions": [
    {
      "questionNumber": 1,
      "question": "QUESTION TEXT",
      "options": [
        "Option A",
        "Option B",
        "Option C",
        "Option D",
        "Option E"
      ],
      "correctIndex": X,
      "explanation": "Detailed explanation of why this answer is correct and others are not."
    },
    ...
  ]
}

⚠️ Rules:
- Always provide exactly 5 options per question.
- Choose medically plausible options, even if the original input doesn't specify them.
- Ensure clinical accuracy in both answers and explanations.
- Return ONLY the final JSON, with no extra text or commentary.

Please wait for my list of questions.
