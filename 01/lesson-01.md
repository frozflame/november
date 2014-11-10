
Lesson 1
--------

#### Install Python ####

Python is already installed if you are using GNU/Linux or Mac OS X. But for
Windows, you have to install if yourself. 

I recommend you to install Anaconda instead of the standard Python release,
since installing packages might be a daunting task for beginners. Anaconda ships
with lots of useful packages which you might need in the future.

Anaconda can be downloaded from <http://repo.continuum.io/archive/.winzip/>.

Please download `Anaconda3` since I will use Python 3 in the rest of my
tutorials.

Unzip the downloaded file and run the installer. You can handle it yourself.


=======================================

#### Play Around ####

It is not a good idea to learn tons of theories before you have any hand-on
experience. So let us begin by playing with it.

Open `IPython (Py 3.4) QTConsole` from you `Start Menu`. If the font size if too
small for you, press `Ctrl` + `Shift` + `=` to zoom in.

Use this program as a calculator and try some simple maths

    In [1]: 365 * 24 * 3600
    Out[1]: 31536000

and for exponential, use `**` operator

    In [2]: 2 ** 10
    Out[2]: 1024

You can try all maths you learned in your high school. How to find square root?
Ask yourself. What about logarithm? Let me show you how

    In [3]: import math

    In [4]: math.log(1024, 2)
    Out[4]: 10.0

The `import` simply brings some stuff called `math` for you. Now you can use
`math.log` to calculate logarithms. Note that the `2` if the base. Actually,
`math` is a *module* which contains a collection of functions. For example

    In [4]: math.sqrt(2)
    Out[4]: 1.4142135623730951

 you found the square root of number *2*, which you might just figured out with
 `2 ** 0.5`. 

 It may be inconvenient to always type `math.`. There is a trick.

    In [5]: from math import log

    In [6]: log(1024, 2)
    Out[6]: 10.0

Now you can simply use the function as `log` instead of `math.log`. But you
still have to use `math.sqrt`. Another trick for the laziest

    In [7]: from math import *

    In [8]: sqrt(2)
    Out[8]: 1.4142135623730951

    In [9]: sin(1)
    Out[9]: 0.8414709848078965

    In [11]: cos(0)
    Out[11]: 1.0
 
`from math import *` means to bring every inside `math` to us, including `sin`
and `cos`.

Note the numbers in brackets after `In` or `Out`. These are auto-incremental. So
yours might be different from mine if you are not following my examples exactly.
In future examples, I will use `In [#]` and `Out[#]` to make my life easier.

=======================================

#### A Simple Plot ####

This section only shows you how easy is it for python to do such a job. Some
details are omitted here and will be expained in near future.

We are going to plot functions *y=sin(x)* and *y=cos(x)* where *x* is in the
interval *[0, 10]*. Follow this example

    In [#]: from pylab import *

    In [#]: x = linspace(0)

    In [#]: y = sin(x)

    In [#]: z = cos(x)

    In [#]: plot(x, y)

    In [#]: plot(x, z)

    In [#]: show()

You may wonder why there is a `show()` here. It is of no use to show the
unfinished figure. You signal `show()` when you know your job is done.

I hope you have learned something. Enjoy! 

