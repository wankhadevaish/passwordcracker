# passwordcracker

import random
import pyautogui
import string

chars = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890!@#$%^&*<>:'~"
char_list =list(chars)#conv the same variable to list type

password = pyautogui.password("Enter password: ")
guess_password =""


while(guess_password!=password):
    guess_password =random.choices(char_list, k=len(password))
    print("<============"+ str(guess_password) +"=============>")

    if(guess_password == list(password)):
        print("Cracked Password: "+"".join(guess_password))
        input()
        break
