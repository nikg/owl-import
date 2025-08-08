### **MOUSE TRIGGER**

#### Control description

This control lets trigger actions based on mouse actions: mousever and mouseout. It is created using the **system-trigger-mouse** control.

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
"type": "system-trigger-mouse",
"position": ["10px", "10px", "100px", "100px" ],
"onMouseOver": [ "show: img" ],
"onMouseLeave": [ "hide: img" ]
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/mouse-trigger-anim.gif" width="45%"/></figure>
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
      <code>"system-trigger-mouse"</code>
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
      N/A
    </td>
    <td>
      Any position can be specified
    </td>
  </tr>
  <tr>
    <td>
      <code>"onMouseOver"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies controls and actions for mouseover, e.g.:
      <code>["show: pop-up", "hide: button"]</code>
      <br><br>More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
    </td>
  </tr>
  <tr>
    <td>
      <code>"onMouseLeave"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies controls and actions for mouseout, e.g.:
      <code>["show: pop-up", "hide: button"]</code>
      <br><br>More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
    </td>
  </tr>
</table>
