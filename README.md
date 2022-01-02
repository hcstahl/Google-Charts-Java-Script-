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
**Line 17- 20:** includes code needed to establish google charts.<br />

**Line 23:** includes all packages needed for every chart and controls to load.<br />

**Line 25-34:** Every chart needs a initilization code **EX: google.charts.setOnLoadCallback()<br />
**It can be named anything but it needs to be established and consistant for each chart. <br />
The name must be referenced back when the code for each chart starts. 

# Query Line 
This is how I was personally able to get the sheet query to work.<br />
Each chart has it's own google sheet to reference the data and is public if given the url.<br />
Every url starts with http://spreadsheets.google.com/tq?key=<br /> 
Then after is each sheets own code which can be found when you visit the google sheet and go to the url above and copy everything after d/<br />

# Chart Template without controls
**Line 41:**  is the charts beginning function which has to match the same name you gave during initilization (Line 25)<br />
**function** Enter name given inside () of set.OnLoadCallback<br />

**Line 43:** is reference to query the data.<br />

var **Then each chart gets it's own name for each query**  this equals the new google.visualization.Query enclosed with each chart's query url from the above section.<br />
Each chart has it's own **name**.send function which sends the data source to a function to be checked for any errors in query. For the first chart this is named queryOne. <br />

**Line 47:** The data source is sent to the function named **checkOne** which takes the parameter **(responseOne)**. This is a name for what the function will recieve in this case it's our queryOne information.<br />

**Line 48 - 50:** The function is handling any errors that can be involved with querying back to the google sheet. The statement must include our parameter name we gave above
**responseOne**. This includes a basic statement if there is an error in query instead of a blank page.<br />

**Line 51 - 62:** Is personalized options for the chart including title options, axis options etc. **This is inside the function name var optionsOne = {**<br />

**Line 62:** }; needed.<br />

**Line 66:** var **Name the data source for each chart** In this case I have seperate date sources for each chart so they will have their own individualized name.<br /> 
This equals **The parameter name we made earlier which went inside our check function** <br />
**responseOne**.getDataTable();<br />
The .getDataTable() is saying our queried data is our data source.<br />

**Line 67:** Here we name our chart and depending on the type of chart this section can look a little different for each section.<br />
it can include **new google.visualization** or **new google.charts** but the . after should be a reference to the type of chart.<br />
Note this should be the correct name from Google Charts and NOT your individual name you give your chart. Make sure it's correct.<br />


**(document.getElementById('first_div'));** This is a reference to the container name that will be put at the end. <br />
('Name')  The name inside needs to be unique to each chart. <br />

**Line 68:** This is the code to draw the actual chart.<br />
This includes the individual chart name you gave above **.draw** and inside the () is your name you gave for the data source and chart options which you personalized above.<br />
chartName.draw(data, options);<br />

**Line 62:**  } ends the code for the chart.<br />

# Chart Template with Controls ***Referencing Chart 9 starting in line 236***<br />
 **Line 236 -249:** is the same template as before.<br />
 
 **Line 250:** starts the difference in code for the chart template. <br />
 We create a variable to hold the dashboard and name the variable and the id div uniquely to the chart.<br />
 
 **Line 254- 261:** This is the control button in the chart we are creating and there are options to customize the type of button we want in the chart.<br />
 
 The  'controlType': 'CategoryFilter'is **not a unique name we give it**. Google Charts has different filter types to choose from and you put the associated name.<br />
 The 'containerId': 'piefilter_div', is a unique name we give for the chart and acess later.<br />
 
 'ui': {'allowNone':false,<br />
     'allowMultiple':false} is a customization to make the chart always choose a default option on the button so the chart doesn't look weird. <br />
  I have also selected to only allow one option in the drop down.<br />
    
'filterColumnIndex': 2, is saying the drop down menu will choose between the categories in column two in your google chart.<br />

**Line 265-285:** This includes the actual chart customization and options.<br />

**Line 287:** You have to bind your dashboard, slider and actual chart every time and this uses the unique names you give in the code.<br />

Below is the line number to reference back to each var creation<br />
piedashboard.bind(pieRangeSlider, chartEight);<br />
***Line 251,(Line 255, Line 265)***<br />
  
**Line 289:** The code which will draw the chart. <br />
This only includes the data and not options because the chart options are inside the var chartEight.<br />

**Line 292:** The required  } to end the chart making. <br />
  
  # End of chart
**Line 389:** Includes indication of ending the chart making process. <br />

**Line 396:** Starts code for HTML customization with the required google chart container inside. I included the google chart container inside HTML to help format.<br />
 
 **The required code for each chart to show must include:**<br />
<div id="div container name you gave the chart" style="width: 800px; height: 500px;"></div> <br />

 **If chart had controls** ***Referencing chart 8 in line 236.***<br />
The div id name you gave the control. Note this is the name in div id, and NOT the name you gave the var.<br />
It's helpful to keep the _div end at the end of the name to keep track.<br />

<div id="piedashboard_div"><br />
In this example we named the control "piedashboard_div" in line 252 inside the document.getElementById().<br />

Next we have to include each div for the control this is under the comment<br />
 <!--Divs that will hold each control and chart--> <br />
 <div id="piefilter_div"></div> piefilter_div is the div name we gave in line 257<br />
 <div id="piechart_div" style="width: 800px; height: 500px;"></div> piechart_div is the div name we gave in line 267. <br />

Note that every important part has <div which has indicator this is required for Google Charts.<br />

