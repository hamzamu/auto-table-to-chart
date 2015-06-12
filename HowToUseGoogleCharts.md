# Prerequisite #

  * jQuery
  * Google jsapi
  * The attc.googleCharts.js file


# Setup #

Add the following to your html head (assuming attc.googleCharts.js is in the same folder as the html page):
```
<head>
    <script type="text/javascript" src="//www.google.com/jsapi"></script>
    <script src="//ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    <script src="attc.googleCharts.js"></script>
    <!--optional css-->
    <link rel="stylesheet" type="text/css" href="attc.css">
</head>
```

Then create a html table - note thead and tbody elements!:
```
<table>
			<thead>
				<tr>
					<th id="colDescription">Description</th>
					<th id="colValue1">Sessions</th>
					<th>%</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<td>Present</td>
					<td>405</td>
					<td>89</td>
				</tr>
				<tr>
					<td>Missing</td>
					<td>1</td>
					<td>0</td>
				</tr>
				<tr>
					<td>Authorised Absent</td>
					<td>36</td>
					<td>7</td>
				</tr>
				<tr>
					<td>Unauthorised Absent</td>
					<td>1</td>
					<td>0</td>
				</tr>
				<tr>
					<td>Late</td>
					<td>10</td>
					<td>2</td>
				</tr>
			</tbody>
		</table>
```

then add the data attributes to the table tag, googleOptions is a pass through of the options for each chart, based on google's chart options:
```
<table
title="Attendance Percentages" 
    		id="AttendancePercentages" 
    		summary="Description of table" 
    		data-attc-createChart="true"
    		data-attc-colDescription="colDescription" 
    		data-attc-colValues="colValue1" 
    		data-attc-location="AttendancePercentagesPie" 
    		data-attc-hideTable="true" 
    		data-attc-type="pie"
    		data-attc-googleOptions='{"is3D":true}'
    		data-attc-controls='{"showHide":true,"create":true,"chartType":true}'
>
```

Add the div to hold the chart:
```
<div id="AttendancePercentagesPie"></div>
```

Finally call the script on page load, on the table element:
```
$(document).ready(function(){
	$('#AttendancePercentages').attc();
});
```