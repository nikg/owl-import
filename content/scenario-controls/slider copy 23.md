### **Controls**

#### **BUTTON**

Button is created using the **button** control. It allows you to take action specified in its properties. Buttons are clickable, should have an action indicated and can’t output text, hence can be combined with a [**label**](/scenario-controls/controls-meta#label) control over them.

Here's an example of a button:

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
    "controls": &#123;
        "btn-next": &#123;
        "type": "button",
        "position": [ 1380, 1300, 123, 32 ],
        "hint": "Click the button to save the form.",
        "hintOptions": &#123; "position": "top-left" &#125;,
        "action": [ "next" ]
       &#125;
     &#125;
    </pre>
    </td>
    <td>
      <figure><img src="/assets/button-1.png"/></figure>
    </td>
  </tr>
</table>

Button properties include:

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
    <pre>
      "type"
    </pre>
    </td>
    <td>
    <pre>
      "button"
    </pre>
    </td>
    <td>
      N/A
    </td>
  </tr>
  <tr>
    <td>
    <pre>
      "position"
    </pre>
    </td>
    <td>
    <pre>
      "10px",
      "10px",
      "100px",
      "100px"
    </pre>
    </td>
    <td>
      Any values can be specified
    </td>
  </tr>
  <tr>
    <td>
    <pre>
      "hint"
    </pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any text can be specified. `#` can be used if there's no hint
    </td>
  </tr>
  <tr>
    <td>
      <pre>
        "hintOptions" &#123;"no box"&#125;
      </pre>
    </td>
    <td>
      <pre>
      true
      </pre>
    </td>
    <td>
      <pre>
      true
      false
      </pre>
    </td>
  </tr>
  <tr>
    <td>
      <pre>
        "hintOptions" &#123;"position"&#125;
      </pre>
    </td>
    <td>
      <pre>
      "right"
      </pre>
    </td>
    <td>
      <pre>
      "left"
      "top-left"
      "top"
      "top-right"
      "right"
      "bottom-right"
      "bottom"
      "bottom-left"
      </pre>
    </td>
  </tr>
  <tr>
    <td>
      <pre>
        "action" 
      </pre>
    </td>
    <td>
      <pre>
      "save",
      "next"
      </pre>
    </td>
    <td>
      <pre>
      "save"
      "next"
      "show"
      "hide"
      "skip"
      "switch"
      "toggle"
      "focus"
      "set"
      "zoom"
      </pre>
      More info on actions can be found here.
    </td>
  </tr>
  <tr>
    <td>
      <pre>
        "style"
      </pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any style can be specified. More info on styles can be found here.
    </td>
  </tr>
  <tr>
    <td>
      <pre>
        "orderNumber"
      </pre>
    </td>
    <td>
      sequential numbering
    </td>
    <td>
      Any number can be given.
    </td>
  </tr>
</table>

#### **DROPDOWN MENU**

Dropdown menu is created using the **input-dropDown-list** control.

Here's an example of a dropdown menu:

TBD

This control has the following properties:

- `“items”` with its value specified as

a. an array: `[ , , ]`

b. a reference to some collection: `“ref:collection”`

c. a reference to a field: `“field:regions.regionName”` (where “region” is a model, “regionName” is a field)

```typescript
"controls": &#123;
   "regionName": &#123;
     "type": "input-dropDown-list",
     "position": [ 1380, 1300, 123, 32 ],
     "hint": "Open the drop-down menu.",
     "items": "field:region.regionName"
   &#125;
&#125;
```

- `“defaultItems”` shown on the drop-down list as a default option, and including “value” to be shown and “label”:

```typescript
"items": "format:{{ '{' }}0{{ '}' }}|region|regionName",
"defaultItems": [{{ '{' }}"value": "Anywhere", "label": "Anywhere"{{ '}' }}]
```

- `“position”`

```typescript
"position": [ 1380, 1300, 123, 32 ]
```

- `“hint”` (can also have `“format”` and `“fields”`)

- `“hintOptions”` which can have `“auto”` and `“position”` elements

- `“bindingOptions”` which can be `“oneWay”` (true/ false). This property should be indicated for all text-input controls. `“oneWay”` means that if a model contains any data, this data will not be shown.

- `“action”` which means action for a definite “item” choice.

```typescript
"items": ["A", "B", "C"],
"action": {{ '{' }}"A": ["save", "next"] {{ '}' }}
```

#### **input-dropDown-tags**

This control can have the following properties:

- `“items”` with its value specified as an array `[ , , ]` or as a reference to some collection `“ref:collection”`

- `“position”`

- `“hint”`

- `“hintOptions”` including `“position”` and `“auto”` properties. We can use the following modifier for the `“auto”`: `"toDropDown:field:model.control"` in case we need to show in this "input-dropDown-tag" not an object from this control, but a field from another object (ex, some "input-text" control).

```typescript
     "type": "input-dropDown-tags",
     "position": [ 1380, 1300, 123, 32 ],
     "hint": "Open the drop-down menu.",
     "hintOptions": {{ '{' }}
        "position": "left",
        "auto": "toDropDown:field:gateway[].gatewayDisplayName"
     {{ '}' }}
```

- `“bindingOptions”` can be `“oneWay”` (true/ false). `“oneWay”` means that if a model contains any data, this data will not be shown.

- `"action"` including "values" (which are case-sensitive and can be indicated in any sequence) and the "action" itself. If some action is needed in case of no choice, then values may be indicated as empty brackets `[ ]`:

```typescript
"filter": {{ '{' }}
      "type": "input-dropDown-tags",
      "position": [ 960, 519, 2800, 96 ],
      "hint": "Let's close the current filter and...",
      "items": ["Name", "Location", "Disk size", "Created by", "Family", "Deprecation", "Source disk", "Creation time", "Labels"],
      "settings": {{ '{' }}
        "placeholder": "Filter images"
      {{ '}' }},
      "hintOptions": {{ '{' }}
        "auto": [],
        "position": "right"
      {{ '}' }},
      "bindingOptions":{{ '{' }}
        "oneWay": true
      {{ '}' }},
      "validate":[
        {{ '{' }}
          "rule": ["__eq_auto"],
          "message": "Press next and filter will be closed automatically"
        {{ '}' }}
      ],
      "action": [
        {{ '{' }}
          "values": [],
          "action": ["save", "next"]
        {{ '}' }}
      ]
    {{ '}' }}
```

#### **input-password**

This control can be used for password fields.

#### **input-slider**

This control allows you to pick a value by dragging a pointer along a line. It supports binding option. It has the following properties:

- `"position"`. Please note that 36 is a standard width for this control. If another one is indicated, it will be scaled.

- `"theme"`

- `"color"`

- `"showTicks"` can be true or false

- `"discrete"` can be true or false

- `"values"` showing the range for the values to be picked

```typescript
"type": "input-slider",
      "position": [200, 320, 1600, 50],
      "settings": {{ '{' }}
        "theme": "material-ui",
        "color": {{ '{' }}
          "bar": "#1976d2",
          "pin": "#1976d2"
        {{ '}' }},
        "showTicks": false,
        "discrete": true,
        "values": {{ '{' }}
          "type": "range",
          "data": [0, 100]
        {{ '}' }}
      {{ '}' }}
```

#### **input-terminal**

This control creates a simulated environment to run a command and see its output the way they look in the CLI. It has the following properties:

- `"position"`

- `"autoFocus"` can be true or false and is used when it's the only control

- `"user"`, `"host"` and `"connector"`

```typescript
     "user": "root",
     "host": "DESKTOP_SSSS",
     "connector": "@"
```

- `"initialOutputs"` copies output from other terminal in other model (if it's empty itself). You need to indicate source model and terminal key identifier:

```typescript
"initialOutputs": {{ '{' }}
    "from": "terminalState.terminal-info-010"
{{ '}' }}
```

Please note that in case you need to show some other text in the terminal, you may use `"text"` instead of `"from"` property:

```typescript
 "type": "input-terminal",
      "position": [ 0, 4557, 4650, 693 ],
      "settings": {{ '{' }}
        "initialOutputs":{{ '{' }}
          "text": "Welcome! Type \"help\" to get started.\nYour Cloud Platform project in this session is set to steadfast-list-271711.\nUse “gcloud config set project [PROJECT_ID]” to change to a different project."
        {{ '}' }}
    {{ '}' }}
```

If you don't need the terminal to show the output from other terminals, you can use the following property:

```typescript
"action": ["this::disable"]
```

- `"actionDelay"` sets the time after which specified action will be activated

- `"initialStr"` showing a command already in the terminal

- `"theme"`:

```typescript
"theme": {{ '{' }}
          "fontFamily": "Courier, monospace",
          "fontSize": "60px",
          "fontWeight": "100"
        {{ '}' }}
```

- `"output"` with a link to a txt file containing the output itself

- `"action"`

Please note that "output", "cmd" and "initialStr" can contain equations, and command input supports "regexp":

```typescript
"type": "input-terminal",
      "position": [ 30, 30, 3786, 2280 ],
      "settings": {{ '{' }}
        "autoFocus": true,
        "actionDelay": 5000,
        "initialStr": "./gslb-commit \"publish routes\"",
        "theme": {{ '{' }}
          "fontSize": "5rem"
        {{ '}' }},
        "prompt": " > ",
        "commands": [
          {{ '{' }}
            "cmd": "what a | b > c",
            "output": "tahw"
          {{ '}' }},
          {{ '{' }}
            "cmd": "./gslb-commit \".*\"",
            "output": "#include:./resources/txt/gslb-commit-aws1.txt"
            "action": ["next"]
          {{ '}' }}
        ]
        {{ '}' }}
```

Please note that if you need to save output of several screens and show it on all of them, model of those screens should be the same since outputs are saved into screen model.

#### **input-text**

- `“bindingOptions”` for “input-text” can be `“oneWay”` (true/ false). This property should be indicated for all text-input controls. `“oneWay”` means that if a model contains any data, this data will not be shown.

- `"action"` is indicated as an array in brackets. This action is fulfilled when a value is typed into the input field. "value" is compared and the first one is taken. Actions are not case sensitive, however if case sensitive actions are required, `"caseSensitive": "true"` should be indicated in settings.

```typescript
"action": [
    {{ '{' }}
        "value": "next",
        "action": ["next"]
    {{ '}' }}
]
```

#### **input-textarea**

This is a multi-line text input control. It has the same properties as `"input-text"`.

#### **integration-form-submit--marketo**

This control is used to create a form in a scenario. This form is aimed at collecting some information about users and is integrated with Marketo server, so all the data filled into the form are sent and stored in Marketo.

```typescript
"integration-form": {{ '{' }}
      "type": "integration-form-submit--marketo"
{{ '}' }}
```

It is to be defined in three file types:

a. `index.json` file includes "integration" property where we indicate the integration server:

```typescript
"integration": {{ '{' }}
      "module": ["marketo"]
{{ '}' }}
```

If we have any other integrations, we can add to this property.

b. `style.css` file describes form styles under `#integrationFormModal`:

```typescript
#integrationFormModal #marketoText {{ '{' }}
    padding-right: 20px;
{{ '}' }}
#integrationFormModal .modal-dialog {{ '{' }}
    min-width: 1000px;
    width: 60vw !important;
    height: auto !important;
    max-height: 90vh !important;
    margin: 0px !important;
    max-width: auto;
    background-color: white;
    border-left: none;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
{{ '}' }}
```

c. `meta` file includes the following properties of the control:

- `"position"` which is a must, but ignored in case of a popup mode.

```typescript
"position": [ 10, 10, "1000px", "1000px" ]
```

- `"binding"` which binds data from models or other sources with form fields. Here one property, which isn't form field, related to Marketo is to be indicated:

```typescript
"binding": {{ '{' }}
        "Additional_Score_Detail__c": "format:{{ '{' }}0{{ '}' }}|__attendeePath|scenario-titles-only",
        "FirstName": "coalesce:field:form.FirstName/firstName:format:{{ '{' }}0{{ '}' }}|user|userName",
        "LastName": "coalesce:field:form.LastName/lastName:format:{{ '{' }}0{{ '}' }}|user|userName"
{{ '}' }}
```

`"Additional_Score_Detail__c"` variable keeps and aggregates the data from the last 200 pages which the user visited. It can include three different parameters meaning the amount of data stored: "standard", "small", "scenario-titles-only".

If you need some definite value to be recorded, you should indicate it as `"dump"` in "settings":

```typescript
"settings": {{ '{' }}
      "dump": "eval:() => `\tName: ${{ '{' }}_bd.user.userName{{ '}' }}`"
{{ '}' }}
```

`coalesce` is used to return the first value which isn't "null" either before or after the "slash". `"firstName"` is the value indicated before space in the Start form, and `"lastName"` is the value after space:

```typescript
"FirstName": "coalesce:field:form.FirstName/firstName:format:{{ '{' }}0{{ '}' }}|user|userName"
```

- `"settings"`:

`"redirect"` defines where the form redirects to, where `"false"` means no redirection, `"true"` means default redirection to the page defined by Marketo for this form.

```typescript
"redirect": false
```

`"mode"` defines the way the form appears:

_"popup"_ displays the form on top of the current page and the user "submits" it

_"embedded"_ displays the form in the specified "position" and the user "submits" it

_"silent"_ mode just submits the form without showing it if all the required data is available. Otherwise, it doesn't submit the form.

_"popup-or-silent"_ mode validates the data in the form, and if the data is valid, the form is submitted without showing.

`"munchkinId"` is a pre-defined parameter for Marketo system.

`"formId"` is a pre-defined parameter for Marketo system.

```typescript
"munchkinId": "653-SMC-783",
"formId": 12255
```

`"delay"` defines time after which the form appears.

```typescript
"delay": 7
```

`"instructions"` to add special instructions to the defined fields:

```typescript
"instructions": {{ '{' }}
    "field": "Additional_Score_Detail_c",
    "text": "#include:./resources/txt/instructions.txt"
{{ '}' }}
```

`"content"` defines how the form looks like and its content. This may include a reference to an HTML stored in `/resources/ folder`. `"success-text"` may be included and will appear when Submit is hit, or it may be skipped as an option.

```typescript
"content": {{ '{' }}
          "header": "#include:./resources/html/marketo-header.html",
          "text": "#include:./resources/html/marketo-text.html",
          "footer": "<b>TBD</b>",
          "success-text": "<div id='integrationSuccessMessage'><b>Thank you for your details.<br/>The article will be emailed to you shortly.</b></div>"
{{ '}' }}
```

`"no-defaults"` defines the default / pre-defined data which is not to be submitted with the form.

```typescript
"no-defaults": {{ '{' }}
          "FirstName": "Awesome",
          "LastName": "Dev",
          "Company": "Awesome Org"
        {{ '}' }}
```

`"model": "form"` is indicated in case if our form belongs to the screen where other data is generated and stored in a model with another name. So, by writing this property, the user creates one more model for the data filled into the form.

Note that if you add `"model": "form"` property, it should be indicated in the `"context"` property of the medatada file.

#### **label**

This control can show the pre-defined value indicated in the `model.json` file, or a value filled in by user and stored by this variable. It is not clickable, so if we need it to lead us to the next step, we add a button which is clickable and can move us on.

```typescript
"name": {{ '{' }}
   "type": "label",
   "position": [ 144, 499, 234, 60 ],
   "style": [ "name-dark" ]
{{ '}' }}
```

#### **link-button**

This control is clickable, should have an action over it and can’t output text, hence can be combined with a `“label” `control over it.

#### **output-animated-arrow**

This control is used for animated attacks and arrows. It includes the following properties:

- `“position”` which indicates properties of a rectangular in which our animated object is to be shown. The first two numbers represent coordinates of the rectangular, and the second two numbers represent its width and height.

- `“path”` which describes the curve for the animated object inside the rectangular described above. It includes `“points”` and `“style”`.
  The curve consists of four control points: starting point, two control points and final point. Path parameters are indicated as an array. The starting point is the reference point for other coordinates inside the rectangular indicated by a user (ex, [10, 10], where one coordinate stands for x axis, and another for y). Three other points are indicated relative to the starting one.
  Please note that the final point is located in the middle of the arrowhead.
  As for the “style”, it includes color and width in pixels. If color is indicated using HEX coding, symbol “#” should go before the code: “#666666”. Width can be indicated as a fractional value in order to regulate size of arrowhead.

- `“animation”` which can have the following characteristics:

`“type”`

`“attack”` (shows just a point without an arrowhead)

`“data-success”` (shows an arrow)

`“data-failed”` (shows an arrow)

`“time”` of animation

`“delay”` of animation start

`“ease”` is optional and defines how animation ends (for now “bounce” option is available).

```typescript
"type": "output-animated-arrow",
"position": [116, 275, "43px", "123px"],
"path": {{ '{' }}
    "points": [ [40, 1],  [10, 50],  [10, 50],  [4, 110] ],
    "style": {{ '{' }}
        "color": "#A4DE59",
        "width": 2
        {{ '}' }}
      {{ '}' }},
    "animation": {{ '{' }}
        "type": "data-success",
        "time": 1,
        "ease": "bounce"
      {{ '}' }}
```

#### **output-animated-link**

This control is used as a link between objects and includes the following properties:

- `“position”` which indicates properties of a rectangular in which our object is to be shown. The first two numbers represent coordinates of the rectangular, and the second two numbers represent its width and height.

- `“path”` which describes the curve for the animated object inside the rectangular described above. It includes `“points”`, `“marker”` and `“style”`.
  The curve consists of four control points: starting point, two control points and final point. Path parameters are indicated as an array. Starting point is the reference point for other coordinates inside the rectangular indicated by a user (ex, [10, 10], where one coordinate stands for x axis, and another for y). Three other points are indicated relative to the starting one.
  As for `“style”`, it includes `“color”`, `“width”` in pixels and `“dash-array”` properties. If color is indicated using HEX coding, symbol “#” should go before the code: “#666666”. Width can be indicated as a fractional value.
  `“marker”` property includes three characteristics: `“size”, “start”` and `“end”` (where start and end can be represented as a “circle”, see the image below).

- `“animation”` which can have the following properties:

`“time”` of animation

`“increment”`

`“delay”` of animation start

`“yoyo”` (true / false) meaning that animation will move one way and then back.

```typescript
"type": "output-animated-link",
"position": [122,335,"192px","100px"],
"path": {{ '{' }}
    "points": [ [1, 80],[95, 38],[95, 38],[191, 16] ],
    "style": {{ '{' }}
        "dash-array": [20, 5],
        "color": "#666666",
        "width": 2.5
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
```

#### **output-animation-lottie**

This control helps show Lottie animation in a scenario and has the following properties:

- `"position"`

- `"img"` showing route to a JSON file

- `"animation"`

```typescript
"type": "output-animation-lottie",
      "position": [ 500, -100, 3000, 2336 ],
      "img": "./resources/anim1.json",
      "animation": {{ '{' }}
        "loop": false,
        "speed": "1"
      {{ '}' }}
```

- `"event"` which defines various actions:

when the animation is over (`"onComplete"`):

```typescript
"event": {{ '{' }}
  "onComplete": [ "#include:./resources/js/set-sellers.js", "save", "skip:[engage,1,0]" ]
{{ '}' }}
```

when the animation starts (`"onStart"`), or it may also define the point in animation, in percent, (`"onFrame"`) when the specified action will happen:

```typescript
"onFrame": {{ '{' }}
          "2%": "show: img-btn-skip, btn-skip",
          "85%": "show: btn-marketing, btn-partners, btn-sellers"
        {{ '}' }}
```

- `"settings"` which include `"startBtn"` having `"text"` and `"style"` properties and `"overflow"`.

`"startBtn"` is used in cases when animation is on, but sound isn't unless you press this `"Start"` button.

```typescript
"anim1": {{ '{' }}
  "type": "output-animation-lottie",
  "position": [ 650, 100, 3000, 2336 ],
  "img": "./resources/anim3.json",
  "animation": {{ '{' }} "loop": false, "speed": "1" {{ '}' }},
  "settings": {{ '{' }}
    "startBtn": {{ '{' }}
      "text": "Click here to start animation",
      "style": "startBtnStyle"
    {{ '}' }}
  {{ '}' }}
{{ '}' }}
```

If `"overflow" `is `"hidden"`, only part of screen inside the `"position"` area is shown. Animation is to be positioned relatively to the upper left corner (0; 0). If `"overflow"` is `"scroll"`, indicate style for `"#lottie"` in the main "css" file.

#### **output-html**

This control is used to show information from JSON file as HTML. It has the following properties:

- `"position"`

- `"html"` indicating the route to the file itself

- `"overflow"`: which can be `"scroll", "hidden", "visible"` or `"auto". "hidden"` means that the overflow is clipped, and the rest of the content will be invisible, whereas `"scroll"` means that the overflow is clipped, and a scrollbar is added to see the rest of the content. `"auto"` is similar to scroll, but it adds scrollbars only when necessary, and `"visible"` doesn't clip the overflow.

- `"style"`

```typescript
"type": "output-html",
      "position": [ 0, 144, 4650, 100 ],
      "visible": false,
      "html": "#include:./resources/html/user-name-hint.html",
      "overflow": "scroll",
      "style": ["name-hint-html"]
```

#### **output-img**

It is visible by default, otherwise, you can set: `“visible”: false/true`. This control can have:

- `“position”`

- `“img”` with storage indicated (./ shows the route to its storage within the current scenario; otherwise it can show a full URL route)

- `“animation”` which can have:

`“style”` (ex, `“like-gif steps (number of steps)-time of animation-forwards”`, where `“forwards”` means it’s played in normal direction. It can also be `“infinite” `which means being looped.)

`“pos”`

`“delay”` (delay for the start of animation)

```typescript
"waiting-man": {{ '{' }}
    "type": "output-img",
    "position": [129, 165, "55px", "111px"],
    "img": "./resources/waiting-man2.png",
    "animation": {{ '{' }}
        "style": "like-gif steps(40) 2s forwards",
        "pos": "-2200px"
      {{ '}' }}
    {{ '}' }}
```

#### **output-randomCounter**

This control has the following properties:

- `“position”` (containing four characteristics)

- `“counter”` (characteristics of the counter itself): `“range”` and `“period”` of its change

- `“legend”` (units)

- `“style”: “color”, “font”` (which includes `“size”` and `“lineHeight”` in px), `“gradientRadius”, “radius”` of the counter

- `“animation”`: `“ease”` (defines how animation appears: `“none”` for no effects, and `“elastic”` is for giving a springy feel to animation), `“delay”` and its `“duration”`

```typescript
"counter7": {{ '{' }}
    "type": "output-randomCounter",
    "position": [710, 1310, 300, 300],
    "counter": {{ '{' }}
        "range": [700, 1000],
        "period": 0.5
      {{ '}' }},
    "legend": "ms",
    "style": {{ '{' }}
        "gradientRadius": "100",
        "radius": 50,
        "color": "#FF421A",
        "font": {{ '{' }}
          "size": "40px",
          "lineHeight": "30px"
        {{ '}' }}
      {{ '}' }},
    "animation": {{ '{' }}
        "ease": "elastic",
        "delay": 0.01,
        "duration": 1
      {{ '}' }}
    {{ '}' }}
```

#### **output-randomGauge**

It can have the following properties:

- `“visible”` (false/ true)

- `“position”`

- `“delay”` (delay for the start of animation, data is generated automatically in milliseconds)

- `“style” (“colors”)`

- `“range”` (for `“gauge”` and for `“value”` to be indicated as arrays)

```typescript
"type": "output-randomGauge",
"position": [710, 1310, 300, 300],
"delay": 800,
"style": {{ '{' }}
    "colors": ["#eb850e", "#f0f0f0"]
        {{ '}' }},
"range": {{ '{' }}
    "gauge": [0, 400],
    "value": [250, 350]
      {{ '}' }}
```

#### **output-table**

This control is used to locate generated data in a table. It has the following properties:

- `“position”`

- `“reverseRows”` in “settings” that shows table lines in the reverse order.

```typescript
"settings": {{ '{' }}
  "reverseRows": true
{{ '}' }}
```

- `“maxRows”` (number of rows in a table)

- `“columns”` which includes names of columns under “binding” (binding between model field and table column name):

- `“style”` (which is specified in style.css file):

```typescript
"table-attacks": {{ '{' }}
    "type": "output-table",
    "position": [ 300, 3220, "4210px", "428px" ],
    "maxRows": 4,
    "columns": {{ '{' }}
        "binding": {{ '{' }}
          "date": "Date",
          "uri": "URI",
          "severity": "Severity",
          "category": "Category",
          "violations": "Violations",
          "attack-type": "Attack type",
          "status": "Status",
          "src-ip": "Source IP Address",
          "src-location": "Source location",
          "ep-location": "Endpoint location"
        {{ '}' }}
      {{ '}' }},
    "style": [ "table-attacks" ]
    {{ '}' }}
```

#### **output-timestamp**

This control indicates timestamp and can have position and style.

```typescript
  "context": ["user","service"],
  "settings": {{ '{' }}
    "dpr": 3
  {{ '}' }},
  "binding": {{ '{' }}
    "userName": "user.userName",
    "companyHeader": "user.company",
    "company": "user.company",
    "lastUpdate": "service.timestamp",
    "zoneName": "service.zoneName",
    "dnsPrimaryServerIp": "service.dnsPrimaryServerIp"
  {{ '}' }},
  "title": "DNS service",
  "description": "TBD.",
  "controls": {{ '{' }}
    "lastUpdate": {{ '{' }}
      "type": "output-timestamp",
      "position": [3830, 1174, 800, 30],
      "style": ["tableCell"]
    {{ '}' }}
  {{ '}' }}
```

Date can have various formats. If you indicate `"localnow"`, the local system time is used.

```typescript
{{ '{' }}
  "date": {{ '{' }}"exact": "format:{{ '{' }}0{{ '}' }}|localnow()|MMM dd, yyyy / HH:mm:ss"{{ '}' }}
  {{ '}' }}
```

#### **output-video-player**

This control allows you to use video in the simulation. It has the following properties:

- `"shared"` in the name of control (`"shared::th3"`) indicates that this control is shared between several screens and is not created again in other screens, where `"th2"` is control name.

- `“position” `or `“size”` (if it’s used in the sidebar):

```typescript
"position": ["10px", "10px", "1000px", "1000px"]
```

```typescript
"size": ["calc(var(--sidebar-size))", "172px"]
```

- `“img”` defining where the mp4 video is stored:

```typescript
"img": "./resources/video/mp4-video.mp4"
```

- `“event”` defining the events and their timing during the video:

```typescript
"event": {{ '{' }}
        "onProgress": {{ '{' }}
          "1": ["next"]
        {{ '}' }}
      {{ '}' }}
```

If `“onProgress”` has `“forced:”` property, it means that the action will be executed both in automatic and in manual mode:

```typescript
"event": {{ '{' }}
        "onProgress": {{ '{' }}
          "forced:1": ["save", "next"]
        {{ '}' }}
      {{ '}' }}
```

- `“settings”` including the following:

```typescript
"sidebar": {{ '{' }}
    "shared::th3": {{ '{' }}
      "type": "output-video-player",
      "size": ["calc(var(--sidebar-size) - 26px)", "172px"],
      "img": "./resources/th/step3.mp4",
      "event": {{ '{' }}
        "onProgress": {{ '{' }}
          "18": "show: area-job-openning",
          "20": "hide: area-job-openning",
          "21": ["next"]
        {{ '}' }}
      {{ '}' }},
      "settings": {{ '{' }}
        "start": "0",
        "stop": "40",
        "idle": {{ '{' }}
          "switchToAuto": {{ '{' }}
            "timeout": "10",
            "action": ["save", "next"]
          {{ '}' }}
        {{ '}' }},
        "progressInterval": 100,
        "autoPlay": true,
        "startBtn": {{ '{' }}
          "styles": {{ '{' }}
            "backgroundColor": "green"
          {{ '}' }}
        {{ '}' }}
      {{ '}' }}
    {{ '}' }}
{{ '}' }}
```

#### **system-generator**

This control is used to generate different data into a model as a list and is specified as an array:

```typescript
"model": "generatedData[]",
"context": [ "sim", "app", "user", "dns", "generatedData" ]
```

Note that in order to get access to the full list and not only its last element, we indicate the name of the whole list in the `“context”` (see an example above).

Also note that in model `“binding”` element, we indicate that our table is bound with the list indicated in `“context”`.

Binding can include equations, which can have JS functions after `“eval”`. It can be used to show, say, the total number of attacks generated.

Several generators can be included in one model. They will generate data and insert it into the array as the last element.

This control has the following properties:

- “selector” is the way to select between available bindings (arrays):

```typescript
"type": "system-generator",
"selector": "rand",
"interval": 2,
    "visible": false
```

`“selector”` can be `“rand”` (random selection) and `“iterate”` (selects one by one from the top to the bottom).

- `“interval”` defines how often data is generated and is indicated in seconds

- `“binding”` is a way to specify generated data inside its model inside corresponding columns. These columns are listed inside this `“binding”` property and are bound.

Each column gets a generator which can be:

`“exact”` which means showing exact data indicated here.

`“random-range”` which means that during every generation it goes through an array and randomly selects one option of all. This can be used, say, to show random types of attacks.

They can be specified in different ways: as a string (see an example of an equation below which shows the current date), as an object, as an HTML to show images which must be stored in `./resources folder.`

```typescript
"binding": [
        {{ '{' }}
          "date": {{ '{' }} "exact": "format:{{ '{' }}0{{ '}' }}|now()|MMM dd, yyyy / HH:mm:ss" {{ '}' }}
{{ '}' }}
]
```

```typescript
"exact": {{ '{' }}
    "__html": "<span><img src='./resources/highrisk.svg' />High-Risk</span>"
            {{ '}' }}
```

- `“visible”:` true (generating mode) or false (non-generating mode)

Note that all images shall be stored in `./resources folder.`

#### **system-trigger-interval**

This control repeats the same action every indicated period of time. It has the following properties:

- `"interval" `indicated in milliseconds

- `"action"`

```typescript
"type": "system-trigger-interval",
      "interval": 3000,
      "action": ["show:nameLabel"]
```

#### **system-trigger-mouse**

This control defines actions based on mouse moves and has the following properties:

- `"position"`

- `"onMouseOver"` (and action)

- `"onMouseLeave"` (and action)

```typescript
"type": "system-trigger-mouse",
      "position": [1179, 770, 1635, 901],
      "onMouseOver": ["show: pop-up", "hide: void"],
      "onMouseLeave": ["hide: pop-up"]
```

- `"onMouseLBtnClick"` (and action) - starts an action on left burron click.

#### **system-trigger-timeline**

This control defines what actions and when will be activated, and has the following properties:

- `"loop"` which can be true/false.

- `"timeline"` indicating when and what action will be activated. Time is indicated in milliseconds. Actions can be `"hide", "show", "toggle"`. `"toggle"` changes the value to the opposite one (say, from true to false).

```typescript
"type": "system-trigger-timeline",
      "loop": false,
      "timeline": {{ '{' }}
        "1": [
          "show:[divider, end-user, end-user-label, app, app-label, help-desk, help-desk-action, help-desk-label, arrow-user-app]",
          "hide:[arrow-mood, arrow-team1]"
        ],
        "1000": [ "show:[error1]"]
      {{ '}' }}
```

#### **system-trigger-timer**

This control defines an action which is activated at some defined time.

It has the following properties:

- `"timeOut"` indicated in milliseconds

- `"action"`

```typescript
"type": "system-trigger-timer",
      "timeOut": 1,
      "action": ["show:void"]
```

##### Common control properties

- `“position”` includes the following four parameters (they can also be auto): `[1, 2, 3, 4]` where

1 – left margin

2 – top margin

3 – width

4 – height

`"position": [200, 320, 1600, 50]`

- `“hint”`. Any field can be with or without a hint. Hints may go with or without hint options. Hints can have their equations:

```typescript
"hint": "format:Input some data. Data from model: <i>{{ '{' }}0{{ '}' }} {{ '{' }}1{{ '}' }}</i>|userInfo|firstName"
```

- `“hintOptions”`. Hints may go with or without hint options. They may include:

`“position”` which is right by default. It can also be specified as `“left”, “right”, "top", "bottom", "top-left", "top-right", "bottom-left", "bottom-right"` and `"none"`, where "none" means that the hint is empty and may be used when we don't need any hint, but we need the focus to move on.

```typescript
"hint": "#",
"hintOptions": {{ '{' }} "position": "none" {{ '}' }}
```

`“auto”` (auto-filling, for example, for email). “auto” can return the indicated object as it is: without any changes or formatting. This can be used in case we work with lists of objects, not lines.

`"size" `indicated in pixels or as "auto": `"size": "150px"`

`"showDelay"` defines time to the moment when hint appears

`"hideTimeout"` defines time when hint is hidden

```typescript
"hintOptions": {{ '{' }}
        "position": "right",
        "auto": "object: ipEndpoint[]",
        "showDelay": 3000,
        "hideTimeout": 10000
      {{ '}' }}
```

- `“style”` can be used for some controls and indicated as an array in case of several properties. All styles are to be defined in `style.css` file for each scenario.

- `“actions”` used for `“button” / “link-button” / “input-dropDown-list”` controls and include:

`“save”`

`“next”`

`“show”`

`“hide”`

`“skip"` (ex, `"skip":[dnslb,0,0]”` where “dnslb” is step name, “0” is screen number”, “0” is hint number) action lets jump to the indicated step – screen – hint.

`"switch"` that let's us jump to another script. In order to jump to the beginning of a script, indicate its ID ("script_one” in the example below):

```typescript
“action”: [
    “switch:script_one”
]
```

In order to jump to a definite screen of that script, indicate the full path:

```typescript
“action”: [
    “switch:script_one/nav/lb/020/0”
]
```

`"switch"` action can be used for any control that supports actions.

`"toggle"` that changes the value of an indicated property.

`"focus"` that changes screen focus.

```typescript
"btn-copy": {{ '{' }}
      "type": "button",
      "position": [ 3309, 993, 36, 42 ],
      "hint": "Click to copy command!",
      "hintOptions": {{ '{' }} "position": "bottom" {{ '}' }},
      "action": [ "show: img-copied", "hide: btn-copy", "focus: btn-ok" ]
    {{ '}' }}
```

`“set”` that saves the result of expression into model.field: `"action"`: [`“set: model|field|format: {{ '{' }}0{{ '}' }} {{ '{' }}1{{ '}' }}|__query|fName, sName”`]

`“zoom”`: `"action": [“zoom: 200”]`

If fit to screen is required, the following is to be specified:

`"action": [“zoom: fit”] `

Actions also support equations:

`"action": ["format:focus:{{ '{' }}0{{ '}' }}|user|ctrl"]`

- `“validation”` helps validate the data which a user indicates in the control. The following types of validation are available:

`"__REQUIRED"` means that this field is to be filled in

```typescript
({{ '{' }}value{{ '}' }}) => new RequireRule(value)
```

```typescript
"netBios": {{ '{' }}
      "type": "input-text",
      "position": [1365, 4689, 1242, 63],
      "hint": "Enter BD",
      "hintOptions": {{ '{' }}
        "position": "right",
        "auto": "BD"
      {{ '}' }},
      "bindingOptions":{{ '{' }}
        "oneWay": true
      {{ '}' }},
      "validate": [
        {{ '{' }}
          "rule": ["__required"],
          "message": "format:Name is required to continue. Press next and {{ '{' }}0{{ '}' }} will be used automatically|__hintOptions|auto"
        {{ '}' }}
      ]
    {{ '}' }}
```

`"__REGEXP_IP"` means IP is to be filled in

```typescript
({{ '{' }}value{{ '}' }}) => new RegexpRule(value, __ipRegexp)
```

```typescript
"email": {{ '{' }}
      "type": "input-text",
      "position": [ 525, 501, 1260, 120 ],
      "hint": "Enter your email to login",
      "hintOptions": {{ '{' }}
        "position": "right",
        "auto": "#include:./resources/js/name.js"
      {{ '}' }},
      "validate":[
        {{ '{' }}
          "rule": ["__regexp_email"],
          "message": "format:{{ '{' }}0{{ '}' }} is required to continue. Press next and it will be used automatically|__hintOptions|auto"
        {{ '}' }}
      ]
    {{ '}' }}
```

`"__REGEXP_NUMBER"` means number is to be filled in

```typescript
({{ '{' }}value{{ '}' }}) => new RegexpRule(value, __numberRegexp)
```

```typescript
"port": {{ '{' }}
    "type": "input-text",
    "position": [4176, 1476, 1191, 120],
        "bindingOptions":{{ '{' }}
         "oneWay": true
      {{ '}' }},
    "hint": "Specify HTTP port.",
    "hintOptions": {{ '{' }}
        "position": "left",
        "auto": "80"
      {{ '}' }},
    "validate":[
        {{ '{' }}
        "rule": ["__regexp_number"],
        "message": "format:Nice try, but how about a port {{ '{' }}0{{ '}' }} or 8080? Keep going, and we'll fill one in for you!<br><br>|__hintOptions|auto"
        {{ '}' }}
      ]
    {{ '}' }}
```

`"__REGEXP_URL"` means URL validation.

```typescript
"fqdn": {{ '{' }}
      "type": "input-text",
      "position": [1365, 8862, 642, 63],
      "hint": "TBD",
      "hintOptions": {{ '{' }}
        "position": "right",
        "auto": "format:{{ '{' }}0{{ '}' }}.com|appInit|appName"
      {{ '}' }},
      "bindingOptions":{{ '{' }}
        "oneWay": true
      {{ '}' }},
      "validate": [
        {{ '{' }}
          "rule": ["__regexp_url"],
          "message": "format:Name is required to continue. Press next and {{ '{' }}0{{ '}' }} will be used automatically|__hintOptions|auto"
        {{ '}' }}
      ]
{{ '}' }}
```

`"__EQ_AUTO"` validates if specified data is equal to the data in `“auto”`. Please note that if auto includes data filled-in before, `“format”` is to be specified.

If the data is not validated by the rule, a message will appear inside the hint. A user cannot skip this control without indicating either valid data or pressing “next”, which will automatically fill in the field with the data indicated in `“auto”` of `“hintOptions”` (`“|__hintOptions|auto”`, see an example below).

```typescript
"zoneName": {{ '{' }}
      "type": "input-text",
      "position": [4235, 336, 1201, 120],
      "hintOptions": {{ '{' }}
        "position": "left",
        "auto": "format:{{ '{' }}0{{ '}' }}|user|serviceName"
      {{ '}' }},
      "hint": "Name your zone.",
      "validate":[
        {{ '{' }}
          "rule": ["__eq_auto"],
          "message": "format:You need to use your service name here. Press next and {{ '{' }}0{{ '}' }} will be used automatically|__hintOptions|auto"
        {{ '}' }}
      ]
{{ '}' }}
```

`"__REGEXP_CUSTOM: ... "` lets us create some custom validation. After the colon symbol, we can indicate the characters we need. Have a look at an example below.

- `“zIndex”` defines the sequence of controls. The higher the index is, the higher the control layer is. Canvas has index 1, so control index is indicated related to it.

```typescript
"zIndex": 5
```

- `“placeholder”` shows a placeholder in the control you need. Let's look at an example below.

```typescript
"searchImage": {{ '{' }}
      "type": "input-text",
      "position": [ 1836, 40, 681, 60 ],
      "settings": {{ '{' }}
        "placeholder": "Search"
      {{ '}' }},
      "hint": "Let's type in 'images' over here!",
      "hintOptions": {{ '{' }}
        "position": "bottom",
        "auto": "images"
      {{ '}' }},
      "style": ["white"],
      "action": [
        {{ '{' }}
          "value": "images",
          "action": ["next"]
        {{ '}' }}
      ]
    {{ '}' }}
```

- `“visible”` is managed by show and hide options. See an example below:

```typescript
"btn-setup2": {{ '{' }}
   "type": "button",
   "position": [84, 84, 428, 161],
   "action": ["show:azure-sub", "show:btn-setup", "hide:btn-setup2"]
 {{ '}' }},
 "btn-setup": {{ '{' }}
   "type": "button",
   "position": [84, 84, 428, 161],
   "action": ["hide:azure-sub", "show:btn-setup2", "hide:btn-setup"]
 {{ '}' }}
```

Please note that `'show'` and `'hide'` options override any value of `'visible'`, including those defined using equations. `‘true’` values for `‘show’` and `‘false’` values for `‘hide’` will be used.
