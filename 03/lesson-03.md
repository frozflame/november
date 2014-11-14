
Lesson 3
--------

#### HTML ####

Open a web page with your browser, save it (the common keyboard shortcut is
`F5`) to a file. Then open it with a text editor (notepad or notepad++, or
whatever you like). You will find that, when parsed as text, the _HTML_ file
seems human-readable. Yes, HTML files, which carry the contents of web pages and
describe their structures, are text files.

A brother of HTML is named _XML_, which is also quite omnipresent these days.
One notable example of XML is _DOCX_, the default format of Microsoft Word 2007
and newer versions. You can try opening a _.docx_ file to confirm that it is a
text file, and see how XML looks like.

=======================================

#### HTML and the Web ####

Let try to serve a simple web page with python's `http.server` module. Create a
folder (directory), and put a file named `index.html` which has the following
content

    <html>
        <head>
            <>
        </head>
