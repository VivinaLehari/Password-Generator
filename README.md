# Password-Generator
import string
import random
length = int(input("Enter the password length: "))
print('''Choose the character options to be used in the passowrd :
1. Alphabets
2. Numbers
3. Special characters
4. Generate''')
characterList = ""
while(True):
	choice = int(input("character options to set password "))
	if(choice == 1):
		characterList += string.ascii_letters
	elif(choice == 2):
		characterList += string.digits
	elif(choice == 3):
		characterList += string.punctuation
	elif(choice == 4):
		break
	else:
		print("Please pick a valid option!")
password = []
for i in range(length):
	randomchar = random.choice(characterList)
	password.append(randomchar)
print("The password generated is " + "".join(password))
