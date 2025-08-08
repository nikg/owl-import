### **FIELD**

#### Control description

Field is created using the **input-text** control and is also [available via Scenario Editor UI](/scenario-edit/controls#control-field). It is used as an input field to let users enter data in a single line. Fields can have hints and be used as a reference for the [label](/scenario-controls/label) control based on their key.

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
"type": "input-text",
"position": [ 144, 499, 234, 60 ],
"hint": "Enter project name.",
"hintOptions": &#123; "position": "top-left" &#125;,
"settings": {{ '{' }} "placeholder": "Name" {{ '}' }},
"style": [ ]
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/field-sample.png"/></figure>
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
     <code>"input-text"</code>
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
     <code>[ 144, 499, 234, 60 ]</code>
   </td>
   <td>
            Any values can be specified
   </td>
  </tr>
  <tr>
   <td>
    <pre><code>
"settings":
  {{ '{' }}"placeholder":
  {{ '}' }}
      </code></pre>
   </td>
   <td>
    N/A
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
      <pre><code>
"hintOptions":
  {{ '{' }}"no box":
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      <code>true</code>
    </td>
    <td>
      <code>true</code> <code>false</code>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"hintOptions":
  {{ '{' }}"position":
  {{ '}' }}
      </code></pre>
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
      <pre><code>
"action": [
  {{ '{' }}
  "value":
  "action":
  {{ '}' }}
  ]
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>"action": ["next", "save", "show", "hide", "skip", "switch", "toggle", "focus", "set", "zoom" ]</code> <br><br>More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>. <br><br><code>"value":</code> Any value can be indicated. Action is fulfilled when the value is typed into the input field.
    </td>
  </tr>
    <tr>
    <td>
      <pre><code>
"action": [
  {{ '{' }}
  "caseSensitive":
  {{ '}' }}
  ]
      </code></pre>
    </td>
    <td>
      <code>false</code>
    </td>
    <td>
      <code>true</code> <code>false</code> for case sensitive actions.
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
