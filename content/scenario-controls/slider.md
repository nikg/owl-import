### **SLIDER**

#### Control description

Slider is created using the **input-slider** control. It is also [available via Scenario Editor UI](/scenario-edit/controls#control-slider). This control allows you to pick a value by dragging a pin along its bar.

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
"type": "input-slider",
"position": [200, 320, 500, 50],
"settings": {{ '{' }}
  "theme": "material-ui",
  "color": {{ '{' }}
  "bar": "rgb(0, 0, 255)",
  "pin": "rgb(0, 0, 255)"
   {{ '}' }},
  "showTicks": true,
  "values": {{ '{' }}
  "type": "range",
  "data": [0, 10]
  {{ '}' }}
{{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/slider-example.png"/></figure>
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
      <code>"input-slider"</code>
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
     <code>[200, 320, 1600, 50]</code>
    </td>
    <td>
      Any values can be specified
    </td>
  </tr>
  <tr>
    <td>
      <code>"theme"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
        <code>"material-ui"</code>
    </td>
  </tr>
  <tr>
    <td>
      <code>"action"</code>
    </td>
    <td>
    N/A
    </td>
    <td>
      <pre><code>
      "action": {{ '{' }}
        "1": [
          "show: btn-test"
        ],
        "3": [
          "hide: btn-test"
        ]
      {{ '}' }}
      </code></pre>
      More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"color":
  "bar":
  "pin":
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any colors can be specified
    </td>
  </tr>
  <tr>
    <td>
        <code>"showTicks"</code>
    </td>
    <td>
        <code>false</code>
    </td>
    <td>
       <code>false</code> <code>true</code>
    </td>
  </tr>
  <tr>
    <td>
        <code>"discrete"</code>
    </td>
    <td>
        <code>false</code>
    </td>
    <td>
       <code>false</code> <code>true</code>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"values":
  "type":
       </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
        <code>"range"</code>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"values":
  "data":
      </code></pre>
    </td>
    <td>
        <code>[1, 10]</code>
    </td>
    <td>
      Any data range can be indicated
    </td>
  </tr>
  <tr>
    <td>
        <code>"style"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any style can be specified. More info on styles can be found <a href="https://docs.upmix.it/scenario/styles">here</a>.
    </td>
  </tr>
  <tr>
    <td>
        <code>"orderNumber"</code>
    </td>
    <td>
      sequential numbering
    </td>
    <td>
      Any number can be given.
    </td>
  </tr>
</table>
