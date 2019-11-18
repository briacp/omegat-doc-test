# OmegaT Documentation

Conversion test from DocBook format to structuredText / ReadTheDocs.

## Conversion DocBook to RST

Using pandoc:

```bash
for FILENAME in *.xml; do
    pandoc -f docbook -t rst -o "${FILENAME/.xml/.rst}" "$FILENAME";
done
```

The xincludes need to be modified to `toctree`.

## Documentation generation

``sphinx-build -b html -D language=en source build/html``

I18N resources generation
``sphinx-build -b gettext source build/gettext``
``sphinx-intl update -p build/gettext -l fr -l uk -l es``
``sphinx-build -b html -D language=fr source build/html/fr``

## Structure Hierarchy RsT

```


Part h1
#######

Chapter h2
**********

Section h3
==========

Subsection h4
-------------

Para h5
~~~~~~~

Subpara h6
^^^^^^^^^^

What h7
"""""""

Aliquam finibus sit amet arcu et placerat.

.. code-block:: ini
    :linenos:

    # foo
    bar=13
    baz=quux

Nam fermentum lacus at est facilisis malesuada.

.. code-block:: javascript
    :linenos:

    var x = 1;
    function foo(bar) {
        if (bar == "foo") {
            return 1;
        }
    }
    console.log("Hello");


Ut faucibus consectetur turpis sit amet tristique.

```
