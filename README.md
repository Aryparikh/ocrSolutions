# ocrSolutions
FOR PYTHON 2 (no library version support for Py3)

There are two kinds of pdf documents ; Scanned and Vectorized.
Scanned documents are pictures, vectorized documents have text that you can select, in them.

This program offers solutions to extract text from both kinds of documents.

This program has a few functions.

- validator() verifies if the doc is scanned or vectorized. It returns True if vectorized and false if scanned

- scan2vec() converts scanned psfs to vectorized pdfs. It takes path as input
and returns the path of the converted PDF.

- vecTextExtractor() extracts text from a vectorized pdf. It returns a list of strings, where each element in this list corresponds to
the text of each page in the pdf. This is very useful later on for further text processing.

- convertWithPdfMiner() takes vectorized pdf as input, and returns a list of strings, as in vecTextExtractor, where each element
corresponds to the text of each page in the pdf.

DEPENDENCIES :

The libraries used here are pypdfocr, PyPDF2 and pdfminer.


- pypdfocr is used for converting scanned to vectorized pdfs.

- PyPDF2 works well for English pdf text extraction.

- pdfminer works well for non english pdf text extraction. (Note : It is REALLY slow.)

* We had to work with documents of all languages (not just english) *

This is really messy, I know, but for our POC, this worked out.
