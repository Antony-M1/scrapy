# Spider
In `Scrapy` Spider is the main feature. in the spider only we wrote all the operation of `crawl` here you can understand some of the `inbuild` attributes & methods

```
import scrapy

class MySpider(scrapy.Spider):
    pass
```
This is the basic format of the spider. you can see.

### Attributes
* **name:`str`** contains the name of `Spider`
* **start_urls:`list`** This attribute contains the list of URLs. It will trigger one by one. after a URL is triggered it will send the `response` to the callback method `parse`

### Methods
* **parse(self, response)** in the `response` contains the response object from there you can do the needed logics

# Class
<details>
<summary><h3><a href="https://docs.scrapy.org/en/latest/topics/spiders.html#scrapy-spider">scrapy.Spider</a></h3></summary>
    
Base class for scrapy spiders. All spiders must inherit from this class.

**Attributes**
* `name: str`  identifies the Spider. It must be unique within a project, that is, you can’t set the same name for different Spiders.
* `custom_settings: Optional[dict] = None`
* `start_urls: list` If you used this attribute you no need to use the [start_request()](https://docs.scrapy.org/en/latest/intro/tutorial.html#a-shortcut-to-the-start-requests-method) method.

**Methods**
* `start_requests():` must return an iterable of Requests (you can return a list of requests or write a generator function) which the Spider will begin to crawl from. Subsequent requests will be generated successively from these initial requests.
* `parse():` a method that will be called to handle the response downloaded for each of the requests made. The response parameter is an instance of TextResponse that holds the page content and has further helpful methods to handle it.
</details>

<details>
    <summary><h3>scrapy.Request</h3></summary>

Represents an HTTP request, which is usually generated in a Spider and
    executed by the Downloader, thus generating a :class:`Response`.
    
</details>
