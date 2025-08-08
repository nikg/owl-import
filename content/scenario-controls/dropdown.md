### **DROPDOWN MENU**

#### Control description

Dropdown menu is created using the **input-dropDown-list** control. Created dropdown menu is a list of options that is revealed after a user clicks it. The menu options appear vertically.

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
"type": "input-dropDown-list",
"position": [ 130, 130, 123, 32 ],
"hint": "Click to open the dropdown menu.",
"hintOptions": &#123; "position": "top-left" &#125;,
"items": ["Default Preview Theme", "Bezel Preview Theme"],
"action": [ "save", "next" ]
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/drop-down-sample.png"/></figure>
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
      <code>"input-dropDown-list"</code>
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
     <code>[ 130, 130, 123, 32 ]</code>
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
    <td>
      <code>true</code> <code>false</code>
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
        <code>"items"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      Items can be specified as:
      <ul>
      <li> an array: <code>[ , , ]</code></li>
      <li> a reference to some collection: <code>"ref:collection"</code></li>
      <li> a reference to a field: <code>"field:regions.regionName</code>" (where <code>region</code> is a model, <code>regionName</code> is a field)</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
        <code>"defaultItems"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>defaultItems</code> is shown on the drop-down list as a default option and include <code>value</code> to be shown and <code>label</code>:
      <pre><code>
"items": "format:{{ '{' }}0{{ '}' }}|region|regionName",
"defaultItems": [{{ '{' }}"value": "Anywhere", "label": "Anywhere"{{ '}' }}]
      </code></pre>
    </td>
  </tr>
  <tr>
    <td>
        <code>"action"</code>
    </td>
    <td>
      <pre>
      <code>
      "save",
      "next"
      </code>
      </pre>
    </td>
    <td>
      <pre><code>
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
