# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:

```

def caesar_cipher(text, shift):
    result = ""

    for char in text:
        if char.isupper():
            result += chr((ord(char) - 65 + shift) % 26 + 65)
        elif char.islower():
            result += chr((ord(char) - 97 + shift) % 26 + 97)
        else:
            result += char

    return result
message = input("Enter the message: ")
shift_value = int(input("Enter shift value: "))
encrypted_text = caesar_cipher(message, shift_value)
print("Encrypted message:", encrypted_text)
decrypted_text = caesar_cipher(encrypted_text, -shift_value)
print("Decrypted message:", decrypted_text)


````


## OUTPUT:

<img width="1512" height="695" alt="image" src="https://github.com/user-attachments/assets/7f6a5088-b1ba-4df3-985d-c3a618ea8b02" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
