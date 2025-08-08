### **IMAGE**

#### Control description

Image is one of supported multimedia types and is created using the **output-img** control. It is also [available via Scenario Editor UI](/scenario-edit/controls#control-multimedia).

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
"type": "output-img",
"position": [ 144, 499, 80, 80 ],
"img": "./resources/folder/portal-image.png"
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/img-control.png"/></figure>
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
      <code>"output-img"</code>
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
     <code>[ 144, 499, 80, 80 ]</code>
    </td>
    <td>
      Any values can be specified
    </td>
  </tr>
  <tr>
    <td>
        <code>"img": "./resources/portal-image.png"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      Image path is to be indicated or its URL link.
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
  <tr>
    <td>
        <code>"visible"</code>
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
"animation": {{ '{' }}
  "style": "like-gif steps(40) 2s forwards",
  "pos": "-2200px"
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>"forwards"</code> <code>"infinite"</code>
    </td>
  </tr>
</table>
