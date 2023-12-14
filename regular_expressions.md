# [Regex](https://www.w3schools.com/python/python_regex.asp)
The regular Expresion is one of the best `library` to handle the texts. In `Scrapy` framework we will use `Regex`. so its better have good knowledge in `Scrapy` is really good.

Python has a built-in package called `re`, which can be used to work with Regular Expressions.

Import `re` module

> import re 

## RegEx Functions
<details>
  <summary><b>findall()</b></summary>

  Returns a list containing `all matches`

  `re.findall(str, str) -> list`

```
import re

txt = "The rain in Spain"
x = re.findall("ai", txt)
print(x)
```
output
```
['ai', 'ai']
```
</details>
    
<details>
  <summary><b>search()</b></summary>

  Returns a `Match object` if there is a match anywhere in the string

  If there is more than one match, only the `first occurrence` of the match will be returned.

  If no matches are found, the value `None` is returned.

  ```
import re

txt = "The rain in Spain"
x = re.search("\s", txt)

print("Match Object -->",x) 
```
output
```
Match Object --> <re.Match object; span=(3, 4), match=' '>
```
</details>


<details>
  <summary><b>split()</b></summary>

  Returns a `list` where the string has been split at each match

  You can control the number of occurrences by specifying the `maxsplit` as `third` positional parameter

  ```
import re

txt = "The rain in Spain"
x = re.split("\s", txt)
print(x
```
Output
```
['The', 'rain', 'in', 'Spain']
```
</details>




<details>
  <summary><b>sub()</b></summary>
  
  The `sub()` function replaces the matches with the text of your choice:

  ```
import re

#Replace all white-space characters with the digit "9":

txt = "The rain in Spain"
x = re.sub("\s", "9", txt)
print(x)
```
Output
```
The9rain9in9Spain
```
</details>

## Metacharacters
Metacharacters are characters with a special meaning:

<details>
  <summary><b><code>[]</code></b> A set of characters</summary>

  Example: `[a-m]`
  ```
import re

txt = "The rain in Spain"

#Find all lower case characters alphabetically between "a" and "m":

x = re.findall("[a-m]", txt)
print(x)
```
Output
```
['h', 'e', 'a', 'i', 'i', 'a', 'i']
```
</details>


<details>
  <summary><b><code>\</code></b>   Signals a special sequence (can also be used to escape special characters)</summary>
  
  ```
import re

txt = "That will be 59 dollars"

#Find all digit characters:

x = re.findall("\d", txt)
print(x)
```
Output
```
['5', '9']
```
</details>


<details>
  <summary><b><code>.</code></b> Any character (except newline character)	</summary>
  
  ```
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed by two (any) characters, and an "o":

x = re.findall("he..o", txt)
print(x)
```
Output
```
['hello']
```
  
</details>


<details>
  <summary><b><code>^</code></b>   Start With</summary>

```
import re
txt = "hello world"
x = re.findall("^hello", txt)
print(x)
```
Output
```
["hello"]
```
</details>


<details>
  <summary><b><code>$</code></b>   Ends with</summary>

```
import re

txt = "hello world"
x = re.findall("world$", txt )
print(x)
```
Output
```
["world"]
```
</details>

<details>
  <summary><b><code>*</code></b>   Zero or more occurrences</summary>


```
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed by 0 or more  (any) characters, and an "o":

x = re.findall("he.*o", txt)

print(x)

```
Output
```
['hello']
```
</details>


<details>
  <summary><b><code>+</code></b> One or more occurrences</summary>

```
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed by 1 or more  (any) characters, and an "o":

x = re.findall("he.+o", txt)

print(x)
```
Output
```
['hello']
```
</details>




<details>
  <summary><b><code>?</code></b> Zero or one occurrences</summary>

```
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed by 0 or 1  (any) character, and an "o":

x = re.findall("he.?o", txt)

print(x)

#This time we got no match, because there were not zero, not one, but two characters between "he" and the "o"
```
Output
```
[]
```
  
</details>


<details>
  <summary><b><code>{}</code></b> Exactly the specified number of occurrences	</summary>

  ```
import re

txt = "hello planet"

#Search for a sequence that starts with "he", followed excactly 2 (any) characters, and an "o":

x = re.findall("he.{2}o", txt)

print(x)
```
Output
```
['hello']
```
</details>

<details>
  <summary><b><code>|</code></b> Either or</summary>

  ```
import re

txt = "The rain in Spain falls mainly in the plain!"

#Check if the string contains either "falls" or "stays":

x = re.findall("falls|stays", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```
Output
```
['falls']
Yes, there is at least one match!
```
</details>


