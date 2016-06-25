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

## Roadmap

* Auto-detect delimiter - try a set of common delimiters and pick the best option
* Step function - do something to each record as it's parsed.
* Filter function - conditionally remove records as they are parsed
* Type conversion - convert to appropriate Stanza type
* Comments - specify a character indicating a comment to skip in the parsing
* Linting - provide CSV standard and ambiguity errors/warnings
* To CSV - convert collections to CSV
