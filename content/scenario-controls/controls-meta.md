### **COMMON CONTROL PROPERTIES**

Information on control types, their specific properties and examples can be found in the [SCENARIO CONTROLS](/scenario-controls/animated-arrow) section.

#### action

<table>
  <tr>
    <td><strong>Supported values</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td><code>focus</code></td>
    <td>focuses on specified control</td>
    <td><code>"action": [ "focus: controlID" ]</code></td>
  </tr>
  <tr>
    <td><code>hide</code></td>
    <td>shows the specified control</td>
    <td><code>"action": [ "hide:controlID" ]</code></td>
  </tr>
  <tr>
    <td><code>navigate</code></td>
    <td>navigates user to the screen whose <a href="https://docs.upmix.it/scenario-edit/screen-settings#title-text-notes--short-name">short name</a> is specified</td>
    <td><code>"action": [ "navigate: screen_short_name" ]</code></td>
  </tr>
  <tr>
    <td>
    <code>next</code>
    </td>
    <td>brings user to the next screen</td>
    <td>
    <code>"action": [ "next" ]</code></td>
  </tr>
  <tr>
    <td>
    <code>prev</code>
    </td>
    <td>brings user to the previous screen</td>
    <td>
    <code>"action": [ "prev" ]</code>
    </td>
  </tr>
  <tr>
    <td>
    <code>restructure</code>
    </td>
    <td>reorders steps (specified as an array) in the flow using their <a href="https://docs.upmix.it/scenario-edit/screen-settings#create-new-screen">short names</a> entered in the <code>Advanced</code> step settings. Note that ALL scenario steps are be to included in the array</td>
    <td>
    <code>"action": ["restructure: [step2, step1, step3]"]</code>
    </td>
  </tr>
  <tr>
    <td>
    <code>save</code>
    </td>
    <td>saves the entered value</td>
    <td><code>"action": [ "save" ]</code></td>
  </tr>
  <tr>
    <td><code>set</code></td>
    <td>saves the result of expression into the specified <code>model.field</code> in specified <a href="https://docs.upmix.it/scenario-controls/controls-meta#expressions">format</a></td>
    <td><code>"action": ["set: model|field|format: {{ '{' }}0{{ '}' }} {{ '{' }}1{{ '}' }}|__query|fName, sName"]</code> </td>
  </tr>
  <tr>
    <td><code>show</code></td>
    <td>shows the specified control</td>
    <td>
    <code>"action": [ "show:controlID" ]</code>
    </td>
  </tr>
  <tr>
    <td><code>skip</code></td>
    <td>skips the flow to the specified step, screen and control</td>
    <td><code>"action": [ "skip:[step,screenNo,hintNo]"]</code></td>
  </tr>
  <tr>
    <td><code>skip-screen-shortName</code></td>
    <td>skips the flow to the specified screen; note that screen <a href="https://docs.upmix.it/scenario-edit/screen-settings#title-text--notes">short name</a> is to be specified</td>
    <td><code>"action": ["skip-screen-shortName: 123456"]</code></td>
  </tr>
  <tr>
    <td><code>switch</code></td>
    <td>brings user to another scenario:
    <ul> 
    <li>scenario beginning if scenario ID is specified</li>
    <li>scenario definite step if the full path is specified</li>
    </ul>
    </td>
    <td>
    <ul> 
    <li><code>"action": [ "switch:script_one" ]</code></li>
    <li><code>"action": [ "switch:script_one/nav/lb/020/0" ]</code></li>
    </ul>
    </td>
  </tr>
  <tr>
    <td><code>this::disable</code></td>
    <td>is used for the <a href="https://docs.upmix.it/scenario-controls/terminal">terminal</a> control for it not to show outputs from other terminals</td>
    <td><code>"action": ["this::disable"]</code></td>
  </tr>
  <tr>
    <td><code>toggle</code></td>
    <td>switches specified control property, e.g. from true to false (useful to make a control visible or not)</td>
    <td><code>"action": [ "toggle: controlID" ]</code></td>
  </tr>
  <tr>
    <td><code>zoom</code></td>
    <td>zooms scenario to specified percent relative to the left upper corner</td>
    <td><code>"action": ["zoom: 200"]</code> or for fit to screen <code>"action": ["zoom: fit"]</code></td>
  </tr>
  <tr>
    <td colspan="2" style="text-align: center; vertical-align: middle;"><strong>note that actions support <code><a href="https://docs.upmix.it/scenario-controls/controls-meta#expressions">format</a></code> expressions</strong></td>
    <td><code>"action": ["format:focus:{{ '{' }}0{{ '}' }}|user|ctrl"]</code></td>
  </tr>
