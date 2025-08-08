### **DROPDOWN TAGS**

#### Control description

Dropdown tags control offers multiple choice options to the user available from the dropdown menu. It is created using the **input-dropDown-tags** control.

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
"type": "input-dropDown-tags",
"position": [ 960, 519, 2800, 96 ],
"hint": "Select the region",
"items": ["USA", "Europe", "Asia"],
"settings": {{ '{' }}
  "placeholder": "Pick a region"
  {{ '}' }},
"hintOptions": {{ '{' }}
  "auto": [],
  "position": "right"
  {{ '}' }},
"action": [
  {{ '{' }}
  "values": [],
  "action": ["save", "next"]
  {{ '}' }}
  ]
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/dropdown-tags.png"/></figure>
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
      <code>"input-dropDown-tags"</code>
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
     <code>[ 960, 519, 2800, 96 ]</code>
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
"hintOptions":
  {{ '{' }}"auto":
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      We can use the following modifier for the <code>"auto"</code>: <code>"toDropDown:field:model.control"</code> if we need to show not an object from this control, but a field from another object (eg, from a <a href="https://docs.upmix.it/scenario-controls/field-control">field</a> control).
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"action": [
  {{ '{' }}
  "values": [],
  "action": []
  {{ '}' }}
  ]
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
    <code>"action": ["next", "save", "show", "hide", "skip", "switch", "toggle", "focus", "set", "zoom" ]</code><br><br> More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.<br><br> <code>"values":</code> is case-sensitive and can be indicated in any sequence. If some action is needed in case of no choice, then values are indicated as empty brackets <code>[ ]</code>
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
      Any value can be specified as an array <code>[ , , ]</code> or as a reference to some collection <code>"ref:collection"</code>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"bindingOptions":{{ '{' }}
  "oneWay": 
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      <code>true</code> <code>false</code>
    </td>
    <td>
      <code>"bindingOptions"</code> can be <code>"oneWay"</code> (<code>true</code> or <code>false</code>).<br><br> <code>"oneWay"</code> means that if a model contains any data, this data will not be shown.
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
