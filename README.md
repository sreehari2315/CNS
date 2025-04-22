## EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
### Name:Sree Hari K
### Register Number:212223230212

## AIM:

To implement the simple substitution technique named Caesar cipher using Python.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


## PROGRAM :-
~~~
# A Python program to illustrate Caesar Cipher Technique

def encrypt(text, s):
    result = ""

    # Traverse the text
    for i in range(len(text)):
        char = text[i]

        # Encrypt uppercase characters
        if char.isupper():
            result += chr((ord(char) + s - 65) % 26 + 65)

        # Encrypt lowercase characters
        elif char.islower():
            result += chr((ord(char) + s - 97) % 26 + 97)
        
        # Keep non-alphabetic characters unchanged
        else:
            result += char

    return result

text = input("Enter the text: ")
s = int(input("Enter the shift value: "))

print("Text  : " + text)
print("Shift : " + str(s))
print("Cipher: " + encrypt(text, s))

~~~
## OUTPUT :-

![image](https://github.com/user-attachments/assets/022c96d5-00d7-4811-9bb2-1b0656e0e04a)

## Result:
Thus To implement the simple substitution technique using Caesar cipher has been executed successfully.
