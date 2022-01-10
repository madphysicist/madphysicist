# Introduction

Hi, I am algorithm engineer with a background in physics and signal processing.
Coding is a hobby of mine. I like to contribute fixes and improvemens to
projects that I use frequently, such as the
[numpy](https://github.com/numpy/numpy) /
[scipy](https://github.com/scipy/scipy) /
[matplotlib](https://github.com/matplotlib/matplotlib) stack. My
ongoing pet project is [scikit-guess](https://github.com/madphysicist/scikit-guess).
It's a collection of linearized optimization routines that started as a
translation and python implementation of Jean Jacquelin's paper, which you can
find in the repo.


# My Repos

Here is a selection of repos with a note about each one:

- [scikit-guess](https://github.com/madphysicist/scikit-guess)
  [[PyPi](https://pypi.org/project/scikit-guess/)]
  [[RTD](https://scikit-guess.readthedocs.io/en/latest/)]
  See above.
- [haggis](https://github.com/madphysicist/haggis)
  [[PyPi](https://pypi.org/project/haggis/)]
  [[RTD](https://haggis.readthedocs.io/en/latest/)]
  Originally made to support [imprint](https://github.com/madphysicist/imprint),
  this library has a whole bunch of routines I find useful on a regular basis
  for all kinds of projects.
- [imprint](https://github.com/madphysicist/imprint)
  [[PyPi](https://pypi.org/project/imprint/)]
  [[RTD](https://imprint.readthedocs.io/en/latest/)]
  A publication system for generating MS Word documents I made while at the
  Detector Characterization Lab at NASA GSFC. Only really useful in the case
  where you want to generate the same document over and over, but with
  different data.
- [is_integer_ufunc](https://github.com/madphysicist/is_integer_ufunc) is a
  foray into the C code of numpy. It contains bit twiddling operations for
  determining whether an IEEE754 float (any format) is an integer or not. It's
  becoming pretty clear that a ufunc is inadequate for the purpose, so I am
  concocting two alternatives to the pure ufunc:

  - A numpy function that labels each element with whether it can be stored in
    an integer of specified bit-width.
  - The number of bits required to store the integer stored in a float, with
    negative numbers indicating a fractional portion.

  See the [Stack Exchange](#StackExchange) section below for the inspiration.
- [puzzle-solvers](https://github.com/madphysicist/puzzle-solvers)
  [[PyPi](https://pypi.org/project/puzzle-solvers/)]
  [[RTD](https://puzzle-solvers.readthedocs.io/en/latest/)]
  Another Stack Overflow-inspired package. This one is currently just a system
  for solving a zebra puzzle, which I really enjoyed writing. See the
  [Stack Exchange](#StackExchange) section for the inspiration.
- [libpluck](https://github.com/madphysicist/libpluck) never got past the
  README phase, as it's more of an April fool's library than anything.
  Developed in conjunction with Ventsy Velev while working on GOES-R together.
  An idea that never made it even this far was a library for generating unit
  tests with gramatically meaningful, fancy sounding names, all of which pass
  after much output and fanfare.
- [BOFH](https://github.com/madphysicist/BOFH) is a small Java program that
  depends on [JTools](https://github.com/madphysicist/JTools), and displays a
  GUI for the excuse generator from Simon Travaglia's BOFH series of articles.
- [JTools](https://github.com/madphysicist/JTools) is a small library of Java
  utilities from many years ago when I coded in Java. It's so old that it was
  written before Java 7 even existed. There were no streams back in those
  days. The library has all sorts of tools for I/O, process management,
  GUI elements, XML parsing and the like.
- [JTools-extras](https://github.com/madphysicist/JTools-extras) is an
  extension of [JTools](https://github.com/madphysicist/JTools) that contains
  utilities with external dependencies (like TestNG).


# Stack Exchange

I've been on Stack Exchange for a while now, and some of the open source work
I've done is a direct consequence of my contributions there. The list below
maps some of my PRs to the questions that they originated with. In most cases,
I added an answer to the question referencing the contribution.

Part of the reason for putting this section here is that my
[SE profile](https://stackoverflow.com/users/2988730/mad-physicist) is limited
to 3000 characters, so I gave up on trying to squeeze it in there.

- [scikit-guess](https://scikit-guess.readthedocs.io/) entirely came about from
  my work with a paper by Jean Jacquelin. It was later supplemented by some
  [Stack Overflow](https://stackoverflow.com/) and
  [Math Stack Exchange](https://math.stackexchange.com/) questions:
  - N-dimensional spheres:
    - https://stackoverflow.com/q/68302951/2988730
    - https://stackoverflow.com/q/26574945/2988730
    - https://stackoverflow.com/q/10344119/2988730
    - https://stackoverflow.com/q/18934805/2988730
    - https://math.stackexchange.com/q/820815/295281
    - https://math.stackexchange.com/q/214661/295281
    - https://math.stackexchange.com/q/2898295/295281
  - N-dimensional Gaussians:
    - https://stackoverflow.com/q/25720600/2988730
    - https://stackoverflow.com/q/27539933/2988730
    - https://stackoverflow.com/q/27230824/2988730
    - https://stackoverflow.com/q/67538941/2988730
  - Exponentials:
    - https://stackoverflow.com/q/53273033/2988730
    - https://stackoverflow.com/q/3433486/2988730
- [`matplotlib.ticker.PrecentFormatter`](https://matplotlib.org/stable/api/ticker_api.html#matplotlib.ticker.PercentFormatter)
  added to [matplotlib](https://matplotlib.org/) in
  [PR #6251](https://github.com/matplotlib/matplotlib/pull/6251) in response to
  these two posts:
  - Y-axis: https://stackoverflow.com/a/36319915/2988730
  - X-axis: https://stackoverflow.com/a/36320013/2988730
- [`scipy.stats.iqr`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.iqr.html)
  added to [scipy](https://scipy.org/) in
  [PR #5805](https://github.com/scipy/scipy/pull/5808) partly in response to
  https://stackoverflow.com/a/38620147/2988730
- `count` parameter added to [`numpy.unpackbits`](https://numpy.org/doc/stable/reference/generated/numpy.unpackbits.html)
  to make it invertible with respect to [`numpy.packbits`](https://numpy.org/doc/stable/reference/generated/numpy.packbits.html)
  in [PR #10855](https://github.com/numpy/numpy/pull/10855) to improve this
  answer: https://stackoverflow.com/q/5602155/2988730
- Relaxed contiguity requirements for
  [`numpy.ndarray.view`](https://numpy.org/doc/stable/reference/generated/numpy.ndarray.view.html)
  (see note about version 1.23.0) in [PR #20722](https://github.com/numpy/numpy/pull/20722),
  which allows for `np.char.slice_` to exist in [PR #20694](https://github.com/numpy/numpy/pull/20694):
  - https://stackoverflow.com/q/70547027/2988730
  - https://stackoverflow.com/q/53296394/2988730
  - https://stackoverflow.com/q/39042214/2988730
  - https://stackoverflow.com/q/40976714/2988730
  - https://stackoverflow.com/q/64981711/2988730
  - https://stackoverflow.com/q/31387047/2988730
  - https://stackoverflow.com/q/69856133/2988730
- [`haggis.numbers.english`](https://haggis.readthedocs.io/en/latest/api.html#haggis.numbers.english) implements the usage rules
  from this answer on English Language and Usage SE: https://english.stackexchange.com/a/111837/207127.
- My first attempt at a ufunc:
  [is_integer_ufunc](https://github.com/madphysicist/isint_ufunc). This still
  needs work before it's ready for review by the numpy community, but the
  question crops up fairly frequently:
  - https://stackoverflow.com/q/35042128/2988730
  - https://stackoverflow.com/q/64044147/2988730
  - https://stackoverflow.com/q/52094533/2988730
  - https://stackoverflow.com/q/6209008/2988730
  - https://stackoverflow.com/q/21583758/2988730
  - https://stackoverflow.com/q/36505879/2988730

Stuff that might get turned into PRs one day:

  - Estimating the size of an index in numpy: https://stackoverflow.com/a/65857268/2988730
  - `np.atleast_nd` function (numpy): https://stackoverflow.com/q/19636487/2988730
  - Reverse winding of paths in matplotlib: https://stackoverflow.com/q/68275413/2988730
  - Weighted partitioning in numpy: https://stackoverflow.com/q/20601872/2988730
