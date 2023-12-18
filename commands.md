# Summary
We are going to see the **scrapy** commands and use them.

Ideally, The `Scrapy` commands start with the prefix of **scrapy** & the Common Function which means **Help** command `--help` pass this argument and get help

* [Available tool commands](https://docs.scrapy.org/en/latest/topics/commands.html#available-tool-commands)

```
scrapy --help
```
Output
```
Scrapy 2.11.0 - no active project

Usage:
  scrapy <command> [options] [args]

Available commands:
  bench         Run quick benchmark test
  fetch         Fetch a URL using the Scrapy downloader
  genspider     Generate new spider using pre-defined templates
  runspider     Run a self-contained spider (without creating a project)
  settings      Get settings values
  shell         Interactive scraping console
  startproject  Create new project
  version       Print Scrapy version
  view          Open URL in browser, as seen by Scrapy

  [ more ]      More commands available when run from project directory

Use "scrapy <command> -h" to see more info about a command
```

### Global Options
```
  --logfile FILE        log file. if omitted stderr will be used
  -L LEVEL, --loglevel LEVEL
                        log level (default: DEBUG)
  --nolog               disable logging completely
  --profile FILE        write python cProfile stats to FILE
  --pidfile FILE        write process ID to FILE
  -s NAME=VALUE, --set NAME=VALUE
                        set/override setting (may be repeated)
  --pdb                 enable pdb on failure
```



<details>
  <summary><b>scrapy bench</b></summary>
  Run quick benchmark test
  
  ```
  scrapy bench --help
  ```
  output
  ```
  Usage
=====
  scrapy bench 

Run quick benchmark test

Options
=======
  -h, --help            show this help message and exit
  ```
</details>

<details>
  <summary><b>scrapy genspider</b></summary>
  
  Generate new spider using pre-defined templates

  ```
  scrapy genspider --help
  ```
  Output
  ```
  Usage
=====
  scrapy genspider [options] <name> <domain>

Generate new spider using pre-defined templates

Options
=======
  -h, --help            show this help message and exit
  -l, --list            List available templates
  -e, --edit            Edit spider after creating it
  -d TEMPLATE, --dump TEMPLATE
                        Dump template to standard output
  -t TEMPLATE, --template TEMPLATE
                        Uses a custom template.
  --force               If the spider already exists, overwrite it with the template
  ```
</details>


<details>
  <summary><b>scrapy runspider</b></summary>

  This command is used to run the `Spider` file running the spider we can store the data and other options also there

  ```
  scrapy runspider --help
  ```
output
```
Usage
=====
  scrapy runspider [options] <spider_file>

Run the spider defined in the given file

Options
=======
  -h, --help            show this help message and exit
  -a NAME=VALUE         set spider argument (may be repeated)
  -o FILE, --output FILE
                        append scraped items to the end of FILE (use - for stdout), to define format set
                        a colon at the end of the output URI (i.e. -o FILE:FORMAT)
  -O FILE, --overwrite-output FILE
                        dump scraped items into FILE, overwriting any existing file, to define format set
                        a colon at the end of the output URI (i.e. -O FILE:FORMAT)
  -t FORMAT, --output-format FORMAT
                        format to use for dumping items

```
</details>

<details>
  <summary><b>scrapy settings</b></summary>
  Get settings values

  ```
  scrapy settings --help
  ```
output
```
Usage
=====
  scrapy settings [options]

Get settings values

Options
=======
  -h, --help            show this help message and exit
  --get SETTING         print raw setting value
  --getbool SETTING     print setting value, interpreted as a boolean
  --getint SETTING      print setting value, interpreted as an integer
  --getfloat SETTING    print setting value, interpreted as a float
  --getlist SETTING     print setting value, interpreted as a list
```
</details>


<details>
  <summary><b>scrapy shell</b></summary>

```
scrapy shell --help
```
Output
```
Usage
=====
  scrapy shell [url|file]

Interactive console for scraping the given url or file. Use ./file.html syntax or full path for local
file.

Options
=======
  -h, --help            show this help message and exit
  -c CODE               evaluate the code in the shell, print the result and exit
  --spider SPIDER       use this spider
  --no-redirect         do not handle HTTP 3xx status codes and print response as-is
```
</details>


<details>
  <summary><b>scrapy startproject</b></summary>

  Create new project

```
scrapy startproject --help
```
Output
```
Usage
=====
  scrapy startproject <project_name> [project_dir]

Create new project

Options
=======
  -h, --help            show this help message and exit
```
</details>


<details>
  <summary><b>scrapy version</b></summary>

  ```
scrapy version --hep
```
Output

```
Usage
=====
  scrapy version [-v]

Print Scrapy version

Options
=======
  -h, --help            show this help message and exit
  --verbose, -v         also display twisted/python/platform info (useful for bug reports)
```
</details>


<details>
  <summary><b>scrapy view</b></summary>
Fetch a URL using the Scrapy downloader and show its contents in a browser

```
scrapy view --help
```
Output
```
Usage
=====
  scrapy view [options] <url>

Fetch a URL using the Scrapy downloader and show its contents in a browser

Options
=======
  -h, --help            show this help message and exit
  --spider SPIDER       use this spider
  --no-redirect         do not handle HTTP 3xx status codes and print response as-is
```
</details>


<details>
  <summary><b>scrapy crawl</b></summary>

  ```
Usage
=====
  scrapy crawl [options] <spider>

Run a spider

Options
=======
  -h, --help            show this help message and exit
  -a NAME=VALUE         set spider argument (may be repeated)
  -o FILE, --output FILE
                        append scraped items to the end of FILE (use - for stdout), to define format set a colon
                        at the end of the output URI (i.e. -o FILE:FORMAT)
  -O FILE, --overwrite-output FILE
                        dump scraped items into FILE, overwriting any existing file, to define format set a
                        colon at the end of the output URI (i.e. -O FILE:FORMAT)
  -t FORMAT, --output-format FORMAT
                        format to use for dumping items
```

</details>


<details>
  <summary><b>scrapy list</b></summary>

  List all the spiders present in the project
</details>


<details>
  <summary><b>scrapy check</b></summary>

  Check spider contracts

**Options**
```
  -h, --help            show this help message and exit
  -l, --list            only list contracts, without checking them
  -v, --verbose         print contract tests for all spiders
```
</details>


<details>
   <summary><b>scrapy edit</b></summary>

  Edit a spider using the editor defined in the `EDITOR` environment variable or else the `EDITOR` setting
</details>


<details>
   <summary><b>scrapy parse</b></summary>

  Parse URL (using its spider) and print the results

**Options**
```

  -h, --help            show this help message and exit
  -a NAME=VALUE         set spider argument (may be repeated)
  -o FILE, --output FILE
                        append scraped items to the end of FILE (use - for stdout), to define format set a colon at
                        the end of the output URI (i.e. -o FILE:FORMAT)
  -O FILE, --overwrite-output FILE
                        dump scraped items into FILE, overwriting any existing file, to define format set a colon at
                        the end of the output URI (i.e. -O FILE:FORMAT)
  -t FORMAT, --output-format FORMAT
                        format to use for dumping items
  --spider SPIDER       use this spider without looking for one
  --pipelines           process items through pipelines
  --nolinks             don't show links to follow (extracted requests)
  --noitems             don't show scraped items
  --nocolour            avoid using pygments to colorize the output
  -r, --rules           use CrawlSpider rules to discover the callback
  -c CALLBACK, --callback CALLBACK
                        use this callback for parsing, instead looking for a callback
  -m META, --meta META  inject extra meta into the Request, it must be a valid raw json string
  --cbkwargs CBKWARGS   inject extra callback kwargs into the Request, it must be a valid raw json string
  -d DEPTH, --depth DEPTH
                        maximum depth for parsing requests [default: 1]
  -v, --verbose         print each depth level one by one
```
</details>


<details>
   <summary><b>scrapy bench</b></summary>

Run quick benchmark test
</details>









