### **CHART**

#### Control description

This control lets us create various chart types: composed, line, area and bar. It is created using the **WIZARD_CHART** or **output-chart** control.

#### Extended control properties

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Default value</strong></td>
    <td>
      <strong>Supported values</strong>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"type": "WIZARD_CHART"     
       </code></pre>
    </td>
    <td>
      <pre><code>
"WIZARD_CHART" / 
"output-chart"
      </code></pre>
    </td>
    <td>
      N/A
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"position": ["   "]    
      </code></pre>
    </td>
    <td>
    N/A
    </td>
    <td>
      Any values can be specified.
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"chartType": "   "
    </code></pre>  
    </td>
    <td>
      N/A
    </td>
    <td>
     <pre><code>
"composed"
"line"
"area"
"bar"
    </code></pre>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>  
"grid": {{ '{' }}
    "visible": 
    {{ '}' }}
      </code></pre>
    </td>
    <td>
N/A
    </td>
    <td>
    <pre><code>
"false"
"true"
    </code></pre>
    </td>
  </tr>
  <tr>
    <td>
<pre><code>   
"grid": {{ '{' }}
"strokeDasharray": "1 2 "
    {{ '}' }}
  </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
    It specifies grid line style: first value stands for dash length, second - gap length.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>    
"grid": {{ '{' }}
  "stroke": "   "
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Specifies chart grid color. Any color can be indicated.
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>     
"grid": {{ '{' }}
  "fill": "   "
  {{ '}' }}
  </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
    Specifies chart background color. Any color can be indicated.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>     
"XAxis": {{ '{' }}
  "hide":
  {{ '}' }} 
      </code></pre>
    </td>
    <td>
      false
    </td>
    <td>
    <pre><code>
"false"
"true"
    </code></pre>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>     
"XAxis": {{ '{' }}
  "label": "  "
  {{ '}' }} 
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Axis name to be displayed on chart. Any name can be specified.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>       
"XAxis": {{ '{' }}
  "data": [
       ]
  {{ '}' }}
      </code></pre>
    </td>
    <td>
    Sequential numbering starting from <code>Tick 1</code>
    </td>
    <td>
    Axis tick values. If not enough values are specified, default values, i.e. <code>Tick 1</code> etc, are used. 
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"XAxis": {{ '{' }}
  "color": "  "
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any color can be specified.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"XAxis": {{ '{' }}
  "fontSize": "   "
  {{ '}' }}
      </code></pre>
    </td>
    <td>
By default, font size is calculated related to the control size. Reference font value is 16px for control height or width of 500px.
    </td>
    <td>
    Any font size can be specified.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"YAxis": {{ '{' }}
  "hide": 
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      false
    </td>
    <td>
    <pre><code>
"false"
"true"
    </code></pre>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"YAxis": {{ '{' }}
  "domain": [ 0, 1000]
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
    Specifies array for a fixed scale.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"YAxis": {{ '{' }}
  "label": "   "
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
  Axis name to be displayed on chart. Any name can be specified.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"YAxis": {{ '{' }}
  "color": "  "
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
Any color can be specified.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"YAxis": {{ '{' }}
  "fontSize": "  "
  {{ '}' }}
      </code></pre>
    </td>
    <td>
    By default, font size is calculated related to the control size. Reference font value is 16px for control height or width of 500px.
    </td>
    <td>
    Any font size can be specified.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"tooltip": {{ '{' }}
  "visible":
{{ '}' }}
      </code></pre>
    </td>
    <td>
    <pre><code>
"false"
    </code></pre>
    </td>
    <td>
Displays text boxes that pop up when you hover over chart.
    <pre><code>
"false"
"true"
    </code></pre>
    </td>
  </tr> 
  <tr>
    <td>
      <pre><code>       
"tooltip": {{ '{' }}
  "fontSize": "  "
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      By default, font size is calculated related to the control size. Reference font value is 16px for control height or width of 500px.
    </td>
    <td>
  Any font size can be specified.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"legend": {{ '{' }}
  "visible":
  {{ '}' }}
      </code></pre>
    </td>
    <td>
    <pre><code>
"false"
    </code></pre>
    </td>
    <td>
    Explains and lists the chart's elements specified as <code>title</code> in <code>series</code> property (see below).
    <pre><code>
"false"
"true"
    </code></pre>
    </td>
    <tr>
    <td>
    <pre><code>   
