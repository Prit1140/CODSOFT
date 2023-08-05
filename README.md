# CODSOFT
# Python Quiz Game

questions = ("Name the deepest ocean in the world?: ",
             "Name the gas which is filled in balloons?: ",
             "Which day is celebrated as Environment Day?: ",
             "Who was the first prime minister of India?: ",
             "Name the father of the Indian Constitution?: ")

options = (("A. Pacific Ocean", "B. Atlantic Ocean", "C. Arctic Ocean", "D. Indian Ocean"),
           ("A. Helium", "B. Argon", "C. Neon", "D. Nitrogen"),
           ("A. 21 June", "B. 5 September", "C. 5 June", "D. 21 December"),
           ("A. Jawaharlal Nehru", "B. Indira Gandhi", "C. Narendra Modi", "D. Rajendra Prasad"),
           ("A. Mahatma Gandhi", "B. Shikhar Dhawan", "C. B.R. Ambedkar", "D. Manmohan Singh"))

answers = ("A", "A", "C", "A", "C")
guesses = []
score = 0
question_num = 0

for question in questions:
    print("----------------------")
    print(question)
    for option in options[question_num]:
        print(option)

    guess = input("Enter (A, B, C, D): ").upper()
    guesses.append(guess)
    if guess == answers[question_num]:
        score += 1
        print("CORRECT!")
    else:
        print("INCORRECT!")
        print(f"{answers[question_num]} is the correct answer")
    question_num += 1

print("----------------------")
print("       RESULTS        ")
print("----------------------")

print("answers: ", end="")
for answer in answers:
    print(answer, end=" ")
print()

print("guesses: ", end="")
for guess in guesses:
    print(guess, end=" ")
print()

score = int(score / len(questions) * 100)
print(f"Your score is: {score}%")
