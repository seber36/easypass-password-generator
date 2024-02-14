import random
import string

def easypassgen(length, use_uppercase, use_lowercase, use_digits, use_special_chars):
    chars = ''
    if use_uppercase:
        chars += string.ascii_uppercase
    if use_lowercase:
        chars += string.ascii_lowercase
    if use_digits:
        chars += string.digits
    if use_special_chars:
        chars += string.punctuation

    if not chars:
        print("Error: No character set selected.")
        return None

    return ''.join(random.choice(chars) for _ in range(length))

def userinput():
    length = int(input("password length: "))
    use_uppercase = input("Include uppercase letters? (yes/no/y/n): ").lower() in ['y', 'yes']
    use_lowercase = input("Include lowercase letters? (yes/no/y/n): ").lower() in ['y', 'yes']
    use_digits = input("Include digits? (yes/no/y/n): ").lower() in ['y', 'yes']
    use_special_chars = input("Include special characters? (yes/no/y/n): ").lower() in ['y', 'yes']
    return length, use_uppercase, use_lowercase, use_digits, use_special_chars

def savepasstofile(password):
    with open("generatedpasses.txt", "a") as file:
        file.write(password + "\n")

length, use_uppercase, use_lowercase, use_digits, use_special_chars = userinput()

password = easypassgen(length, use_uppercase, use_lowercase, use_digits, use_special_chars)
print("Generated Password:", password)

savepasstofile(password)
print("password saved")
