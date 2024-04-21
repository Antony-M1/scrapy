# [XPath](https://docs.scrapy.org/en/latest/intro/tutorial.html#xpath-a-brief-intro)

`XPath` expressions are very powerful, and are the foundation of Scrapy Selectors. In fact, CSS selectors are converted to `XPath under-the-hood`. You can see that if you read closely the text representation of the selector objects in the shell.

While perhaps not as popular as CSS selectors, XPath expressions offer more power because besides navigating the structure, it can also look at the content. Using XPath, you’re able to select things like: select the link that contains the text `Next Page`. This makes XPath very fitting to the task of scraping, and we encourage you to learn XPath even if you already know how to construct CSS selectors, it will make scraping much easier.

* [Xpath Playground](https://scrapinghub.github.io/xpath-playground/)

## Special Characters
* `/` : Select the `children` from the node set on the left side of this character.
* `//` : Specifies that the matching node set should be located `at any level` within the document.
* `.` : Specifies the count context should be used (refers to `present` node)
* `..` : Refers to a `parent` node.

## Reference Document:
* [Learn XPath through examples](http://zvon.org/comp/r/tut-XPath_1.html)
    * [List of Xpath](http://zvon.org/comp/r/tut-XPath_1.html#Pages~List_of_XPaths)
* [Selectors](https://docs.scrapy.org/en/latest/topics/selectors.html#topics-selectors)
* [Xpath Mozila 🔥](https://developer.mozilla.org/en-US/docs/Web/XPath)

Take this site for practice [quotes.toscrape.com](https://quotes.toscrape.com/)

## List Of XPath
<details>
   <summary><b>XPath as filesystem addressing</b></summary>

   The basic XPath syntax is similar to filesystem addressing. If the path starts with the slash `/` , then it represents an   `absolute path` to the required element.
```
/AAA
/AAA/CCC
/AAA/DDD/BBB
```
For More Example this path is start from the `HTML`. Try this in the `quotes.toscrape.com` site.
```
/html/body/div/div[2]/div/div[6]
```
</details>

<details>
   <summary><b>Start with <code>//</code></b></summary>

   If the path starts with `//` then all elements in the document which fulfill the following criteria are selected.
```
//BBB
//DDD/BBB
```
```
//body//div
```
</details>


<details>
   <summary><b>All elements: <code>*</code></b></summary>

   The star * selects all elements located by preceding path
```
/AAA/CCC/DDD/*
/*/*/*/BBB
//*
```
</details>



<details>
   <summary><b>Further conditions inside <code>[]</code></b></summary>

   Expression in square brackets can further specify an element. A number in the brackets gives the position of the element in the selected set. The function `last()` selects the last element in the selection.
```
/AAA/BBB[1]
/AAA/BBB[last()]
```
</details>


<details>
   <summary><b>Attributes</b></summary>

   Attributes are specified by `@` prefix.
```
//@id
//BBB[@id]
//BBB[@name]
//BBB[@*]
//BBB[not(@*)]
```
</details>


<details>
   <summary><b>Attribute values</b></summary>

   Values of attributes can be used as selection criteria. Function normalize-space removes leading and trailing spaces and replaces sequences of whitespace characters by a single space.

```
//BBB[@id='b1']
//BBB[@name='bbb']
//BBB[normalize-space(@name)='bbb']
```
</details>



<details>
   <summary><b>Nodes counting</b></summary>

   Function `count()` counts the number of selected elements
```
//*[count(BBB)=2]
//*[count(*)=2]
//*[count(*)=3]
```

</details>


<details>
   <summary><b>Playing with names of selected elements</b></summary>

Function `name()` returns `name` of the `element`, the `starts-with` function returns true if the first argument string starts with the second argument string, and the `contains` function returns true if the first argument string contains the second argument string.
```
//*[name()='BBB']
//*[starts-with(name(),'B')]
//*[contains(name(),'C')]
```
</details>


<details>
   <summary><b>Length of string</b></summary>

   The `string-length` function returns the number of characters in the string. You must use &lt; as a substitute for < and &gt; as a substitute for > .
```
//*[string-length(name()) = 3]
//*[string-length(name()) < 3]
//*[string-length(name()) > 3]
```
</details>


<details>
   <summary><b>Combining XPaths with <code>|</code></b></summary>

   Several paths can be combined with | separator.
   ```
//CCC | //BBB
/AAA/EEE | //BBB
/AAA/EEE | //DDD/CCC | /AAA | //BBB
```
</details>


For more documents please refere the [Referencce Document Section](#reference-document)





















