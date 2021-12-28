# Google-Charts-Java-Script-
<html>
  <head>
<style>
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@100&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Raleway:wght@700&display=swap');
</style>

<style>
  <title>Hailey Stahl</title>

    
    </style>
  </head>
  <body>


 <html>
  <head>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">

      // Load Charts and the corechart package.
      google.charts.load('current', {'packages':['corechart','line','table','bar','geochart','controls']});
     
 <!--load call for all of charts-->
	google.charts.setOnLoadCallback(initialize);
	google.charts.setOnLoadCallback(initialize2);
	google.charts.setOnLoadCallback(initialize3);
	google.charts.setOnLoadCallback(initialize4)
	google.charts.setOnLoadCallback(initialize6);
	google.charts.setOnLoadCallback(initialize7);
	google.charts.setOnLoadCallback(initialize8);
	google.charts.setOnLoadCallback(initialize9);
	google.charts.setOnLoadCallback(initialize10);
     	
     	
     
     
     
 <!--chart1-->
 	function initialize() {
        // The URL of the spreadsheet to source data from.
        var queryOne = new google.visualization.Query('http://spreadsheets.google.com/tq?key=1khxrdEzOrQc0xkcO1Pajei5aB_Tqmkdeu-UYeqJ62Dw');
        queryOne.send(checkOne);
      }

      function checkOne(responseOne) {
        if (responseOne.isError()) {
          alert('Error in query');
        }
	 var optionsOne = {
	title:'Number of Endangered Species',
	titlePosition:'in',
	axisTitlesPosition: 'none',
	titleTextStyle:{color: 'gray',fontName: 'Raleway', fontSize:24,bold:true},
                       chartArea:{left:70,top:40,width:'70%',height:'90%'},
legend: {position: 'right', textStyle: {color: 'gray', fontSize: 20,fontName:'Raleway'}},
colors: ['#DB7093','#708090','#D2B48C'],
hAxis: {gridlines: {color: 'transparent'},baselineColor:'white',textStyle:{ fontName: 'Raleway',fontSize: 24,bold:false,color: 'gray'},textPosition:'in'},
 vAxis: {gridlines: {color: 'transparent'},format:'',ticks: [2010,2015,2020],textStyle:{ fontName: 'Raleway',fontSize: 24,bold:false,color: 'gray'},textPosition:'out'}

};
        


	var dataOne = responseOne.getDataTable();
	var chartOne = new google.visualization.BarChart(document.getElementById('first_div'));
        chartOne.draw(dataOne, optionsOne);
     
 }

     
 <!--chart2-->
function initialize2() {
        // The URL of the spreadsheet to source data from.
        var queryTwo = new google.visualization.Query('http://spreadsheets.google.com/tq?key=1fHl7KDKmM0AVLilxZaCfCo7bzrguHrrS4HeYTRkI0tc');
        queryTwo.send(checkTwo);
      }

      function checkTwo(responseTwo) {
        if (responseTwo.isError()) {
          alert('Error in query');
        }
	 var optionsTwo = {title:'Internet Usage in Croatia',
	 subtitle: 'Croatia',
         titleTextStyle:{color: 'gray',fontName: 'Raleway', fontSize:24,bold:true},
	  legend: {position: 'right', textStyle: {color: 'gray', fontSize: 20,fontName:'Raleway'}},
		pieSliceTextStyle: {color: 'white', fontSize: 28,fontName:'Raleway',bold:true},
                       chartArea:{left:50,top:30,width:'75%',height:'75%'},
			colors: ['#D2B48C','#F6ECE3']};
        


	var dataTwo = responseTwo.getDataTable();
	var chartTwo = new google.visualization.PieChart(document.getElementById('second_div'));
        chartTwo.draw(dataTwo, optionsTwo);

}


 <!--chart3-->
