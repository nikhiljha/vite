<h1 align="center">
	<img width="200" src="https://xix.ph0x.me/vitelogo.png" alt="Vite">
</h1>

> A simple and mnml static site generator that Just Works™

[![forthebadge](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/powered-by-electricity.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/uses-git.svg)](https://forthebadge.com)

<h1 align="center">
    <img width="350" src="https://xix.ph0x.me/vite_epi.png" alt="Vite demo">
</h1>
Installation
------------

```console
$ pip install vite
```
Usage
-----

```console
$ vite new <project-path>
```
Write your Markdown files in the `pages` directory and execute:
```console
$ vite build   # in project directory
```
Rendered HTML will be in the `build` directory.

Finally, run:
```console
$ vite serve  # also in the project directory
```
to serve the contents of the `build` directory.

Configuration
-------------

Not very sophisticated, but basic configuration can be acheived using
  `config.py` found in the project directory.
Example config:

```python
# config.py 
title = ''
author = ''
header = ''
footer = '' 
template = 'index.html'  # default is templates/index.html
```

Templating
----------

Vite uses Jinja2 templating, so template files must be placed in a separate `templates/` directory.  
**NOTE**: Stylesheets, images and JS can be accessed from the `static` folder.  
**ANOTHER NOTE**: `index.html`, i.e. your website's homepage, should be `_index.md` in the `pages/` directory.

A basic example would be:
```html
<link rel="stylesheet" href="../static/sakura-earthy.css">

<title> {{ title }} </title>

<body>
{{ body }}
</body>

<footer>
{{ footer }}
</footer>
```

Directory tree
--------------

    example
    ├── build
    ├── config.py
    ├── pages
    │   └── test.md
    ├── static
    └── templates
        └── index.html

TODO
----

- [x] Templating
- [x] CSS support
- [x] Implement a simple HTTP server (*later*)
- [x] Add example site
- [x] Basic config (`config.py`)
- [ ] Parsing frontmatter (JSON, YAML, TOML)
- [x] Better support for home page (main `index.html` page)


## Credits
_Logo credits_: <a href="http://www.freepik.com" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a> is licensed by <a href="http://creativecommons.org/licenses/by/3.0/" title="Creative Commons BY 3.0" target="_blank">CC 3.0 BY</a>  
_Hue_: [UltimateHackers/hue](https://github.com/UltimateHackers/hue)

