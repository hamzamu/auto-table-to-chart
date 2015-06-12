# Introduction #

Auto-table-to-chart (AttC) is a bit a javascript that converts a standard HTML table to a Open Flash Chart on the page.
It is built on the following:
  * Open Flash Chart 2 - http://teethgrinder.co.uk/open-flash-chart-2
  * Jquery  - http://jquery.com

# Details #

To use you need to include the javascript in the head of your page:
```
<script src="js/jquery/jquery.js" type="text/JavaScript"></script>
<script src="js/openflashchart/js/swfobject.js" type="text/JavaScript"></script>
<script type="text/javascript" src="js/openflashchart/js/json2.js"></script>
<script type="text/javascript" src="js/attc.js"></script>
```

and then add the basic css to the head:
```
<style type="text/css">
@import url(css/flash_chart_style.css);
</style>
```

Your table should be of the format:
```
<table>
<caption>Some totals</caption>
<thead>
<tr>
<th>Heading</th>
</tr>
</thead>		
<tbody>
<tr>
<th>content</th>
</tr>
</tbody>
<table>
```
as the script looks for <thead> and <tbody> sections to get its information, <tfoot> can be used but is ignored at present<br>
<br>
to get a basic bar graph you add some css classes to the <code>&lt;table&gt;</code> tag and the <code>&lt;th&gt;</code> tags - like this:<br>
<pre><code>&lt;table class="graph_table chart_type_pie" id="a_table"&gt;<br>
&lt;caption&gt;Some totals&lt;/caption&gt;<br>
&lt;thead&gt;<br>
&lt;tr&gt;<br>
&lt;th class="graph_id" title="heading"&gt;Heading&lt;/th&gt;<br>
&lt;th class="graph_value" title="total"&gt;Total&lt;/th&gt;<br>
&lt;/tr&gt;<br>
&lt;/thead&gt;		<br>
&lt;tbody&gt;<br>
&lt;tr&gt;<br>
&lt;th&gt;south&lt;/th&gt;<br>
&lt;th&gt;10&lt;/th&gt;<br>
&lt;/tr&gt;<br>
&lt;tr&gt;<br>
&lt;th&gt;north&lt;/th&gt;<br>
&lt;th&gt;20&lt;/th&gt;<br>
&lt;/tr&gt;<br>
&lt;/tbody&gt;<br>
&lt;table&gt;<br>
</code></pre>
possible <code>&lt;table&gt;</code> css classes to setup the graph are:<br>
<ul><li>graph_table - needed to get the table to be converted to a graph on page load<br>
</li><li>chart_type_pie - Show the graph as a pie chart<br>
</li><li>chart_type_bar - Show the graph as a bar chart<br>
</li><li>chart_type_bar_3d - Show the graph as a bar_3d chart<br>
</li><li>chart_type_line - Show the graph as a line chart<br>
</li><li>table_hidden - default the table to hidden<br>
</li><li>chart_hidden - default the chart to hidden</li></ul>

possible <code>&lt;th&gt;</code> css classes to setup the plots are:<br>
<br>
<ul><li>graph_id the x axis labels (only one <code>&lt;th&gt;</code> can should this class)<br>
</li><li>graph_value the y axis values (multiple <code>&lt;th&gt;</code> can have this class, unless it is a pie chart, then only one is used)<br>
</li><li>graph_value_stack combined with 'chart_type_bar' shows the values stacked on top of one another - use instead of 'graph_value'<br>
</li><li>skip<code>#_#_#_#</code> - where # are the row numbers to skip<br>
</li><li>steps<code>_#</code> - where # is the value of steps to use on the y axis, overrides the automatic calculation of steps (only one <code>&lt;th&gt;</code> should have this class)</li></ul>


You can style the chart using the style sheet: 'flash_chart_style.css' in the css folder of the download, please see the comments in there for more info. The chart id for css and javascript is 'flash_chart<i>'+the_table_id.</i>

take a look at the download for working examples of the various css class options.