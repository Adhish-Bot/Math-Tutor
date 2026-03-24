import random
import time

firstNumber = [0,1,2,3,4,5,6,7,8,9,10,11,12]
secondNumber = [0,1,2,3,4,5,6,7,8,9,10,11,12]
numOfCorrect = 0
numOfWrong = 0

numOfQuestion = int(input("How many question would you like to answer?: "))

start_time = time.time() 

for question in range(numOfQuestion):
    firstNumAsked = random.choice(firstNumber)
    secondNumAsked = random.choice(secondNumber)
    correctAnswer = firstNumAsked * secondNumAsked
    questionAnswered = int(input(f"{question + 1}. {firstNumAsked} * {secondNumAsked}"))
    
    if questionAnswered == correctAnswer:
        numOfCorrect += 1
    else:
        numOfWrong += 1
end_time = time.time()  
total_time = end_time - start_time 
percentage = (numOfCorrect / numOfQuestion) * 100

print("Thank you for playing this game!!!")
print("---Summary---")
print(f"\nYou took {total_time:.2f} seconds to finish the quiz.")
print(f"Correct answers: {numOfCorrect}")
print(f"Wrong answers: {numOfWrong}")
print(f"Your grade: {percentage}")
