# UFOs

Module 11: UFO Sightings with JavaScript

## Overview of the project

In this week, the student helped Dana, a data journalist, to write a HTML page focused on UFOs. Dana wanted to include several items in the same page; an image header with a title, an article, a table with information about UFOs that were seen and easy to use filters for the table.

The table shows the date, city, state, country, UFO shape, duration and comments. The user should be able to use the dynamic table and select one or more filters to narrow down the search on the table. This can be extremely helpful to provide insights on specific cities, dates, forms etc. of the UFOs seen in the sky. 

## Results

### HTML page

  ![ScreenShot]( https://github.com/liviamiyabara/UFOs/blob/main/static/images/screen_shot_webpage.png)


As shown above, the HTML page has a navigation bar on top, followed by a header with an image and title and an article right below it. The interactive part of the website is the filters on the left and the table at the bottom.

The user can search for specific data of the UFOs seen by applying the filters by date, city, state, country and/or UFO shape; there is a sample of the type of data to be typed in for each one of the filter boxes. The person can use only one filter or a combination of the filters to select the data. In the example below, the user filters the search only by the triangle shape: 

  ![ScreenShot]( https://github.com/liviamiyabara/UFOs/blob/main/static/images/screen_shot_triangle.png)


But now, let us assume that the user would like to see the data of UFOs that have a triangle shape and were spotted in California. By typing in triangle in the shape filter and ‘ca’ in the state filter, the user will see the table filtered by those two criteria:

  ![ScreenShot]( https://github.com/liviamiyabara/UFOs/blob/main/static/images/screen_shot_triangle_california.png)


The user can also apply all filters available. In the example below, the two results shown based on the criteria below: 
* date = 1/1/2010 
* city = el cajon
* state = ca
* country = us 
* shape = triangle


  ![ScreenShot]( https://github.com/liviamiyabara/UFOs/blob/main/static/images/screen_shot_allfilters.png)



## Summary

The dynamic table works well when the user wants to apply one of more filters to the search, but one of the limitations is that if the person is doing multiple searches, instead of having a button to clean up all the filters previously applied and start a new search, the user needs to manually remove each filter criteria. For example, if in the first search the person applied the filter for the shape to be ‘light’ and the state to be ‘ny’ and now the user would like to make a second search and only look for a specific date, the user would need to remove the criteria in the ‘shape’ and ‘state’ filters and then add the date, otherwise all the previous filters of the last search would be used again on top of the date selected. 

Another potential draw back that was enhanced in this code is related to case sensitivity. A common use case is that the user would type in the state in capital letters. The script was optimized and despite of the use of the lower or upper case in the filters of HTML page, all letters are converted to lower case to match the format of the data. Below is the snippet of the code, the function toLowerCase() was used:

  ![ScreenShot]( https://github.com/liviamiyabara/UFOs/blob/main/static/images/lowercase.png)


To improve the user experience in the HTML site, a couple of enhancements could be developed:

* Creation of a button to clean up previous filters
* In the case of a search with no results, instead of showing the blank table only with the headers, replace it by a message: “No results found”
* Create a drop-down list for the selection of country, state and shape since there are not too many possible items in the directory 
* For the ‘Enter date’ open a calendar when user clicks on the filter box to enable selection of a specific date based on the calendar view
* Improve the HTML code to be more mobile responsive
