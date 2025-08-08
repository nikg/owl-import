### **ANIMATION**

#### Control description

Animation is implemented using the lightweight and scalable LottieFile animation. It is a JSON-based file format that simplifies the process of animation delivery and is suitable for demos and mini animations. It is created using the **output-animation-lottie** control and is also [available via Scenario Editor UI](/scenario-edit/controls#control-multimedia).

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
"type": "output-animation-lottie",
"position": [ 650, 100, 500, 500 ],
"img": "./resources/lottie.json",
"animation": {{ '{' }} "loop": true, "speed": "1" {{ '}' }}
     </code>
    </pre>
    </td>
    <td>
      <figure><img src="/assets/lottie.gif"/></figure>
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
    <code>"output-animation-lottie"</code>
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
    <code>[ 650, 100, 500, 500 ]</code>
    </td>
    <td>
       Any values can be specified
    </td>
  </tr>
  <tr>
    <td>
    <code>"img": "./resources/lottie.json"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      Indicates file directory.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"animation": {{ '{' }} 
  "loop": true
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td><code>true</code> <code>false</code>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"animation": {{ '{' }}
  "speed": "1"
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Indicate required speed.
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
    <code>"event"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      <pre><code>onComplete</code></pre> enables actions when the animation is over
      <pre><code>onStart</code></pre> enables actions when the animation starts
      <pre><code>onFrame</code></pre> enables actions at specified time frame
      <pre><code>
"event": {{ '{' }}
  "onComplete": [ "save"],
  "onFrame": {{ '{' }}
  "2%": "show: img-btn-skip",
  "85%": "show: btn-marketing, btn-partners"
  {{ '}' }}
{{ '}' }}
      </code></pre> More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "startBtn": {{ '{' }}
    "text": "Click here to start animation",
    "style": "startBtnStyle",
    {{ '}' }}
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      This feature is used in cases when animation is on, but sound isn't unless you press this button.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "overflow": "hidden"
   {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <pre><code>hidden</code></pre> shows only part of screen inside the 'position' area. Animation is to be positioned relatively to the upper left corner (0; 0).
      <pre><code>scroll</code></pre> means that style for Lottie is specified in the main <a href="https://docs.upmix.it/scenario/styles">css</a> file.
    </td>
  </tr>
</table>
