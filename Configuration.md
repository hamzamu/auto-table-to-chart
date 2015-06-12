# Options #
```
.attc(
location:elementId,
tableHide : true/false,
chartHide : true/false,
type:'bar/pie/column/area/etc',
googleOptions:{
  Google chart options: [https://developers.google.com/chart/interactive/docs/gallery/piechart#Configuration_Options Pie chart option]
}
'controls':{
showHide:true/false,
create:true/false,
chartType:true/false
},
'controlsLabels':{
showChart:"Show chart",
hideChart:"Hide chart",
showTable:"Show table",
hideTable:"Hide table",
createChart:"Edit chart",
changeChart:"Change chart"
},
chartOptionList:'<option value="bar">Bar</option><option value="pie">Pie</option><option value="column">Column</option><option value="area">Area</option><option value="line">Line</option>'
)
```

# location #
```
location:elementId
```
The Id of the html element in which to put the chart

# tableHide #
```
tableHide : true/false
```
Whether to hide the table by default

# chartHide #
```
chartHide : true/false
```
Whether to hide the chart by default

# type #
```
type:'bar/pie/column/area/etc'
```
The type of chart to convert the table to - one of 'bar/pie/column/area/line'

# googleOptions #
```
googleOptions:{}
```
Object containing options to use when creating the chart, these are simply passed through to google for setting up the chart, details for pie charts here:
[Google Pie chart options](https://developers.google.com/chart/interactive/docs/gallery/piechart#Configuration_Options)

# controls #
```
controls:{
showHide:true/false,
create:true/false,
chartType:true/false
}
```
Object containing options for the controls that appear above the table, to allow chart editing/changing and show/hide table and chart.

# controlsLabels #
```
'controlsLabels':{
showChart:"Show chart",
hideChart:"Hide chart",
showTable:"Show table",
hideTable:"Hide table",
createChart:"Edit chart",
changeChart:"Change chart"
}
```
Text labels that will appear next to the controls of the chart.

# chartOptionList #
```
chartOptionList:'<option value="bar">Bar</option><option value="pie">Pie</option><option value="column">Column</option><option value="area">Area</option><option value="line">Line</option>'
)
```
The values that appear in the select list of possible chart types. Remove charts from here that you do not want selecting for this table