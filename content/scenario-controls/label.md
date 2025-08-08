### **LABEL**

#### Control description

Label is created using the **label** control also [available via Scenario Editor UI](/scenario-edit/controls#control-label). This control displays text over pre-defined area that cannot be edited by the user. It is not clickable so if we want it to lead us to the next step, we add a [button](/scenario-controls/button-control) which is clickable and can move us on.

The label control can display:

- a pre-defined value indicated in the [values.json](/scenario/values) file or
- a value filled in by the user earlier in a [field](/scenario-controls/field-control) referenced in screen **binding** property.

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
<ul><li><b>label control</b>:
"type": "label",
"position": [ 144, 499, 234, 60 ],
"style": [ ]</li>
<li><b><a href="https://docs.upmix.it/scenario/screens#meta-file">binding reference</a></b>:
"binding": {{ '{' }}
    "label": "wizardGeneratedModel.referenceControlId"
  {{ '}' }}</li>
  </ul>
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/label-sample.png"/></figure>
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
      <code>"label"</code>
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
