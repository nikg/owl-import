### **TERMINAL**

#### Control description

Command line interface is created using the **input-terminal** control. It is also [available via Scenario Editor UI](/scenario-edit/controls#control-terminal). It is used to let users interact with a computer by inputting commands. It imitates work of a CLI with some predefined input and output.

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
"type": "input-terminal",
"position": [ 0, 4557, 4650, 693 ],
"settings": {{ '{' }}
  "autoFocus": true,
  "initialStr": "curl http...",
  "theme": {{ '{' }}
  "fontFamily": "Courier, monospace",
  "fontSize": "3rem",
  "fontWeight": "100"
  {{ '}' }},
  "user": "ubuntu",
  "host": "ip-172-24-10-94",
  "connector": "@",
  "prompt": "~$ ",
  "commands": [
    {{ '{' }} "cmd": "what a | b > c", "output": "tahw" {{ '}' }},
    {{ '{' }}
    "cmd": "curl http",
    "output": "output here",
    "default": true,
    "action": [ "save", "this::disable" ]
    {{ '}' }}
  ]
{{ '}' }}
      </code></pre>
    </td>
    <td>
      <figure><img src="/assets/terminal-sample.png"/></figure>
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
     <code>"input-terminal"</code>
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
     <code>[ 0, 4557, 4650, 693 ]</code>
   </td>
   <td>
            Any values can be specified
   </td>
  </tr>
  <tr>
   <td>
    <pre><code>
"settings":
  {{ '{' }}"autoFocus":
  {{ '}' }}
    </code></pre>
   </td>
   <td>
      <code>true</code>
   </td>
   <td>
      <code>true</code> <code>false</code>
   </td>
  </tr>
    <tr>
    <td>
    <pre><code>
"settings":
  {{ '{' }}"initialStr":
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any command can be written to be shown in the CLI by default. Can contain equations
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings":
  {{ '{' }}"theme":
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any theme can be configured
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "user":
  "host":
  "connector":
  "prompt":
  {{ '}' }}
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Any required user, host and connector can be specified
    </td>
  </tr>
    <tr>
    <td>
      <pre><code>
"settings": {{ '{' }}
  "initialOutputs": {{ '{' }}
    "from": "terminalState.terminal-info-010"
    {{ '}' }}
  {{ '}' }}
       </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      This property copies output from other terminal in other model. You need to indicate source model and terminal key identifier. Please note if you need to show other text in output, you may use <code>text</code> instead of <code>from</code> property. If you need to disable this property, you can indicate the <code>this::disable</code> action.
    </td>
  </tr>
  <tr>
    <td>
      <pre><code>
"commands": [
  {{ '{' }} "cmd": "what a | b > c", "output": "tahw" {{ '}' }}
  ]
      </code></pre>
    </td>
    <td>
    <code>{{ '{' }} "cmd": "what a | b > c", "output": "tahw" {{ '}' }}</code>
    </td>
    <td>
      N/A
    </td>
  </tr>
    <tr>
    <td>
      <pre><code>
"commands": [
  {{ '{' }}
    "cmd": "curl http"
   {{ '}' }}
]
      </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Can contain any commands and equations
    </td>
  </tr>
  <tr>
   <td>
    <pre><code>
"commands": [
  {{ '{' }}
    "output": "#include:./resources/10.txt"
  {{ '}' }}
]
    </code></pre>
   </td>
   <td>
            N/A
   </td>
   <td>
            Can be text, link to a file with the output, and contain equations
   </td>
  </tr>
  <tr>
   <td>
    <pre><code>
"commands": [
  {{ '{' }}
    "action": [  ]
  {{ '}' }}
]
    </code></pre>
   </td>
   <td>
             N/A
   </td>
   <td>
      <code>"action": ["next", "save", "show", "hide", "skip", "switch", "focus", "set", "actionDelay", "this::disable" ]</code>
      <br><br>More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
   </td>
  </tr>
  <tr>
   <td>
     <code>"orderNumber"</code>
   </td>
   <td>
             sequential numbering
   </td>
   <td>
             Any number can be given.
   </td>
  </tr>
</table>
