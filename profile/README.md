# ATONEN SEQUENTIA
Open-Source Sicentific Mathematical And Computational Studies Project

Atonen Sequentia is a mathematical number sequence that has been around for a while,\
which had never been named anything, but now by [Victor Kolis](https://github.com/victorkolis) as The Atone Sequence (Sequência Átona, PT [🇧🇷]).

This sequence contains the numbers: `[1, 3, 7, 15, 31]`
The mathematical [Gogito Ergo Sum](https://en.wikipedia.org/wiki/Discourse_on_the_Method), or function is:

`(n * 2) + 1`

"I believe this sequence is the Pascal's triangle outlier that sits in both sides of it. The Atone Triangles" - Victor Kolis
<pre>
1   1   1   1   1   1   1
  1   1   1   1   1   1
    1   1   2   1   1
      1   3   3   1
</pre>

## The name origin
The numbers in the sequence themselves, cannot represent much at first in the decimal layer. However,
in the binary form each number represents a line in the (triangle) sequence.
"Since all the numbers have the binary `'1'` in common I decided to name it Atonen Sequentia, which means the sequence of ones" - Victor Kolis

## Binary to Decimal conversion
binary -> decimal

1 -> 1\
11 -> 3\
111 -> 7\
1111 -> 15\
11111 -> 31

## A Python code representation of that sequence
```python
# Author: Victor Kolis
# Date: 2022-11-19
# Purpose: Generate the Atone Sequence

def atonen(amount=5):
    atonen_sequence = []
    for i in range(amount):
        try:
            atonen_sequence += [int((i+1) * '1', 2)]
        except OverflowError as e:
            raise e('This value cannot be processed')
    return atonen_sequence
```
