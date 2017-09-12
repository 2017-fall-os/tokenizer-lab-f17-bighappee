/*******************************************************
Christopher K. Tarango
9/11/17
CS4375
Tokenizer Lab

README.md
*******************************************************/


Read Me
-------------------------------------------------
This program mimics a shell prompt, when input is given it will take the input, count the number of tokens, create
a null terminated array/vector, and copy the tokens into said vector.

Memory allocation takes place in mytoc function of mytoc.c
Memory freed in main function of test.c

Maximum number of bytes read per program execution is 8192

Spaces and line feed are only characters treated as delimiters

Compilation:
 make

Usage:
 to run file : ./test 

SPECIAL CASE:
To end program type "exit" at the mock prompt, no spaces leading or trailing or else it is treated as a token


TEST CASES USED:

$ Hello my dog's name is Darwin.
Number of Tokens Read : 6
Address of Vector is 0x7fff23774338
Token at index: 0	Hello0
Token at index: 1	my0
Token at index: 2	dog's0
Token at index: 3	name0
Token at index: 4	is0
Token at index: 5	Darwin.0

$      Hello   World!    
Number of Tokens Read : 2
Address of Vector is 0x7ffd094b0bf8
Token at index: 0	Hello0
Token at index: 1	World!0

(empty input)
$ 
Number of Tokens Read : 0
Address of Vector is 0x7ffd094b0bf8

$  HelloWorld
Number of Tokens Read : 1
Address of Vector is 0x7ffd094b0bf8
Token at index: 0	HelloWorld0

(spaces included)
$   
Number of Tokens Read : 0
Address of Vector is 0x7ffd094b0bf8

$   exit
Number of Tokens Read : 1
Address of Vector is 0x7ffd06678848
Token at index: 0	exit0

$ "How about with quotes"
Number of Tokens Read : 4
Address of Vector is 0x7ffd06678848
Token at index: 0	"How0
Token at index: 1	about0
Token at index: 2	with0
Token at index: 3	quotes"0

$ exit
(program exited)