# GUI-Project
import random
import tkinter
fred = tkinter.Tk()
fred.title("PadLock- Get your passwords secure")
homePage = tkinter.Frame(fred, bg="blue", height=500, width=500)
homePage.grid_propagate(False)
homePage.grid(row=0, column=0, sticky="nsew")
pageOne = tkinter.Frame(fred, bg="blue")
pageOne.grid(row=0,column=0, sticky="nsew")
homePage.tkraise()
def showHome():
    homePage.tkraise()
def showPageOne():
    pageOne.tkraise()
label1=tkinter.Label(pageOne, text="First Name:",bg='blue', fg='white')
label2=tkinter.Label(pageOne, text="Last Name:",bg='blue', fg='white')
label3=tkinter.Label(pageOne, text="What's your favorite number?",bg='blue', fg='white')
label4=tkinter.Label(pageOne, text="Your password will be at least 15 characters.",bg='blue',fg='white')
space=tkinter.Label(pageOne, text="",bg='blue')
space2=tkinter.Label(pageOne, text="",bg='blue')
space3=tkinter.Label(pageOne, text="",bg='blue')
space4=tkinter.Label(pageOne, text="",bg='blue')
entry1=tkinter.Entry(pageOne)
entry2=tkinter.Entry(pageOne)
entry3=tkinter.Entry(pageOne)
label1.grid(row=1, sticky='w')
label2.grid(row=3, sticky='w')
label3.grid(row=5, sticky='w')
label4.grid(row=7, sticky='w')
space.grid(row=2, sticky='w')
space2.grid(row=4,sticky='w')
space3.grid(row=6,sticky='w')

entry1.grid(row=1, column=1)
entry2.grid(row=3, column=1)
entry3.grid(row=5, column=1)
label5=tkinter.Label(pageOne,text="",bg='blue')
label5.grid(row=8,columnspan=20,sticky='w')
def generator():
    password = entry1.get()+""+entry2.get()+""+entry3.get()
    characters = ["!","@","#","$","%","^","&","*"]
    while(len(password)<15):
        symbol_index = random.randrange(len(characters))
        new_symbol = characters[symbol_index]
        password += new_symbol
    label5.configure(text="Your password is: " + password,bg='blue', fg='white', font=('Helvetica',12,'bold'))



home_label= tkinter.Label(homePage, text="Welcome to PadLock!", fg="white",bg="blue",height=10,font=("Times New Roman",25))
home_label.grid(column=0,row=0)
home_label.config(width=30)
fred.columnconfigure(0, weight=1)
fred.rowconfigure(0, weight=1)
goToOne=tkinter.Button(homePage, text= "Create a password!", bg="white", fg="blue",command=showPageOne,width=20)
goToOne.grid(row=1,column=0)
generate= tkinter.Button(pageOne, text="Generate password", bg="white", fg="blue",width=20, command=generator)
generate.grid(row=9, column=0,sticky='w')
goHome= tkinter.Button(pageOne, text= "Go to Home Page", bg="black", fg="white",command=showHome,width=20)
goHome.grid(row=11,column=0,sticky='w')
fred.mainloop()
