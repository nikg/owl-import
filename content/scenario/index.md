### **index.json**

**index.json** gives general information about scenarios. Each scenario should have an **index.json** file that can specify:

- scenario title, description and icon
- scenario tags
- what systems scenario is integrated with
- steps of the scenario
- controls that can be used on all screens.

The structure of **index.json** can include the following objects: **integration**, **title**, **settings**, **all-screen-controls** & **steps** with their own keys and values.

Scenarios can have videos, and auto mode can be used in that case. Auto mode means that the scenario will automatically move from one step to another based on some trigger. If auto mode is selected, then the whole scenario created for the video is on. If manual mode is selected, only video is on.

<table>
  <tr>
    <td>Object</td>
    <td>
      Key
    </td>
    <td>Description</td>
    <td>Example</td>
  </tr>
  <tr>
    <td>"integration"</td>
    <td>
      "module"
    </td>
    <td>defines what scenario is integrated with</td>
    <td><code>"integration": {{ '{' }} 
      "module": [ 
        "marketo", "tealium" 
        ] {{ '}' }}</code>
    </td>
  </tr>
  <tr>
    <td rowspan="3" style="vertical-align: middle;">"settings"</td>
    <td>
      "visible"
    </td>
    <td>
      defines if the script is visible on the list among other scenarios. If “visible” is “false”, then the script isn’t shown there, but we can jump to it directly from other scripts if it’s indicated in them.
    </td>
    <td><code>"settings": {{ '{' }} "visible": false {{ '}' }}</code>
    </td>
  </tr>
  <tr>
    <td>
      "autoMode"
    </td>
    <td>defines auto-mode for the script. If it’s not specified, then it’s “false” by default.</td>
    <td><code>"settings": {{ '{' }}
      "autoMode": {{ '{' }}
        "enabled": true, 
        "default": true 
      {{ '}' }} 
    {{ '}' }}</code>
    </td>
  </tr>
  <tr>
    <td>
      "cta"
    </td>
    <td>specifies requirements for the call to action.</td>
    <td><pre><code>
"cta": {{ '{' }}
 "header": {{ '{' }}
   "link": {{ '{' }}
    "title": "Learn more about this app",
     "href": "TBD"
     {{ '}' }}
    {{ '}' }},
 "sidebar": {{ '{' }}
  "box": "{{ '<' }}div class='scenario-cta-class' onclick='ctaClick()'{{ '>' }}Contact our expert!{{ '<' }}div{{ '>' }}"
  {{ '}' }}
{{ '}' }}
    </code></pre>
    </td>
  </tr>
  <tr>
    <td>"all-screen-controls"</td>
    <td>
      "all-screen-form-marketo"
    </td>
    <td>specifies the controls that will be used on all screens</td>
    <td><pre><code>
"all-screen-controls": {{ '{' }}
 "all-screen-form-marketo": {{ '{' }}
  "type": "integration-form-submit--marketo",
  "position": ["10px", "10px", "200px", "200px" ],
  "action": {{ '{' }}
  "hide": [
    "hide: all-screen-form-marketo"
    ],
  "submit": [
    "hide: all-screen-form-marketo",
    "eval: (bm, bd, ap) => cside.monitor('form-submit', 'cta', 'tbd', ap)"
    ],
  "silentSubmit": [
    "hide: all-screen-form-marketo"
    ]
  {{ '}' }}
 {{ '}' }}
{{ '}' }}
     </code></pre>
    </td>
  </tr>
  <tr>
    <td rowspan="5" style="vertical-align: middle;">"tile"</td>
    <td>
      "title"
    </td>
    <td>defines name of your scenario</td>
    <td><code>"tile": {{ '{' }}
      "title": "Scenario Title"{{ '}' }}</code>
    </td>
  </tr>
  <tr>
    <td>
      "text"
    </td>
    <td>provides description for your scenario</td>
    <td><code>"tile": {{ '{' }}
        "text": "Scenario Description."{{ '}' }}</code>
    </td>
  </tr>
  <tr>
    <td>
      "icon"
    </td>
    <td>
      scenario icon which is stored in “images” folder and the route is indicated as follows: "icon": "./images/icon.png
    </td>
    <td><code>"tile": {{ '{' }}
        "icon": "./resources/img/main-icon.png",{{ '}' }}</code>
    </td>
  </tr>
  <tr>
    <td>
      "tags"
    </td>
    <td>any tags for your scenario can be indicated here</td>
    <td><code>"tile": {{ '{' }}
    "tags": [ "TAG1", "TAG2" ],{{ '}' }}</code>
   </td>
  </tr>
  <tr>
    <td>
      "orderNumber"
    </td>
    <td>it defines the order of scenarios on the landing page</td>
    <td><code>"tile": {{ '{' }}
        "orderNumber": 1,{{ '}' }}</code>
    </td>
  </tr>
  <tr>
    <td rowspan="2" style="vertical-align: middle;">"steps"</td>
    <td>
      "order"
    </td>
    <td>defines the order of steps and is indicated as an array</td>
    <td><pre><code>
"steps": {{ '{' }}
  "order": [
    "step1",
    "step2",
    "step3"
    ]
  {{ '}' }}</code></pre>
    </td>
  </tr>
  <tr>
    <td>
      "data"
    </td>
    <td>
      “data” object enumerates steps and their keys (“title”, “description”, “screens”) and values; “screens” can be set to “default” and engine will go through all screens in the “screens” subfolder
    </td>
    <td><pre><code>
"data": {{ '{' }}
  "intro": {{ '{' }}
    "title": "Intro",
    "screens": {{ '{' }}
      "default": true
      {{ '}' }}
    {{ '}' }}
{{ '}' }}</code></pre>
    </td>
  </tr>
</table>
