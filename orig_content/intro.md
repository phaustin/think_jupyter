
# Preface

## The strange history of this book

In January 1999 I was preparing to teach an introductory programming
class in Java. I had taught it three times and I was getting frustrated.
The failure rate in the class was too high and, even for students who
succeeded, the overall level of achievement was too low.

One of the problems I saw was the books. They were too big, with too
much unnecessary detail about Java, and not enough high-level guidance
about how to program. And they all suffered from the trap door effect:
they would start out easy, proceed gradually, and then somewhere around
Chapter 5 the bottom would fall out. The students would get too much new
material, too fast, and I would spend the rest of the semester picking
up the pieces.

Two weeks before the first day of classes, I decided to write my own
book. My goals were:

  - Keep it short. It is better for students to read 10 pages than not
    read 50 pages.

  - Be careful with vocabulary. I tried to minimize jargon and define
    each term at first use.

  - Build gradually. To avoid trap doors, I took the most difficult
    topics and split them into a series of small steps.

  - Focus on programming, not the programming language. I included the
    minimum useful subset of Java and left out the rest.

I needed a title, so on a whim I chose <span>*How to Think Like a
Computer Scientist*</span>.

My first version was rough, but it worked. Students did the reading, and
they understood enough that I could spend class time on the hard topics,
the interesting topics and (most important) letting the students
practice.

I released the book under the GNU Free Documentation License, which
allows users to copy, modify, and distribute the book.

What happened next is the cool part. Jeff Elkner, a high school teacher
in Virginia, adopted my book and translated it into Python. He sent me a
copy of his translation, and I had the unusual experience of learning
Python by reading my own book. As Green Tea Press, I published the first
Python version in 2001.

In 2003 I started teaching at Olin College and I got to teach Python for
the first time. The contrast with Java was striking. Students struggled
less, learned more, worked on more interesting projects, and generally
had a lot more fun.

Since then I’ve continued to develop the book, correcting errors,
improving some of the examples and adding material, especially
exercises.

The result is this book, now with the less grandiose title <span>*Think
Python*</span>. Some of the changes are:

  - I added a section about debugging at the end of each chapter. These
    sections present general techniques for finding and avoiding bugs,
    and warnings about Python pitfalls.

  - I added more exercises, ranging from short tests of understanding to
    a few substantial projects. Most exercises include a link to my
    solution.

  - I added a series of case studies—longer examples with exercises,
    solutions, and discussion.

  - I expanded the discussion of program development plans and basic
    design patterns.

  - I added appendices about debugging and analysis of algorithms.

