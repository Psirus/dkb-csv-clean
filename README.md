# dkb-csv-clean

The CSV files from the DKB (a German bank) are a mess; this attempts to fix
them.

## What's wrong?

- The dates are [wrong](https://xkcd.com/1179/).
- The encoding is not Unicode. Come on, it's almost 2017.
- The amounts are in German locale. (Dear DKB, have you considered that I
  actually might want parse these files with a computer, not use them as
  bedtime reading material?)
- Their own billings include html markup in the Verwendszweck field. Seriously.

## How do I use it?

    ./dkb-csv-clean input.csv > output.csv

## Prerequisites

Python3 and the [babel library](http://babel.pocoo.org/en/latest/).

Under Ubuntu/Debian:

    sudo apt-get install python3 python3-babel
