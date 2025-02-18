# Mini Quiz Program with Options

def mini_quiz():
    questions = [
        {
            "question": "1. What is the capital of India?",
            "options": ["A. Mumbai", "B. New Delhi", "C. Kolkata", "D. Chennai"],
            "answer": "B"
        },
        {
            "question": "2. Which direction does the Sun rise?",
            "options": ["A. North", "B. South", "C. East", "D. West"],
            "answer": "C"
        },
        {
            "question": "3. Who created the Python programming language?",
            "options": ["A. James Gosling", "B. Guido van Rossum", "C. Dennis Ritchie", "D. Bjarne Stroustrup"],
            "answer": "B"
        }
    ]
    
    score = 0
    
    print("Welcome to the Mini Quiz! Answer the following questions:")
    
    for q in questions:
        print(q["question"])
        for option in q["options"]:
            print(option)
        
        user_answer = input("Your answer (Enter A, B, C, or D): ").strip().upper()
        
        if user_answer == q["answer"]:
            print("Correct! 👍\n")
            score += 1
        else:
            print(f"Wrong! The correct answer is: {q['answer']}\n")
    
    print(f"Your final score: {score}/{len(questions)}")
    if score == len(questions):
        print("Awesome! You got all the answers right! 🎉")
    else:
        print("Good try! You can do better next time! 😊")

# Run the quiz
mini_quiz()
