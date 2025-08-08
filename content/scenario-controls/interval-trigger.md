### **INTERVAL TRIGGER**

#### Control description

This control lets us repeat the same action every indicated period of time by triggering it. It is created using the **system-trigger-interval** control.

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
"type": "system-trigger-interval",
"interval": 4000,
"action": ["show:<a href="https://docs.upmix.it/scenario-controls/html-control">popup</a>"]
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
      <code>"system-trigger-interval"</code>
    </td>
    <td>
      N/A
    </td>
  </tr>
  <tr>
    <td>
      <code>"interval"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any interval in milliseconds can be specified
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
      <pre>
      <code>
      "save"
      "next"
      "show"
      "hide"
      "skip"
      "switch"
      "toggle"
      "focus"
      "set"
      "zoom"
      </code>
      </pre>
      More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
    </td>
  </tr>
</table>
