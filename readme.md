# rbdt - Robots.txt Parser

_rbdt is a work in progress, currently being extracted out of another (private) project for the purpose of open sourcing and better software engineering._

rbdt is a python library written in rust that parses robots.txt files.

rbdt features: 
* MIT license, have fun. 
* Written in Rust, so it is fast. 
* Callable from Python, so it is useful. 
* Has been and continues to be run against millions of unique robots.txt files.
* Forgiving, corrects some typical mistakes in files written by hand, like recognizing `dissallows` probably meant to be `disallow`. 
* Intentionally provides direct access to the parsed robots.txt representation (unlike [Reppy](https://github.com/seomoz/reppy) or [Google's parser](https://github.com/google/robotstxt)).
* Ability to compare which user agent has more privilege given to it by the website owner, both heuristically and logically. 

rbdt anti-features:
* rbdt isn't meant to be used as part of a web crawler, but as part of a large scale analysis of robots.txt files. If ends up being useful for web crawlers eventually, that's great and only incidental. 


# Development 

```
maturin develop
python py_tests/tests.py
```

# Contributions

File a ticket or send a PR if you'd like. 

# To Do 
* Real Open Sourcing Hours
** Get it up on pypi 
** Versions 
** Changelog 
** Write documentation and put them somewhere 
* Crawl-delay parsing and restructuring of the data representation. 
* Be able to detect whether a crawler can access a specific page.
* More tests of all the various edge cases. 
* Benchmarks, (maybe someday never). 
* Publish it as a Rust library as well (maybe).
* Get Rust tests working (maybe).
