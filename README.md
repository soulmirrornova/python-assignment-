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





#python-assignment2.py
import requests
from bs4 import BeautifulSoup
import pandas as pd

url = "https://books.toscrape.com/"

response = requests.get(url)

soup = BeautifulSoup(response.text, "html.parser")

books = soup.find_all("h3")

titles = []

for book in books:
    title = book.text
    titles.append(title)

print(titles)

data = pd.DataFrame({
    "Book Titles": titles
})

data.to_csv("books.csv", index=False)

print("Data saved to books.csv")