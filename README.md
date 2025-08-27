# Experiment-1-Jupyter-Notebook-Test

This repository contains a Jupyter Notebook with three solved Python problems:

        1. ALPHABET SOUP PROBLEM
        2. EMOTICON PROBLEM
        3. UNPACKING LIST PROBLEM

each explained with code, outputs, and syntax definitions. It also includes step-by-step instructions on how to get started with Jupyter Notebook in Anaconda and how to upload your completed work to GitHub.

_____________________________________

Getting Started with Jupyter Noteboook

        To begin creating your Python code using Jupyter Notebook:
        
                1. Open Anaconda Navigator on your computer.
                2. Look for Jupyter Notebook and open it.
                3. Once Jupyter Notebook launches in your browser, you can create a folder to keep all your Jupyter files organized.
                4. Open the folder where you want to save your work.
                5. Click the New button (on the top-right side).
                6. From the dropdown, select Python 3 (ipykernel).
                
        A new Jupyter Notebook will open — and now you can start writing and running your Python code!

_____________________________________



Problem # 1.  

ALPHABET SOUP PROBLEM
                       - This program asks the user to enter a word, then rearranges the letters of that word in alphabetical order. It shows how to work with strings and sorting in Python.

---- CODE ---

     ALPHABET SOUP PROBLEM  # This is  the heading, it is a markdown cell that tells the reader that a problem is starting. 

	[]: def alphabet_soup(word):                                 # 'def' defines a function named alphabet_soup with parameter 'word'
              sorted_letters = sorted(word)                          # 'sorted()' arranges the letters in alphabetical order
              result = ''.join(sorted_letters)                       # "''.join()" combines the letters into one string
              return result                                          # 'return' gives back the final sorted string

     
	[]: word = input ("Enter a word: ")                          # 'input()' asks the user to type a word
            print("Alphabetically sorted: ", alphabet_soup(word))    # 'print()' calls the function and prints the result

--- EXECUTION / RUNNING THE CODE ---

To execute the code cell:

	1. Click inside the cell
	2. Then click the Run botton
	3. The output will appear dirctly below the cell

Note this are the outputs it may give:

         1. No Output: Nothing is displayed because the code only defines something it can be a function or variable but does not print it yet.
         2. Normal Output: This is when the program successfully prints a result. 
         3. Input Prompt: The program asks the user to type something before continuing.
         4. Error Message: A red message shown when the code has a mistake or when an undefined variable or function is used.
 

--- OUTPUT ---
     
	Enter a word: computer                  # This is the input prompt created by the input() function in Python. The program asks the user to type a word, and here the user typed "computer".
  	Alphabetically sorted: cemoprtu         # After the user enters teh word, the program processes it. It uses Python’s sorted() function to arrange the letters of the word in alphabetical order. Finally, the print() function displays the result.
 
--- DEFINITON OF SYNTAX USED ---

	1. def → keyword to define a function.
 	2. sorted() → built-in function that arranges items in ascending order.
	3. ''.join() → joins elements of a list into one string.
	4. return → sends back a value from inside a function.
	5. input() → lets the user type an answer.
	6. print() → displays output on the screen.



_____________________________________


Problem # 2

EMOTICON PROBLEM
                       - This program asks the user to enter a sentence, then replaces certain words (like "smile" or "sad") with their matching emoticons. It shows how to use dictionaries and string manipulation in Python.

---- CODE ---

        EMOTICON PROBLEM # This is  the heading, it is a markdown cell that tells the reader that a new problem is starting.
        
	[]: def emotify(sentence):                         #'def' defines a function named emotify with parameter 'sentence'
                replacements = {                           # dictionary to map words to emoticons
                    "smile": " :)",                        # "smile" is replaced by :)
                    "grin": " :D",                         # "grin" is replaced by :D
                    "sad": " :((",                         # "sad" is replaced by :((
                    "mad": " >:("                          # "mad" is replaced by >:(
    }
                words = sentence.split()                                             # 'split()' breaks the sentence into a list of words   
                converted = [replacements.get(word, word) for word in words]         # for each word, replace it if found in dictionary otherwise, keep the original word
                return "".join(converted)                                            # join the list into a single string and return it
                
	[]: sentence = input ("Enter a sentence: ")                                  # 'input()' asks the user to type a sentence
            print("Converted sentence: ", emotify(sentence))                         #'print()' calls the function and displays the converted sentence

