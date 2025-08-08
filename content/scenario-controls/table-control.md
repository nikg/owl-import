### **TABLE**

#### Control description

This control is used to locate [generated data](/scenario-controls/generator#data-generator) in a table. It is created using the **output-table** control.

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
<li><b>control in json:</b>
      "type": "output-table",
      "position": [
        "300px",
        "3220px",
        "4210px",
        "600px"
      ],
      "maxRows": 4,
      "columns": {{ '{' }}
        "binding": {{ '{' }}
          "date": "DATE",
          "app": "APP",
          "attack-type": "ATTACK TYPE"
        {{ '}' }}
      {{ '}' }},
      "visible": true,
      "style": [
        "table-attacks"
      ]</li>
<li><b>control style in <a href="https://docs.upmix.it/scenario-edit/assets#default-asset-groups">assets</a>:</b>
.table-attacks {{ '{' }}
    width: 1000px;
    background-color: white;
    border: 3px solid rgb(224, 224, 224);
{{ '}' }}
.table-attacks tr {{ '{' }}
    border: 3px solid rgb(224, 224, 224);
{{ '}' }}
.table-attacks th {{ '{' }}
    font-family: proxima-nova;
    font-size: 42px;
    padding: 0px 36px;
    height: 99px;
{{ '}' }}
</li>
</ul>
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/generator.png"/></figure>
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
      <code>"output-table"</code>
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
     <code>[ 300, 3220, "4210px", "428px" ]</code>
    </td>
    <td>
      Any values can be specified
    </td>
  </tr>
  <tr>
    <td>
      <code>"maxRows"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies the required number of rows
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "reverseRows":
{{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It lets show table rows in the reverse order and can be <code>true</code> or <code>false</code>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"columns": {{ '{' }}
  "binding": {{ '{' }}
    {{ '}' }}
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies names of columns under <code>binding</code> (binding between model field and table column name).
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
      It specifies table style via the <a href="https://docs.upmix.it/scenario/styles">CSS</a> file.
    </td>
  </tr>
</table>
