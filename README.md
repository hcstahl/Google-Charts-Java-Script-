# Data Visualization with Google Charts https://sites.google.com/view/hcstahlgc/home 
Data modeled by querying from Google Sheets and using Java Script to create inveractive charts.
 ### Table of Contents

  
# Languages
Java Script
HTML
# Launch
Visit the link above or copy the code in notepad save as .html and bring up in browser.

# Formatting  Line 1-14 
Imported fonts from Google by putting witin style tags.
Code within these lines is only for establishing html stlyle.

# Start Up 17-34
**Line 17- 20:** includes code needed to establish google charts.
**Line 23:** includes all packages needed for every chart and controls to load.
**Line 25-34:** Every chart needs a initilization code **EX: google.charts.setOnLoadCallback()
**It can be named anything but it needs to be established and consistant for each chart. The name must be referenced back when the code for each chart starts. 

# Query Line 
This is how I was personally able to get the sheet query to work.
Each chart has it's own google sheet to reference the data and is public if given the url.
Every url starts with http://spreadsheets.google.com/tq?key= 
Then after is each sheets own code which can be found when you visit the google sheet and go to the url above and copy everything after 
d/
# Chart Template without controls
**Line 41:**  is the charts beginning function which has to match the same name you gave during initilization (Line 25)
**function** Enter name given inside () of set.OnLoadCallback

**Line 43:** is reference to query the data.

var **Then each chart gets it's own name for each query**  this equals the new google.visualization.Query enclosed with each chart's query url from the above section.
Each chart has it's own **name**.send function which sends the data source to a function to be checked for any errors in query. For the first chart this is named queryOne. 

**Line 47:** The data source is sent to the function named **checkOne** which takes the parameter **(responseOne)**. This is a name for what the function will recieve in this case it's our queryOne information.

**Line 48 - 50:** The function is handling any errors that can be involved with querying back to the google sheet. The statement must include our parameter name we gave above
**responseOne**. This includes a basic statement if there is an error in query instead of a blank page.

**Line 51 - 62:** Is personalized options for the chart including title options, axis options etc. **This is inside the function name var optionsOne = {**
**Line 62:** }; needed.
**Line 66:** var **Name the data source for each chart** In this case I have seperate date sources for each chart so they will have their own individualized name. 
This equals **The parameter name we made earlier which went inside our check function** 
**responseOne**.getDataTable();
The .getDataTable() is saying our queried data is our data source.

**Line 67:** Here we name our chart and depending on the type of chart this section can look a little different for each section.
it can include **new google.visualization** or **new google.charts** but the . after should be a reference to the type of chart.
Note this should be the correct name from Google Charts and NOT your individual name you give your chart. Make sure it's correct.


**(document.getElementById('first_div'));** This is a reference to the container name that will be put at the end. 
('Name')  The name inside needs to be unique to each chart. 

**Line 68:** This is the code to draw the actual chart.
This includes the individual chart name you gave above **.draw** and inside the () is your name you gave for the data source and chart options which you personalized above.
chartName.draw(data, options);

**Line 62:**  } ends the code for the chart.

# Chart Template with Controls ***Referencing Chart 9 starting in line 236***
 **Line 236 -249:** is the same template as before.
 **Line 250:** starts the difference in code for the chart template. 
 We create a variable to hold the dashboard and name the variable and the id div uniquely to the chart.
 **Line 254- 261:** This is the control button in the chart we are creating and there are options to customize the type of button we want in the chart.
 
 The  'controlType': 'CategoryFilter'is **not a unique name we give it**. Google Charts has different filter types to choose from and you put the associated name.
 The 'containerId': 'piefilter_div', is a unique name we give for the chart and acess later.
 
 'ui': {'allowNone':false,
		  'allowMultiple':false} is a customization to make the chart always choose a default option on the button so the chart doesn't look weird. 
    I have also selected to only allow one option in the drop down. 
    
'filterColumnIndex': 2, is saying the drop down menu will choose between the categories in column two in your google chart.
**Line 265-285:** This includes the actual chart customization and options.
**Line 287:** You have to bind your dashboard, slider and actual chart every time and this uses the unique names you give in the code.

Below is the line number to reference back to each var creation
piedashboard.bind(pieRangeSlider, chartEight);
***Line 251,(Line 255, Line 265)***
  
**Line 289:** The code which will draw the chart. 
This only includes the data and not options because the chart options are inside the var chartEight.
**Line 292:** The required  } to end the chart making. 
  
  # End of chart
**Line 389:** Includes indication of ending the chart making process. 
**Line 396:** Starts code for HTML customization with the required google chart container inside. I included the google chart container inside HTML to help format.
 
 **The required code for each chart to show must include:**
<div id="div container name you gave the chart" style="width: 800px; height: 500px;"></div> 

 **If chart had controls** ***Referencing chart 8 in line 236.***
The div id name you gave the control. Note this is the name in div id, and NOT the name you gave the var.
It's helpful to keep the _div end at the end of the name to keep track.

<div id="piedashboard_div">
In this example we named the control "piedashboard_div" in line 252 inside the document.getElementById().

Next we have to include each div for the control this is under the comment
 <!--Divs that will hold each control and chart--> 
 <div id="piefilter_div"></div> piefilter_div is the div name we gave in line 257
 <div id="piechart_div" style="width: 800px; height: 500px;"></div> piechart_div is the div name we gave in line 267. 

Note that every important part has <div which has indicator this is required for Google Charts.

