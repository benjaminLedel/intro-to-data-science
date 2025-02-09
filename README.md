# Introduction to Data Science

Source repository for the online book [Introduction to Data Science](https://sherbold.github.io/intro-to-data-science/). 

## Modifying the Contents

Modifying the contents of this book is relatively simple. 

- If you want to modify the contents of a chapter, simply edit the respective Jupyter Notebook in the contents directory.
- New chapters can be added with additional Jupyter Notebooks in the contents folder. The chapters must be added to the `_data/toc.yml` to appear in the online book and the `pdfconfig/index.rst` to appear in the PDF.
- Images that are used in chapters and not generated by the source code should be placed in the `contents/images` directory. 
- Additional exercises and solutions can be added as Jupyter Notebooks to the exercises directory. The reference to the notebook must also be added to the `_data/toc.yml` to appear int he online book. Moreover, the exercises should be linked in the `content/Exercises.ipynb`, solutions should be linked in the `content/Solutions.ipynb`. Exercises and solutions are currently not part of the PDF.

## Building the Book

The online book is created with [jupyter-book 0.6.4](https://legacy.jupyterbook.org/intro), the PDF version with [nbsphinx 0.7.0](https://nbsphinx.readthedocs.io/en/0.7.0/). To build the book, you need to clone the repository and setup a virtual environment in which the dependencies for building the book are installed. 

```sh
git clone https://github.com/sherbold/intro-to-data-science
cd intro-to-data-science
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

You can now build the Website and the PDF. To ensure that the latest PDF is part of the online book, you must build the pdf first. 

```sh
make pdf
make build
```

> :warning: You may need to install additional dependencies directly using the operating system, e.g., texlive or latexmk. A list of required dependencies will be added later. 

## Contributing

Contributions in form of corrections are always welcome, either directly as a pull request or though an issue that describes the problem. If you would like to see or provide additional contents (e.g., additional algorithms, chapters, or exercises) this should always be discussed in an issue first.

## License

All content in this book (ie, any files and content in the content/ folder) is licensed under the Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license.
