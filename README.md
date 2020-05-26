## sphinx-multimodule-docexample
Simple Sphinx example how to document multiple modules.

### Howto

Note: This projects code folder already contains the files which are created by the following procedures. If you want to go through the whole creation process yourself, start with a project directory only containing the folders module1 and module2.

Install Sphinx:

```bash
pip3 install sphinx
```

Go to the project's root directory and run following command. This creates a minimal working Sphinx structure: 

```bash
sphinx-quickstart
```

This example contains two dummy modules (module1 and module2). For each module we must create reStructuredText files (.rst ending). Therefore go to each module folder and run:

```bash
sphinx-apidoc -o ./ ./
```

Move the newly created module1.rst and module2.rst files to the ./source directory. Therefore execute following commands in the project's root directory:

```bash
mv ./module1/module1.rst ./source
mv ./module2/module2.rst ./source
```

To include the modules in the build process add the rst-filenames to the master document index.rst:

<pre><code>
...

.. toctree::
   :maxdepth: 2
   :caption: Contents:

    <b>module1</b>
   __module2__
   
...
</pre></code>

Make following changes in the ./source/conf.py file:

```bash
import os
import sys
# sys.path.insert(0, os.path.abspath('.'))
print(os.path.abspath('../'))
sys.path.insert(0, os.path.abspath('../'))

...

extensions = ['sphinx.ext.todo', 'sphinx.ext.viewcode', 'sphinx.ext.autodoc']

...
```

To build a html documentation, run following command in the project's root directory:
```bash
make html
```

To see the result, open ./build/html/index.html in your browser.
