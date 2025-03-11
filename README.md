import random
import string

def generate_password():
    letters = string.ascii_letters  # Uppercase and lowercase letters
    digits = string.digits  # Numbers
    special_chars = string.punctuation  # Special characters
    
    # Ensure password meets criteria
    password = (
        random.choices(letters, k=5) +  # 5 letters
        random.choices(digits, k=2) +  # 2 numbers
        random.choices(special_chars, k=3)  # 3 special characters
    )
    
    random.shuffle(password)  # Shuffle to randomize order
    return "".join(password)

# Generate and print a password
print(generate_password())
