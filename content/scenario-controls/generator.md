### **DATA GENERATOR**

#### Control description

This control lets us generate data in predefined ranges / lists. The data is generated into a model as a list and is specified as an array. Note that in order to get access to the full list and not only its last element, we indicate the name of the whole list in the **context**:

<pre><code>
"model": "generatedData[]",
"context": [ "generatedData" ]
</code></pre>

Also note that in model **binding** element, we indicate that our [table](/scenario-controls/table-control) is bound with the list indicated in **context**.

<pre><code>
  "binding": {{ '{' }}
    "table-attacks": "generatedData",
    "generated-control": "*"
  {{ '}' }}
</code></pre>

Binding can include equations, which can have JS functions after **eval**. It can be used to show, say, the total number of attacks generated.

Several generators can be included in one model. They will generate data and insert it into the array as the last element.

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
"type": "system-generator",
"selector": "rand",
"interval": 1,
"bindObj": [
  {{ '{' }}
  "ts": {{ '{' }} "exact": "format:{{ '{' }}0{{ '}' }}|now()|MMM dd, yyyy HH:mm:ss.SSS" {{ '}' }},
  "date": {{ '{' }} "exact": "format:{{ '{' }}0{{ '}' }}|now()|MMM dd, yyyy" {{ '}' }},
  "app": {{ '{' }}
    "random-range": [
      "App1",
      "App2"
      ]
    {{ '}' }},
  "attack-type": {{ '{' }}
    "random-range": [
      "Forceful Browsing",
      "Non-browser Client",
      "Information Leakage",
      "Abuse of Functionality"
      ]
    {{ '}' }}
  {{ '}' }}
  ]
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
      <code>"system-generator"</code>
    </td>
    <td>
      N/A
    </td>
  </tr>
  <tr>
    <td>
    <code>"selector"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      <pre><code>rand</code></pre> for random selection among array
      <pre><code>iterate</code></pre> for one-by-one selection from the top to the bottom
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
      It defines how often data is generated and is indicated in seconds
    </td>
  </tr>
  <tr>
    <td>
      <code>"bindObj"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
  <code>Timestamp</code> is responsible for the frequency of model data display.

 <pre><code>"ts": {{ '{' }} "exact": "format:{{ '{' }}0{{ '}' }}|now()|MMM dd, yyyy / HH:mm:ss" {{ '}' }}</code></pre>

The data for each column of the table is defined below accordingly. Columns can be specified: as a string, as an object, as an HTML to show images which are to be stored in resources.

  <pre><code> "date": {{ '{' }} "exact": "format:{{ '{' }}0{{ '}' }}|now()|MMM dd, yyyy / HH:mm:ss" {{ '}' }}</code></pre>

  </tr>
</table>
