# pdfappendix
A command line tool to "stamping" am existing PDF file with a text caption (for instance *Appendix 1*)

This version is intended for MacOS. A Linux version may follow, if God is willing.

**Prerequisites:**
* **Python3**  must be installed (standard on MacOs)
* **htmldoc** must be installed (http://macappstore.org/htmldoc/) and included in PATH
* **PyPDF2** must be installed with pip/pip3 (*pip install PyPDF2*) 
* **pdfappendix** must be given executable permission (*sudo chmod +x pdfappendix*)

**Usage syntax:**

pdfappendix [-h] [-o OUTPUT] [-p PAGE] [-s {1,2,3,4,5,6}] inputfile text

inputfile = input file name (must be PDF)
text = text to stamp on to PDF (must be in quotes if it contains whitespace)

verbose arguments:

-h == --help ==> show help

-o == --output ==> set output file name (default: inputfile+_)

-p == --page ==> set page number (in input file) to place stamp on (default: 1)

-s == --size ==> set caption size (1 is biggest and 6 is smallest, c.f. < h 1 > to < h 6 > in HTML; default: 4)

**Example usage:**

*pdfappendix mypdf.pdf "Appendix 1"* <-- creates a new file called mypdf_.pdf with the first page stamped with "Appendix 1"

*pdfappendix -p 3 mypdf.pdf "Third page here"* <-- creates a new file called mypdf_.pdf with the third page stamped with "Third page here"

*pdfappednix -o output.pdf -s 6 mypdf.pdf "Smaller caption"* <-- creates a new file called output.pdf with the first paged stamped with "Smaller caption" (in smaller text)

**Credits:**

Code: Enterprise (A complete amateur, but pretty smart)

Thanks to Dinero for PyPDF2 tips and vhe for general "housekeeping" tips.

*This project was made possible with the help of https://www.flashback.org*
