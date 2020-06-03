# timeseries-logparser

A tool for creating csv files that can be inserted into timeseries databases (specifically SiriDB) from text files.

## getting started
> For convience place file where your system can execute it. (known to your PATH environment variable)

Make executable:
``` 
chmod +x ./logparser 
```

Run with:
```
logparser
```

## usage 
usage: logparser [-h] [-o OUTPUT] series in

A command line tool for parsing comma separated log into a SiriDB understandable CV file

positional arguments:
  series                The name of the series. This is used in each line of the result as "SERIES,col-name,time,value"
  in                    The input file

optional arguments:
  -h, --help            show this help message and exit
  -o OUTPUT, --output OUTPUT
                        Optionally specify output file name, default=[input file name].csv
