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
