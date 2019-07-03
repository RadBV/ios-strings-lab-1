# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)

```swift
var bebus = 1...10

for i in bebus{
    print("\(i)", terminator: " ")
}
```

***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

```swift
var bebus = 5...51

for i in bebus where i % 2 == 0{
        print("\(i)", terminator: " ")
}
```

***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

```swift
var bebus = 1...60

for i in bebus where i % 10 == 4{
    print("\(i)", terminator: " ")
}
```
***
## Question 4

Print each character in the string `"Hello world!"`

```swift
var chungus = "Hello World!"

for i in chungus {
    print(i)
}
```

***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`

```swift
let myStringSeven = "Hello world!"

print(myStringSeven.last!)

```
***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

`print("\u{0048}\u{0045}\u{004c}\u{004c}\u{004f} \u{0057}\u{004f}\u{0052}\u{004c}\u{0044}\u{0021}")`

***
## Question 10

**Using only Unicode**, print out your name.

`print("\u{0052}\u{0061}\u{0064}\u{0068}\u{0061}\u{0072}\u{0061}\u{006e}\u{0069}")`

***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

`print("\u{004f}\u{004c}\u{00c1} \u{004d}\u{0055}\u{004e}\u{0044}\u{004f}\u{0021}")`
***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```

```swift
var flower  = "\u{2698} "
var verticalSymbol = "\u{007c} "
var horizontalSymbol = "\u{005f} "
var short = "\(verticalSymbol)\(flower)\(verticalSymbol)\(flower)\(verticalSymbol)\(flower)\(verticalSymbol)\(flower)\(verticalSymbol)\(flower)\(verticalSymbol)"

for _ in 0...11 {
    print(horizontalSymbol, terminator: "")
}
print()
print()
for _ in 1...7 {
    print(short)
}

for _ in 0...11 {
    print(horizontalSymbol, terminator: "")
}
```
***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜
```
```swift
var whiteChess = "\u{2656} \u{2658} \u{2657} \u{2655} \u{2654} \u{2657} \u{2658} \u{2656}"
var whitePawn = "\u{2659} "
var blackChess = "\u{265c} \u{265e} \u{265d} \u{265b} \u{265a} \u{265d} \u{265e} \u{265c}"
var blackPawn = "\u{265f} "


print(whiteChess)
let whitePawn8 = String(repeating: whitePawn, count: 8)
print(whitePawn8)
print()
print()
let blackPawn8 = String(repeating: blackPawn, count: 8)
print(blackPawn8)
print(blackChess)
```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// Your code here
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

```
var aString = "Replace the letter e with *"
var bla = ""

for scalar in aString.unicodeScalars {
    let char = "\(scalar)"
    if char == "e" {
        bla = bla + "*"
        } else {
        bla = bla + char
    }
}
print(bla)
```
***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

for _ in aString{
    reverse = String(aString.reversed())
}
print(reverse)
```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// Your code here
```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

let problemArray = problem.split(separator: " ")

for word in problemArray{
print(word)
}
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines
```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

let problemArray = problem.split(separator: " ")
var container = 0

for _ in problemArray{
    if problemArray.count > container {
        container = problemArray.count - 1
}

}
print(problemArray[container])
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

```
var hueHue = "bebus boyo bingo bongo "
let hueHueArray = hueHue.split(separator: " ")
var lastWord = hueHueArray.last

if hueHueArray.count == 0{
    print("No last word")
    } else {
        print(lastWord!.count)
}
```
***