"legend": {{ '{' }}
  "fontSize": "   "
   {{ '}' }}
      </code></pre>
    </td>
    <td>
      By default, font size is calculated related to the control size. Reference font value is 16px for control height or width of 500px.
    </td>
    <td>
  Any font size can be specified.
    </td>
  </tr>
  <tr>
    <td>
        <pre><code>        
"series": [
  {{ '{' }}
    "type": "  "
  {{ '}' }}
  ]
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
     <code>series</code> are sets of related data points plotted together and showed on chart.
     <ul>
     <li>Supported values for the <code>"composed"</code> <strong>chart types</strong> (see above):
     <pre><code>    
"line"
"area"
"bar"
    </code></pre></li>
    <li><code>"line"</code>, <code>"area"</code>, <code>"bar"</code> <strong>chart types</strong> support only types specific to them. i.e. <code>"line"</code>, <code>"area"</code>, <code>"bar"</code></li>
    </ul>
    </td>
</tr>
  <tr>
    <td>
            <pre><code>            
"series": [
  {{ '{' }}
   "title": " "
  {{ '}' }}
   ]
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
Data set name which is used for the legend and tooltip, as well as for data array.
    </td>
</tr>
<tr>
    <td>
     <pre><code>
"series": [
  {{ '{' }}
    "data": 
  {{ '}' }}
   ]
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
    Data can be specified:
    <ul>
    <li>as array:
<pre><code>"data": [100, 200, 300, 400, 500]</code></pre></li>
    <li>as any required function, e.g.:
<pre><code>"data": "eval:() => {{ '{' }} const randomArray = []; for (let i = 0; i < 5; i++) {{ '{' }} const randomValue = Math.floor(Math.random() * 500) + 1;  randomArray.push(randomValue); {{ '}' }} return randomArray;{{ '}' }}"</code></pre></li>
    <li>as reference to a <code>js</code> file uploaded to <a href="https://docs.upmix.it/scenario-edit/assets#add-an-asset">assets</a> using <code>"#include:"</code>: <pre><code>"data": "#include:./..."</code></pre>
    </li>
    </ul>
    </td>
  </tr>
  <tr>
    <td>
<pre><code>  
"series": [
  {{ '{' }}
  "stroke": {{ '{' }}
    "color": "   "
  {{ '}' }}
 {{ '}' }}
 ]
  </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
  Stroke is a line that defines the shape of a graphic element and is used for <code>line</code> and <code>area</code> chart types.
  <br><br>Any <code>color</code> can be specified.
    </td>
  </tr>
  <tr>
  <tr>
    <td>
    <pre><code>   
"series": [{{ '{' }}
  "stroke": {{ '{' }}
    "width":  
   {{ '}' }}
  {{ '}' }}
 ]
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
  Stroke is a line that defines the shape of a graphic element and is used for <code>line</code> and <code>area</code> chart types.
  <br><br>Any <code>width</code> can be specified.
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>   
"series": [{{ '{' }}
  "stroke": {{ '{' }}
    "dasharray": "   "
    {{ '}' }}
   {{ '}' }}
   ]
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
  Stroke is a line that defines the shape of a graphic element and is used for <code>line</code> and <code>area</code> chart types.
  <br><br>Any <code>dasharray</code> (first value stands for dash length, second - gap length) can be specified.
    </td>
  </tr>
  <tr>
  <tr>
    <td>
    <pre><code>
"series": [
  "fill": {{ '{' }}
     "color": "   "   
   {{ '}' }}
    ]
      </code></pre>
    </td>
    <td>
      <pre><code>N/A</code></pre>
    </td>
    <td>
  <code>"fill"</code> is used for <code>area</code> and <code>bar</code> types.
  Any <code>color</code> can be specified.
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"series": [
  "fill": {{ '{' }}
    "opacity":   
  {{ '}' }}
  ]
      </code></pre>
    </td>
    <td>
      <pre><code>N/A</code></pre>
    </td>
    <td>
  <code>"fill"</code> is used for <code>area</code> and <code>bar</code> types.
  Any <code>color</code> can be specified. 
  The <code>opacity</code> value is set within a range from 0 to 1. 
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"series": [
  {{ '{' }}
    "stackID": "a"
  {{ '}' }}
  ]
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
<code>stackID</code> is used in <code>bar</code>, <code>area</code> type.
Different charts with the same <code>stackID</code> will be displayed on top of each other.
    </td>
  </tr>
    <tr>
    <td>
    <pre><code>
"series": [
  {{ '{' }}
  "barSize": "30"
  {{ '}' }}
  ]
      </code></pre>
    </td>
    <td>
      30
    </td>
    <td>
