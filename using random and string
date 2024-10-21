import random
import string

def generate_password(length):
    if length < 4:
        raise ValueError("Password length should be at least 4 characters.")
    
    # Define the character sets
    upper = string.ascii_uppercase
    lower = string.ascii_lowercase
    digits = string.digits
    special = string.punctuation
    
    # Ensure the password contains at least one character from each set
    password = [
        random.choice(upper),
        random.choice(lower),
        random.choice(digits),
        random.choice(special)
    ]
    
    # Fill the rest of the password length with a mix of all characters
    all_characters = upper + lower + digits + special
    password += random.choices(all_characters, k=length - 4)
    
    # Shuffle the password list to ensure random order
    random.shuffle(password)
    
    # Convert list to string
    return ''.join(password)

# Example usage
password_length = 12  # Set your desired password length
print(generate_password(password_length))
