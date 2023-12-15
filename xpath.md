# [XPath](https://docs.scrapy.org/en/latest/intro/tutorial.html#xpath-a-brief-intro)

`XPath` expressions are very powerful, and are the foundation of Scrapy Selectors. In fact, CSS selectors are converted to `XPath under-the-hood`. You can see that if you read closely the text representation of the selector objects in the shell.

While perhaps not as popular as CSS selectors, XPath expressions offer more power because besides navigating the structure, it can also look at the content. Using XPath, you’re able to select things like: select the link that contains the text `Next Page`. This makes XPath very fitting to the task of scraping, and we encourage you to learn XPath even if you already know how to construct CSS selectors, it will make scraping much easier.