--- EXECUTE / RUN THE CODE ---

Execute the code as you did previously.

--- OUTPUT ---

        Enter a sentence:  I am mad    # This is the input prompt created by the input() function. The program asks the user to type a sentence, and here the user typed "I am mad"
        Converted sentence:  I am >:(  # After the user enters the sentence, the program checks each word. It uses a dictionary to find matches and replace them with emoticons. The word mad was replaced with ">:("

--- DEFINITON OF SYNTAX USED ---

        1. def → keyword to define a function.
        2. dictionary { } → stores key-value pairs (ex: "smile": ":)").
        3. split() → breaks a string into a list of words.
        4. list comprehension [ ] → creates a new list in one line of code.
        5. .get() → gets a value from the dictionary; if not found, keeps the original word.
        6. ''.join() → joins elements of a list into one string.
        7. return → sends back a value from inside a function.
        8. input() → lets the user type a sentence.
        9. print() → shows text or results on the screen.


_____________________________________


Problem # 3        

UNPACKING LIST PROBLEM 
                       - This program asks the user to enter numbers separated by spaces, then splits the input into a list and unpacks it into the first item, the middle items, and the last item. It shows how to unpack lists and convert input to numbers in Python.

--- CODE --- 

        EMOTICON PROBLEM  #This is the heading, it is a markdown cell that tells the reader that a new problem is starting.
        
	[]:def unpack_list(lst):                                      # 'def' defines a function named unpack_list with parameter 'lst'
                first, *middle, last = lst                            # Unpacking: take the first item, middle items (as a list), and last item
                return first, middle, last                            # return the three parts
	[]:user_input = input("Enter number seperated by spaces: ")   # 'input()' asks the user to type numbers separated by spaces
           lst = [int(x) for x in user_input.split()]                 # Convert each piece to int and make a list
           first, middle, last = unpack_list(lst)                     # Call the function to unpack the list
           print("First: ", first)                                    # Print the first item
           print("Middle: ", middle)                                  # Print the middle items as a list
           print("Last: ", last)                                      # Print the last item

--- EXECUTE / RUN THE CODE ---

Execute the code as you did previously.

--- OUTPUT ---

        Enter number seperated by spaces:  1 2 3 4 5 6   # This is the input prompt created by the input() function. The program asks the user to type numbers separated by spaces, and here the user typed "1 2 3 4 5 6".
        First:  1                                        # The function returned the first item of the list (1). print() shows this value.
        Middle:  [2, 3, 4, 5]                            # The function returned the middle items as a list. print() shows the list [2, 3, 4, 5]
        Last:  6                                         # The function returned the last item of the list (6). print() shows this value.

--- DEFINITON OF SYNTAX USED ---

        1. def → keyword to define a function.
        2. Unpacking first, *middle, last → takes the first item, groups the middle items into a list, and takes the last item.
        3. list [] → stores multiple values in order.
        4. list comprehension [int(x) for x in user_input.split()] → short way to make a new list by converting each split string to an integer.
        6. split() → breaks the input string into parts using spaces.
        7. int() → converts a string to an integer.
        8. input() → lets the user type a line of text.
        9. print() → shows text or values on the screen.
        10. return → sends back values from a function.

        
_____________________________________


Now that you’re done with all the problems, the next step is to upload your Jupyter Notebook file to GitHub so it can be saved, shared, and accessed easily.

--- PROCEDURE FOR UPLOADING TO GITHUB ---

        1. After finishing all problems in the Jupyter Notebook, click File → Download as → Notebook (.ipynb) to save the file on your computer.
        2. Open your web browser and go to GitHub.
        3. Sign in to your GitHub account.
        4. On the top-right, click the + (plus) button and choose New repository.
        5. Enter a Repository Name (for example: Experiment-1-Jupyter-Notebook-Test).
        6. Turn on "Add a README file" so the repository starts with a description.
        7. Click Create repository.
        8. Once inside the repository, click Add file → Upload files.
        9. Click Choose your files and select the Jupyter Notebook file (.ipynb) you downloaded.
        10. Scroll down and click Commit changes to upload it.

Now your Jupyter Notebook is saved and viewable in your GitHub repository. 


        
