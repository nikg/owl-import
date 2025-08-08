### **GAUGE**

#### Control description

This control lets us simulate a gauge with range indicated. It is created using the **output-randomGauge** control.

#### Control example

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
"type": "output-randomGauge",
"position": [710, 1310, 600, 600],
"delay": 800,
"settings": {{ '{' }}
  "colors": ["#A9B0B5", "#000000"]
  {{ '}' }},
"range": {{ '{' }}
  "gauge": [0, 100],
  "value": [0, 75]
   {{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/gauge-sample.gif"/></figure>
    </td>
  </tr>
</table>

#### Control properties

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
      <code>"type"</code>
    </td>
    <td>
      <code>"output-randomGauge"</code>
    </td>
    <td>
      N/A
    </td>
  </tr>
  <tr>
    <td>
      <code>"position"</code>
    </td>
    <td>
     <code>[710, 1310, 300, 300]</code>
    </td>
    <td>
      Any values can be specified
    </td>
  </tr>
  <tr>
    <td>
      <code>"delay"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies delay for the gauge start, then data is generated automatically in milliseconds
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "colors": [ ]
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies gauge colors
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"range": {{ '{' }}
  "gauge": [ ]
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies gauge range as an array
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"range": {{ '{' }}
  "value": [ ]
   {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies gauge values as an array
    </td>
  </tr>
</table>
