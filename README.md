![alt text](https://github.com/prozorro-sale/tor.ea/blob/master/LICENSE.txt "License Apache Version 2.0")
[![Documentation Status](https://readthedocs.org/projects/torea/badge/?version=latest)](https://propertylease.readthedocs.io/uk_UA/latest/)

# Introduction

`tor.ea` repository contains documentation for propertyLease procedure.

## Documentation

Documentation can be found here 

### Building documentation

Use the following commands to build documentation from `docs/source` into `docs/html`:
 
 ```
 python bootstrap.py -c docs.cfg
 bin/buildout -N -c docs.cfg
 bin/docs 
 ```

To have the documentation translated into *<lang>* [2 letter ISO language code](https://en.wikipedia.org/wiki/List_of_ISO_639-2_codes "Wikipedia"), you have to follow the scenario below:

 1. Pull all the translatable strings out of the documentation:
       
```
(cd docs/_build; make gettext)
      
```

 2. Update translation with new/changed strings::
 
```
bin/sphinx-intl update -c docs/source/conf.py -p docs/_build/locale -l <lang>
 
```
    
 3. Update updated/missing strings in `docs/source/locale/<lang>/LC_MESSAGES/*.po` with your-favorite-editor/poedit/transifex/pootle/etc. to have all translations complete/updated.

 4. Compile the translation:
 
```
bin/sphinx-intl build -c docs/source/conf.py
  
```

 5. Build translated documentation(s):
 
```
(cd docs/_build; make -e SPHINXOPTS="-D language='uk'" html)
```
