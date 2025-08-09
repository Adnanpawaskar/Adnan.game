# Adnan.game
import random
import time

# Bestie's name
bestie_name = "Sara"

# Your custom secret words
secret_words = ["best friend", "sara", "padhaku", "moti", "chocolate"]

# Pick a random secret word
word = random.choice(secret_words)

print(f"💖 Hey {bestie_name}! Welcome to the BEST game ever made just for you! 💖")
time.sleep(1)
print("I have chosen a secret word... Can you guess it? 😏")
time.sleep(1)

attempts = 5

while attempts > 0:
    guess = input("Enter your guess: ").lower()

    if guess == word:
        print(f"🎉 OMG {bestie_name}! You guessed it! The word was '{word}'! You're amazing! 🎉")
        break
    else:
        attempts -= 1
        print(f"❌ Nope! You have {attempts} tries left.")
        
        # Give a hint
        if attempts == 3:
            print(f"Hint: It starts with '{word[0]}' 😉")
        elif attempts == 1:
            print(f"Hint: It has {len(word)} letters... Hurry! 😅")

if attempts == 0:
    print(f"😢 Oh no! You lost. The word was '{word}'. But don't worry, you're still awesome {bestie_name}! 💖")