</table>

#### expression

<table>
  <tr>
    <td><strong>Expression</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td>
    <code>eval</code>
    </td>
    <td>
    <ul>
    <li>evaluates or executes an argument</li>
    <li>can be specified directly or via <code>#include:</code></li>
    <li>can return values from <code>bd</code> (global binding data) and <code>bm</code> (binding model of current screen)</li>
    </ul>
    </td>
    <td>
    <ul>
    <li>to return randomly calculated values for chart <code>"eval: () => {{ '{' }} const randomArray = []; for (let i = 0; i < 5; i++) {{ '{' }} const randomValue = Math.floor(Math.random() * 500) + 1;  randomArray.push(randomValue); {{ '}' }}  return randomArray;{{ '}' }}"</code></li>
    <li>to return specified array for chart <code>"eval: () => {{ '{' }} return [400, 500, 287]{{ '}' }}"</code></li>
    <li>to return date <code>eval:(bm) => {{ '{' }} var date = new Date(); var dateStr = date.toDateString(); var str = dateStr.substr(4); return str {{ '}' }}</code></li>
    <li>to return value entered by user in a string <code>"eval: (bm) => bm.model.value + '@email.com'",</code></li>
    <li>to return specified value under specified conditions <code>"visible": "eval:(bm) => {{ '{' }} if(bm.flags.scenario === 2 && !(bm.flags.marketing  && bm.flags.partners && bm.flags.sellers)) return true; else return false {{ '}' }}",</code></li>
    <li>sample with the include: <code>"#include:./resources/js/init-vars.js"</code></li>
    <li>etc</li>
    </ul>
    </td>
  </tr>
  <tr>
    <td><code>field</code>*</td>
    <td>returns referenced value from referenced model</td>
    <td><code>"field:model.value"</code></td>
  </tr>
  <tr>
    <td><code>format</code>*</td>
    <td>returns the formatted string: formats the specified values and returns them inside the string placeholder defined inside <code>{{ '{' }} {{ '}' }}</code></td>
    <td>
    <ul>
    <li>example with one variable <code>"format:Press next and {{ '{' }}0{{ '}' }} will be used automatically|model|value"</code></li>
    <li>example with few variables <code>"format:text here {{ '{' }}0{{ '}' }}.{{ '{' }}1{{ '}' }}|model|value1,value2"</code></li>
    </ul>
    </td>
  </tr>
  <tr>
    <td colspan="2" style="vertical-align: middle;"><strong>* expressions can be used as <code>coalesce</code> that accepts a list of parameters separated by <code>/</code> and returns the first non-NULL value from the list</strong></td>
    <td><code>"coalesce:field:form.FirstName/firstName:format:{{ '{' }}0{{ '}' }}|user|userName"</code></td>
  </tr>
</table>

#### function

<table>
  <tr>
    <td><strong>Function</strong></td>
    <td><strong>Example</strong></td>
    <td>
      <strong>Description</strong>
    </td>
  </tr>
  <tr>
    <td><pre><code>cside.act</code></pre></td>
    <td><ul><li><pre><code>cside.act('btn-left');</code></pre></li></ul>
    </td>
    <td><ul><li>enables the object identified by <code>control ID</code></li></ul></td>
  </tr>
  <tr>
    <td>
    <pre><code>cside.bind</code></pre>
    </td>
    <td>
    <ul>
    <li><code>field</code> expression<pre><code>cside.bind(".value", "field:model.value");</code></pre></li>
    <li><code>format</code> expression<pre><code>cside.bind(".value", "format:{{ '{' }}0{{ '}' }}|model|value");</code></pre></li>
    <li>context example <pre><code>"context": [ "model" ],</code></pre></li>
    </ul>
    </td>
    <td>
    <ul>
