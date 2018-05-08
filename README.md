This fork is a slight adaptation of work by Zheyuan Yu to generate output in a comma separated value format.

Original Repository: https://github.com/jerry2yu/ngrams

## How to use it:

1. Download and save the source code in a directory
2. Execute `make` in that directory

## Using from Command Line

Get word Ngrams

```bash
./ngrams --type=word --n=3 --in= sample.txt > sample.csv
```

Get character Ngrams
```
./ngrams --type=character -n=3 --in= sample.txt > sample.csv
```


Get byte Ngrams e.g., getting ngrams from binary file.

```
./ngrams --type=byte -n=3 --in= sample.txt > sample.csv
```

## Using from `R`

+ Unless you installed `ngrams` in `/bin` _(Which I'm not sure I'd recommend)_ the path for the `ngrams` command needs to be defined relative to the current `R` working directory or as an absolute path
+ Similarly, the `--in` and `stdout` paths also need to be defined relative to the current `R` working directory or as an absolute path


```r
system2(command = "ngrams/ngrams",args = "--type=word --n = 3 --in sample.txt", stdout = "sample.csv")
```