### **ANIMATED ARROW**

#### Control description

Arrow control lets us use an animated arrow which is perfect for design clues, easy navigation and various kinds of animations. It is created using the **output-animated-arrow** control and is also [available via Scenario Editor UI](/scenario-edit/snippets#arrow).

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
"type": "output-animated-arrow",
"position": [ 180, 100, 250, 250 ],
"visible": true,
"path": {{ '{' }}
  "points": [ [40, 1],  [10, 50],  [10, 50],  [4, 110] ],
  "style": {{ '{' }}
    "color": "#000000",
    "width": 5
    {{ '}' }}
  {{ '}' }},
"animation": {{ '{' }}
  "type": "data-success",
  "time": 1,
  "ease": "bounce",
  "delay": 0
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      <figure><img src="/assets/arrow-sample.gif"/></figure>
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
      <code>"output-animated-arrow"</code>
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
      <code>[10, 10, 100, 100]</code>
    </td>
    <td>
       It indicates properties of a rectangular in which our animated object is to be shown. The first two numbers represent coordinates of the rectangular, and the second two numbers represent its width and height.
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"path": {{ '{' }}
  "points":
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>path</code> is the curve for the animated object inside the rectangular specified by the 'position' coordinates. It consists of four control points: starting, two control and final point indicated as an array. Note that the starting point is the reference point for other coordinates inside the rectangular. Three other points are indicated relative to the starting one. Also note that the final point is located in the middle of the arrowhead.
      <pre><code>
"path": {{ '{' }}
  "points": [ [40, 1],  [10, 50],  [10, 50],  [4, 110] ]
  {{ '}' }}
      </code></pre>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"path": {{ '{' }}
  "style":
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>style</code> includes <code>color</code> and <code>width</code> in pixels.
      <pre><code>
"path": {{ '{' }}
  "style": {{ '{' }}
    "color": "#A4DE59",
    "width": 2
    {{ '}' }}
  {{ '}' }}
      </code></pre>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"animation": {{ '{' }}
  "type": "data-success"
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <pre><code>attack</code></pre> for a point without an arrowhead
      <pre><code>data-success</code></pre> for a success arrow
      <pre><code>data-failed</code></pre> for a failure arrow
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"animation": {{ '{' }}
  "time": 1
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
  "ease": "bounce"
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      This property is optional and defines how animation ends. For now “bounce” option is available.
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
</table>
