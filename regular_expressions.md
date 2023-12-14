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
  <summary><b>[]</b></summary>

  A set of characters

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
  <summary><b>\</b></summary>
  
  Signals a special sequence (can also be used to escape special characters)

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
  <summary><b>.</b></summary>
Any character (except newline character)	
  
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
  <summary><b>^</b></summary>

  Start With
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
