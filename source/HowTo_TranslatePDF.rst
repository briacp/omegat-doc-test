Translate a PDF file
====================

PDF files are a special case. They contain text formatting information,
but such information cannot be reused by OmegaT in order to create
target files. Thus, PDF files are handled as plain text files, and
output files are plain text files.

If you need to reproduce text formatting (as well as other things such
as drawings) in your translation, there are three ways to try:

1. Use OmegaT’s default filter (PDF input), translate, create a target
   file (it will be a plain text file), add relevant formatting and
   items manually.

2. Use the Iceni Infix filter. See `Howto - Translating PDF files with
   Iceni Infix and
   OmegaT <https://omegat.org/howtos/iceni_infix.html>`__.

3. Import the source file to `LibreOffice
   Draw <https://www.libreoffice.org/discover/draw/>`__, save it as an
   ODG file, translate, export to PDF as needed.

**Note:** the above information applies only to PDF files with a text
layer. If you have a PDF file made of scanned pages (sometimes such
files are referred to as ‘dead’ PDFs), you need to use an OCR (optical
character recognition) program to recognize the text and convert it to a
format that can be handled by OmegaT.

Other file formats
------------------

Other plain text or formatted text file formats suitable for processing
in OmegaT may also exist.

External tools can be used to convert files to supported formats. The
translated files will then need to be converted back to the original
format. For example, if you have an outdated Microsoft Word version,
that does not handle the ODT format, here's a round trip for Word files
with the DOC extension:

-  import the file into ODF writer

-  save the file in ODT format

-  translate it into the target ODT file

-  load the target file in ODF writer

-  save the file as a DOC file

The quality of formatting of the translated file will depend on the
quality of the round-trip conversion. Before proceeding with such
conversions, be sure to test all options. Check the `OmegaT home
page <http://www.omegat.org>`__ for an up-to-date listing of auxiliary
translation tools.
