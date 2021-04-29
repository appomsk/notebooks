## Installation

(* Manually - jupyter serverextension enable jupytext *)

In most cases, Jupytext's contents manager is activated automatically by
Jupytext's server extension. When you restart either jupyter lab or jupyter
notebook, you should see a line that looks like:

```
  [I 10:28:31.646 LabApp] [Jupytext Server Extension] ...
```

If you don't have the notebook icon on text documents after a fresh restart of
your Jupyter server, you can either enable our server extension explicitly
(with `jupyter serverextension enable jupytext`), or install the contents
manager manually. Append

`c.NotebookApp.contents_manager_class = "jupytext.TextFileContentsManager"` to
your `.jupyter/jupyter_notebook_config.py` file (generate a Jupyter config, if
you don't have one yet, with `jupyter notebook --generate-config`). Our contents
manager accepts a few options: default formats, default metadata filter, etc.
Then, restart Jupyter Notebook or JupyterLab, either from the JupyterHub
interface or from the command line with

```
jupyter notebook # or lab
```

## Paired notebooks

The most convenient way to use Jupytext is probably through paired notebooks.

To pair a given .ipynb or text notebook to an additional notebook format, use
either

* the "pair notebook with..." commands in Jupyter Lab

* the "pair notebook with..." menu entries in Jupyter Notebook jupytext at the
command line or a local or global jupytext.toml configuration file. When you

* save a paired notebook in Jupyter, both the .ipynb file and the text version
are updated on disk.

When a paired notebook is opened or reloaded in Jupyter, the input cells are
loaded from the text file, and combined with the output cells from the .ipynb
file.

You can edit the text representation of the notebook in your favorite editor,
and get the changes back in Jupyter by simply reloading the notebook (Ctrl+R
in Jupyter Notebook, "reload notebook" in Jupyter Lab). And the changes are
propagated to the .ipynb file when you save the notebook.

Alternatively, you can synchronise the two representations by running jupytext
--sync notebook.ipynb at the command line.

## Which text format? 

Jupytext implements many text formats for Jupyter Notebooks. If your notebook
is mostly made of code, you will probably prefer to save it as a script:

* Use the percent format, a format with explicit cell delimiters (# %%),
supported by many IDE (Spyder, Hydrogen, VS Code, PyCharm and PTVS) Or use the
light format, if you prefer to see fewer cell markers. If your notebook
contains more text than code, if you are writing a documentation or a book,
you probably want to save your notebook as a Markdown document

* Use the Jupytext Markdown format if you wish to render your notebook as a .md
file (without its outputs) on GitHub

* Use the MyST Markdown format, a markdown flavor that “implements the best
parts of reStructuredText”, if you wish to render your notebooks using Sphinx
or Jupyter Book.

* Use the R Markdown format if you want to open your Jupyter Notebooks in
RStudio.


