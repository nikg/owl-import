### **values.json**

**values.json** file specifies predefined values for the flow, as well as data mapping:

<table>
  <tr>
    <td>Property</td>
    <td>
      Description
    </td>
    <td>Example</td>
  </tr>
  <tr>
    <td><code>"init"</code></td>
    <td>
      predefined values for flow when we suppose that a value already exists. <code>"\_autofill": false</code> means that data won’t be shown in the <code>values</code> file and context for auto-filling when there’s a binding option
    </td>
    <td><pre><code>
"init": {{ '{' }}
  "start": {{ '{' }}
    "nameLabel": "Name",
    "companyLabel": "Company",
    "__autofill": false
    {{ '}' }}
  {{ '}' }}
    </code></pre>
    </td>
  </tr>
  <tr>
    <td><code>"mapping"</code></td>
    <td>
      mapping of data from the <code>values</code> file to simulator UI (and vice versa)
    </td>
    <td><pre><code>
"mapping": {{ '{' }}
 "ui": {{ '{' }}
    "__userInfo": {{ '{' }} 
      "user": {{ '{' }}
        "userName": "__userName",
        "company": "__userCompany"
        {{ '}' }}
    {{ '}' }}
  {{ '}' }}
{{ '}' }}
    </code></pre>
    </td>
  </tr>
</table>
