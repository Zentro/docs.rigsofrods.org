## Setup & Running
```
git clone https://github.com/RigsOfRods/ror-docs.git .
```

A recent version of Python and the Python package manager, pip, needs to be installed on your system.

Using `pip`, install MkDocs:
```
pip install mkdocs
```

Using `pip` again, install all the required packages:
```
pip install -r requirements.txt
```

Then, using `mkdocs` you can build a local static site with:
```
mkdocs build
```

Or, use a dev-server that compiles and hot-reloads for development:
```
mkdocs serve
```

## License