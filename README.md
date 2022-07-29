# Python30A-project
#Business Python Program
print('Hello thank you for choosing StalkHunt')
print('This resturant provides a unique experience for every single one of our customers')
print()
print('The winner of the hunt will be rewarded with a delectable meal for twenty people.')
#providing overview infomation

#retrieving participants name
"""class name_input:
    def na(self):
        n = 6
        c = 0
        name = input('Please input name')
        c += c
        if c <= n:
            name.append()
    
        
            if name.isalnum() == True:
                print('The contestants name is: ', name)
            else:
                print('This is not a valid name')
                quit()""""


def nameinput():
    name = input('Please provide an alphanumeric name for the contestant: ')
    #checking if the name is valid
    print()
    if name.isalnum() == True:
        print('The contestants name is: ', name)
    else:
        print('This is not a valid name')
        quit()
        
print()
print('''The goal of the game is to hunt down as many animals as possible,
different animals are worth a certain amount of points.
Boars = 15 pts
Ducks = 5  pts
Deer  = 20 pts''')


def weapons_menu():
    print()
    print('**********Weapon Options**********')
    print('Choose an option')
    print('''
            option 1: Bow with 50 arrows
            option 2: Axe and a Bow with 15 arrows
            option 3: Spear and a Bow with 10 arrows
            ''')
weapons_menu()
choice = input('Please make a selection from 1, 2, or 3: ')

while choice != 0:
    if choice == 1:
        print('You have chosen a Bow with 50 arrows')
    elif choice == 2:
        print('You have chosen an Axe and Bow with 15 arrows')
    elif choice == 3:
        print('You have chosen a Spear and a Bow with 10 arrows')
    else:
        print('Invalid option')

#Calendar

from tkinter import *
from tkcalendar import*

window = Tk()
window.minsize(800,600)
window.title('StalkHunt Calendar')
window.configure(background = "#E10600")
#function will get the date once the button is pressed
def selectDate():
    myDate = mycalendar.get_date()
    Date_selected = Label(text = myDate)
    #placing button on the screen
    Date_selected.place(x = 425, y = 345)
    

mycalendar = Calendar(window, setmode = 'day', date_pattern = 'm/d/yy')
mycalendar.place(x = 350, y = 100)
#adding button
opencal = Button(window, text = 'Select your hunt date', command = selectDate) #this lines creates the button
#this next line puts the button on the screen
opencal.place(x = 425, y = 300)