<li><a href="https://docs.upmix.it/scenario/screens#meta-file">binding</a>  allows assigning model data into a variable. Binding is to be specified inside <code>csideScripting</code> tag;</li>
<li>useful for cases when we, for example, need to address a user with the name typed in at the first step throughout the scenario;</li>
<li><a href="https://docs.upmix.it/scenario-controls/controls-meta#expression">format and field</a> expressions can be used for binding;</li>
<li>In order to apply script binding, specify <strong>model</strong> name from where the variable is taken in <a href="https://docs.upmix.it/scenario/screens#meta-file">context</a> field of <code>.meta</code> file that describes the screen this HTML control belongs to.</li>
    </ul>
    </td>
  </tr>
  <tr>
    <td><pre><code>cside.eval</code></pre></td>
    <td><ul><li><pre><code>function ctaClick() {{ '{' }}
    cside.show("all-screen-form-marketo-zero");
    window.cside.eval('form-open', 'CTA');{{ '}' }}</code></pre></li></ul>
    </td>
    <td><ul><li>used with function which processes the indicated expression and returns it</li></ul></td>
  </tr>
  <tr>
    <td><pre><code>cside.hide</code></pre></td>
    <td><ul><li><pre><code>onclick='cside.hide("controlID")';</code></pre></li></ul>
    </td>
    <td><ul><li>hides the object identified by <code>control ID</code> on specified action</li></ul></td>
  </tr>
 <tr>
    <td><pre><code>cside.navigate</code></pre></td>
    <td><ul><li><pre><code>onclick='cside.navigate("screen_short_name")'</code></pre></li></ul>
    </td>
    <td><ul><li>navigates user to the screen whose <a href="https://docs.upmix.it/scenario-edit/screen-settings#title-text-notes--short-name">short name</a> is specified;</li>
    <li>only one screen can be specified;</li>
    <li>when used with <a href="https://docs.upmix.it/scenario-edit/scenario-settings#decision-tree">decision tree (dynamic filter)</a>, screen short name is to be specified in decision tree;</li>
    <li>when used with <a href="https://docs.upmix.it/scenario-edit/scenario-settings#decision-tree">decision tree (dynamic filter)</a>, decision tree is formed using the first case where the specified screen is available, e.g. if one screen is used in several places, the feature will navigate us to the first one;</li>
    <li>function is specified in the description of a screen you want to navigate from using the <code>a</code> tag with the text: <figure><img src="/assets/navigate_sample.png" width="70%"/></figure></li>
    </ul></td>
  </tr>
  <tr>
    <td><pre><code>cside.next</code></pre></td>
    <td><ul><li><pre><code>onclick='cside.next()';</code></pre></li></ul>
    </td>
    <td><ul><li>proceeds to the next screen on specified action</li></ul></td>
  </tr>
  <tr>
    <td><pre><code>cside.show</code></pre></td>
    <td><ul><li><pre><code>onclick="cside.show('all-screen-form-marketo')";</code></pre></li></ul>
    </td>
    <td><ul><li>shows the specified control on indicated action</li></ul></td>
  </tr>
  <tr>
    <td><pre><code>cside.skip</code></pre></td>
    <td><ul><li><pre><code>onclick='cside.skip("sim1",0,0)';</code></pre></li></ul>
    </td>
    <td><ul><li>slips to a specified step, screen, hint</li></ul></td>
  </tr>
</table>

#### hint

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Supported values</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td><code>"hint"</code></td>
    <td>Hints can include: <ul><li>text</li> <li>equations</li> <li>be empty but specified for the focus</li></ul></td>
    <td>Hints can give instruction, more details or other useful info for the flow. Hints may go with or without hint options.</td>
    <td><ul>
    <li><code>"hint": "Proceed here."</code></li>
    <li><code>"hint": "format:Enter your app name{{ '{' }}0{{ '}' }}|yourModel|controlID"</code></li>
    <li><code>"hint": "#"</code></li>
    </ul></td>
  </tr>
</table>

#### hintOptions

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Supported values</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td><code>"hintOptions"</code></td>
    <td><ul><li><code>position</code>: <code>left</code>, <code>right</code> (by default), <code>top</code>, <code>bottom</code>, <code>top-left</code>, <code>top-right</code>, <code>bottom-left</code>, <code>bottom-right</code>, <code>none</code></li> <li><code>size</code>: specified in pixels or <code>auto</code></li><li><code>auto</code> any values for autofill</li><li><code>showDelay</code> time in milliseconds</li><li><code>hideTimeout</code> time in milliseconds</li></ul></td>
    <td>Hint options specify properties for hints. Hints may go with or without hint options.</td>
    <td><ul>
    <li><code>"hintOptions": {{ '{' }} "position": "left"{{ '}' }}</code></li>
    <li><code>"hintOptions": {{ '{' }} "size": "170px" {{ '}' }}</code></li>
    <li><code>"hintOptions": {{ '{' }} "auto": "Company"{{ '}' }}</code></li>
    <li><code>"hintOptions": {{ '{' }} "showDelay": 3000 {{ '}' }}</code></li>
    <li><code>"hintOptions": {{ '{' }} "hideTimeout": 6000 {{ '}' }}</code></li>
    </ul></td>
  </tr>
