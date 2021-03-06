Create an EPUB file (or HBP package) based on directory contents
Usage: packepub [-i=newid] <epubname>

packepub looks at the current directory for 'mimetype' and META-INF if they don't exist it will issue an error and exit.
It checks the META-INF/container.xml for the OPF file and then looks at the OPF file.

Files are packed according to OPF contents.

dcterms:modified metadata is changed according to current time.
There is an option to change the book unique identifier e.g. packepub -i="newid" demo.epub

Uses XML::Parser and Archive::Zip

Works with books in all languages.
It will not work if one of the files contains spaces or special characters in it's name.
It is also assumed that there is a new line at the end of each line in OPF file.

Note: This script can also pack an HBP package. HBP is a package format defined by Helicon books, based on EPUB that allowes packing PDF files or video files.

