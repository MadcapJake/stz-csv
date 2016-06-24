# Stanza CSV Package

Parses CSV files into a Tuple of Tuples

## Install

```sh
git clone https://github.com/MadcapJake/stz-csv.git vendor/csv
stanza vendor/csv/source/csv.stanza -pkg pkgs # only this line is needed
stanza vendor/csv/source/csv.stanza -pkg fast-pkgs -optimize
```
You could also just include `csv.stanza` in your list of source files when you compile.

## Synopsis

```stanza
defpackage foo :
    import core
    import csv

defn main () :
    val csv = CSV("/path/to/file.csv", false, ',')
    val records = parse(csv)

main()
```
