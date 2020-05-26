## sphinx-multimodule-docexample
Simple Sphinx example how to document multiple modules.

### Howto

Install Sphinx:

```bash
pip3 install sphinx
```

Go to your Python project's root directory and run following command. This creates a minimal working Sphinx structure: 

```bash
sphinx-quickstart
```

This example contains two dummy modules (module1 and module2). For each module we must create reStructuredText files (.rst ending).
Therefore go to each module folder and run:

```bash
sphinx-apidoc -o ./ ./
```

Move the newly created module1.rst and module2.rst files in the ./source directory.

