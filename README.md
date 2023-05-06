# Message_Encode_Decode
This objective of this project is to encode and decode messages using a common key. This project will be built using the Tkinter and base64 library.
In this project, users have to enter the message to encode or decode. Users have to select the mode to choose the encoding and decoding process. The same key must be used to process the encoding and decoding for the same message.

## Project Prerequisites

To build this project we will use basic concept of python, Tkinter, and base64 library.
Tkinter is a standard GUI python library
base64 module provides a function to encode the binary data to ASCII characters and decode that ASCII characters back to binary data.
To install the library we use pip install command on the command prompt

pip install tkinter
pip install base64

## Project File Structure
These are the step to build message encode – decode python project
Import module
Create display window
Define function
Define labels and buttons

## Steps to develop message encode-decode project

### 1. Import Libraries

### 2. Initialize Window

Tk(): initialized tkinter which means window created
	geometry(): set the width and height of the window
	resizable(0,0): set the fixed size of the window
	title(): set the title of the window
Label(): widget use to display one or more than one line of text that users aren’t able to modify.
root is the name which we refer to our window
text which we display on the label
font in which the text is written
pack organized widget in block

### 3. Define variables
Text variable stores the message to encode and decode
	private_key variable store the private key used to encode and decode
	mode is used to select that is either encoding or decoding
	Result store the result
  
### 4. Function to encode
Encode function have arguments – key and message
enc = [] is an empty list
We run loop till the length of the message
i% of len(key) gives the remainder of division between i and len(key) and that remainder used as an index of key the value of key at that index is stored in key_c
ord() function takes string argument of a single unicode character and return its integer unicode value
chr() function takes an integer argument and returns the string.
ord (message[i]) convert the value of message at index i into the integer value
ord(key_c) converts the key_c value to integer value
ord(message[i]) + ord(key_c)) % 256 gives the remainder of division of addition of ord(message[i]) and ord( key_c) with 256 and passes that remainder to chr() function
chr() function converts that integer value to string and store to enc
base64.urlsafe_b64encode encode a string.
The join() method joins each element of list, string, and tuple by a string separator and returns the concatenated string.
encode() method returns utf-8 encoded message of the string.
decode() method decodes the string.
return gives the result of the encoded string.

### 5. Function to decode
Decode() function has arguments – key, message
dec=[] is an empty list
Decode the content from input and write the result in binary to the output
We ran the loop till the length of the message
256 + ord(message[i]) – ord(key_c)) % 256 gives the remainder of addition of 256 with subtraction of ord(message[i]) – ord( key_c) and then division with 256 and passes that remainder to chr() function
chr() function convert integer value to string and store to dec
return “”.join(dec) return the result

### 6. Function to set mode
If the mode set by the user is ‘e’ then the Encode() function will be called
If the mode set to ‘d‘ then the Decode() function will be called
Else print ‘invalid mode’
private_key.get() and Text.get() values are pass to the arguments of Encode() and Decode() function

### 7. Function to exit window

root.destroy() will quit the program by stopping the mainloop()

### 8. Function to reset window
This function set all variables to empty string

### 9. Labels and Buttons
Label() widget use to display one or more than one line of text that users aren’t able to modify.
Entry() widget used to create an input text field.
Button() widget used to display button on our window
root is the name which we refer to our window
text which we display on the label
font in which the text is written
insertwidth use to set the width of the insertion cursor
bg sets the background colour
command is call when the button is click
textvariable used to retrieve the current text to the entry widget
root.mainloop() is a method that executes when we want to run our program.

# Message Encode-Decode Project output
![Screenshot (25)](https://user-images.githubusercontent.com/132753347/236623803-8cde0f23-c087-47ac-88ae-c50d5aa9917a.png)
![Screenshot (26)](https://user-images.githubusercontent.com/132753347/236623813-8b7c4341-aa80-4ae9-a093-9bd6fd67729c.png)


