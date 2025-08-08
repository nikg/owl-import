### **TIMESTAMP**

#### Control description

This control lets apply timestamp on a screen. It is created using the **output-timestamp** control.

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
<ul>
<li><b>control properties in json:</b>
"type": "output-timestamp",
"position": [3830, 1174, 508, 68],
"style": [ ]</li>
<li><b><a href="https://docs.upmix.it/scenario/screens#meta-file">binding</a> in json:</b>
"binding": {{ '{' }}
  "controlID": "wizardGeneratedModel.timestamp"
{{ '}' }}
</li>
</ul>
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/timestamp-sample.png"/></figure>
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
      <code>"output-timestamp"</code>
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
    <code>[3830, 1174, 508, 68]</code>
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
      Style can be specified in the <a href="https://docs.upmix.it/scenario/styles">CSS</a> file.
    </td>
  </tr>
</table>
