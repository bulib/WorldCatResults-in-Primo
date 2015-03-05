# WorldCatResults-in-Primo

###html and javascript for a custom tile in the Ex Libris Primo UI to include WorldCat Results in the brief results display.


## Purpose:
To address the possibility that a 'known item' search in Primo did not return the desired result, BU Libraries decided to add a custom tile to the Primo UI that would allow the user to include the results for the same search executed in OCLC WorldCat. The current design captures the search string when the page loads and executes a WorldCat search using the OCLC WorldCat Search API. This happens after the Primo results have been loaded, but the results are not displayed by default, so the user generally doesn't notice any response delay in the initial display of Primo results. Visibility of the WorldCat results is toggled by checking an "Include results from WorldCat" box in the "Expand My Results" section of the brief results page.

## Dependencies
Use of the WorldCat Search API requires a key. Information about the API including instructions for requesting a key can be found at:
[http://www.oclc.org/developer/services/worldcat-search-api](http://www.oclc.org/developer/services/worldcat-search-api)

In this case, the search is executed using OCLC's OpenSearch protocol. The result set is returned as an RSS feed. This script uses the jquery.zrssfeed.js library available from: 

[http://www.zazar.net/developers/jquery/zrssfeed/](http://www.zazar.net/developers/jquery/zrssfeed/)

## Installing

1. The javascript is contained in the html file 'WCL.html'
2. Edit the file to add your WorldCat Search API key.
3. Edit the file to reflect the location of the zrssfeed library.
4. Edit the css to reflect desired styling for the results page.
5. The URL that is created to allow the user to display the desired result in WorldCat links to www.worldcat.org. If you want the result to be displayed in an instance of WorldCat Local, you can modify the URL to point to the desired site.
6. Follow the procedures outlined in the Ex Libris Primo *Back Office Guide* for configuring a custom layout. In the December 2014 version of the guide, the section for configuring custom layouts begins on page 221.


## To Do...
1.  Boston University Libraries allows our users to request books held by other libraries in the Boston Library Consortium through our instance of WorldCat Local. Ultimately, we want to make it possible to request the resource from within the Primo interface rather than directing the user to WorldCat. 
2.  The script works as long as the Primo search returns at least one result. If no results are returned, a different page is loaded. We want to explore adding the code to be displayed on the "no results" page as well.



*developer: j ammerman / date: march 2015
