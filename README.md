# ECE2112_Programming-Assignment-1
Advance Computer Programming SY 2025-2026
- Name: Ruiz, Justin Danrei C || 2ECE-C
- Intended Learning Outcomes:
  1. To identify the basic codes and functions in Python Programming
  2. To be able to apply the different codes and functions in creating a Python program
## 📝Contents of this Assignment 📝
- Contains the assignment of the Programming Assignment, with 3 problems:
   1. **Alphabet Soup Problem** - A program that sorts the letters of a word alphabetically using list and sorts
      ``Ex: hello - ehllo``
``` python
# Alphabet Soup Problem
# The function alphabet_soup takes a word
# and returns the letters arranged in alphabetical order.
# Arranging using lists and for loops
def alphabet_soup(strng):  # declaring alphabet_soup
    lists = [] # Declaring the list as an empty list first
    lists = list(strng)  # the lists variable will hold the list version of as string
    lists.sort()      # with the .sort function, it sorts each letter alphabetically
    result = ""         # empty string that we will us to go back to normal
    
    for x in lists:  # For every x in the lists, result will have "" + the value of x in list
        result += "" + x # let's say result = "" + x (which is currently h)
    print(result) # prints the result
# Test cases
alphabet_soup("hello")   # prints hello to ehllo
alphabet_soup("hacker")  # prints hacker to acehkr
```
   2. **Emoticon Problem** - A program that checks a sentence and replaces emotion words with emoticons/emojis using get function
      ``Ex: Happy - :)``
``` python
# Emoticon Problem
# The function emotify takes a phrase string,
# checks if certain emotion words are detected,
# and replaces them with the appropriate emoticon.
def emotify(phrase): # Declares emotify function
    # Replaces "smile" in any capitalization with :D
    phrase = phrase.replace("smile", ":)")  # Replaces smile with :)
    phrase = phrase.replace("Smile", ":)")  # Replaces Smile with :)
    phrase = phrase.replace("SMILE", ":)")   # Replaces SMILE with :)
    # replaces "grin" in any capitalization with ":D"
    phrase = phrase.replace("grin", ":D") # Replaces grin with :D
    phrase = phrase.replace("Grin", ":D") # Replaces Grin with :D
    phrase = phrase.replace("GRIN", ":D") # Replaces GRIN with :D
    # replaces "sad" in any capitalization with ":(("
    phrase = phrase.replace("sad", ":((") # Replaces sad with :((
    phrase = phrase.replace("Sad", ":((") # Replaces Sad with :((
    phrase = phrase.replace("SAD", ":((") # Replaces SAD with :((
    # replaces "mad" in any capitalization with ">:("
    phrase = phrase.replace("mad", ">:(") # Replaces mad with >:(
    phrase = phrase.replace("Mad", ">:(") # Replaces Mad with >:(
    phrase = phrase.replace("MAD", ">:(") # Replaces MAD with >:(
    return phrase # returns the phrase
print(emotify("Make me smile"))    # Make me :)
print(emotify("I am mad"))         # I am >:(
```
   3. **Unpacking list** - A program that shows the first list, the last element, and the rest as a middle element of the list using dictionary and list
      `` Ex: first, middle, last``
``` python
# Unpack List Problem
# The function unpack_list takes a list
# prints the list with the appropriate index and using slicing 
def unpack_list(lst): # Declares function unpack_list
    print("first:", lst[0], "   middle:", lst[1:-1], "   last:", lst[-1]) # Since list's elements start at 0, it picks the 0 index, in the middle, the 1st index or the 2nd element up until the -1 which is the last
    # then the last prints the -1 index or the last element
unpack_list([1, 2, 3, 4, 5, 6]) # Prints the result based on the list
```
### Code Explanation

1. **Alphabet Soup Problem**
   - A function `alphabet_soup(strng)` is defined to **arrange letters of a word in alphabetical order**.  
   - The word is converted into a list using `list(strng)` and sorted with `.sort()`.  
   - A loop then rebuilds the sorted list into a string.  
   - Example: `"hello"` → `"ehllo"`, `"hacker"` → `"acehkr"`.  

2. **Emoticon Problem**
   - A function `emotify(phrase)` checks for certain words and **replaces them with emoticons**.  
   - Words like `"smile"`, `"grin"`, `"sad"`, `"mad"` (case-sensitive variations included) are replaced with symbols like `:)`, `:D`, `:((`, `>:(`.  
   - Example: `"Make me smile"` → `"Make me :)"`, `"I am mad"` → `"I am >:("`.  

3. **Unpack List Problem**
   - A function `unpack_list(lst)` prints the **first, middle, and last elements** of a list.  
   - `lst[0]` gives the first element, `lst[1:-1]` gives all elements except the first and last, and `lst[-1]` gives the last element.  
   - Example: `[1, 2, 3, 4, 5, 6]` → `first: 1   middle: [2, 3, 4, 5]   last: 6`.  

## 💭 Why it's useful 💭
- Alphabet Soup Problem explores the creative use of sorting operations and the use of lists
- Emoticon Problem explores how we can use the replace or get operation
- A useful way to define a variable using the index (as well as a negative index)
## Personal Notes
- Python is quite difficult to learn for me compared to C++, which is odd because the majority agree that Python is easier. I hope that I'll continue to learn more in Python
- I use several resources online in my coding assignment; however, I try to use the code from the Basic Computing.ipynb as much as possible
## 📁How to run 📁
1. Clone or download the repository
2. Open the .ipynb file in Jupyter Notebook, preferably in the latest version
3. Run all cells in order to test the program
