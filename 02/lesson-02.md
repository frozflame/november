
Lesson 2
--------

#### Use Keyboard Shortcuts ####

Lots of people are abusing their mice. But to become an efficient user, you
should try to use keyboard shortcuts whenever possible. That will dramatically
increase your productivity working with a computer. 

Try the following shortcuts if you are using Windows

+ `win` + `e`
+ `win` + `r`
+ `win` + `tab`
+ `alt` + `tab`
+ `alt` + `tab` + `shift`

Close a window with `alt` + `f4`.

Close a tab with `ctrl` + `w` in most browsers. I recommend *Chrome* or
*Firefox* instead of *Internet Explorer*.

Try the following in *Microsoft Word* or *Kingsoft WPS*; type some words first 

+ `ctrl` + `e` 
+ `ctrl` + `r`
+ `ctrl` + `l`

Do move your hand to your mouse if you can submit a form with the key `enter`.

=======================================

#### Path ####

Do not confuse with the *PATH* environment variable.

A *path* if a way to locate a file or a directory. Using Windows, you see paths
like

    c:\anaconda\python.exe

Note that it starts with a letter plus a colon, `c:` as in this example. The
letter `c` here is called drive letter, which corresponds to a partition
(accuately speaking, a *volumne*, but it does not make a lot of sense distinguish
the two here). `c:` or `c:\` is called root direcotry. 

Paths in Windows are **case insensitive**, which means that

    C:\Anaconda\Python.exe

locates exactly the same file as the previous example does. But this is NOT the
case for GNU/Linux or Mac OS X.

Also note that the delimiter used is backslash (`\`). In most cases, you can use
forward slash (`/`) too. e.g.

    c:/anaconda/python.exe

Paths used in GNU/Linux or Mac OS X look like

    /usr/bin/python

where forword slashes are always used, and there are no such concept called
drive letter, and root directory is simply represented by the leading `/`.

The word *folder* refers to the same thing as *directory*.

=======================================

#### Shell ####

What is a shell? Quoted from
[wikipedia](http://en.wikipedia.org/wiki/Shell_%28computing%29)

>    In computing, a shell is a user interface for access to for access to an
>    operating system's services. ...

Please read the leading 4 paragraphs of that wikipedia article.

But in most context, the word *shell* refers to command-line interface
exclusively. For Windows, *CMD* the default option; for GNU/Linux and Mac OS X,
*Bash* is the mostly used.

*IPython* is also a shell.

=======================================

#### Run a Python script ####

You have learned to used the IPython shell to play with Python interactively.
But that is for exploratory jobs only, such as

+ learn Python
+ data analysis

For most jobs, instead of typing statements line by line, you write all your
Python code in files. We begin with a single file program, named `hello.py`. 

In your shell, type

    python hello.py

and you will see the result. Let me explain how this worked.

You should know a program named *notepad* in Windows. Try this in CMD

    notepad

You see *notepad* launched. Now try

    notepad hello.py

You see *notepad* launched with file `hello.py` opened. So you see this mini syntax.
The first part if the program name, the second is an argument to the program;
very likely this is the name (or path) of the file to be opened by the program.

By typing `python hello.py`, you launch Python interpreter and pass argument
`hello.py` to it. Python interpreter will open `hello.py`; then interprete it
and run it.

Learn a new trick call output redirect. Simply

    python hello.py > output.txt

Then open the file `output.txt`.

One more thing to understand: when you do `notepad hello.py` or `python
hello.py`, you **explicitly** choose the program to handle the file, so the
extension `.py` does NOT imply the type of that file. You can change `hello.py`
to `hello.abc` or `hello.txt`, and run

    python hello.txt

You get exactly the same result. 

This is different from clicking an icon in Windows Explorer (`Computer` or `My
Computer`), which looks the extension to guess file type, and launches the
corresponding program to handle the file.

Try open a file with `arglist.exe`.

=======================================

#### Simple HTTP Server ####

Try in shell

    python -m http.server 5000

If you are using Python 2, you should do

    python -m SimpleHTTPServer 5000

Now go to your web browser, type the following in the address bar

    localhost:5000

If you have the privilege, you can open you server at port 80

    python -m http.server 80

Then you don't need to specify the port number to your browser

    localhost

It will work. 

Create a file named `index.html` at your current working directory, and put some
contents in it. Try opening the server again, see the result.

Create a local network and practice these using two computers (two hosts). You
type the IP address of the server instead of `localhost` in your browser. e.g.

    192.168.0.12:5000

=======================================