The second edition of <span>*Think Python*</span> has these new
features:

  - The book and all supporting code have been updated to Python 3.

  - I added a few sections, and more details on the web, to help
    beginners get started running Python in a browser, so you don’t have
    to deal with installing Python until you want to.

  - For Chapter [5.1](#turtle) I switched from my own turtle graphics
    package, called Swampy, to a more standard Python module, <span>` 
    turtle `</span>, which is easier to install and more powerful.

  - I added a new chapter called “The Goodies”, which introduces some
    additional Python features that are not strictly necessary, but
    sometimes handy.

I hope you enjoy working with this book, and that it helps you learn to
program and think like a computer scientist, at least a little bit.

Allen B. Downey  
Olin College  

## Acknowledgments

Many thanks to Jeff Elkner, who translated my Java book into Python,
which got this project started and introduced me to what has turned out
to be my favorite language.

Thanks also to Chris Meyers, who contributed several sections to
<span>*How to Think Like a Computer Scientist*</span>.

Thanks to the Free Software Foundation for developing the GNU Free
Documentation License, which helped make my collaboration with Jeff and
Chris possible, and Creative Commons for the license I am using now.

Thanks to the editors at Lulu who worked on <span>*How to Think Like a
Computer Scientist*</span>.

Thanks to the editors at O’Reilly Media who worked on <span>*Think
Python*</span>.

Thanks to all the students who worked with earlier versions of this book
and all the contributors (listed below) who sent in corrections and
suggestions.

## Contributor List

More than 100 sharp-eyed and thoughtful readers have sent in suggestions
and corrections over the past few years. Their contributions, and
enthusiasm for this project, have been a huge help.

If you have a suggestion or correction, please send email to
<span>`feedback@thinkpython.com`</span>. If I make a change based on
your feedback, I will add you to the contributor list (unless you ask to
be omitted).

If you include at least part of the sentence the error appears in, that
makes it easy for me to search. Page and section numbers are fine, too,
but not quite as easy to work with. Thanks\!

  - Lloyd Hugh Allen sent in a correction to Section 8.4.

  - Yvon Boulianne sent in a correction of a semantic error in Chapter
    5.

  - Fred Bremmer submitted a correction in Section 2.1.

  - Jonah Cohen wrote the Perl scripts to convert the LaTeX source for
    this book into beautiful HTML.

  - Michael Conlon sent in a grammar correction in Chapter 2 and an
    improvement in style in Chapter 1, and he initiated discussion on
    the technical aspects of interpreters.

  - Benoît Girard sent in a correction to a humorous mistake in Section
    5.6.

  - Courtney Gleason and Katherine Smith wrote
    <span>`horsebet.py`</span>, which was used as a case study in an
    earlier version of the book. Their program can now be found on the
    website.

  - Lee Harr submitted more corrections than we have room to list here,
    and indeed he should be listed as one of the principal editors of
    the text.

  - James Kaylin is a student using the text. He has submitted numerous
    corrections.

  - David Kershaw fixed the broken <span>`catTwice`</span> function in
    Section 3.10.

  - Eddie Lam has sent in numerous corrections to Chapters 1, 2, and 3.
    He also fixed the Makefile so that it creates an index the first
    time it is run and helped us set up a versioning scheme.

  - Man-Yong Lee sent in a correction to the example code in Section
    2.4.

  - David Mayo pointed out that the word “unconsciously" in Chapter 1
    needed to be changed to “subconsciously".

  - Chris McAloon sent in several corrections to Sections 3.9 and 3.10.

  - Matthew J. Moelter has been a long-time contributor who sent in
    numerous corrections and suggestions to the book.

  - Simon Dicon Montford reported a missing function definition and
    several typos in Chapter 3. He also found errors in the
    <span>`increment`</span> function in Chapter 13.

  - John Ouzts corrected the definition of “return value" in Chapter 3.

  - Kevin Parks sent in valuable comments and suggestions as to how to
    improve the distribution of the book.

  - David Pool sent in a typo in the glossary of Chapter 1, as well as
    kind words of encouragement.

  - Michael Schmitt sent in a correction to the chapter on files and
    exceptions.

  - Robin Shaw pointed out an error in Section 13.1, where the printTime
    function was used in an example without being defined.

  - Paul Sleigh found an error in Chapter 7 and a bug in Jonah Cohen’s
    Perl script that generates HTML from LaTeX.

  - Craig T. Snydal is testing the text in a course at Drew University.
    He has contributed several valuable suggestions and corrections.

  - Ian Thomas and his students are using the text in a programming
    course. They are the first ones to test the chapters in the latter
    half of the book, and they have made numerous corrections and
    suggestions.

  - Keith Verheyden sent in a correction in Chapter 3.

  - Peter Winstanley let us know about a longstanding error in our Latin
    in Chapter 3.

  - Chris Wrobel made corrections to the code in the chapter on file I/O
    and exceptions.

  - Moshe Zadka has made invaluable contributions to this project. In
    addition to writing the first draft of the chapter on Dictionaries,
    he provided continual guidance in the early stages of the book.

  - Christoph Zwerschke sent several corrections and pedagogic
    suggestions, and explained the difference between
    <span>*gleich*</span> and <span>*selbe*</span>.

  - James Mayer sent us a whole slew of spelling and typographical
    errors, including two in the contributor list.

  - Hayden McAfee caught a potentially confusing inconsistency between
    two examples.

  - Angel Arnal is part of an international team of translators working
    on the Spanish version of the text. He has also found several errors
    in the English version.

  - Tauhidul Hoque and Lex Berezhny created the illustrations in Chapter
    1 and improved many of the other illustrations.

  - Dr. Michele Alzetta caught an error in Chapter 8 and sent some
    interesting pedagogic comments and suggestions about Fibonacci and
    Old Maid.

  - Andy Mitchell caught a typo in Chapter 1 and a broken example in
    Chapter 2.

  - Kalin Harvey suggested a clarification in Chapter 7 and caught some
    typos.

  - Christopher P. Smith caught several typos and helped us update the
    book for Python 2.2.

  - David Hutchins caught a typo in the Foreword.

  - Gregor Lingl is teaching Python at a high school in Vienna, Austria.
    He is working on a German translation of the book, and he caught a
    couple of bad errors in Chapter 5.

  - Julie Peters caught a typo in the Preface.

  - Florin Oprina sent in an improvement in <span>`makeTime`</span>, a
    correction in <span>`printTime`</span>, and a nice typo.

  - D. J. Webre suggested a clarification in Chapter 3.

  - Ken found a fistful of errors in Chapters 8, 9 and 11.

  - Ivo Wever caught a typo in Chapter 5 and suggested a clarification
    in Chapter 3.

  - Curtis Yanko suggested a clarification in Chapter 2.

  - Ben Logan sent in a number of typos and problems with translating
    the book into HTML.

  - Jason Armstrong saw the missing word in Chapter 2.

  - Louis Cordier noticed a spot in Chapter 16 where the code didn’t
    match the text.

  - Brian Cain suggested several clarifications in Chapters 2 and 3.

  - Rob Black sent in a passel of corrections, including some changes
    for Python 2.2.

  - Jean-Philippe Rey at École Centrale Paris sent a number of patches,
    including some updates for Python 2.2 and other thoughtful
    improvements.

  - Jason Mader at George Washington University made a number of useful
    suggestions and corrections.

  - Jan Gundtofte-Bruun reminded us that “a error” is an error.

  - Abel David and Alexis Dinno reminded us that the plural of “matrix”
    is “matrices”, not “matrixes”. This error was in the book for years,
    but two readers with the same initials reported it on the same day.
    Weird.

  - Charles Thayer encouraged us to get rid of the semi-colons we had
    put at the ends of some statements and to clean up our use of
    “argument” and “parameter”.

  - Roger Sperberg pointed out a twisted piece of logic in Chapter 3.

  - Sam Bull pointed out a confusing paragraph in Chapter 2.

  - Andrew Cheung pointed out two instances of “use before def”.

  - C. Corey Capel spotted the missing word in the Third Theorem of
    Debugging and a typo in Chapter 4.

  - Alessandra helped clear up some Turtle confusion.

  - Wim Champagne found a brain-o in a dictionary example.

  - Douglas Wright pointed out a problem with floor division in
    <span>`arc`</span>.

  - Jared Spindor found some jetsam at the end of a sentence.

  - Lin Peiheng sent a number of very helpful suggestions.

  - Ray Hagtvedt sent in two errors and a not-quite-error.

  - Torsten Hübsch pointed out an inconsistency in Swampy.

  - Inga Petuhhov corrected an example in Chapter 14.

  - Arne Babenhauserheide sent several helpful corrections.

  - Mark E. Casida is is good at spotting repeated words.

  - Scott Tyler filled in a that was missing. And then sent in a heap of
    corrections.

  - Gordon Shephard sent in several corrections, all in separate emails.

  - Andrew Turner <span>`spot`</span>ted an error in Chapter 8.

  - Adam Hobart fixed a problem with floor division in
    <span>`arc`</span>.

  - Daryl Hammond and Sarah Zimmerman pointed out that I served up
    <span>`math.pi`</span> too early. And Zim spotted a typo.

  - George Sass found a bug in a Debugging section.

  - Brian Bingham suggested
    Exercise [\[exrotatepairs\]](#exrotatepairs).

  - Leah Engelbert-Fenton pointed out that I used <span>`tuple`</span>
    as a variable name, contrary to my own advice. And then found a
    bunch of typos and a “use before def”.

  - Joe Funke spotted a typo.

  - Chao-chao Chen found an inconsistency in the Fibonacci example.

  - Jeff Paine knows the difference between space and spam.

  - Lubos Pintes sent in a typo.

  - Gregg Lind and Abigail Heithoff suggested
    Exercise [\[checksum\]](#checksum).

  - Max Hailperin has sent in a number of corrections and suggestions.
    Max is one of the authors of the extraordinary <span> *Concrete
    Abstractions*</span>, which you might want to read when you are done
    with this book.

  - Chotipat Pornavalai found an error in an error message.

  - Stanislaw Antol sent a list of very helpful suggestions.

  - Eric Pashman sent a number of corrections for Chapters 4–11.

  - Miguel Azevedo found some typos.

  - Jianhua Liu sent in a long list of corrections.

  - Nick King found a missing word.

  - Martin Zuther sent a long list of suggestions.

  - Adam Zimmerman found an inconsistency in my instance of an
    “instance” and several other errors.

  - Ratnakar Tiwari suggested a footnote explaining degenerate
    triangles.

  - Anurag Goel suggested another solution for `is_abecedarian` and sent
    some additional corrections. And he knows how to spell Jane Austen.

  - Kelli Kratzer spotted one of the typos.

  - Mark Griffiths pointed out a confusing example in Chapter 3.

  - Roydan Ongie found an error in my Newton’s method.

  - Patryk Wolowiec helped me with a problem in the HTML version.

  - Mark Chonofsky told me about a new keyword in Python 3.

  - Russell Coleman helped me with my geometry.

  - Nam Nguyen found a typo and pointed out that I used the Decorator
    pattern but didn’t mention it by name.

  - Stéphane Morin sent in several corrections and suggestions.

  - Paul Stoop corrected a typo in `uses_only`.

  - Eric Bronner pointed out a confusion in the discussion of the order
    of operations.

  - Alexandros Gezerlis set a new standard for the number and quality of
    suggestions he submitted. We are deeply grateful\!

  - Gray Thomas knows his right from his left.

  - Giovanni Escobar Sosa sent a long list of corrections and
    suggestions.

  - Daniel Neilson corrected an error about the order of operations.

  - Will McGinnis pointed out that <span>`polyline`</span> was defined
    differently in two places.

  - Frank Hecker pointed out an exercise that was under-specified, and
    some broken links.

  - Animesh B helped me clean up a confusing example.

  - Martin Caspersen found two round-off errors.

  - Gregor Ulm sent several corrections and suggestions.

  - Dimitrios Tsirigkas suggested I clarify an exercise.

  - Carlos Tafur sent a page of corrections and suggestions.

  - Martin Nordsletten found a bug in an exercise solution.

  - Sven Hoexter pointed out that a variable named <span>`input`</span>
    shadows a build-in function.

  - Stephen Gregory pointed out the problem with <span>`cmp`</span> in
    Python 3.

  - Ishwar Bhat corrected my statement of Fermat’s last theorem.

  - Andrea Zanella translated the book into Italian, and sent a number
    of corrections along the way.

  - Many, many thanks to Melissa Lewis and Luciano Ramalho for excellent
    comments and suggestions on the second edition.

  - Thanks to Harry Percival from PythonAnywhere for his help getting
    people started running Python in a browser.

  - Xavier Van Aubel made several useful corrections in the second
    edition.

  - William Murray corrected my definition of floor division.

  - Per Starb<span>ä</span>ck brought me up to date on universal
    newlines in Python 3.

  - Laurent Rosenfeld and Mihaela Rotaru translated this book into
    French. Along the way, they sent many corrections and suggestions.
    
    In addition, people who spotted typos or made corrections include
    Czeslaw Czapla, Dale Wilson, Francesco Carlo Cimini, Richard Fursa,
    Brian McGhie, Lokesh Kumar Makani, Matthew Shultz, Viet Le, Victor
    Simeone, Lars O.D. Christensen, Swarup Sahoo, Alix Etienne, Kuang
    He, Wei Huang, Karen Barber, and Eric Ransom.

# The way of the program

The goal of this book is to teach you to think like a computer
scientist. This way of thinking combines some of the best features of
mathematics, engineering, and natural science. Like mathematicians,
computer scientists use formal languages to denote ideas (specifically
computations). Like engineers, they design things, assembling components
into systems and evaluating tradeoffs among alternatives. Like
scientists, they observe the behavior of complex systems, form
hypotheses, and test predictions.

The single most important skill for a computer scientist is <span>
**problem solving**</span>. Problem solving means the ability to
formulate problems, think creatively about solutions, and express a
solution clearly and accurately. As it turns out, the process of
learning to program is an excellent opportunity to practice
problem-solving skills. That’s why this chapter is called, “The way of
the program”.

On one level, you will be learning to program, a useful skill by itself.
On another level, you will use programming as a means to an end. As we
go along, that end will become clearer.

## What is a program?

A <span>**program**</span> is a sequence of instructions that specifies
how to perform a computation. The computation might be something
mathematical, such as solving a system of equations or finding the roots
of a polynomial, but it can also be a symbolic computation, such as
searching and replacing text in a document or something graphical, like
processing an image or playing a video.

The details look different in different languages, but a few basic
instructions appear in just about every language:

  - input:  
    Get data from the keyboard, a file, the network, or some other
    device.

  - output:  
    Display data on the screen, save it in a file, send it over the
    network, etc.

  - math:  
    Perform basic mathematical operations like addition and
    multiplication.

  - conditional execution:  
    Check for certain conditions and run the appropriate code.

  - repetition:  
    Perform some action repeatedly, usually with some variation.

Believe it or not, that’s pretty much all there is to it. Every program
you’ve ever used, no matter how complicated, is made up of instructions
that look pretty much like these. So you can think of programming as the
process of breaking a large, complex task into smaller and smaller
subtasks until the subtasks are simple enough to be performed with one
of these basic instructions.

## Running Python

One of the challenges of getting started with Python is that you might
have to install Python and related software on your computer. If you are
familiar with your operating system, and especially if you are
comfortable with the command-line interface, you will have no trouble
installing Python. But for beginners, it can be painful to learn about
system administration and programming at the same time.

To avoid that problem, I recommend that you start out running Python in
a browser. Later, when you are comfortable with Python, I’ll make
suggestions for installing Python on your computer.

There are a number of web pages you can use to run Python. If you
already have a favorite, go ahead and use it. Otherwise I recommend
PythonAnywhere. I provide detailed instructions for getting started at
<http://tinyurl.com/thinkpython2e>.

There are two versions of Python, called Python 2 and Python 3. They are
very similar, so if you learn one, it is easy to switch to the other. In
fact, there are only a few differences you will encounter as a beginner.
This book is written for Python 3, but I include some notes about Python
2.

The Python <span>**interpreter**</span> is a program that reads and
executes Python code. Depending on your environment, you might start the
interpreter by clicking on an icon, or by typing <span>`python`</span>
on a command line. When it starts, you should see output like this:

    Python 3.4.0 (default, Jun 19 2015, 14:20:21) 
    [GCC 4.8.2] on linux
    Type "help", "copyright", "credits" or "license" for more information.
    >>> 

The first three lines contain information about the interpreter and the
operating system it’s running on, so it might be different for you. But
you should check that the version number, which is <span>`3.4.0`</span>
in this example, begins with 3, which indicates that you are running
Python 3. If it begins with 2, you are running (you guessed it) Python
2.

The last line is a <span>**prompt**</span> that indicates that the
interpreter is ready for you to enter code. If you type a line of code
and hit Enter, the interpreter displays the result:

    >>> 1 + 1
    2

Now you’re ready to get started. From here on, I assume that you know
how to start the Python interpreter and run code.

## The first program

Traditionally, the first program you write in a new language is called
“Hello, World\!” because all it does is display the words “Hello,
World\!”. In Python, it looks like this:

    >>> print('Hello, World!')

This is an example of a <span>**print statement**</span>, although it
doesn’t actually print anything on paper. It displays a result on the
screen. In this case, the result is the words

    Hello, World!

The quotation marks in the program mark the beginning and end of the
text to be displayed; they don’t appear in the result.

The parentheses indicate that <span>`print`</span> is a function. We’ll
get to functions in Chapter [4](#funcchap).

In Python 2, the print statement is slightly different; it is not a
function, so it doesn’t use parentheses.

    >>> print 'Hello, World!'

This distinction will make more sense soon, but that’s enough to get
started.

## Arithmetic operators

After “Hello, World”, the next step is arithmetic. Python provides
<span>**operators**</span>, which are special symbols that represent
computations like addition and multiplication.

The operators <span>`+`</span>, <span>`-`</span>, and <span>`  `</span>
perform addition, subtraction, and multiplication, as in the following
examples:

    >>> 40 + 2
    42
    >>> 43 - 1
    42
    >>> 6 * 7
    42

The operator <span>`/`</span> performs division:

    >>> 84 / 2
    42.0

You might wonder why the result is <span>`42.0`</span> instead of
<span>`42`</span>. I’ll explain in the next section.

Finally, the operator <span>`*`</span> performs exponentiation; that is,
it raises a number to a power:

    >>> 6**2 + 6
    42

In some other languages, `^` is used for exponentiation, but in Python
it is a bitwise operator called XOR. If you are not familiar with
bitwise operators, the result will surprise you:

    >>> 6 ^ 2
    4

I won’t cover bitwise operators in this book, but you can read about
them at <http://wiki.python.org/moin/BitwiseOperators>.

## Values and types

A <span>**value**</span> is one of the basic things a program works
with, like a letter or a number. Some values we have seen so far are
<span>`2`</span>, <span>`42.0`</span>, and `'Hello, World!'`.

These values belong to different <span>**types**</span>:
<span>`2`</span> is an <span>**integer**</span>, <span>`42.0`</span> is
a <span>**floating-point number**</span>, and `'Hello, World!'` is a
<span>**string**</span>, so-called because the letters it contains are
strung together.

If you are not sure what type a value has, the interpreter can tell you:

    >>> type(2)
    <class 'int'>
    >>> type(42.0)
    <class 'float'>
    >>> type('Hello, World!')
    <class 'str'>

In these results, the word “class” is used in the sense of a category; a
type is a category of values.

Not surprisingly, integers belong to the type <span>`int`</span>,
strings belong to <span>`str`</span> and floating-point numbers belong
to <span>`float`</span>.

What about values like `'2'` and `'42.0'`? They look like numbers, but
they are in quotation marks like strings.

    >>> type('2')
    <class 'str'>
    >>> type('42.0')
    <class 'str'>

They’re strings.

When you type a large integer, you might be tempted to use commas
between groups of digits, as in <span>`1,000,000`</span>. This is not a
legal <span>*integer*</span> in Python, but it is legal:

    >>> 1,000,000
    (1, 0, 0)

That’s not what we expected at all\! Python interprets
<span>`  1,000,000 `</span> as a comma-separated sequence of integers.
We’ll learn more about this kind of sequence later.

## Formal and natural languages

<span>**Natural languages**</span> are the languages people speak, such
as English, Spanish, and French. They were not designed by people
(although people try to impose some order on them); they evolved
naturally.

<span>**Formal languages**</span> are languages that are designed by
people for specific applications. For example, the notation that
mathematicians use is a formal language that is particularly good at
denoting relationships among numbers and symbols. Chemists use a formal
language to represent the chemical structure of molecules. And most
importantly:

> <span>**Programming languages are formal languages that have been
> designed to express computations.**</span>

Formal languages tend to have strict <span>**syntax**</span> rules that
govern the structure of statements. For example, in mathematics the
statement \(3 + 3 = 6\) has correct syntax, but \(3 + = 3 \$ 6\) does
not. In chemistry \(H_2O\) is a syntactically correct formula, but
\(_2Zz\) is not.

Syntax rules come in two flavors, pertaining to <span>**tokens**</span>
and structure. Tokens are the basic elements of the language, such as
words, numbers, and chemical elements. One of the problems with
\(3 += 3 \$ 6\) is that \(\$\) is not a legal token in mathematics (at
least as far as I know). Similarly, \(_2Zz\) is not legal because there
is no element with the abbreviation \(Zz\).

The second type of syntax rule pertains to the way tokens are combined.
The equation \(3 +/ 3\) is illegal because even though \(+\) and \(/\)
are legal tokens, you can’t have one right after the other. Similarly,
in a chemical formula the subscript comes after the element name, not
before.

This is @ well-structured Engli$h sentence with invalid t\*kens in it.
This sentence all valid tokens has, but invalid structure with.

When you read a sentence in English or a statement in a formal language,
you have to figure out the structure (although in a natural language you
do this subconsciously). This process is called
<span>**parsing**</span>.

Although formal and natural languages have many features in
common—tokens, structure, and syntax—there are some differences:

  - ambiguity:  
    Natural languages are full of ambiguity, which people deal with by
    using contextual clues and other information. Formal languages are
    designed to be nearly or completely unambiguous, which means that
    any statement has exactly one meaning, regardless of context.

  - redundancy:  
    In order to make up for ambiguity and reduce misunderstandings,
    natural languages employ lots of redundancy. As a result, they are
    often verbose. Formal languages are less redundant and more concise.

  - literalness:  
    Natural languages are full of idiom and metaphor. If I say, “The
    penny dropped”, there is probably no penny and nothing dropping
    (this idiom means that someone understood something after a period
    of confusion). Formal languages mean exactly what they say.

Because we all grow up speaking natural languages, it is sometimes hard
to adjust to formal languages. The difference between formal and natural
language is like the difference between poetry and prose, but more so:

  - Poetry:  
    Words are used for their sounds as well as for their meaning, and
    the whole poem together creates an effect or emotional response.
    Ambiguity is not only common but often deliberate.

  - Prose:  
    The literal meaning of words is more important, and the structure
    contributes more meaning. Prose is more amenable to analysis than
    poetry but still often ambiguous.

  - Programs:  
    The meaning of a computer program is unambiguous and literal, and
    can be understood entirely by analysis of the tokens and structure.

Formal languages are more dense than natural languages, so it takes
longer to read them. Also, the structure is important, so it is not
always best to read from top to bottom, left to right. Instead, learn to
parse the program in your head, identifying the tokens and interpreting
the structure. Finally, the details matter. Small errors in spelling and
punctuation, which you can get away with in natural languages, can make
a big difference in a formal language.

## Debugging

Programmers make mistakes. For whimsical reasons, programming errors are
called <span>**bugs**</span> and the process of tracking them down is
called <span>**debugging**</span>.

Programming, and especially debugging, sometimes brings out strong
emotions. If you are struggling with a difficult bug, you might feel
angry, despondent, or embarrassed.

There is evidence that people naturally respond to computers as if they
were people. When they work well, we think of them as teammates, and
when they are obstinate or rude, we respond to them the same way we
respond to rude, obstinate people (Reeves and Nass, <span>*The Media
Equation: How People Treat Computers, Television, and New Media Like
Real People and Places*</span>).

Preparing for these reactions might help you deal with them. One
approach is to think of the computer as an employee with certain
strengths, like speed and precision, and particular weaknesses, like
lack of empathy and inability to grasp the big picture.

Your job is to be a good manager: find ways to take advantage of the
strengths and mitigate the weaknesses. And find ways to use your
emotions to engage with the problem, without letting your reactions
interfere with your ability to work effectively.

Learning to debug can be frustrating, but it is a valuable skill that is
useful for many activities beyond programming. At the end of each
chapter there is a section, like this one, with my suggestions for
debugging. I hope they help\!

## Glossary

  - problem solving:  
    The process of formulating a problem, finding a solution, and
    expressing it.

  - high-level language:  
    A programming language like Python that is designed to be easy for
    humans to read and write.

  - low-level language:  
    A programming language that is designed to be easy for a computer to
    run; also called “machine language” or “assembly language”.

  - portability:  
    A property of a program that can run on more than one kind of
    computer.

  - interpreter:  
    A program that reads another program and executes it

  - prompt:  
    Characters displayed by the interpreter to indicate that it is ready
    to take input from the user.

  - program:  
    A set of instructions that specifies a computation.

  - print statement:  
    An instruction that causes the Python interpreter to display a value
    on the screen.

  - operator:  
    A special symbol that represents a simple computation like addition,
    multiplication, or string concatenation.

  - value:  
    One of the basic units of data, like a number or string, that a
    program manipulates.

  - type:  
    A category of values. The types we have seen so far are integers
    (type <span>`int`</span>), floating-point numbers (type <span>` 
    float `</span>), and strings (type <span>`str`</span>).

  - integer:  
    A type that represents whole numbers.

  - floating-point:  
    A type that represents numbers with fractional parts.

  - string:  
    A type that represents sequences of characters.

  - natural language:  
    Any one of the languages that people speak that evolved naturally.

  - formal language:  
    Any one of the languages that people have designed for specific
    purposes, such as representing mathematical ideas or computer
    programs; all programming languages are formal languages.

  - token:  
    One of the basic elements of the syntactic structure of a program,
    analogous to a word in a natural language.

  - syntax:  
    The rules that govern the structure of a program.

  - parse:  
    To examine a program and analyze the syntactic structure.

  - bug:  
    An error in a program.

  - debugging:  
    The process of finding and correcting bugs.

## Exercises

It is a good idea to read this book in front of a computer so you can
try out the examples as you go.

Whenever you are experimenting with a new feature, you should try to
make mistakes. For example, in the “Hello, world\!” program, what
happens if you leave out one of the quotation marks? What if you leave
out both? What if you spell <span>`print`</span> wrong?

This kind of experiment helps you remember what you read; it also helps
when you are programming, because you get to know what the error
messages mean. It is better to make mistakes now and on purpose than
later and accidentally.

1.  In a print statement, what happens if you leave out one of the
    parentheses, or both?

2.  If you are trying to print a string, what happens if you leave out
    one of the quotation marks, or both?

3.  You can use a minus sign to make a negative number like
    <span>`-2`</span>. What happens if you put a plus sign before a
    number? What about <span>`2++2`</span>?

4.  In math notation, leading zeros are ok, as in <span>`09`</span>.
    What happens if you try this in Python? What about
    <span>`011`</span>?

5.  What happens if you have two values with no operator between them?

Start the Python interpreter and use it as a calculator.

1.  How many seconds are there in 42 minutes 42 seconds?

2.  How many miles are there in 10 kilometers? Hint: there are 1.61
    kilometers in a mile.

3.  If you run a 10 kilometer race in 42 minutes 42 seconds, what is
    your average pace (time per mile in minutes and seconds)? What is
    your average speed in miles per hour?
