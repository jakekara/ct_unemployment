# CT Unemployment

Get unemployment data from DOL in a more usable format.

I think this probably works on Python 3, but I use 2, so I wouldn't know.

## install from github

    pip install git+git://github.com/jakekara/ct_unemployment.git


## usage in python script

   from ct_unemployment import unemployment as unemp 

## DataFrames

   ### unemp.ct

       Unmodified table from CT DOL site. Cols are years, rows are months 
   
   ### unemp.us

       Unmodified table from CT DOL site. Cols are years, rows are months 

   ### unemp.ct_chron

       Corresponding table reformatted with a month col and rate col in
       chronological order.

   ### unemp.us_chron

       Corresponding table reformatted with a month col and rate col in
       chronological order.
       
   ### unemp.both

       us_chron and ct_chron joined with rate columns renamed "CT" and "US"

## Demo

	$ python

	>>> from ct_unemployment import unemployment as unemp
	>>> unemp.ct.head(1)
       1982  1983  1984  1985  1986  1987  1988  1989  1990  1991  ...   2008  \
       Month                                                              ...
       Jan     6.6   7.1   4.9   4.9   3.9   3.7   2.9   3.1   4.8   5.5  ...    5.0

       2009  2010  2011  2012  2013  2014  2015  2016  2017
       Month
       Jan     7.0   9.0   9.2   8.2   8.1   7.1   6.1   5.5   4.5

       [1 rows x 36 columns]
       >>> unemp.both.to_csv("~/both.csv")
       >>> exit()
       $ head ~/both.csv
       month,CT,US
       1982-01-01,6.6,8.6
       1982-02-01,6.6,8.9
       1982-03-01,6.7,9.0
       1982-04-01,6.8,9.3
       1982-05-01,6.8,9.4
       1982-06-01,6.9,9.6
       1982-07-01,6.9,9.8
       1982-08-01,6.9,9.8
       1982-09-01,7.0,10.1

