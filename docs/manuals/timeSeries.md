[__<--__ Return to home page](index.html)

## Multiple timeseries data

### Description
A __timeseries__ represents an  ordered collection of values of an event (or item) over time. 
A __multiple timeseries__ represents the collection of multiple timeseries gathered from multiple items over a particular duration.
Depending on the values stored in a series, a multiple timeseries can be broadly classified into two types: 
- _binary multiple timeseries_ and 
- _(non-binary) multiple timeseries_. 

### Binary Multiple Timeseries
#### About
A binary multiple time series represents the binary data of multiple items split into temporal windows.
An example of this series is shown below. 

| windowID | binary sequences                    |
|----------|-------------------------------------|
| 1        | (a,1) (a,3) (b,2) (b,3) (c,2) (c,3) |
| 2        | (a,1) (b,1) (b,2) (b,3) (c,1)       |
| 3        | (a,1) (a,2) (b,1) (b,3) (c,2)       |
| 4        | (a,1) (b,1) (b,2) (c,3)             |
| 5        | (a,1) (a,3) (b,3) (c,2) (c,2)       |
| 6        | (a,1) (a,2) (b,2) (b,3)             |
 
#### Rules to create a binary multiple time series.
1. First column must contain an integer representing an windowID. 
2. Remaining columns must contain items and their timestamps within braces.
3. In the braces, starting from left hand side, the first word/letter represents an item and the other word/letter represents an timestamp.
3. Columns are seperated with a seperator. 
4. '_Tab space_' is the default seperator.   However, transactional databases can be constructed using other seperators, such as comma and space.

#### Format of a binary multiple time series
 
    windowID<sep>(item,timestamp)<sep>(item,timestamp)<sep>...<sep>(item, timestamp)

#### An example

    1 (a,1) (a,3) (b,2) (b,3) (c,2) (c,3)
    2 (a,1) (b,1) (b,2) (b,3) (c,1)
    3 (a,1) (a,2) (b,1) (b,3) (c,2)
    4 (a,1) (b,1) (b,2) (c,3)
    5 (a,1) (a,3) (b,3) (c,2) (c,2)
    6 (a,1) (a,2) (b,2) (b,3)
 
### Non-binary Multiple Timeseries
 __Coming soon...__