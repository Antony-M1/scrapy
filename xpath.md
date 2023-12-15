# [XPath](https://docs.scrapy.org/en/latest/intro/tutorial.html#xpath-a-brief-intro)

`XPath` expressions are very powerful, and are the foundation of Scrapy Selectors. In fact, CSS selectors are converted to `XPath under-the-hood`. You can see that if you read closely the text representation of the selector objects in the shell.

While perhaps not as popular as CSS selectors, XPath expressions offer more power because besides navigating the structure, it can also look at the content. Using XPath, you’re able to select things like: select the link that contains the text `Next Page`. This makes XPath very fitting to the task of scraping, and we encourage you to learn XPath even if you already know how to construct CSS selectors, it will make scraping much easier.

## Reference Document:
* [Learn XPath through examples](http://zvon.org/comp/r/tut-XPath_1.html)
    * [List of Xpath](http://zvon.org/comp/r/tut-XPath_1.html#Pages~List_of_XPaths)
* [Selectors](https://docs.scrapy.org/en/latest/topics/selectors.html#topics-selectors)

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
   <summary><b>XPath as filesystem addressing</b></summary>
</details>
