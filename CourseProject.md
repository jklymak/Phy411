---
layout: page
title: Course Project
---

The project will involve analyzing temperature data from the
[UVic School Weather Network](http://www.victoriaweather.ca).  Two types of data are to be considered:

<contents>

## Minute-resolution data

[Data/MinuteData.zip](http://web.uvic.ca/~jklymak/Phy411/Data/MinuteData.zip).

Temperature data with one-minute resolution is provided from four schools in the
format of decimal days as discussed below and the second column is
temperature in degrees Celcius.  

Present the data, and characterize it using  techniques discussed in
class.  Obvious things to do are just plot the time series, find
means, PDFs, spectra.  More involved projects will present
correlations between the different stations (thats why you have 4!).
What differences and patterns can you find between the four stations,
and can you explain using your knowledge of the local climate?  

### Handling dates

The data sets start on 1 Jan 2009 a minute after midnight local, or at
08:00 UTC = 733408.333.  

In matlab, these dates can be manipulated with `datestr.m`
and `datenum`.  If `d` is a date, then `datestr(d)` will return a nice
string with the date.  `datenum(2009,1,1)` will return `733408.0`.  For
plotting, its OK do simply plot decimal days (days from 1 Jan 2009 is
useful), or to plot as normal and use `datetick` to (try) and make
date-formated ticks. 

In python, you need to `import datetime`, and then  `datestr2num` will give a similar number:
`datestr2num('2009-01-01')` yields `733408.0`.  Better is to do things as 
```python
d=datetime.date(2012,1,1)
d.toordinal
d.fromordinal(733408)
```
which yields the same.  If you have an array of ordinal times
(i.e. the format you've been given), then 
`plot_date(time,temp,'-')` will make nice xlabels.  I found they don't
fit too well sometimes, so you can play w/ rotating them.  

```python
labels = ax.get_xticklabels() 
for label in labels: 
    label.set_rotation(20)
    label.set_ha('right')
```



## Hour resolution, many stations

[Data/AllHourly.zip](http://web.uvic.ca/~jklymak/Phy411/Data/AllHourly.zip)

One-hour resolution temperature data is taken from the same network of
stations.  Data is on an even time grid, from 2009-01-01 08:00 UTC,
with each row representing a time, and each column a station.  The
first two rows are the longitude (degrees E) and latitude (degrees N)
of each station.  

First, it would be nice to replicate the map on
[http://www.victoriaweather.ca](http://www.victoriaweather.ca).  Use some sort of 2-D interpolation to
put the sparse data on a lon/lat grid, and then plot.  I'll provide a
coastline file to plot the coast on.  Indicate station locations.

[Data/Coast.txt](http://web.uvic.ca/~jklymak/Phy411/Data/Coasts.txt): longitudes followed by latitudes.  Note the islands
etc are missing.  

Then use this data set to look for spatial patterns of variability
between the stations (i.e. calculate the Emperical Orthonormal
Eigienfunctions, or Principal Components).  Plot the strongest modes
of variability and indicate what fraction of the variance they
represent.  Plotting time series of the modal amplitudes is also very
effective way of thinking about the system.

Again, spend a couple of paragraphs explaining the patterns you found,
and indicate if those patterns might have a physical meaning.  Looking
at the seasonality of the amplitudes may help.

### Dealing with geographic data

I'll give you coastlines so you can make nice contours on your maps.
One thing to keep in mind is that 1 degree of latitude is 60 nautical
miles, but 1 degree of longitude is only 60*cos(lat) nautical miles,
so it is useful to scale your x and y axis so the aspect ratio is [1
cos(lat)], where "lat" is some latitude that is on the center of your
plot.  This area is small enough that this approximation will be good
enough - for larger areas you need to choose a projection from a
sphere onto a map (i.e. the "Mercator", "Azimuthal" etc projections).  

## Final Product

I want this written as a report, with a very brief introduction, a
short description of how the data was collected, and then sections
that present your observations.  I'd expect that you will have around
20 plots.  You should describe in the text the most important
observations that you make about your data.  In making these
statements, hopefully you will come up with other analyses to try.

Grading:  
  
   - Complete set of plots: 20%
      - make sure you plot enough of the data to explain it, and that
        you do the "basics".  
   - Well-made and easy to follow plots: 20%
      - proper captions
      - proper labels
      - economical use of space (20 plots, one to a page, where the
        same info could have been in 1 plot will not get you full marks)
   - Complete prose: 20%
      - explains data techniques: not in gory detail, but enough that
        someone who had taken this class will know what you did. 
      - Explains salient features of the data concisely and in such a
        way as to point out to the reader the importance of what they
        are seeing. Don't describe plots line by line, but sumarize
        what the plot tells us
   - Well-organized and -written: 20%
      - Good grammar
      - paragraphs that have a topic sentence, and keep to that
        topic. Stream of consciousness is bad.  Saving the point of
        the paragraph for the last sentence is great for mystery
        novels, terrible for expository writing.  
   - Go the extra mile: 20% 
      - show that you've thought about the data to some extent and
        done an extra analysis or two to dig into it more than just
        applying the basic techniques of the course.  
