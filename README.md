# CT Unemployment

Get unemployment data from DOL in a more usable format.

I think this probably works on Python 3, but I use 2, so I wouldn't know.

## install

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
   >>> unemp>>> unemp.ct.head()
          1982  1983  1984  1985  1986  1987  1988  1989  1990  1991  ...   2008  \
	  Month                                                              ...
	  Jan     6.6   7.1   4.9   4.9   3.9   3.7   2.9   3.1   4.8   5.5  ...    5.0
	  Feb     6.6   6.9   4.8   4.9   3.9   3.7   2.8   3.1   4.9   5.7  ...    5.0
	  Mar     6.7   6.8   4.7   5.0   3.9   3.6   2.8   3.2   5.0   5.9  ...    5.1

	  [...]

	  >>> unemp.us.head(1)
       1982  1983  1984  1985  1986  1987  1988  1989  1990  1991  ...   2008  \
       Month                                                              ...
       Jan     8.6  10.4   8.0   7.3   6.7   6.6   5.7   5.4   5.4   6.4  ...    5.0

       2009  2010  2011  2012  2013  2014  2015  2016  2017
       Month
       Jan     7.8   9.8   9.1   8.3   8.0   6.6   5.7   4.9   4.8

       [1 rows x 36 columns] 

