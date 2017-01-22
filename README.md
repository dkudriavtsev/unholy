

## UNHOLY

Compile Ruby to Python bytecode. And,
in addition, translate that bytecode
back to Python source code using
Decompyle (included.)

Requires Ruby 1.9 and Python 2.5.


## INSTALL

First, install decompyle:

    > cd decompyle
    > python setup.py build
    # python setup.py install

Then, in the main directory, use the tools.

---

To compile Ruby to a .pyc:

    > bin/unholy test.rb
    > PYTHONPATH=python python test.rb.pyc
  
---

To translate to Python:

    > decompyle test.rb.pyc > test.py

---

And, to view the disassembled bytes:
  
    > bin/py-dis test.rb.pyc

Thanks to Ned Batchelder for his
rather juicy posts on dissecting
Python bytecode. It is only too
bad that a Rubyist got a hold
of them. :(

## POTION

Now, imagine if Ruby and Python were to combine into something new.  Let's call it "potion":

    > potion test.py
    HELLO FROM PYTHON
    > potion test.rb
    KONNICHIWA FROM RUBY

You know, it's crazy that Python
and Ruby fans find themselves
battling so much. While syntax
is different, this exercise
proves how close they are to
each other! And, yes, I like
Ruby's syntax and can think much
better in it, but it would be
nice to share libs with Python
folk and not have to wait forever
for a mythical VM that runs all
possible languages.