</table>

#### order number

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Supported values</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td><code>"zIndex"</code></td>
    <td>Any number can be specified</td>
    <td>It defines the sequence of controls. The higher the index is, the higher the control layer is. Canvas has index 1, so control index is indicated related to it.</td>
    <td><code>"zIndex": 5</code></td>
  </tr>
</table>

#### position

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Supported values</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td><code>"position"</code></td>
    <td>Any values can be specified</td>
    <td>It has four parameters: left margin, top margin, width, height</td>
    <td><code> "position": [1, 2, 3, 4]</code></td>
  </tr>
</table>

#### style

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Supported values</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td><code>"style"</code></td>
    <td>Any style can be specified</td>
    <td>Styles are specified as arrays and are to be defined in <a href="https://docs.upmix.it/scenario/styles">style.css</a> file for each scenario</td>
    <td><code>"style": [ "app-name" ]</code></td>
  </tr>
</table>

#### validate

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Supported rules</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td><code>"validate"</code></td>
    <td><ul>
<li><code>["__required"]</code>: field is to be filled out</li>
<li><code>["__regexp_ip"]</code>: IP is required</li>
<li><code>["__regexp_email"]</code>: email is required</li>
<li><code>["__regexp_number"]</code>: number is required</li>
<li><code>["__regexp_url"]</code>: URL is validated</li>
<li><code>["__eq_auto"]</code>: auto value compliance validation</li>
<li><code>["__regexp_custom:^[symbols]]</code>: creates custom validation</li></ul></td>
<td>This property consists of validation rule/s and a message. <br><br>If the value is not validated by the rule, a message will appear inside the hint. User cannot skip this control without indicating either valid data or pressing “next”, which will automatically fill in the field with the data indicated in “auto” of “hintOptions” <code>“|__hintOptions|auto”</code>.<br><br>'format' is applied for values filled-in before.</td>
<td><ul>
<li>field is to be filled out:<pre><code>
"validate": [
  {{ '{' }}
    "rule": ["__required"],
    "message": "format:Name is required to continue. Press next and {{ '{' }}0{{ '}' }} will be used automatically|__hintOptions|auto"
  {{ '}' }}
  ]
</code></pre></li>
<li>IP is required:<pre><code>
"validate": [
  {{ '{' }}
    "rule": ["__regexp_ip"],
    "message": "format:Your Server IP is required. Press next and {{ '{' }}0{{ '}' }} will be used automatically|__hintOptions|auto"
  {{ '}' }}
  ]
</code></pre></li>
<li>email is required:<pre><code>
"validate": [
  {{ '{' }}
    "rule": ["__regexp_email"],
    "message": "format:{{ '{' }}0{{ '}' }} is required to continue. Press next and it will be used automatically|__hintOptions|auto"
  {{ '}' }}
  ]
</code></pre></li>
<li>number is required:<pre><code>
"validate": [
  {{ '{' }}
    "rule": ["__regexp_number"],
    "message": "format:You can use port {{ '{' }}0{{ '}' }} or 8080. Keep going, and we'll fill one in for you!|__hintOptions|auto"
  {{ '}' }}
  ]
</code></pre></li>
<li>URL validation:<pre><code>
"validate": [
  {{ '{' }}
    "rule": ["__regexp_url"],
    "message": "format:App is required to continue. Press next and {{ '{' }}0{{ '}' }} will be used automatically|__hintOptions|auto"
  {{ '}' }}
  ]
</code></pre></li>
<li>auto value validation:<pre><code>
"validate": [
  {{ '{' }}
    "rule": ["__eq_auto"],
    "message": "format:Fill in app name. Press next and {{ '{' }}0{{ '}' }} will be used automatically|__hintOptions|auto"
  {{ '}' }}
  ]
</code></pre></li>
<li>custom validation:<pre><code>
"validate": [
  {{ '{' }}
    "rule": [ "__regexp_custom:^[a-zA-Z0-9][a-zA-Z0-9_]*[a-z0-9]$" ],
    "message": "format:Press next and {{ '{' }}0{{ '}' }} will be used automatically|__hintOptions|auto"
  {{ '}' }}
  ]
</code></pre></li>
</ul></td>
  </tr>
</table>

#### visible

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Supported values</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Code sample</strong></td>
  </tr>
  <tr>
    <td><code>"visible"</code></td>
    <td><code>true</code><code>false</code></td>
    <td>It defines if control is visible</td>
    <td><code>"visible": true</code></td>
  </tr>
</table>
