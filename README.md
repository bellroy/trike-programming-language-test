# TrikeApps Programming Challenges

1. Clone (don't fork) this repo and make a branch for your changes.
2. Please complete _all_ of the following problems.
3. We expect to see evidence of good development processes. Write tests, and commit often. Use
   [git bundle](https://git-scm.com/docs/git-bundle) to bundle all your commits together so you can
   send them to us. Do **not** submit a pull request to this repo.
4. Send your bundle through to [jobs@trikeapps.com](mailto:jobs@trikeapps.com).

## Problem 1 - String Munging

Write a `StringDemystifier` class that - when its `demystify` function is called - applies the
following rules (in order of precedence, and until they can no longer be applied) to any string it
is given in its constructor:

* If a character has the same character to its left and right, it should be replaced with that other
  character (i.e. AWA becomes AAA) unless the surrounding character is a space
* Any sequence of six characters should be replaced with a single character, i.e. AAAAAA becomes A
* Any instance of the exclamation mark (!) character causes the string to be reversed, and the
  exclamation mark character removed

Commit each step of your development process. When you're done, try running it on the following
string and see what result you get (hint: you'll know when you've done it right):

```
!YTIRCO!IQIIQIDEMGMMIM FO YMJMMSM!RA !EGEEJEHT ROEOOSOF PAEJEEBEL TN!AIKIITIG ENVNNMNO ,GQGGCGN!ILEKIZIISIRT A RJRRDROF PETOTTJTS LLZLLEL!AMSXSSMS ENODOOSO
```

## Problem 2 - Number Wrangling

There's a competition on the internet. Every night at midnight they publish a sequence of integers
and a desired result. The first person to enter an equation that only uses addition / subtraction /
multiplication / division, uses all of the integers and achieves the desired result wins $1,000.
We want to win.

Write a `EquationGuesser` class that in its constructor takes as one argument an sequence of
integers (we'll call these the operands), and as another argument another integer (we'll call this
the desired result). Your class should provide a method `guess` that takes an integer (`guesses`).
When `guess` is called, your class should attempt to output string representations of equations,
their result, and the difference between that result and the desired result `guesses` times.
Finally, the class should output the number of guesses and what the best guess was.

e.g.

```
> equation_guesser = EquationGuesser.new([1, 2, 3, 4], 24)
> equation_guesser.guesses(3)
1 + 2 + 3 + 4 = 10 (-14)
1 * 2 * 3 * 4 = 24 (0)
Guesses: 2 Best Guess: 1 * 2 * 3 * 4 = 24 (0)
```

If the equation is exactly equal to the desired result, the program should exit. For the sake of
this exercise, you only need consider positive integers (i.e. use integer division). Your equations
should honour standard operator precedence (e.g. multiplication before addition) and do not need
to consider bracketed subexpressions (e.g. `(1 + 2) * (3 + 4)`).

For extra points:
* make it so your `guess` method can process up to 10 operands and 1000 guesses without taking more
  than 5 seconds
* do at least one thing that reduces the average number of guesses your class needs to make for each
  call to `guess` before it is able to achieve the desired result (given that it is possible to
  achieve the desired result with the operands)

## Problem 3 - Expanding Your Horizons

We love programming at Trike. Although we primarily do a lot of
[Ruby](https://www.ruby-lang.org/en/) programming, we love to explore what benefits and tradeoffs
that other languages have to offer in solving our day to day problems.

Here is the challenge. Either:

1. Take a list of integers on standard input, one per line, and return them in reverse order on
   standard output, or;
2. Take a string on standard input and return the string reversed on standard output.

Conditions:

1. You must do this in a language that you have not programmed in before.
2. You must not use a library that provides a `reverse` method or function.

Here are some of the languages (in no particular order) that we use at Trike on the side to help us
solve problems.

* [Rust](https://www.rust-lang.org/en-US/)
* [Swift](https://swift.org)
* [Haskell](http://haskell.org)
* [C](https://en.wikipedia.org/wiki/C_(programming_language))
* [Elm](http://elm-lang.org)
* [Elixir](http://elixir-lang.org)

Feel free to use one of these languages, or choose your own, there are
[a lot of programming languages](https://en.wikipedia.org/wiki/List_of_programming_languages) to
choose from :)
