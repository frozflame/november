
Lesson 3
--------

#### Read and Write Files ####

You can open a file for read simple with

    myfile = open('d:/hailong/story.txt')

Then `myfile` refers to a _file object_. Don't worry if you don't know what a
file object is. It is just of a new type of data. Also note the path: I am using
forward slash as delimiter. If you use backslash, you should do

    myfile = open('d:\\hailong\\story.txt')

or use raw string representation (prefixing _r_)

    myfile = open(r'd:\hailong\story.txt')

Read content of that file

    content = myfile.read()

Now `content` refers to a string which represents the content of that file.
Easy?

Try to write some string to a file. To do this, you have to open a file in
_write mode_. Example

    outfile = open('d:/hailong/simply.txt', 'w')

If `d:/hailong/simply.txt` does NOT exist, it will be created. If it does, if will
be OVERWRITTEN and you previous data in that file will be LOST! So be sure of
what you are doing.

Now write some content

    text = "If you can't explain it simply, you don't understand it well enough."
    outfile.write(text)
    outfile.close()

You can open a file in _append mode_, which does not destroy previous data, but
add new content at the end of the file.

    outfile = open('d:/hailong/simply.txt', 'a')
    outfile.write('\n')
    outfile.write('Albert Einstein')
    outfile.close()

=======================================    

#### HTML and Others ####

Open a web page with your browser, save it (the common keyboard shortcut is
`F5`) to a file. Then open it with a text editor (notepad or notepad++, or
whatever you like). You will find that, when parsed as text, the _HTML_ file
seems human-readable. Yes, HTML files, which carry the contents of web pages and
describe their structures, are text files.

A brother of HTML is named _XML_, which is also quite omnipresent these days.
One notable example of XML is _DOCX_, the default format of Microsoft Word 2007
and newer versions. 

A DOCX file is a compressed archive containing some XML files and other
resources as separate files, e.g. images. Texts and tables, as well as their
format information,  are stored in XML files. Try uncompress a DOCX file and
find XML files in it. Open an XML file with a text editor to see how it looks
like.  

Scalable Vector Graphics a vector image format widely used. It is based on XML,
so obviously it is text. 

Before we dive into the details of these formats, please ask yourself: what will
I be able to do after learning these? 

You will be able to generate files of these formats _programmatically_!

=======================================

#### HTML and the Web ####

Let try to serve a simple web page with python's `http.server` module. Create a
folder (directory), and put a file named `index.html` which has the following
content

    <html>
        <head>
            <title>Welcome!</title>
        </head>
        <body>
            <h1>Welcome to My Site!</h1>
            <hr>
            It works!
        </body>
    </html>

Change you current working directory to your newly create folder. Serve with 

    python -m http.server 5000

Open your browser and go to URL

    localhost:5000/index.html

You can omit the trailing `/index.html` actually, since it is the default.
Simply

    localhost:5000

will work. 

**Static** v.s. **Dynamic** web pages

Date back to the early days of World Wide Web. Most websites serve web pages
were _static_, which means they were premade before you visit, and whenever or
whoever visit the content remains the same until the staff of the company change
that manually, similar to a blackboard.

With the advent of Web 2.0, which highlights user generated data, _dynamic_ web
pages become mainstream. Dynamic pages are pages generated _ad hoc_ by backend
applications. These applications are mostly written in PHP, Java, Python and
Ruby, among other languages.

=======================================

#### More Keyboard Shortcuts ####

Select a file or folder in your Windows File Manager (Explorer, or Computer, or
My Computer), then press `F2`. Rename.

Try `F3` and `F4`.

