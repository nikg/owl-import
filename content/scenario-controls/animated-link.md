### **ANIMATED LINE**

#### Control description

Animated line is a dotted line that is used for connecting or relating different elements. It is created using the **output-animated-link** control.

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
    <pre>
    <code>
"type": "output-animated-link",
"position": [ 140, 45, 250, 250 ],
"path": {{ '{' }}
  "points": [ [ 5, 5 ], [ 5, 5 ], [ 5, 5 ], [ 5, 665 ] ],
  "style": {{ '{' }}
    "dash-array": [20, 5],
    "color": "#000000",
    "width": 5.5
    {{ '}' }},
  "marker": {{ '{' }}
    "size": 5,
    "start": "circle",
    "end": "circle"
    {{ '}' }}
    {{ '}' }},
"animation": {{ '{' }}
  "time": 0.35,
  "increment": 25,
  "delay": 0.2,
  "yoyo": true
  {{ '}' }}
     </code>
    </pre>
    </td>
    <td>
      <figure><img src="/assets/line-anim.gif" width="45%"/></figure>
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
    <code>[ 1380, 1300, "100px", "10px" ]</code>
    </td>
    <td>
      It indicates properties of a rectangular in which our animated object is to be shown. The first two numbers represent coordinates of the rectangular, and the second two numbers represent its width and height.
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"path": {{ '{' }}
  "points": [ [40, 1],  [10, 50],  [10, 50],  [4, 110] ]
   {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>path</code> is the curve for the animated object inside the rectangular specified by the 'position' coordinates. <code>path</code> consists of four control points: starting, two control and final point indicated as an array. Note that the starting point is the reference point for other coordinates inside the rectangular. Three other points are indicated relative to the starting one.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"path": {{ '{' }}
  "style": {{ '{' }}
    "dash-array": [20, 5],
    "color": "#666666",
    "width": 2.5
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>style</code> includes <code>dash-array</code>, <code>color</code> and <code>width</code> in pixels.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"animation": {{ '{' }}
  "increment": 25
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any values can be indicated.
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
  "yoyo": true
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
       Defines if animation will move one way and then back and can be: <code>true</code> or <code>false</code>
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
"marker": {{ '{' }}
  "size": 5
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines line marker size
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"marker": {{ '{' }}
  "start": "circle",
  "end": "circle"
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>circle</code>
    </td>
  </tr>
</table>
