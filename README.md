Download Link: https://assignmentchef.com/product/solved-encode_decode-py
<br>
<span class="kksr-muted">Rate this product</span>

In this program, you’ll write two functions that “encode” and “decode” a string: num_to_let and let_to_num. You’ll use these two functions in an interactive program that allows a user to enter strings to be encoded and decoded.



If you use chr and ord for this assignment, this table of unicode to code point translations may come in handy:

<a href="http://www.utf8-chartable.de/unicode-utf8-table.pl?utf8=dec" target="_blank" rel="nofollow noopener">http://www.utf8-chartable.de/unicode-utf8-table.pl?utf8=dec</a>

Part 1—–

Write a function called num_to_let that takes a string that consists of numbers separated by dashes, and decodes (translates) it to letters  by converting each number into its corresponding uppercase letter in the alphabet based on position. Assume that the numeric position of  a letter starts at 1:

1 = A, 2 = B, 3 = C … Z = 26

So, passing the string “1-3-3-26-1” into the function would give back the resulting string: “ACCZA”. Note that the dashes serve as separators between the numbers, and the resulting string discards the dashes.

If the value between the dashes is not a number and it’s not between 1  and 26 inclusive, ignore it. Passing the string, “1-100-??-26” would result in “AZ” because 100 and ?? do not correspond to a position of a letter.

YOU MUST FIND A WAY TO SPLIT THE STRING MANUALLY. Do not use the “split”  method on your string (there will be a 50% penalty for using split).

Feel free to write assertions to test your function. Here are some examples  of how your function should work:

print(num_to_let(‘1-13-26’)) # – AMZprint(num_to_let(‘1-100-26’)) # – AZprint(num_to_let(‘1-!-?’)) # – Aprint(num_to_let(‘—26’)) # – Z

Part 2—–Write a function called let_to_num. It will do the opposite of what your previous function did. It’ll take a word and encode it into a series of numbers and dashes, with the numbers corresponding to the position of the letter in the alphabet (regardless of casing). If the character is  not a letter, then ignore it.

Again, feel free to write assertions to test your function. Here are someexamples of how this function should work:

print(let_to_num(‘AZ’)) # – 1-26print(let_to_num(”)) # – (empty string)print(let_to_num(‘A?Z’)) # – 1-26print(let_to_num(‘AZ?’)) # – 1-26print(let_to_num(‘AbzC’)) # – 1-3-26-2

Part 3—–

Use the functions that you wrote above in an interactive program. Write this program with an if statement so that it only runs if this file is being run on its own rather than being used as a module:

if __name__ == ‘__main__’:# your program goes here

The program will:

1. continually ask the user for a command, n, l or q (both uppercase  and lowercase commands should work): (n)um_to_let, (l)et_to_num or (q)uit?2. if the user enters n, N, l, or L, then ask the user for a string3. depending on whether or not the input was n or l, decode the input with num_to_let or encode the input with let_to_num … and print  out the result4. … then ask for a command again5. however, if the input was q, then stop the program6. finally, if the command was not n, l or q (in any casing), then just askfor a command again

Here’s an example of a single run of this program: