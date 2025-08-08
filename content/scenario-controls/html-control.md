### **HTML**

#### Control description

This control lets user show information from JSON file as HTML, such as highlights, popups, various bubbles and more. It is created using the **output-html** control.

#### Functions

HTML control file can include functions. Detailed info & examples on functions can be found [here](/scenario/resources#html-file).

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
<ul> 
<li><b>json</b>:
  "type": "output-html",
  "position": [ "0px", "143px", "947px", "238px" ],
  "visible": true,
  "html": "Click here",
  "overflow": "scroll",
  "style": ["sample-html"]</li>
<li><b>styles</b>:
.sample-html {{ '{' }}
background-image: url("./resources/454/bubble2.png");
font-family: sans-serif;
color: #CCCCCC;
text-align: left;
font-size: 60px;
font-weight: 100;
padding: 80px 150px 20px 250px;
{{ '}' }}</li>
<li><a href="https://api.upmix.it/api/v1/linked-object/67212de631c174ecc4cf0904">image</a>
</li>
</ul>
</code></pre>
</td>
<td>
<figure><img src="/assets/html-sample.png"/></figure>
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
     <code>"output-html"</code>
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
     <code>[ 0, 144, 650, 100 ]</code>
   </td>
   <td>
            Any values can be specified
   </td>
  </tr>
  <tr>
   <td>
      <code>"html": "#include:./resources/html/sample.html"</code>
   </td>
   <td>
    N/A
   </td>
   <td>
      Directory to the HTML file
   </td>
  </tr>
  <tr>
    <td>
    <code>"action"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>"action": ["next", "save", "show", "hide", "skip", "switch", "toggle", "focus", "set", "zoom" ]</code><br><br>More info on actions can be found <a href="https://docs.upmix.it/scenario-controls/controls-meta#action">here</a>.
    </td>
  </tr>
    <tr>
    <td>
    <code>"overflow"</code>
    </td>
    <td>
      N/A
    </td>
    <td>
      <pre><code>"hidden"</code></pre> means that the overflow is clipped, and the rest of the content will be invisible
      <pre><code>"scroll"</code></pre> means that the overflow is clipped, and a scrollbar is added to see the rest of the content
      <pre><code>"auto"</code></pre> is similar to scroll, but it adds scrollbars only when necessary
      <pre><code>"visible"</code></pre> doesn't clip the overflow
    </td>
  </tr>
  <tr>
   <td>
     <code>"style"</code>
   </td>
   <td>
            N/A
   </td>
   <td>
            Any style can be specified. More info on styles can be found <a href="https://docs.upmix.it/scenario/styles">here</a>.
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
