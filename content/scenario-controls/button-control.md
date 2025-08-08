### **BUTTON**

#### Control description

Button is created using the **button** control and is also [available via Scenario Editor UI](/scenario-edit/controls#control-hotspot). It allows you to take action specified in its properties. Buttons are clickable, should have an action indicated and can’t output text, hence can be combined with a [label](/scenario-controls/label) control over them.

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
"type": "button",
"position": [ 1380, 1300, 123, 32 ],
"hint": "Click the button to save the form.",
"hintOptions": &#123; "position": "top-left" &#125;,
"action": [ "next" ]
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/button-1.png"/></figure>
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
      <code>"button"</code>
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
    <code>[ 1380, 1300, 123, 32 ]</code>
    </td>
    <td>
      Any values can be specified
    </td>
  </tr>
  <tr>
    <td>
    <code>"hint"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any text can be specified. <code>#</code> can be used if there's no hint
    </td>
  </tr>
  <tr>
    <td>
        <code>"hintOptions": &#123;"no box"&#125;</code>
    </td>
    <td>
      <code>true</code>
    </td>
    <td><code>true</code> <code>false</code>
    </td>
  </tr>
  <tr>
    <td>
      <code>"hintOptions": &#123;"position"&#125;</code>
    </td>
    <td>
      <code>"right"</code>
    </td>
    <td>
      <pre><code>
"left"
"top-left"
"top"
"top-right"
"right"
"bottom-right"
"bottom"
"bottom-left"
      </code></pre>
    </td>
  </tr>
  <tr>
    <td>
      <code>"action"</code>
    </td>
    <td>
    <code>"save", "next"</code>
    </td>
    <td>
      <pre><code>
"save"
"next"
"show"
"hide"
"skip"
"skip-screen-shortName"
"switch"
"toggle"
"focus"
"set"
"zoom"
      </code></pre>
      More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
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
