# python-
The great part of creating your own GUI apps is that you can customize them however you want. From text font to background colour, all features are available for customization. In this article, I will take you through how to create a digital clock with Python.

Digital Clock with Python
In this section, I will show you how to create a digital clock using python. This is a simple task to get started with the Tkinter library in Python, which is a built-in package that comes with Python. Tkinter has some cool features that can be used to build simple apps.

Also, Read – 100+ Machine Learning Projects Solved and Explained.

Now let’s see how to create a digital clock GUI application with Python. I will first start with importing the libraries:

from tkinter import Label, Tk 
import time
Now let’s define the title and size of our application. Note that in the code below I will set both the height and width of the resizable function as True(1,1) if you want a fixed window and don’t want to maximize or minimize the output you can set it to False(0,0):

app_window = Tk() 
app_window.title("Digital Clock") 
app_window.geometry("420x150") 
app_window.resizable(1,1)
Now here I will define the font of the time and its colour, its border width and the background colour of the digital clock:

text_font= ("Boulder", 68, 'bold')
background = "#f2e750"
foreground= "#363529"
border_width = 25
Now here I will combine all the elements to define the label of the clock application:

label = Label(app_window, font=text_font, bg=background, fg=foreground, bd=border_width) 
label.grid(row=0, column=1)
Now let’s define the main function of our digital clock. Here I will set the text of the label as the realtime:

def digital_clock(): 
   time_live = time.strftime("%H:%M:%S")
   label.config(text=time_live) 
   label.after(200, digital_clock)
Now let’s run and see our output:

digital_clock()
app_window.mainloop()
digital_clock()
app_window.mainloop()
