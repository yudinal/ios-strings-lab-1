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

```
Answer:

var numString = ""
for num in 1...10 {
    numString += String(num)
}
print(numString)
```
***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.
```
Answer:
var numString = ""
for num in 5...51 {
    if num % 2 == 0 {
        numString += String(num)
    }
}
print(numString)
```
***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.

```
Answer:
var numString = ""
for num in 1...60 {
    if num % 10 == 4 {
        numString += String(num)
    }
}
print(numString)
```
***
## Question 4

Print each character in the string `"Hello world!"`
```
Answer:
var message = "Hello world!"
for char in message {
print(char)
}
```

***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`
```
Answer:
let myStringSeven = "Hello world!"

let endIndex = myStringSeven.endIndex

let lastCharacterIndex = myString.index(before: endIndex)

//let lastCharacter = myStringSeven[lastCharacterIndex]
print("last charcter in \(myStringSeven) is", myStringSeven[lastCharacterIndex])
```
***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.

***
```
switch message {
case message where message.count % 2 == 0:
    for char in message {
        print(char, terminator: " ")
    }
default:
    for (index, char) in message.enumerated() where index % 2 == 1 {
        print(char, terminator: " ")
    }
}

```
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

***
```
let character: Character = "a"

let str = String(character)

print(type(of: character))
print(type(of: str))
```
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

***
```
let unicodeFire = "\u{1F525}"
let fireCharacter = "🔥"
if unicodeFire == fireCharacter {
    print("they are equal")
}

let unicodeSunflower = "\u{1F33B}"
let sunflowerCharacter = "🌻"
if unicodeSunflower == sunflowerCharacter {
    print("they are equal")
}

let unicodeFlower = "\u{1F940}"
let flowerCharacter = "🥀"
if unicodeFlower == flowerCharacter {
    print("they are equal")
}

let unicodeCloud = "\u{1F327}"
let cloudCharacter = "🌧"
if unicodeCloud == cloudCharacter {
    print("they are equal")
}

let unicodeTornado = "\u{1F32A}"
let tornadoCharacter = "🌪"
if unicodeTornado == tornadoCharacter {
    print("they are equal")
}
```
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

***
```
let greetingString = "HELLO WORLD!"
for scalar in greetingString.unicodeScalars {
    print("\(scalar) ")
}
```
## Question 10

**Using only Unicode**, print out your name.

***
```
let nameString = "Lilia"
for scalar in nameString.unicodeScalars {
    print("\(scalar) ")
}
```
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

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

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"*"`.

```swift
var aString = "Replace the letter e with *"
// Your code here
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""

// Your code here
```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`


## 16. Mad-Libs! Add a value to the declared variables below in playgrounds. Insert the variables (already in correct order) inside the stringmadLib and print. 

```swift


var geographicLocation: String
var adjective1: String
var pluralNoun1: String
var adjective2: String
var pluralNoun2: String
var number1: Int
var number2: Int
var articleOfClothing: String

var madLib = "Here is tomorrow's weather report for \()
and vicinity. Early tomorrow, a \()-front will
collide with a mass of hot \() moving from the
north. This means we can expect \() winds and
occasional \() by late afternoon. Wind velocity will
be \() miles an hour, and the high temperature should
be around \() degrees. So, if you're going out, you had
better plan on wearing your \()".
```

***

# Bonus :)

***
## Question 1

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
## Question 2

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
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
## Question 3

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

// Your code here
```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 4

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"
```

***
## Question 5

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

***

## Question 8

Given a string `testString` create a new variable called `condensedString` that has any consecutive spaces in `testString` replaced with a single space.

```swift
let testString = "  How   about      thesespaces  ?  "
//condensedString = " How about thesespaces ? "
```

***
## Question 9

Given a string with multiple words. Reverse the string word by word.

Example:

Sample Input: `"Swift is the best language"`

Sample Output: `"language best the is Swift"`

***
## Question 10

Given a string with multiple words. Write code that prints how many of them are palindromes.

Example:

Sample Input: `"danaerys dad cat civic bottle"`

Sample Output: `2`

***
## Question 11

You are given a string representing an **attendance record** for a student. The record only contains the following three characters:

`'A' : Absent.`

`'L' : Late.`

`'P' : Present.`

If a student has more than one 'A' or more than 2 continuous 'L's that student should not be rewarded. Print true if student is to be rewarded and False if they shouldn't.

Example:

Sample Input: `"PPALLP"`

Sample Output: `true`

***
## Question 12

Given a tuple with two strings. The first string is a **ransom note**, the second string being the characters from a magazine. Determine whether or not you can construct the ransom note using the characters from the magazine.

Each letter from the magazine can only be used once. You can assume all letters are lowercased.

Examples:

Sample Input1: `("a", "b")`

Sample Output1: `False`

Sample Input2: `("aa", "aab")`

Sample Output2: `True`

