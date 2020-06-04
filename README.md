# Log Parser

A tool for creating csv files that can be inserted into SiriDB from text files.
(only works for files formatted exactly like below)

## What does it do

Original comma-separated (example-file.log):

| date | col1 | col2 | col3 |
| ------ | ------ | ------ | ------ |
| date1 | val-1a | val-2a | val-3a |
| date2 | val-1b | val-2b | val-3b |

Parsed comma-separated (example-file.csv):

| series | timestamp | value |
| ------ | ------ | ------ |
| seriesname-col1 | timestamp1 | val-1a | 
| seriesname-col1 | timestamp2 | val-1b |
| seriesname-col2 | timestamp1 | val-2a | 
| seriesname-col2 | timestamp2 | val-2b |
| seriesname-col3 | timestamp1 | val-3a | 
| seriesname-col3 | timestamp2 | val-3b |


## Getting Started
> For convience place file somewhere where your system can execute it. (known to your PATH environment variable)

Make executable:
``` 
chmod +x ./logparser 
```

Run with:
```
logparser [series-name] [input-file]
```

## Usage 

Run:
```
logparser -h
```

Output:
```
usage: logparser [-h] [-o OUTPUT] series in

A tool for parsing files into CSV files which can be inserted into SiriDB

positional arguments:
  * series              The name of the series. This is used in each line of the result as "SERIES-column,time,value"
  * in                  The input file

optional arguments:
  * -h, --help          show this help message and exit
  * -o , --output       Optionally specify output file name, default=[input file name].csv
```
