### **TIMER**

#### Control description

Timer lets us execute an action at its set time. It is created using the **system-trigger-timer** control.

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
"type": "system-trigger-timer",
"timeOut": 1,
"action": ["show:popup"]
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
      <code>"system-trigger-timer"</code>
    </td>
    <td>
      N/A
    </td>
  </tr>
  <tr>
    <td>
      <code>"timeOut"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It is specified in milliseconds
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
      It specifies actions. More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
    </td>
  </tr>
</table>
