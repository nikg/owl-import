### **TIMELINE**

#### Control description

System timeline enables actions at their specified timing. It is also [available via Scenario Editor UI](/scenario-edit/controls#control-timeline). It is created using the **system-trigger-timeline** control.

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
"type": "system-trigger-timeline",
"loop": false,
"timeline": {{ '{' }}
   "1": [ "hide: popup" ],
   "2000": [ "show: popup" ]
  {{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/html-sample.gif"/></figure>
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
      <code>"system-trigger-timeline"</code>
    </td>
    <td>
      N/A
    </td>
  </tr>
  <tr>
    <td>
      <code>"loop"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>true</code> <code>false</code>
    </td>
  </tr>
  <tr>
    <td>
      <code>"timeline"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies actions and their timing in milliseconds, e.g.:
      <pre><code>
"timeline": {{ '{' }}
  "100": [ "show: arrow1" ],
  "2000": [ "focus: open" ]
  "9500": [ "show: img-btn-next, next-btn" ]
{{ '}' }}
      </code></pre>
      More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
    </td>
  </tr>
</table>
