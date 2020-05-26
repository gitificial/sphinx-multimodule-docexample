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



