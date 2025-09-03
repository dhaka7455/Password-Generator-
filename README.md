# Password-Generator-
import random
import string

def generate_password(length=12, use_digits=True, use_special=True):
    # Basic character set
    characters = string.ascii_letters  
    
    # Add digits if selected
    if use_digits:
        characters += string.digits  
    
    # Add special symbols if selected
    if use_special:
        characters += string.punctuation  
    
    # Generate password
    password = ''.join(random.choice(characters) for _ in range(length))
    return password

# Example usage
print("🔑 Generated Password:", generate_password(12))