Width of a bar in a <code>bar</code> type chart.
<code>barSize</code> is used in <code>bar</code>, <code>area</code> types.
    </td>
  </tr>
</table>

#### Minimum required control properties

<table>
  <tr>
    <td><strong>Minimum settings</strong></td>
    <td><strong>Description</strong></td>
  </tr>
  <tr>
  <td>
    <pre><code>
  "controls": {{ '{' }}
     "chart": {{ '{' }}
      "type": "WIZARD_CHART",
     "position": [
        "95.61715696139px",
        "74.47681049226108px",
        "1030.143240846632px",
        "585.0551161363044px"
      ],
      "chartType": "composed",
      "series": [
        {{ '{' }}
          "type": "line",
          "data": [100, 200, 300, 400, 500]
        {{ '}' }},
        {{ '{' }}
          "type": "bar",
          "data": [50, 100, 125, 200, 300]
        {{ '}' }},
        {{ '{' }}
          "type": "area",
          "data": [90, 100, 150, 200, 250]
        {{ '}' }}
      ]
    {{ '}' }}
  {{ '}' }}
    </code></pre>
    </td>
    <td>
    The minimum required control properties include:
    <ul>
    <li><code>chart Type</code></li>
    <li><code>type</code> for <code>series</code></li>
    <li><code>data</code> for <code>series</code></li>
    </ul>
    </td>
  </tr>
</table>

#### Snippet: area chart

