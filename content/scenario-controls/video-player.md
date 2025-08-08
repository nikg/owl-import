### **VIDEO**

#### Control description

This control lets us use video in the simulation. It is created using the **output-video-player** control. It is also [available via Scenario Editor UI](/scenario-edit/controls#control-multimedia).

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
"type": "output-video-player",
"position": ["0px", "0px", "500px", "500px" ],
"img": "./resources/folder/intro.mp4",
"settings": {{ '{' }}
 "start": "0",
  "stop": "3",
  "autoPlay": true
  {{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/video-player.gif"/></figure>
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
      <code>"output-video-player"</code>
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
      N/A
    </td>
    <td>
      It is applied if the control is not used in the sidebar but on the main screen. Any values can be specified:
      <pre><code>"position": ["10px", "10px", "1000px", "1000px"]</code></pre>
    </td>
  </tr>
   <tr>
    <td>
      <code>"size"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It is applied if the control is used in the sidebar and not on the main screen. Any values can be specified:
      <pre><code>"size": ["calc(var(--sidebar-size))", "172px"]</code></pre>
    </td>
  </tr>
  <tr>
    <td>
    <code>"shared::control1"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
       It is specified in the name of control to indicate that this control is shared between several screens and is not created again in other screens, where <code>control1</code> is the control name in this example.
         <pre><code>
"shared::control1": {{ '{' }}
  "type": "output-video-player"
  {{ '}' }}
        </code></pre>
    </td>
  </tr>
  <tr>
    <td>
        <code>"img"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines where the mp4 video is stored
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
      It defines events and their timing during the video. <code>onProgress</code> has <code>forced</code> property that executes the actions both in automatic and in manual modes.
      <pre><code>
"event": {{ '{' }}
  "onProgress": {{ '{' }}
    "forced:53.3": [
      "#include:./resources/js/email-test.js",
      "zoom: fit",
      "show: focus1",
      "hide: focus2, focus3, popup"
      ]
    {{ '}' }}
  {{ '}' }}
      </code></pre>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>      
"settings": {{ '{' }}
  "start": 
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines video start
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "stop": 
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines video end
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "idle": {{ '{' }}
    "switchToAuto": {{ '{' }}
      "timeout": 
      "action": 
      {{ '}' }}
    {{ '}' }}
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines when video will switch to auto mode, as well as its <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">actions</a>
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "progressInterval":
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines interval before progressing
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
 "autoPlay": 
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It can be <code>true</code> or <code>false</code> and defines if auto mode is enabled
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "startBtn": {{ '{' }}
    "img": 
    {{ '}' }}
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It specifies directory to the start button image
    </td>
  </tr>
</table>
