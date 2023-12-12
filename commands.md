# Summary
We are going to see the **scrapy** commands and use them.

Ideally, The `Scrapy` commands start with the prefix of **scrapy** & the Common Function which means **Help** command `--help` pass this argument and get help

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
  <summary><b>Template</b></summary>
</details>

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