<table>
  <tr>
    <td><strong>Source Code</strong></td>
    <td>
      <strong>Result</strong>
    </td>
  </tr>
    <tr>
    <td>
    <pre><code>
   "controls": {{ '{' }}
    "chart": {{ '{' }}
      "type": "WIZARD_CHART",
      "position": [
        "95.61715696139px",
        "74.47681049226108px",
        "1030.143240846632px",
        "585.0551161363044px"
      ],
      "chartType": "area",
      "grid": {{ '{' }}
        "visible": true,
        "strokeDasharray": "3 3",
        "stroke": "#ccc",
        "fill": "#fafafa"
      {{ '}' }},
      "XAxis": {{ '{' }}
        "hide": false,
        "label": "X",
        "data": [
          "0",
          "1",
          "2",
          "3",
          "4"
        ],
        "color": "red",
        "fontSize": "22px"
      {{ '}' }},
      "YAxis": {{ '{' }}
        "hide": false,
        "label": "Y",
        "color": "blue",
        "fontSize": "22px"
      {{ '}' }},
      "tooltip": {{ '{' }}
        "visible": "true",
        "fontSize": "22px"
      {{ '}' }},
      "legend": {{ '{' }}
        "visible": true,
        "fontSize": "30px"
      {{ '}' }},
      "series": [
        {{ '{' }}
          "type": "area",
          "title": "area 1",
          "data": [
            100,
            200,
            300,
            400,
            500
          ],
          "style": {{ '{' }}
            "fill": {{ '{' }}
              "color": "#6495ED",
              "opacity": 1
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "area",
          "title": "area 2",
          "data": "eval: () => {{ '{' }} return [400, 500, 287, 451] {{ '}' }}",
          "style": {{ '{' }}
            "stroke": {{ '{' }}
              "color": "#c71585",
              "width": 4,
              "dasharray": "5 10"
            {{ '}' }},
            "fill": {{ '{' }}
              "color": "#ffc658",
              "opacity": 0.2
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "area",
          "title": "area 3",
          "data": "eval: () => {{ '{' }} const randomArray = []; for (let i = 0; i < 5; i++) {{ '{' }} const randomValue = Math.floor(Math.random() * 500) + 1;  randomArray.push(randomValue); {{ '}' }}  return randomArray;{{ '}' }}",
          "style": {{ '{' }}
            "stroke": {{ '{' }}
              "color": "#fc1442",
              "width": 4
            {{ '}' }},
            "fill": {{ '{' }}
              "color": "#fc1442",
              "opacity": 0.5
            {{ '}' }}
          {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/area-for-gif.png"/></figure>
  </tr>
</table>

#### Snippet: bar chart

<table>
<tr>
    <td><strong>Source Code</strong></td>
    <td>
      <strong>Result</strong>
    </td>
  </tr>
<tr>
    <td>
    <pre><code>
    "controls": {{ '{' }}
    "chart": {{ '{' }}
      "type": "WIZARD_CHART",
      "position": [
        "95.61715696139px",
        "74.47681049226108px",
        "1030.143240846632px",
        "585.0551161363044px"
      ],
      "chartType": "bar",
      "grid": {{ '{' }}
        "visible": true,
        "strokeDasharray": "3 3",
        "stroke": "#ccc",
        "fill": "#fafafa"
      {{ '}' }},
      "XAxis": {{ '{' }}
        "hide": false,
        "label": "X",
        "data": [
          "0",
          "100",
          "200",
          "300",
          "400"
        ],
        "color": "red",
        "fontSize": "22px"
      {{ '}' }},
      "YAxis": {{ '{' }}
        "hide": false,
        "label": "Y",
        "color": "blue",
        "fontSize": "22px"
      {{ '}' }},
      "tooltip": {{ '{' }}
        "visible": "true",
        "fontSize": "22px"
      {{ '}' }},
      "legend": {{ '{' }}
        "visible": true,
        "fontSize": "25px"
      {{ '}' }},
      "series": [
        {{ '{' }}
          "type": "bar",
          "title": "bar 1",
          "data": [
            324,
            234,
            234,
            545,
            456
          ],
          "style": {{ '{' }}
            "fill": {{ '{' }}
              "color": "#adff2f",
              "opacity": 0.3
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "bar",
          "title": "bar 2",
          "data": "eval: () => {{ '{' }} return [400, 500, 287, 451] {{ '}' }}",
          "stackId": "a",
          "barSize": 30,
          "style": {{ '{' }}
            "fill": {{ '{' }}
              "color": "#6495ed",
              "opacity": 0.3
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "bar",
          "title": "bar 3",
          "data": "eval: () => {{ '{' }} const randomArray = []; for (let i = 0; i < 5; i++) {{ '{' }} const randomValue = Math.floor(Math.random() * 500) + 1;  randomArray.push(randomValue); {{ '}' }}  return randomArray;{{ '}' }}",
          "style": {{ '{' }}
            "fill": {{ '{' }}
              "color": "#fc1442",
              "opacity": 1
            {{ '}' }}
          {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/bar-chart-gif.png"/></figure>
    </td>
  </tr>
</table>

#### Snippet: composed chart

<table>
<tr>
    <td><strong>Source Code</strong></td>
    <td>
      <strong>Result</strong>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
    "controls": {{ '{' }}
    "chart": {{ '{' }}
      "type": "WIZARD_CHART",
      "position": [
        "147.24255714696px",
        "179.46141426225387px",
        "1125.4156971020307px",
        "608.5738089232685px"
      ],
      "chartType": "composed",
      "grid": {{ '{' }}
        "visible": true,
        "strokeDasharray": "3 3",
        "stroke": "#ccc",
        "fill": "#fafafa"
      {{ '}' }},
      "XAxis": {{ '{' }}
        "hide": false,
        "label": "X",
        "data": [
          "a",
          "b",
          "c",
          "d",
          "e"
        ],
        "color": "red",
        "fontSize": "22px"
      {{ '}' }},
      "YAxis": {{ '{' }}
        "hide": false,
        "label": "Y",
        "color": "blue",
        "fontSize": "22px"
      {{ '}' }},
      "tooltip": {{ '{' }}
        "visible": "true",
        "fontSize": "22px"
      {{ '}' }},
      "legend": {{ '{' }}
        "visible": true,
        "fontSize": "30px"
      {{ '}' }},
      "series": [
        {{ '{' }}
          "type": "line",
          "title": "line",
          "data": [
            324,
            234,
            234,
            545,
            456
          ],
          "style": {{ '{' }}
            "stroke": {{ '{' }}
              "color": "#adff2f",
              "width": 2,
              "dasharray": "5 5"
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "bar",
          "title": "bar",
          "data": "eval: () => {{ '{' }} return [400, 500, 287, 451] {{ '}' }}",
          "barSize": 30,
          "style": {{ '{' }}
            "fill": {{ '{' }}
              "color": "#8884d8",
              "opacity": 0.3
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "area",
          "title": "area",
          "data": "eval: () => {{ '{' }} const randomArray = []; for (let i = 0; i < 5; i++) {{ '{' }} const randomValue = Math.floor(Math.random() * 500) + 1;  randomArray.push(randomValue); {{ '}' }}  return randomArray;{{ '}' }}",
          "style": {{ '{' }}
            "stroke": {{ '{' }}
              "color": "#c71585",
              "width": 4,
              "dasharray": "0 0"
            {{ '}' }},
            "fill": {{ '{' }}
              "color": "#ffc658",
              "opacity": 0.5
            {{ '}' }}
          {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/composed-for-gif.png"/></figure>
    </td>
  </tr>
</table>

#### Snippet: line chart

<table>
  <tr>
    <td><strong>Source Code</strong></td>
    <td>
      <strong>Result</strong>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
    "controls": {{ '{' }}
    "chart": {{ '{' }}
      "type": "WIZARD_CHART",
      "position": [
        "95.61715696139px",
        "74.47681049226108px",
        "1030.143240846632px",
        "585.0551161363044px"
      ],
      "chartType": "line",
      "grid": {{ '{' }}
        "visible": true,
        "strokeDasharray": "3 3",
        "stroke": "#ccc",
        "fill": "#fafafa"
      {{ '}' }},
      "XAxis": {{ '{' }}
        "hide": false,
        "label": "X",
        "data": [
          "0",
          "1",
          "2",
          "3",
          "4"
        ],
        "color": "red",
        "fontSize": "22px"
      {{ '}' }},
      "YAxis": {{ '{' }}
        "hide": false,
        "label": "Y",
        "color": "blue",
        "fontSize": "22px"
      {{ '}' }},
      "tooltip": {{ '{' }}
        "visible": "true",
        "fontSize": "22px"
      {{ '}' }},
      "legend": {{ '{' }}
        "visible": true,
        "fontSize": "30px"
      {{ '}' }},
      "series": [
        {{ '{' }}
          "type": "line",
          "title": "line 1",
          "data": [
            324,
            234,
            234,
            545,
            456
          ],
          "style": {{ '{' }}
            "stroke": {{ '{' }}
              "color": "green",
              "width": 5,
              "dasharray": "5 5"
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "line",
          "title": "line 2",
          "data": "eval: () => {{ '{' }} return [400, 500, 287, 451] }",
          "style": {{ '{' }}
            "stroke": {{ '{' }}
              "color": "#6495ed",
              "width": 5,
              "dasharray": "0 0"
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "line",
          "title": "line 3",
          "data": "eval: () => {{ '{' }} const randomArray = []; for (let i = 0; i < 5; i++) {{ '{' }} const randomValue = Math.floor(Math.random() * 500) + 1;  randomArray.push(randomValue); {{ '}' }}  return randomArray;{{ '}' }}",
          "style": {{ '{' }}
            "stroke": {{ '{' }}
              "color": "#fc1442",
              "width": 4,
              "dasharray": "0 0"
            {{ '}' }}
          {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/line-for-gif.png"/></figure>
    </td>
  </tr>
</table>

<!--
#### Snippet: pie chart

<table>
<tr>
    <td><strong>Source Code</strong></td>
    <td>
      <strong>Result</strong>
    </td>
</tr>
<tr>
    <td>
    <pre><code>
    "controls": {{ '{' }}
    "chart": {{ '{' }}
      "type": "WIZARD_CHART",
      "position": [
        "95.61715696139px",
        "74.47681049226108px",
        "1030.143240846632px",
        "585.0551161363044px"
      ],
      "chartType": "pie",
      "tooltip": {{ '{' }}
        "visible": "true",
        "fontSize": "22px"
      {{ '}' }},
      "legend": {{ '{' }}
        "visible": true,
        "fontSize": "30px"
      {{ '}' }},
      "series": [
        {{ '{' }}
          "type": "pie",
          "title": "pie 1",
          "data": [
            324,
            234,
            234,
            545,
            456
          ],
          "style": {{ '{' }}
            "fill": {{ '{' }}
              "color": "#6495ed",
              "opacity": 1
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "pie",
          "title": "pie 2",
          "data": "eval: () => {{ '{' }} return [400, 500, 287, 451] {{ '}' }}",
          "style": {{ '{' }}
            "fill": {{ '{' }}
              "color": "#6495ed",
              "opacity": 1
            {{ '}' }}
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "pie",
          "title": "pie 3",
          "data": "eval: () => {{ '{' }} const randomArray = []; for (let i = 0; i < 5; i++) {{ '{' }} const randomValue = Math.floor(Math.random() * 500) + 1;  randomArray.push(randomValue); {{ '}' }}  return randomArray;{{ '}' }}",
          "style": {{ '{' }}
            "fill": {{ '{' }}
              "color": "#6495ed",
              "opacity": 1
            {{ '}' }}
          {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/TBD.gif"/></figure>
    </td>
  </tr>
</table>
-->
