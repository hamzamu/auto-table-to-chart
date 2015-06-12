# Options #

```
<table 
    		title="Table title" 
    		id="tableId" 
    		summary="Description of chart and table" 
    		data-attc-colDescription="DescriptionCol" 
    		data-attc-colValues="ValuesCol,ValuesCol2" 
    		data-attc-location="ChartLocationId" 
    		data-attc-hideTable="true" 
                data-attc-hideChart="true" 
    		data-attc-type="pie"
    		data-attc-googleOptions='{"is3D":true}'
                data-attc-controls='{"showHide":true,"create":true,"chartType":true}'
                data-attc-controlsLabels='{"showChart":"Show chart","hideChart":"Hide chart","showTable":"Show table","hideTable":"Hide table","createChart":"Edit chart","changeChart":"Change chart"}'
                data-attc-chartOptionList='<option value="bar">Bar</option><option value="pie">Pie</option><option value="column">Column</option><option value="area">Area</option><option value="line">Line</option>'
    		>
```


# title #
```
title="Table title" 
```
The chart title, overrides any set when attc called via js

# id #
```
id="tableId" 
```
The table id, you should add this

# summary #
```
summary="Description of chart and table" 
```
The table/chart description - isn't used yet, but will be...

# data-attc-colDescription #
```
data-attc-colDescription="DescriptionCol"
```
The column ID to use for the text description of the chart items

# data-attc-colValues #
```
data-attc-colValues="ValuesCol,ValuesCol2"
```
The column ID to use for the values of the chart items, pie would only have one id, others might have n number of ids, separated by a comma.

# data-attc-location #
```
data-attc-location="ChartLocationId"
```
ID of the HTML element that will contain the chart

# data-attc-hideTable #
```
data-attc-hideTable="true"
```
Whether to show or hide the html table that was used to create the chart - overrides defaults from js setup

# data-attc-hideChart #
```
data-attc-hideChart="true"
```
Whether to show or hide the chart - overrides defaults from js setup

# data-attc-type #
```
data-attc-type="pie"
```
The type of chart - one of Pie,Column,Line,Bars,Area - overrides defaults from js setup

# data-attc-googleOptions #
```
data-attc-googleOptions='{"is3D":true}'
```
JSON data object to pass along to the google chart api, based on options for each chart. e.g pie: [Options](https://developers.google.com/chart/interactive/docs/gallery/piechart#Configuration_Options)

# data-attc-controls #
```
data-attc-controls='{"showHide":true,"create":true,"chartType":true}'
```
Which controls to show above the table, in order to show/hide or edit/change the chart

# data-attc-controlsLabels #
```
data-attc-controlsLabels='{"showChart":"Show chart","hideChart":"Hide chart","showTable":"Show table","hideTable":"Hide table","createChart":"Edit chart","changeChart":"Change chart"}'
```
The labels to show against each control option

# data-attc-chartOptionList #
```
data-attc-chartOptionList='<option value="bar">Bar</option><option value="pie">Pie</option><option value="column">Column</option><option value="area">Area</option><option value="line">Line</option>'
```
The options to show in the select list of chart types