### **Screens**

Each UI screen needs a `.png` and a `.meta` file to be deployed. Sometimes screens can also have referenced files and layouts. They all are to be stored in the **screens** folder.

#### **layouts**

Any screen can have its layout. Layouts are stored in a folder inside the `screens` folder. Layout folder name is to coincide with the name of metadata file it refers to plus `.layout`:

<pre>00$start-001.meta.layout</pre>

**A few notes on layouts:**

- Layouts use the model indicated in main screen's metadata file, whereas contexts can be different.

- Layout folder may contain as many files as needed. Numbering can be any, but extension shall always be `.layout`: `01.layout`

- If needed, layout files can include: `"context"`, `"binding"`, `"controls"`, and `"settings"` for the layout itself including `"title", "description"` and `"visible"` (this property can have equations).

- If a layout is visible, its own title and description will be used rather than default screen’s. If it doesn’t have its own title and description, default screen’s are used.

- Metadata file has the priority over the layouts.

- Each layout file can have its own screen image. Such image prevails over the image of the main metadata file if `"visible"` property of the layout is `"true"`. Such images are named according to the rules for naming screenshots for screens:

<pre>
    03name-060.layout
    03name-060.layout.t.png
</pre>

#### **.meta** file

**.meta** file contains all the necessary metadata for a screen, including all controls available for interaction, prepopulated data, as well as binding. Its name has the following pattern:

<pre>{{ '{' }}step name{{ '}' }}-{{ '{' }}order id{{ '}' }}.meta</pre>

Here's an example:

<pre>02$signup-003.meta</pre>

**A few notes on meta files:**

- Meta files can have comments: `//` and `/ /`.