## Special Sequences
A special sequence is a `\` followed by one of the characters in the list below, and has a special meaning:

<details>
  <summary><b><code>\A</code></b> Returns a match if the specified characters are at the beginning of the string	</summary>

  This is same like `^` Starts with

  ```
import re

txt = "The rain in Spain"

#Check if the string starts with "The":

x = re.findall("\AThe", txt)

print(x)

if x:
  print("Yes, there is a match!")
else:
  print("No match")

```
Output
```
['The']
Yes, there is a match!
```
</details>



<details>
  <summary><b><code>\b</code></b> Returns a match where the specified characters are at the beginning or at the end of a word
(the "r" in the beginning is making sure that the string is being treated as a "raw string")</summary>

Example 1
```
import re

txt = "The rain in Spain"

#Check if "ain" is present at the beginning of a WORD:

x = re.findall(r"\bain", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```
Output
```
[]
No match
```

Example 2
```
import re

txt = "The rain in Spain"

#Check if "ain" is present at the end of a WORD:

x = re.findall(r"ain\b", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")

```
Output
```
['ain', 'ain']
Yes, there is at least one match!
```
</details>


<details>
  <summary><b><code>\B</code></b> 	Returns a match where the specified characters are present, but NOT at the beginning (or at the end) of a word
(the "r" in the beginning is making sure that the string is being treated as a "raw string")	</summary>

  Example 1
  ```
import re

txt = "The rain in Spain"

#Check if "ain" is present, but NOT at the beginning of a word:

x = re.findall(r"\Bain", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")

```
Output
```
['ain', 'ain']
Yes, there is at least one match!
```

Example 2
```
import re

txt = "The rain in Spain"

#Check if "ain" is present, but NOT at the end of a word:

x = re.findall(r"ain\B", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```
Output
```
[]
No match
```
</details>

<details>
  <summary><b><code>\d</code></b> Returns a match where the string contains digits (numbers from 0-9)		</summary>

```
import re

txt = "The rain in Spain"

#Check if the string contains any digits (numbers from 0-9):

x = re.findall("\d", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```
Output
```
[]
No match
```
</>



<details>
  <summary><b><code>\D</code></b> 	Returns a match where the string DOES NOT contain digits</summary>

```
import re

txt = "Hello World"

#Return a match at every no-digit character:

x = re.findall("\D", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```
Output
```
['H', 'e', 'l', 'l', 'o', ' ', 'W', 'o', 'r', 'l', 'd']
Yes, there is at least one match!
```
</details>


<details>
  <summary><b><code>\s</code></b> 	Returns a match where the string contains a white space character</summary>

  ```
import re

txt = "The rain in Spain"

#Return a match at every white-space character:

x = re.findall("\s", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```
Output
```
[' ', ' ', ' ']
Yes, there is at least one match!
```
</details>



<details>
  <summary><b><code>\S</code></b> 		Returns a match where the string DOES NOT contain a white space character</summary>

  ```
import re

txt = "Hello World"

#Return a match at every NON white-space character:

x = re.findall("\S", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")

```
Output
```
['H', 'e', 'l', 'l', 'o', 'W', 'o', 'r', 'l', 'd']
Yes, there is at least one match!
```
</details>


<details>
  <summary><b><code>\w</code></b> 	Returns a match where the string contains any word characters (characters from a to Z, digits from 0-9, and the underscore _ character)</summary>

```
import re

txt = "The rain in Spain"

#Return a match at every word character (characters from a to Z, digits from 0-9, and the underscore _ character):

x = re.findall("\w", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")
```

Output
```

['T', 'h', 'e', 'r', 'a', 'i', 'n', 'i', 'n', 'S', 'p', 'a', 'i', 'n']
Yes, there is at least one match!
```
</details>


<details>
  <summary><b><code>\W</code></b> 	Returns a match where the string DOES NOT contain any word characters</summary>

  ```
import re

txt = "The rain in Spain"

#Return a match at every NON word character (characters NOT between a and Z. Like "!", "?" white-space etc.):

x = re.findall("\W", txt)

print(x)

if x:
  print("Yes, there is at least one match!")
else:
  print("No match")

```
Output
```
[' ', ' ', ' ']
Yes, there is at least one match!
```
</details>


<details>
  <summary><b><code>\Z</code></b> Returns a match if the specified characters are at the end of the string</summary>

  ```
import re

txt = "The rain in Spain"

#Check if the string ends with "Spain":

x = re.findall("Spain\Z", txt)

print(x)

if x:
  print("Yes, there is a match!")
else:
  print("No match")
```
Output
```
['Spain']
Yes, there is a match!
```
</details>
