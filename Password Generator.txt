import random
import string

def generate_password(length=12, include_digits=True, include_symbols=True):
    characters = string.ascii_letters
    
    if include_digits:
        characters += string.digits
        
    if include_symbols:
        characters += string.punctuation

    password = ''.join(random.choice(characters) for _ in range(length))
    return password

def main():
    print("\nWelcome to the Password Generator!")
    
    length = int(input("Enter the password length: "))
    include_digits = input("Include digits? (yes/no): ").lower() == "yes"
    include_symbols = input("Include symbols? (yes/no): ").lower() == "yes"

    password = generate_password(length, include_digits, include_symbols)
    print("Generated Password:", password)

if __name__ == "__main__":
    main()