- Each metadata file can have its own folder with layout files. They shall have the same model, but can have different contexts. More detailed info on layout files can be found in [layouts](/scenario/screens#layouts) subsection.

- In variables that define screen visibility and layouts, binding model can’t be used, only binding data.

- If a meta file has a [reference](/scenario/screens#references), the name of its attribute describes model name and field it is referenced to. For example, "userId" means reference to object "user" and field "id".

##### **Properties of a meta file**

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td><code>"title"</code></td>
    <td>
      specifies screen title
    </td>
    <td><code>"title": "Intro"</code></td>
  </tr>
  <tr>
    <td><code>"description"</code></td>
    <td>
      includes a short description for the screen. It can contain text or include a reference to an <code>.html</code> file to execute specified actions 
    </td>
    <td>
    <code>"description": "#include:./resources/name.html"</code>
    </td>
  </tr>
  <tr>
    <td>
    <code>"settings"</code>
    </td>
    <td><ul>
      <li><code>dpr</code> (Device Pixel Ratio) of an original image: 1, 2, 3. DPR property is obligatory and is used for scaling the images</li>
      <li><code>events</code> define actions for the screen. These actions are activated before the screen is shown and even if the screen is skipped</li>
      <li><code>visible</code> makes it visible or not</li>
      <li><code>exclude</code> lets completely skip the indicated screen in the scenario flow</li>
      <li><code>ui</code> can be either <code>noUi</code> (hides sidebar and toolbar) or <code>demoMode</code> (hides only sidebar)</li>
      <li><code>autoScrollDescription</code> enables autoscroll for the description in the left panel</li>
      <li><code>scroll</code> autoscrolls the page to the desired element</li>
    </ul><td>
    <pre><code>
"settings": {{ '{' }}
  "dpr": 1,
  "events": {{ '{' }}
    "show": "#include:./resources/js/set-vars.js"
    {{ '}' }},
  "visible": "#include:./resources/js/ubuntu.js",
  "exclude": "#include:./resources/js/suse.js",
  "ui": "noUi",
  "autoScrollDescription": false,
  “scroll”: “hintId”
{{ '}' }}
    </code></pre>
    </td>
  </tr>
  <tr>
    <td>
    <code>"model"</code>
    </td>
    <td>
      specifies the object containing data of the current screen. Screen model can be specified in its <code>context</code>. Model name must not contain points!
    </td>
    <td><code>"model": "name"</code>
    </td>
  </tr>
  <tr>
    <td>
    <code>"context"</code>
    </td>
    <td>
      is specified in case we need to use something from another object or source. Context can be indicated without any model inside the file. Context is to be indicated as an array <code>[ ]</code>. Several models can be referred to in context
    </td>
    <td><code>"context": ["user", "site"]</code>
    </td>
  </tr>
  <tr>
    <td>
    <code>"merge"</code>
    </td>
    <td>
      defines how many screens will be included into one group having one title and description
    </td>
    <td><code>"merge": "2"</code>
    </td>
  </tr>
  <tr>
    <td>
    <code>"binding"</code>
    </td>
    <td>
    <ul>
      <li>indicates binding values and controls where <code>*</code> means that value corresponds to control name</li>
      <li>binding options may be indicated as one way only which means data isn’t shown in a control when showing the screen</li>
      <li>binding can include <a href="https://docs.upmix.it/scenario-controls/controls-meta#expression">expressions</a> which may contain JS functions or be added as a separate JS document using the <code>#include:</code></li>
      </ul>
    </td>
    <td>
    <ul>
    <li>example with a referenced file <pre><code>
"context": [ "user", "site" ],
  "binding": {{ '{' }}
    "aName": "user.aName",
    "company": "*",
    "eName": "site.eName",
    "date2": "#include:./resources/js/date.js"
  {{ '}' }},
  "bindingOptions": {{ '{' }}
    "oneWay": true
  {{ '}' }}
    </code></pre>
    </li>
    <li>example with a function <pre><code>
"binding": {{ '{' }}
    "aName": "eval:({{ '{' }}generatedData{{ '}' }}) => `${{ '{' }}generatedData.length{{ '}' }}`"
  {{ '}' }}
    </code></pre></li>
    <li>example with a format <pre><code>
"binding": {{ '{' }}
    "campaign":"format:{{ '{' }}0{{ '}' }}|model|value"
  {{ '}' }}
    </code></pre></li>
    </ul>
    </td>
  </tr>
  <tr>
    <td>
    <code>"screenOptions"</code>
    </td>
    <td>
      lets skip a screen. It is verified by model
    </td>
    <td>
    <pre><code>
"screenOptions": {{ '{' }}
    "hideIfDataAvailable": true,
    "modelFieldsRequired": ["userName", "company]
    {{ '}' }}
    </code></pre>
    </td>
  </tr>
  <tr>
    <td>
    <code>"controls"</code>
    </td>
    <td>
      help navigate the flow and make it interactive. Controls must not contain spaces in their names. Control name can include <code>shared::</code> property which means that this control is shared between several screens
    </td>
    <td>
    <pre><code>
"sidebar": {{ '{' }}
    "shared::th3": {{ '{' }}
      "type": "output-video-player",
      "img": "./resources/th/step3.mp4"
    {{ '}' }}
{{ '}' }}
    </code></pre>
    </td>
  </tr>
</table>

#### **.png** file

This file shows a template which will be shown during simulation. Its name has the following pattern:

<pre>{{ '{' }}step name{{ '}' }}-{{ '{' }}order id{{ '}' }}.t.png</pre>

Here's an example:

<pre>00$start-001.t.png</pre>

For more information on screenshots [proceed here](/scenario-edit/screenshots#screenshots).

#### **references**

If the same screenshots are used for different steps/screens of the scenario, there’s no need to add this file for each step/screen. Instead:

1. Specify file format as `.ref` rather than `.png` (for the step you don’t want to duplicate), e.g.

<pre>
    000000$intro-00000003.t.ref
</pre>

2. Open the created .ref file and specify name of the screenshot which you want to use inside it:

<pre>
    {{ '{' }}step name{{ '}' }}-{{ '{' }}order id{{ '}' }}.t.png
</pre>

3. Don't forget to create a [meta](/scenario/screens#meta-file) file for it.
