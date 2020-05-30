
# Case study: word play

This chapter presents the second case study, which involves solving word
puzzles by searching for words that have certain properties. For
example, we’ll find the longest palindromes in English and search for
words whose letters appear in alphabetical order. And I will present
another program development plan: reduction to a previously solved
problem.

## Reading word lists

For the exercises in this chapter we need a list of English words. There
are lots of word lists available on the Web, but the one most suitable
for our purpose is one of the word lists collected and contributed to
the public domain by Grady Ward as part of the Moby lexicon project (see
<http://wikipedia.org/wiki/Moby_Project>). It is a list of 113,809
official crosswords; that is, words that are considered valid in
crossword puzzles and other word games. In the Moby collection, the
filename is <span>`113809of.fic`</span>; you can download a copy, with
the simpler name <span>`words.txt`</span>, from
<http://thinkpython2.com/code/words.txt>.

This file is in plain text, so you can open it with a text editor, but
you can also read it from Python. The built-in function
<span>`open`</span> takes the name of the file as a parameter and
returns a <span>**file object**</span> you can use to read the file.

    >>> fin = open('words.txt')

<span>`fin`</span> is a common name for a file object used for input.
The file object provides several methods for reading, including
<span>`readline`</span>, which reads characters from the file until it
gets to a newline and returns the result as a string:

    >>> fin.readline()
    'aa\n'

The first word in this particular list is “aa”, which is a kind of lava.
The sequence `\n` represents the newline character that separates this
word from the next.

The file object keeps track of where it is in the file, so if you call
<span>`readline`</span> again, you get the next word:

    >>> fin.readline()
    'aah\n'

The next word is “aah”, which is a perfectly legitimate word, so stop
looking at me like that. Or, if it’s the newline character that’s
bothering you, we can get rid of it with the string method
<span>`strip`</span>:

    >>> line = fin.readline()
    >>> word = line.strip()
    >>> word
    'aahed'

You can also use a file object as part of a <span>`for`</span> loop.
This program reads <span>`words.txt`</span> and prints each word, one
per line:

    fin = open('words.txt')
    for line in fin:
        word = line.strip()
        print(word)

## Exercises

There are solutions to these exercises in the next section. You should
at least attempt each one before you read the solutions.

Write a program that reads <span>`words.txt`</span> and prints only the
words with more than 20 characters (not counting whitespace).

In 1939 Ernest Vincent Wright published a 50,000 word novel called
<span>*Gadsby*</span> that does not contain the letter “e”. Since “e” is
the most common letter in English, that’s not easy to do.

In fact, it is difficult to construct a solitary thought without using
that most common symbol. It is slow going at first, but with caution and
hours of training you can gradually gain facility.

All right, I’ll stop now.

Write a function called `has_no_e` that returns <span>`True`</span> if
the given word doesn’t have the letter “e” in it.

Write a program that reads <span>`words.txt`</span> and prints only the
words that have no “e”. Compute the percentage of words in the list that
have no “e”.

Write a function named <span>`avoids`</span> that takes a word and a
string of forbidden letters, and that returns <span>`True`</span> if the
word doesn’t use any of the forbidden letters.

Write a program that prompts the user to enter a string of forbidden
letters and then prints the number of words that don’t contain any of
them. Can you find a combination of 5 forbidden letters that excludes
the smallest number of words?

Write a function named `uses_only` that takes a word and a string of
letters, and that returns <span>`True`</span> if the word contains only
letters in the list. Can you make a sentence using only the letters
<span>`acefhlo`</span>? Other than “Hoe alfalfa”?

Write a function named `uses_all` that takes a word and a string of
required letters, and that returns <span>`True`</span> if the word uses
all the required letters at least once. How many words are there that
use all the vowels <span>`aeiou`</span>? How about
<span>`aeiouy`</span>?

Write a function called `is_abecedarian` that returns
<span>`True`</span> if the letters in a word appear in alphabetical
order (double letters are ok). How many abecedarian words are there?

## Search

All of the exercises in the previous section have something in common;
they can be solved with the search pattern we saw in
Section [9.6](#find). The simplest example is:

    def has_no_e(word):
        for letter in word:
            if letter == 'e':
                return False
        return True

The <span>`for`</span> loop traverses the characters in
<span>`word`</span>. If we find the letter “e”, we can immediately
return <span>`False`</span>; otherwise we have to go to the next letter.
If we exit the loop normally, that means we didn’t find an “e”, so we
return <span>`True`</span>.

You could write this function more concisely using the <span>`in`</span>
operator, but I started with this version because it demonstrates the
logic of the search pattern.

<span>`avoids`</span> is a more general version of `has_no_e` but it has
the same structure:

    def avoids(word, forbidden):
        for letter in word:
            if letter in forbidden:
                return False
        return True

We can return <span>`False`</span> as soon as we find a forbidden
letter; if we get to the end of the loop, we return <span>`True`</span>.

`uses_only` is similar except that the sense of the condition is
reversed:

    def uses_only(word, available):
        for letter in word: 
            if letter not in available:
                return False
        return True

Instead of a list of forbidden letters, we have a list of available
letters. If we find a letter in <span>`word`</span> that is not in
<span>`available`</span>, we can return <span>`False`</span>.

`uses_all` is similar except that we reverse the role of the word and
the string of letters:

    def uses_all(word, required):
        for letter in required: 
            if letter not in word:
                return False
        return True

Instead of traversing the letters in <span>`word`</span>, the loop
traverses the required letters. If any of the required letters do not
appear in the word, we can return <span>`False`</span>.

If you were really thinking like a computer scientist, you would have
recognized that `uses_all` was an instance of a previously solved
problem, and you would have written:

    def uses_all(word, required):
        return uses_only(required, word)

This is an example of a program development plan called <span>
**reduction to a previously solved problem**</span>, which means that
you recognize the problem you are working on as an instance of a solved
problem and apply an existing solution.

## Looping with indices

I wrote the functions in the previous section with <span>`for`</span>
loops because I only needed the characters in the strings; I didn’t have
to do anything with the indices.

For `is_abecedarian` we have to compare adjacent letters, which is a
little tricky with a <span>`for`</span> loop:

    def is_abecedarian(word):
        previous = word[0]
        for c in word:
            if c < previous:
                return False
            previous = c
        return True

An alternative is to use recursion:

    def is_abecedarian(word):
        if len(word) <= 1:
            return True
        if word[0] > word[1]:
            return False
        return is_abecedarian(word[1:])

Another option is to use a <span>`while`</span> loop:

    def is_abecedarian(word):
        i = 0
        while i < len(word)-1:
            if word[i+1] < word[i]:
                return False
            i = i+1
        return True

The loop starts at <span>`i=0`</span> and ends when
<span>`i=len(word)-1`</span>. Each time through the loop, it compares
the \(i\)th character (which you can think of as the current character)
to the \(i+1\)th character (which you can think of as the next).

If the next character is less than (alphabetically before) the current
one, then we have discovered a break in the abecedarian trend, and we
return <span>`False`</span>.

If we get to the end of the loop without finding a fault, then the word
passes the test. To convince yourself that the loop ends correctly,
consider an example like `'flossy'`. The length of the word is 6, so the
last time the loop runs is when <span>`i`</span> is 4, which is the
index of the second-to-last character. On the last iteration, it
compares the second-to-last character to the last, which is what we
want.

Here is a version of `is_palindrome` (see
Exercise [\[palindrome\]](#palindrome)) that uses two indices; one
starts at the beginning and goes up; the other starts at the end and
goes down.

    def is_palindrome(word):
        i = 0
        j = len(word)-1
    
        while i<j:
            if word[i] != word[j]:
                return False
            i = i+1
            j = j-1
    
        return True

Or we could reduce to a previously solved problem and write:

    def is_palindrome(word):
        return is_reverse(word, word)

Using `is_reverse` from Section [\[isreverse\]](#isreverse).

## Debugging

Testing programs is hard. The functions in this chapter are relatively
easy to test because you can check the results by hand. Even so, it is
somewhere between difficult and impossible to choose a set of words that
test for all possible errors.

Taking `has_no_e` as an example, there are two obvious cases to check:
words that have an ‘e’ should return <span>`False`</span>, and words
that don’t should return <span>`True`</span>. You should have no trouble
coming up with one of each.

Within each case, there are some less obvious subcases. Among the words
that have an “e”, you should test words with an “e” at the beginning,
the end, and somewhere in the middle. You should test long words, short
words, and very short words, like the empty string. The empty string is
an example of a <span>**special case**</span>, which is one of the
non-obvious cases where errors often lurk.

In addition to the test cases you generate, you can also test your
program with a word list like <span>`words.txt`</span>. By scanning the
output, you might be able to catch errors, but be careful: you might
catch one kind of error (words that should not be included, but are) and
not another (words that should be included, but aren’t).

In general, testing can help you find bugs, but it is not easy to
generate a good set of test cases, and even if you do, you can’t be sure
your program is correct. According to a legendary computer scientist:

> Program testing can be used to show the presence of bugs, but never to
> show their absence\!
> 
> — Edsger W. Dijkstra

## Glossary

  - file object:  
    A value that represents an open file.

  - reduction to a previously solved problem:  
    A way of solving a problem by expressing it as an instance of a
    previously solved problem.

  - special case:  
    A test case that is atypical or non-obvious (and less likely to be
    handled correctly).

## Exercises

This question is based on a Puzzler that was broadcast on the radio
program <span>*Car Talk*</span>
(<http://www.cartalk.com/content/puzzlers>):

> Give me a word with three consecutive double letters. I’ll give you a
> couple of words that almost qualify, but don’t. For example, the word
> committee, c-o-m-m-i-t-t-e-e. It would be great except for the ‘i’
> that sneaks in there. Or Mississippi: M-i-s-s-i-s-s-i-p-p-i. If you
> could take out those i’s it would work. But there is a word that has
> three consecutive pairs of letters and to the best of my knowledge
> this may be the only word. Of course there are probably 500 more but I
> can only think of one. What is the word?

Write a program to find it. Solution:
<http://thinkpython2.com/code/cartalk1.py>.

Here’s another <span>*Car Talk*</span> Puzzler
(<http://www.cartalk.com/content/puzzlers>):

> “I was driving on the highway the other day and I happened to notice
> my odometer. Like most odometers, it shows six digits, in whole miles
> only. So, if my car had 300,000 miles, for example, I’d see
> 3-0-0-0-0-0.
> 
> “Now, what I saw that day was very interesting. I noticed that the
> last 4 digits were palindromic; that is, they read the same forward as
> backward. For example, 5-4-4-5 is a palindrome, so my odometer could
> have read 3-1-5-4-4-5.
> 
> “One mile later, the last 5 numbers were palindromic. For example, it
> could have read 3-6-5-4-5-6. One mile after that, the middle 4 out of
> 6 numbers were palindromic. And you ready for this? One mile later,
> all 6 were palindromic\!
> 
> “The question is, what was on the odometer when I first looked?”

Write a Python program that tests all the six-digit numbers and prints
any numbers that satisfy these requirements. Solution:
<http://thinkpython2.com/code/cartalk2.py>.

Here’s another <span>*Car Talk*</span> Puzzler you can solve with a
search (<http://www.cartalk.com/content/puzzlers>):

> “Recently I had a visit with my mom and we realized that the two
> digits that make up my age when reversed resulted in her age. For
> example, if she’s 73, I’m 37. We wondered how often this has happened
> over the years but we got sidetracked with other topics and we never
> came up with an answer.
> 
> “When I got home I figured out that the digits of our ages have been
> reversible six times so far. I also figured out that if we’re lucky it
> would happen again in a few years, and if we’re really lucky it would
> happen one more time after that. In other words, it would have
> happened 8 times over all. So the question is, how old am I now?”

Write a Python program that searches for solutions to this Puzzler.
Hint: you might find the string method <span>`zfill`</span> useful.

Solution: <http://thinkpython2.com/code/cartalk3.py>.
