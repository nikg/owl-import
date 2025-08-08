### **COUNTER**

#### Control description

This control lets us simulate a counter with any units needed. It is created using the **output-randomCounter** control.

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
"type": "output-randomCounter",
"position": [710, 1310, 300, 300],
"counter": {{ '{' }}
  "range": [1, 100],
  "period": 0.5
  {{ '}' }},
"legend": "%",
"style": {{ '{' }}
  "gradientRadius": "100",
  "radius": 50,
  "color": "#0000",
  "font": {{ '{' }}
    "size": "40px",
    "lineHeight": "30px"
    {{ '}' }}
  {{ '}' }},
"animation": {{ '{' }}
  "ease": "none",
  "delay": 0,
  "duration": 5
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/counter-sample.gif"/></figure>
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
      <code>"output-randomCounter"</code>
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
     <code>[710, 1310, 300, 300]</code>
    </td>
    <td>
      Any values can be specified
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"counter": {{ '{' }}
  "range": [700, 1000]
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies counter range
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"counter": {{ '{' }}
  "period": 0.5
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies period of counter range change
    </td>
  </tr>
  <tr>
    <td>
      <code>"legend": "ms"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies counter units
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"animation": {{ '{' }}
  "duration": 1
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any time can be indicated.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"animation": {{ '{' }}
  "ease": 
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines how animation appears:
      <pre><code>none</code></pre> without effects
      <pre><code>elastic</code></pre> gives a springy feel to animation
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"animation": {{ '{' }}
  "delay": 0
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines delay of animation start and can be any.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"style": {{ '{' }}
  "gradientRadius": "100",
  "radius": 50,
  "color": "#000000",
  "font": {{ '{' }}
    "size": "40px",
    "lineHeight": "30px"
    {{ '}' }}
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Various style properties can be specified.
    </td>
  </tr>
</table>
