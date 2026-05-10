# python-assignment-
import random
import string

# Lottery numbers
lottery = random.sample(range(1, 51), 6)
print("Lottery Numbers:", lottery)

# Random password generator
letters = string.ascii_letters
digits = string.digits

all_characters = letters + digits

password = ''.join(random.choice(all_characters) for i in range(10))

print("Generated Password:", password)

# Random quiz question
questions = [
    "What is Python?",
    "What is a loop?",
    "What is a function?",
    "What is GitHub?"
]

question = random.choice(questions)

print("Practice Question:", question)