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
<summary><h3>scrapy.Spider</h3></summary>
    
Base class for scrapy spiders. All spiders must inherit from this class.

**Attributes**
* **name:** `str`
* **custom_settings:** `Optional[dict] = None`

</details>

<details>
    <summary><h3>scrapy.Request</h3></summary>

Represents an HTTP request, which is usually generated in a Spider and
    executed by the Downloader, thus generating a :class:`Response`.
    
</details>