function initialize3() {
        // The URL of the spreadsheet to source data from.
        var queryThree = new google.visualization.Query('http://spreadsheets.google.com/tq?key=13axh9Sv4DDf08BX2f86WVOZQokzAOF4jnX8AKBqIjz8');
        queryThree.send(checkThree);
      }

      function checkThree(responseThree) {
        if (responseThree.isError()) {
          alert('Error in query');
        }
	var dataThree = responseThree.getDataTable();
	var optionsThree = {
	
        title: 'United States Bird Egg Imports in Millions of dollars',
	titleTextStyle:{color: 'gray',fontName: 'Raleway', fontSize:24,bold:true},
	legend: {position: 'right', textStyle: {color: 'gray', fontSize: 20,fontName:'Raleway'}},
        chartArea:{left:50,top:20,width:'90%',height:'75%'},
	colors: ['#BC8F8F','#800000','#8FBC8F'],
         hAxis: {format:'',textStyle:{ fontName: 'Raleway',fontSize: 24},gridlines: {color: 'transparent'}},
          vAxis:{format:'$',gridlines: {color: 'transparent'},baselineColor:'white',textStyle:{ fontName: 'Raleway',fontSize: 24}}
      };

      var chartThree = new google.charts.Line(document.getElementById('third_div'));

chartThree.draw(dataThree,google.charts.Line.convertOptions(optionsThree));
    }


 <!--chart4-->
 	function initialize4() {
        // The URL of the spreadsheet to source data from.
        var queryFour = new google.visualization.Query('http://spreadsheets.google.com/tq?key=1czQrh_mxm5iZ03NKDjAjyzQ0vjw74PSlDFsXtFO4iwo');
        queryFour.send(checkFour);
      }

      function checkFour(responseFour) {
        if (responseFour.isError()) {
          alert('Error in query');
        }
	 var optionsFour = {
	bar:{groupWidth: '65%'},
	isStacked:true,
	title:' Australia Employment Percentage',
	titleTextStyle:{color: 'gray',fontName: 'Raleway', fontSize:24,bold:true},
   legend: {position: 'top', textStyle: {color: 'gray', fontSize: 20,fontName:'Raleway'}},
chartArea:{left:70,top:90,width:'70%',height:'20%'},

colors: ['#FFC1CC','#FC8EAC','#DB7093'],
hAxis: {gridlines: {color: 'transparent'},format:'percent',baselineColor:'white',textStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray'}},
 vAxis: {gridlines: {color: 'transparent'},textStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray'}}

};
        


	var dataFour = responseFour.getDataTable();
	var chartFour = new google.visualization.BarChart(document.getElementById('four_div'));
        chartFour.draw(dataFour, optionsFour);
     
 }


 <!--Chart6-->

function initialize6() {
        // The URL of the spreadsheet to source data from.
        var querySix = new google.visualization.Query('http://spreadsheets.google.com/tq?key=1OrRr7kcowyD-odStrU7bNP2zqqn3Rr14MVZL0YHKnIA');
        querySix.send(checkSix);
      }

      function checkSix(responseSix) {
        if (responseSix.isError()) {
          alert('Error in query');
        }
	

	var dataSix = responseSix.getDataTable();
        var optionsSix = {
	isStacked:true,
	 chart: {
         title: 'takingupspace',
	 Area:{left:50,top:100,width:'60%',height:'80%'}
	    },
	titleTextStyle:{color: 'white',fontName: 'Raleway', fontSize:20,bold:true},titlePosition:'in',
	
   legend: {position: 'top', textStyle: {color: 'gray', fontSize: 20,fontName:'Raleway'}},
	colors: ['#D2B48C','#F6ECE3'],
	hAxis: {gridlines: {color: 'transparent'},textStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray'},format:'',title:''},
 vAxis: {gridlines: {color: 'transparent'},baselineColor:'white',format:'percent',textStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray'}}
};
	   
	   
	    

        var chartSix = new google.charts.Bar(document.getElementById('six_div'));

        chartSix.draw(dataSix,google.charts.Bar.convertOptions(optionsSix));
      }
      

 <!--Chart7-->


function initialize7() {
        // The URL of the spreadsheet to source data from.
        var querySeven = new google.visualization.Query('http://spreadsheets.google.com/tq?key=1omXdSKgtLgT9-KQKGUDQaZBtVbLcbqfRG5Ww5ex5pHs');
        querySeven.send(checkSeven);
      }

      function checkSeven(responseSeven) {
        if (responseSeven.isError()) {
          alert('Error in query');
        }
	
	var dataSeven = responseSeven.getDataTable();
	
        var optionsSeven = {
	 chart: {
         title: ' The Number of Endangered Species in Australia',
	 Area:{left:40,top:80,width:'90%',height:'75%'}
	    },
	titleTextStyle:{color: 'gray',fontName: 'Raleway', fontSize:24,bold:true},titlePosition:'in',
	colors: ['#DB7093'],
	legend: {position:'none'},
	hAxis: {gridlines: {color: 'transparent'},textStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray'},format:''},
 vAxis: {gridlines: {color: 'transparent'},baselineColor:'white',format:'decimal',textStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray'}}
};
        var chartSeven = new google.charts.Bar(document.getElementById('seven_div'));

        chartSeven.draw(dataSeven,google.charts.Bar.convertOptions(optionsSeven));
      }



 <!--Chart8-->
function initialize8() {
        // The URL of the spreadsheet to source data from.
        var queryEight = new google.visualization.Query('http://spreadsheets.google.com/tq?key=1wcjKyQvShMj355E2nM0WmCrqBRxc6FarzZdsQIH4h3U');
        queryEight.send(checkEight);
      }

      function checkEight(responseEight) {
        if (responseEight.isError()) {
          alert('Error in query');
        }
	
       
	var dataEight = responseEight.getDataTable();

	var piedashboard = new google.visualization.Dashboard(
            document.getElementById('piedashboard_div'));

        // Create a range slider, passing some options
        var pieRangeSlider = new google.visualization.ControlWrapper({
          'controlType': 'CategoryFilter',
          'containerId': 'piefilter_div',
          'options': {
           'filterColumnIndex': 2,
	    'ui': {'allowNone':false,
		  'allowMultiple':false}
	    
          }
        });
	var chartEight = new google.visualization.ChartWrapper({
	  'chartType': 'PieChart',
          'containerId': 'piechart_div',
          'options': {
	chartArea:{left:50,top:100,width:'70%',height:'75%'},
	legend: {fontName:'Raleway',fontSize:20,color:'gray'},
          title: 'Percentage of seats held in National Parliment',
	titleTextStyle:{color: 'gray',fontName: 'Raleway', fontSize:24,bold:true},
	 pieSliceText: 'value',
	pieSliceTextStyle: {color: 'white', fontSize: 28,fontName:'Raleway'},
	  colors: ['#FA8072','#B0E0E6'],
          pieHole: 0.5
        

    
      },
	 
    // The pie chart will use the columns 'Name' and 'Donuts eaten'
    // out of all the available ones.
    'view': {'columns': [0, 1]}
  });

	piedashboard.bind(pieRangeSlider, chartEight);

 	piedashboard.draw(dataEight);


}



      <!--Chart9-->
function initialize9() {
        // The URL of the spreadsheet to source data from.
        var queryNine = new google.visualization.Query('http://spreadsheets.google.com/tq?key=1iLJgWhkIwaT2cTvzbJrpifmKJVTkrPWpfP11UNIkR3U');
        queryNine.send(checkNine);
      }

      function checkNine(responseNine) {
        if (responseNine.isError()) {
          alert('Error in query');
        }
	
var dataNine = responseNine.getDataTable();
	var dashboard = new google.visualization.Dashboard(
            document.getElementById('dashboard_div'));

        // Create a range slider, passing some options
        var mapRangeSlider = new google.visualization.ControlWrapper({
          'controlType': 'CategoryFilter',
          'containerId': 'filter_div',
          'options': {
           'filterColumnIndex': 1,
	    'ui': {'allowNone':false,
		  'allowMultiple':false},
		
	    
	    
          }
        });

        var chartNine = new google.visualization.ChartWrapper({
	
	  'chartType': 'GeoChart',
          'containerId': 'chart_div',
          'options': {
           chartArea:{left:50,top:20,width:'70%',height:'75%'},
	   colorAxis: {colors: ['#696969', '#000000']}
	  
          },
	 
    // The pie chart will use the columns 
    // out of all the available ones.
    'view': {'columns': [0, 2]}
  });

dashboard.bind(mapRangeSlider, chartNine);

 dashboard.draw(dataNine);
      }  

   <!--last chart yay-->

function initialize10() {
        // The URL of the spreadsheet to source data from.
        var queryTen = new google.visualization.Query('http://spreadsheets.google.com/tq?key=1akAWWFQrb1ppGY_sfklW_rjGgYUBx7TKl0Ai4_33kxc');
        queryTen.send(checkTen);
      }

      function checkTen(responseTen) {
        if (responseTen.isError()) {
          alert('Error in query');
        }
	
       
	var dataTen = responseTen.getDataTable();
	var optionsTen = {
        title: 'population size',
	colorAxis:{colors: ['#BF565A','#D9001D'],legend:{textStyle:{fontName:'Raleway',fontSize:20}}},
	titleTextStyle:{color: 'gray',fontName: 'Raleway', fontSize:24,bold:false},
	hAxis: {title:'co2 emissions in tons per capita',gridlines:{color: 'transparent'},
	textStyle:{ fontName:'Raleway',fontSize: 24,color:'gray',italic:false,textPosition:'in'},
	titleTextStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray',italic:false,textPosition:'in'}},
        vAxis: {title:' Number of Endangered Species',gridlines:{color: 'transparent'},
	titleTextStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray',italic:false},
	textStyle:{ fontName: 'Raleway',fontSize: 24,color:'gray',textPosition:'in',italic:false}},
	bubble:{opacity:1.0,textStyle:{fontName:'Raleway',fontSize:18,color:'gray'}},
	chartArea:{left:90,top:90,width:'60%',height:'65%'}
      

      };	


	
        chartTen = new google.visualization.BubbleChart(document.getElementById('ten_div'));
	chartTen.draw(dataTen, optionsTen);

}






 <!--needed to end code of charts-->
 </script>
  </head>
  <body>
   


 <!--Table and divs that hold the pie charts-->
    <table class="columns">

<p><span style="color:#808080;font-family:Raleway; font-size:55"><b>Data Visualization with Google Charts</b></span></p>

<span style="color:#808080;font-family:Raleway;font-size:12">by Hailey Stahl</span></p>
 

<span style="color:#808080;font-family:Raleway;font-size:12">
data sources: data.un.org and ers.usda.gov</span></p>
<tr><td><hr size="10" width="100%" color="#BC8F8F"<\hr>    <div id="third_div" style="width: 1000px; height: 500px;"></div>

<p><span style="color:#808080;font-family:Raleway;"></span></p>

<p><span style="color:#808080;font-family:Raleway;"></span></p><hr size="10" width="100%" color="#BC8F8F"<\hr></td></tr>
        

<td><div id="first_div" style="width: 1200px; height: 800px;"></div>
<p><span style="color:#808080;font-family:Raleway;">According to natureaustralia.org as of March 2021 the animal in most danger is ...the Numbat.</span></p>
<p><span style="color:#808080;font-family:Raleway;"></span></p>
<hr size="10" width="100%" color="#BC8F8F"<\hr></td></tr>



<tr> <td><div id="second_div" style="width: 800px; height: 500px;"></div>
<p><span style="color:#808080;font-family:Raleway;"></span></p>
<p><span style="color:#808080;font-family:Raleway;"></span></p>
<hr size="10" width="100%" color="#BC8F8F"<\hr></td></tr>


<tr><td> <div id="four_div" style="width: 800px; height: 400px;"></div>

<p><span style="color:#808080;font-family:Raleway;"></span></p>
<hr size="10" width="100%" color="#BC8F8F"<\hr></td></tr></tr></td> 





<tr><td>
<p><span style="color:#808080;font-family:Raleway; font-size:24"><b>The percentange of the population in Croatia is drinking...</b></span>
<div id="six_div" style="width: 300px; height: 600px;"></div>
<p><span style="color:#808080;font-family:Raleway;"></span></p>
<hr size="10" width="100%" color="#BC8F8F"<\hr></td></tr></td></tr>






<tr><td><div id="seven_div" style="width: 800px; height: 500px;"></div>

<p><span style="color:#808080;font-family:Raleway;">The second animal in danger is the Goulden Finch.</span></p>
<p><span style="color:#808080;font-family:Raleway;"></span></p>
<hr size="10" width="100%" color="#BC8F8F"<\hr></td></tr></td></tr>



<tr><td>
<div id="piedashboard_div">
      <!--Divs that will hold each control and chart-->
      <div id="piefilter_div"></div>
      <div id="piechart_div" style="width: 800px; height: 500px;"></div>




</div>
<p><span style="color:#808080;font-family:Raleway;"></span></p>
<hr size="10" width="100%" color="#BC8F8F"<\hr></td></tr></td></tr>


<tr><td>
<div id="dashboard_div">
      <!--Divs that will hold each control and chart-->
	<p><span style="color:#808080;font-family:Raleway;font-size:24"><b> US Imports in Millions of Dollars in 2017</b></span></p>
      <div id="filter_div"></div>
      <div id="chart_div"></div>



</div>
<p><span style="color:#808080;font-family:Raleway;"></span></p>
<hr size="10" width="100%" color="#BC8F8F"<\hr></td></tr></td></tr>



<tr><td><p><span style="color:#808080;font-family:Raleway;font-size:30"><b></b></span></p><div id="ten_div" style="width: 975px; height: 800px;"></div>
<p><span style="color:#808080;font-family:Raleway;"></span></p>
<tr><td>


</table>
  </body>
</html>
      

      
