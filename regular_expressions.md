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
