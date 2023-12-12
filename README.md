# [Scrapy](https://docs.scrapy.org/en/latest/#scrapy-version-documentation)
![image](https://github.com/Antony-M1/scrapy/assets/96291963/05164721-af67-4e3f-92a4-605b725dd117)

Scrapy is a fast high-level **web crawling** and **web scraping** framework, used to crawl websites and extract structured data from their pages. It can be used for a wide range of purposes, from data mining to monitoring and automated testing. For [Official Document](https://docs.scrapy.org/en/latest/#scrapy-version-documentation)

# Summary
The main motto of this document is to get knowledge from the different sources and documentation. In this repo you can find lots of documents regarding the scrappy and efficient way to scrap a page handle the data and store the data.

# [Architecture](https://docs.scrapy.org/en/latest/topics/architecture.html)
![image](https://github.com/Antony-M1/scrapy/assets/96291963/888ab328-7c5f-4790-89ad-1296c7c000f2)

# [Default structure of Scrapy projects](https://docs.scrapy.org/en/latest/topics/commands.html#default-structure-of-scrapy-projects)

```
scrapy.cfg
myproject/
    __init__.py
    items.py
    middlewares.py
    pipelines.py
    settings.py
    spiders/
        __init__.py
        spider1.py
        spider2.py
        ...
```

# VS-Code Debugger
Past this in `.vscode/launch.json` file
```
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Scrapy",
      "type": "python",
      "request": "launch",
      "module": "scrapy",
      "args": ["runspider", "${file}"],
      "console": "integratedTerminal",
      "justMyCode": false
    }
  ]
}


```


# Table Of Content
* [Algoritham](https://github.com/Antony-M1/scrapy/blob/main/algorithm.md)
* [Library](https://github.com/Antony-M1/scrapy/blob/main/library.md)

