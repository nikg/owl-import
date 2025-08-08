### Title & Description

Fill in scenario title and description.

<figure><img src="/assets/scenario-summary-settings.png" /></figure>

### Scenario Logo

- Each scenario can have its individual brand icon. It will be displayed in the upper left corner in [Default Preview Theme](/portal/preview#scenario-preview-details) only.

<figure><img src="/assets/brand-icon-sample.png" /></figure>

- To assign an icon, navigate to the **Branding** section on the **Summary** tab and add an icon that was preliminary uploaded to [assets](/scenario-edit/assets).

<figure><img src="/assets/brand_icon.png"/></figure>

- Add forward link for icon on-click if needed.

<figure><img src="/assets/brand-icon-link.png"/></figure>

### Additional Links

- 'Additional Links' lets us add a menu with links in it to every screen of the scenario. It will be displayed in the bottom right corner in [Default Preview Theme](/portal/preview#scenario-preview-details) only.

<figure><img src="/assets/res-menu-sample.png"/></figure>

- To configure the Additional Links, navigate to the **Branding** section and click the **ADD MENU** button. Give it a name and save it.

<figure><img src="/assets/resource_menu.png"/></figure>

- Next, add links with description if needed.

<figure><img src="/assets/resource_link.png"/></figure>

### Typography Styles

Styles can be configured and applied across the whole scenario. Configure and add styles for the current scenario as follows:

**ADD FONT**

- Add fonts to the scenario by clicking the **FONTS** button:

<figure><img src="/assets/add-fonts.png"/></figure>

- Then click **LINK NEW FONT** and fill in the form. Paste link or add reference from [Assets](/scenario-edit/assets#add-an-asset). Check the box to use as Stylesheet if needed. Click the **LINK** button.

<figure><img src="/assets/link-new-font-window.png"/></figure>

**IMPORT STYLE**

- Import styles by uploading a `json` file in the **Branding** section of the **Summary** tab:

<figure><img src="/assets/jsonimport.png"/></figure>

**ADD STYLE**

- Click the **ADD** and then **LINK NEW FONT** button or, if you have already added the font needed, just select the font name in the drop-down menu:

<figure><img src="/assets/summary_style.png"/></figure>

- If you selected **LINK NEW FONT** in the previous step, a font form will open. Type in font name and paste link or add reference from [Assets](/scenario-edit/assets#add-an-asset). Check the box to use as Stylesheet if needed. Click the **LINK** button.

<figure><img src="/assets/link-new-font-popup.png"/></figure>

- Back in the style form, fill in style name and configure other settings as needed. Style name shall be unique in the current scenario and can't be modified later. Font name is applied automatically from the font configuration form. Click the **ADD** button to add the style.

<figure><img src="/assets/style-config.png"/></figure>

**APPLY STYLE**

Detailed info on applying styles to controls on screens can be found [here](/scenario-edit/controls#apply-styles).

**EXPORT STYLE**

Typography Styles can be downloaded as a `json` file:

<figure><img src="/assets/jsonexport.png"/></figure>

### Autoplay Mode

- Autoplay allows the entire scenario to be displayed automatically, without the need to manually switch to the next screen or enter any data into a field.
- Autoplay is enabled by default when the scenario preview is opened.
- Autoplay can be disabled manually by turning off the toggle.
- Autoplay is automatically disabled if any interaction with the screen occurs.
- If autoplay is off, and no interaction with the screen occurs within 10 seconds, autoplay turns on again automatically (if there are no additional / other settings for the screen automode).
- The video in the screen or sidebar plays to the end both with autoplay enabled and disabled.
- When autoplay is enabled, the mode displays its toggle whose status can be either configured by default (see points below) or changed manually:

<figure><img src="/assets/autoplay-toggle.png"/></figure>

- Enable the mode from the **Summary** tab. This will enable autoplay mode in its `off` status.

<figure><img src="/assets/enable_automode.png"/></figure>

<figure><img src="/assets/autoplay-off.png"/></figure>

- In order to add autoplay mode in its `on` status by default, enable it in the settings:

<figure><img src="/assets/automode-by-default.png"/></figure>

<figure><img src="/assets/autoplay-on.png"/></figure>

- Autoplay is configured for each screen separately. We can configure its `idle time`, `action time` and `actions`. Click [here](/scenario-edit/screen-settings#autoplay-mode) to configure autoplay mode for a screen.

### Main Icon

Scenario can have its own main icon displayed on the landing page within a [project](/portal/projects). Main icon is displayed only in [Default Theme](/portal/projects#theme-for-landing-page) of landing page.

- First, add icon image to [assets](/scenario-edit/assets).

- Then assign it to the scenario:

<figure><img src="/assets/main_icon_add.png"/></figure>

### Intro Messages

By default each scenario has INTRO guide when you first open it:

<figure><img src="/assets/quick_guide.png"/></figure>

If you want to disable INTRO for a specific scenario, navigate to **Summary** => **Advanced**. Check the box.

<figure><img src="/assets/disable_intro.png"/></figure>

### Tags

Scenarios can have tags which can be used to filter them on landing page within a [project](/portal/projects). In the **Advanced** section type in tags one by one pressing `Enter` after each one:

<figure><img src="/assets/tags.png"/></figure>

### Decision Tree:

#### Code Samples

<table>
  <tr>
    <td><strong>Source Code</strong></td>
    <td>
      <strong>Result</strong>
    </td>
    <td>
      <strong>Prerequisites</strong>
    </td>
  </tr>
  <tr>
    <td colspan="3" style="text-align: center; vertical-align: middle;"><strong>ALT-SELECTOR</strong></td>
  </tr>
  <tr>
    <td>
    <pre><code>
{{ '{' }}
  "maxResults": "10000",
  "recommendationOrder": [
    [
      "s1",
      "s2",
      "s3"
    ]
  ],
  "groups": [
    {{ '{' }}
      "label": "Group 1: alt-selector",
      "type": "open",
      "qq": [
        {{ '{' }}
          "text": "This is Question 1:",
          "orderNumber": 0,
          "key": "key1",
          "type": "alt-selector",
          "extend": false,
          "settings": {{ '{' }}
            "values": [
              "screens 1 & 2",
              "screens 2 & 3",
              "screens 3"
            ],
            "default": "screens 3"
          {{ '}' }},
          "optionsValue": {{ '{' }}
            "screens 1 & 2": [
              "s1",
              "s2"
            ],
            "screens 2 & 3": [
              "s2",
              "s3"
            ],
            "screens 3": [
              "s3"
            ]
         {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  ]
{{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/alt-selector.png"/></figure>
    </td>
      <td>
      flow has 3 screens with <code>s1</code>, <code>s2</code> & <code>s3</code> screen short names
    </td>
  </tr>
  <tr>
    <td colspan="3" style="text-align: center; vertical-align: middle;"><strong>CHECKBOX</strong></td>
  </tr>
  <tr>
    <td>
    <pre><code>
{{ '{' }}
  "maxResults": "10000",
  "recommendationOrder": [
    [
      "s1",
      "s2"
    ]
  ],
  "groups": [
    {{ '{' }}
      "label": "Group 2: checkbox",
      "type": "additional",
      "qq": [
        {{ '{' }}
          "text": "Question 2 here:",
          "orderNumber": 2,
          "key": "key-checkbox",
          "note": "",
          "type": "checkbox",
          "extend": false,
          "settings": {{ '{' }}
            "default": "unchecked"
          {{ '}' }},
          "optionsValue": {{ '{' }}
            "checked": [
              "s2"
            ],
            "unchecked": [
              "s1"
            ]
          {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  ]
{{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure ><img src="/assets/checkbox-sample.png" /></figure>
    </td>
      <td>
      flow has 2 screens with <code>s1</code> & <code>s2</code> short screen names
    </td>
  </tr>
  <tr>
    <td colspan="3" style="text-align: center; vertical-align: middle;"><strong>DROPDOWN</strong></td>
  </tr>
  <tr>
    <td>
    <pre><code>
{{ '{' }}
  "maxResults": "10000",
  "recommendationOrder": [
    [
      "s1",
      "s2",
      "s3"
    ]
  ],
  "groups": [
    {{ '{' }}
      "label": "Group 1: dropdown",
      "type": "open",
      "qq": [
        {{ '{' }}
          "text": "This is Question 1:",
          "orderNumber": 1,
          "key": "key-dropdown",
          "type": "dropdown",
          "extend": false,
          "settings": {{ '{' }}
            "values": [
              "1",
              "2",
              "3"
            ],
            "default": "3"
          {{ '}' }},
          "optionsValue": {{ '{' }}
            "1": [
              "s1"
            ],
            "2": [
              "s2"
            ],
            "3": [
              "s3"
            ]
          {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  ]
{{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure ><img src="/assets/drop-sample.png" /></figure>
    </td>
      <td>
      flow has 3 screens with <code>s1</code>, <code>s2</code> & <code>s3</code> screen short names
    </td>
  </tr>
  <tr>
    <td colspan="3" style="text-align: center; vertical-align: middle;"><strong>RANGE-SELECTOR</strong></td>
  </tr>
  <tr>
    <td>
    <pre><code>
{{ '{' }}
  "maxResults": "10000",
  "recommendationOrder": [
    [
      "s1",
      "s2",
      "s3",
      "s4"
    ]
  ],
  "groups": [
    {{ '{' }}
      "label": "Group 1: range-selector",
      "type": "open",
      "qq": [
       {{ '{' }}
          "text": "This is Question 1:",
          "orderNumber": 1,
          "key": "key-rangesel",
          "type": "range-selector",
          "extend": false,
          "settings": {{ '{' }}
            "default": 4,
            "out": "eval: ({{ '{' }}v, d, i{{ '}' }}) => {{ '{' }} return i === 5 ? {{ '{' }}v, d: 'TB+'{{ '}' }} : {{ '{' }}v, d: ''{{ '}' }}{{ '}' }}"
          "optionsRange": [
            {{ '{' }}
              "range": [
                1,
                25
              ],
              "res": [
                "s1"
              ]
            {{ '}' }},
            {{ '{' }}
              "range": [
                25,
                40
              ],
              "res": [
                "s2"
              ]
            {{ '}' }},
            {{ '{' }}
              "range": [
                40,
                100
              ],
              "res": [
                "s3"
              ]
            {{ '}' }},
            {{ '{' }}
              "range": [
                100,
                200
              ],
              "res": [
                "s1",
                "s2",
                "s3",
                "s4"
              ]
            {{ '}' }}
          ]
        {{ '}' }}
      ]
    {{ '}' }}
  ]
{{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure ><img src="/assets/range-selector-sample.png" /></figure>
    </td>
      <td>
      flow has 4 screens with <code>s1</code>, <code>s2</code>, <code>s3</code> & <code>s4</code> short screen names
    </td>
  </tr>
  <tr>
    <td colspan="3" style="text-align: center; vertical-align: middle;"><strong>SLIDER</strong></td>
  </tr>
  <tr>
    <td>
    <pre><code>
{{ '{' }}
  "maxResults": "10000",
  "recommendationOrder": [
    [
      "s2",
      "s3"
    ]
  ],
  "groups": [
    {{ '{' }}
      "label": "Group 2: dropdown",
      "type": "open",
      "qq": [
        {{ '{' }}
          "text": "Question: slider control",
          "orderNumber": 10,
          "key": "cpu",
          "note": "",
          "type": "slider",
          "settings": {{ '{' }}
            "default": 2,
            "range": [
              1,
              10
            ],
            "labels": [
              "2",
              "3"
            ],
            "out": "eval: ({{ '{' }}v, d{{ '}' }}) => (v > 224) ? ({{ '{' }}v: 224, d: 'units'{{ '}' }}) : ({{ '{' }}v, d: 'units'{{ '}' }})",
            "in": "eval: ({{ '{' }}v, d{{ '}' }}) => ({{ '{' }}v, d{{ '}' }})"
          {{ '}' }},
          "optionsRange": [
            {{ '{' }}
              "range": [
                0,
                5
              ],
              "res": [
                "s2"
              ]
            {{ '}' }},
            {{ '{' }}
              "range": [
                6,
                10
              ],
              "res": [
                "s3"
              ]
            {{ '}' }}
          ]
        {{ '}' }}
      ]
    {{ '}' }}
  ]
{{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure ><img src="/assets/slider-sample.png" /></figure>
    </td>
      <td>
      flow has 2 screens with <code>s2</code> & <code>s3</code> screen short names
    </td>
  </tr>
</table>

#### Enabling

- Navigate to the **Summary** tab and scroll down to the **Decision Tree** section. Click the `EDIT JSON` button.

<figure><img src="/assets/enable-dec-tree.png"/></figure>

#### Properties

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Sample</strong></td>
    <td>
      <strong>Description</strong>
    </td>
  </tr>
  <tr>
    <td colspan="3" style="text-align: center; vertical-align: middle;"><strong>BASIC PROPERTIES</strong></td>
  </tr>
  <tr>
    <td>
    <code>"maxResults"</code>
    </td>
    <td>
      <code>"maxResults": "10000"</code>
    </td>
    <td>
      max number of available results
    </td>
  </tr>
  <tr>
    <td>
    <code>"extendValues"</code>
    </td>
    <td>
      <pre><code>
"extendValues": [
  "screen1",
  "screen2",
  "screen3"
  ]
</code></pre>
    </td>
    <td>
      values specified here (screen <a href="https://docs.upmix.it/scenario-edit/screen-settings#title-text-notes--short-name">short names</a> or control key) will be added to the question where <code>"extend": true</code> is specified. Note that only values that go <b>AFTER</b> the selected option in the question will be added. Say, if <code>screen2</code> is selected, then <code>screen3</code> will be added as part of <code>extend</code> functionality.
    </td>
  </tr>
  <tr>
    <td>
      <code>"recommendationOrder"</code>
    </td>
    <td>
    <pre><code>
"recommendationOrder": [
  [
    "screen1",
    "screen2",
    "screen3"
  ]
]
</code></pre>
    </td>
    <td>
      lists keys of objects (screens & controls) to be used in decision tree. Screen keys are their <a href="https://docs.upmix.it/scenario-edit/screen-settings#title-text-notes--short-name">short names</a>. 
    </td>
  </tr>
  <tr>
    <td colspan="3" style="text-align: center; vertical-align: middle;"><strong>GROUP PROPERTIES</strong></td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "label": 
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "label": "Group 1"
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      group name
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "type": 
  {{ '}' }}
]
    </code></pre>
    </td>
    <td><ul>
    <li>open:
    <pre><code>
"groups": [
  {{ '{' }}
    "type": "open"
  {{ '}' }}
]
    </code></pre></li>
    <li>additional:
    <pre><code>
"groups": [
  {{ '{' }}
    "type": "additional"
  {{ '}' }}
]
    </code></pre></li>
    </ul>
    </td>
    <td><ul>
    <li><code>open</code> shows group unfolded</li>
    <li><code>additional</code> shows group folded</li>
    </ul>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      question settings
    </td>
  </tr>
  <tr>
    <td colspan="3" style="text-align: center; vertical-align: middle;"><strong>QUESTION CONFIGURATION</strong></td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "text": 
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "text": "Question 1"
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      question text
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "orderNumber":
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "orderNumber": 0
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      question order number
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "key":
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "key": "uniqueKey"
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      question unique key
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "type": 
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "type": "dropdown"
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      the following types are available: 
      <ul>
      <li><code>"dropdown"</code></li>
      <li><code>"checkbox"</code></li>
      <li><code>"alt-selector"</code></li>
      <li><code>"range-selector"</code></li>
      <li><code>"slider"</code></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "extend": 
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "extend": false / true
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      if it is true for a question, decision tree adds all values specified in <code>"extendValues"</code> that go <b>AFTER</b> the selected option in the question
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "append": 
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "append": true / false
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      if it is true, then despite valid intersections the decision tree adds the corresponding selections specified in <code>"optionsValue"</code> based on the choice made
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
          "values": [   ]
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
            "values": [
              "Other",
              "1",
              "2"
            ]
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      specifies possible values for <b>dropdown</b> & <b>alt-selector</b>  types and their default option
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
          "default": " "
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <ul>
    <li>sample for <b>slider</b>, <b>range-selector</b>:
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
            "default": 2
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </li>
    <li>sample for <b>checkbox</b>:
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
            "default": "unchecked"
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </li>
    <li>sample for <b>dropdown</b>, <b>alt-selector</b>:
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
            "default": "1"
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </li>
    </ul>
    </td>
    <td>
      specifies default option 
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "optionsValue": {{ '{' }}
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <ul>
    <li>sample for <b>dropdown</b>, <b>alt-selector</b>:
    <pre><code>
"optionsValue": {{ '{' }}
  "1": "bundle:[q1]",
  "2": "bundle:[q2]",
  "3": [
              "scr1",
              "scr2"
            ],
  "Other": []
{{ '}' }}
    </code></pre></li>
    <li>sample for <b>checkbox</b>:
    <pre><code>
"optionsValue": {{ '{' }}
  "checked": "bundle:[q1]",
  "unchecked": "bundle:[q2]"
{{ '}' }}
    </code></pre>
    </li>
    </ul>
    </td>
    <td>
      specifies options that are related to each value. Values can be specified directly or as a bundle to another question. If bundle to another question is specified, the question is shown only if the value is true (<code>"checked"</code> or <code>"unchecked"</code>) 
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
          "range": [   ],
          "labels": [   ]
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
          "range": [ 1, 10 ],
          "labels": [
              "<1 units",
              ">10 units"
            ]
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      specifies range and its value labels for <b>slider</b> type. If both values of range are the same, say, <code>"range": [200, 200]</code>, then only one value will be shown in UI.
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "optionsRange": [ ]
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "optionsRange": [
  {{ '{' }}
    "range": [
        0,
        3
    ],
    "res": [
        "scr1"
    ]
    {{ '}' }},
    {{ '{' }}
      "range": [
        4,
        10
    ],
      "res": [
        "scr2"
    ]
    {{ '}' }}
]
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      specifies result for each range for <b>slider</b> and <b>range-selector</b>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
            "in":
            "out":
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
    <pre><code>
"groups": [
  {{ '{' }}
    "qq": [
      {{ '{' }}
        "settings": {{ '{' }}
            "out": "eval: ({{ '{' }}v, d, i{{ '}' }})) => {{ '{' }} return i === 5 ? {{ '{' }}v, d: 'TB+'{{ '}' }}) : {{ '{' }}v, d: ''{{ '}' }}){{ '}' }})",
            "in": "eval: ({{ '{' }}v, d{{ '}' }}) => (d === 'GB') ? ({{ '{' }}d, v{{ '}' }}) : ({{ '{' }}d, v: v * 1000{{ '}' }})"
          {{ '}' }}
      {{ '}' }}
    ]
  {{ '}' }}
]
    </code></pre>
    </td>
    <td>
      these properties are used to convert values for <b>slider</b> & <b>range-selector</b> controls as specified in the <code>eval</code>, where <code>out</code> stands for output value and <code>in</code> stands for the input value. In the <code>eval</code>, <code>v</code> is the value, <code>d</code> is the dimension/unit, and <code>i</code> is index that specifies element position, where <code>0</code> is the first one, <code>1</code> is the second, etc.  
    </td>
  </tr>
</table>

#### Logic

- only matching results among all questions (selections) are shown
  (e.g., if in group 1 options 1 & 2 are selected, but in group 2 – only option 1, then option 1 will be shown as a result);
- if same screen is a match in new selection, it does not change. It will be changed only if it is not available in the newly selected option;
- if screen title starts with **!--**, it is not shown in navigation panel of preview mode:
  <figure><img src="/assets/no-screen-title.png"/></figure>

### Action Plan

Action plan lets users assign an action plan to screens and add it. Action plan can only be used with [Default preview theme](/portal/workspace#preview-theme) that has left sidebar.

**Action plan example**

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
{{ '{' }}
  "id": "eerjewjrew",
  "title": "YOUR ACTION PLAN",
  "controls": {{ '{' }}
    "add": "Add this solution to my <b>Action Plan</b>",
    "btnMyPlan": "My Action Plan: <b>{{ '{' }}{{ '{' }}qty{{ '}' }}{{ '}' }}</b> items",
    "btnShare": "SHARE"
  {{ '}' }},
  "actions": [
    {{ '{' }}
      "id": "e5d0f48e-927b-4887-a137-4e8f76692f74",
      "title": "<div>Solution 1</div>",
      "screens": [
        "scr1"
      ],
      "block": [
        {{ '{' }}
          "type": "html",
          "dataObj": {{ '{' }}
            "html": "<div>Solution 1:<ul><li>Lorem Ipsum is simply dummy text</li><li>Lorem Ipsum is simply dummy text</li></ul></div><div><p>Lorem Ipsum is simply dummy text of.</p><p>Lorem Ipsum is simply dummy text of. </p></div>"
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "links",
          "dataArr": [
            {{ '{' }}
              "label": "Solution 1",
              "href": "https://google.com"
            {{ '}' }}
          ]
        {{ '}' }}
      ]
    {{ '}' }},
    {{ '{' }}
      "id": "e4bd5e70-aee9-47f0-b4b2-dc234612ad95",
      "title": "<div>Solution 2</div>",
      "screens": [
        "scr2"
      ],
      "block": [
        {{ '{' }}
          "type": "html",
          "dataObj": {{ '{' }}
            "html": "<div>Solution 2:<ul><li>Lorem Ipsum is simply dummy text</li><li>Lorem Ipsum is simply dummy text</li></ul></div><div><p>Lorem Ipsum is simply dummy text of.</p><p>Lorem Ipsum is simply dummy text of. </p></div>"
          {{ '}' }}
        {{ '}' }},
        {{ '{' }}
          "type": "links",
          "dataArr": [
            {{ '{' }}
              "label": "Solution 2",
              "href": "https://google.com"
            {{ '}' }}
          ]
        {{ '}' }}
      ]
    {{ '}' }}
  ]
{{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/action-plan.png"/></figure>
    </td>
  </tr>
</table>

**Action plan configuration**

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td>
      <strong>Description</strong>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "id": "unique-id-here"
     </code></pre>
    </td>
    <td>
      a unique ID of action plan. If various scenarios have the same action plan, ID is to be the same
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "title": "YOUR ACTION PLAN"
     </code></pre>
    </td>
    <td>
      any action plan title
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "controls": {{ '{' }}
    "add": "Add this solution to my <b>Action Plan</b>"
  {{ '}' }}
     </code></pre>
    </td>
    <td>
      any text to add a plan
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "controls": {{ '{' }}
    "btnMyPlan": "My Action Plan: <b>{{ '{' }}{{ '{' }}qty{{ '}' }}{{ '}' }}</b> items"
  {{ '}' }}
     </code></pre>
    </td>
    <td>
      any button text to show the added plan(s)
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "controls": {{ '{' }}
    "btnShare": "SHARE"
  {{ '}' }}
     </code></pre>
    </td>
    <td>
      lets share the added action plan via a copied URL link
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
   "actions": [
    {{ '{' }}
      "id": "id-here"
        {{ '}' }}
      ]
     </code></pre>
    </td>
    <td>
      a unique ID of actions. Can be shared between various action plans
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "actions": [
    {{ '{' }}
      "title": "<div>Solution 1</div>"
    {{ '}' }}
  ]
     </code></pre>
    </td>
    <td>
      any action title
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "actions": [
    {{ '{' }}
      "screens": [
        "screen-short-name"
      ]
    {{ '}' }}
  ]
     </code></pre>
    </td>
    <td>
      specifies screens where action plan is enabled and applicable. In order to add action plan to a screen, you need to specify screen <a href="https://docs.upmix.it/scenario-edit/screen-settings#title-text-notes--short-name
      ">short name</a>
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "actions": [
    {{ '{' }}
      "block": [
        {{ '{' }}
          "type": "html",
          "dataObj": {{ '{' }}
            "html": "html here"
          {{ '}' }}
        {{ '}' }}
      ]
    {{ '}' }}
  ]
     </code></pre>
    </td>
    <td>
      information block of HTML type
    </td>
  </tr>
  <tr>
    <td>
    <pre><code>
  "actions": [
    {{ '{' }}
      "block": [
         {{ '{' }}
          "type": "links",
          "dataArr": [
            {{ '{' }}
              "label": "link text",
              "href": "link here"
            {{ '}' }}
          ]
        {{ '}' }}
      ]
    {{ '}' }}
  ]
     </code></pre>
    </td>
    <td>
      information block of link type
    </td>
  </tr>
</table>
