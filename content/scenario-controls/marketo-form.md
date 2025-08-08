### **MARKETO FORM**

#### Control description

Marketo forms let us capture data from marketing campaigns. They send people to our website or Marketo landing pages. **integration-form-submit--marketo** control is used to create Marketo forms. It also [available via Portal UI](/portal/integrations#marketo-form). In our flows this form is aimed at collecting some information about users and is integrated with Marketo server, so all the data filled into the form are sent and stored in Marketo.

In order to integrate the form you need:

1. Go to the [index.json](/scenario/index) file and specify integration server in the`"integration"` property:

<pre><code>
"integration": {{ '{' }}
      "module": ["marketo"]
{{ '}' }}
</code></pre>

2. Go to the [style.css](/scenario/styles) file and specify form styles under `#integrationFormModal`:

<pre><code>
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
</code></pre>

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
"type": "integration-form-submit--marketo",
"position": [ 10, 10, "1000px", "1000px" ],
"binding": {{ '{' }}
  "Additional_Score_Detail__c": "format:{{ '{' }}0{{ '}' }}|__attendeePath|scenario-titles-only",
  "FirstName": "coalesce:field:form.FirstName/firstName:format:{{ '{' }}0{{ '}' }}|user|userName",
  "LastName": "coalesce:field:form.LastName/lastName:format:{{ '{' }}0{{ '}' }}|user|userName",
  "Company": "coalesce:field:form.Company/format:{{ '{' }}0{{ '}' }}|user|company/format:{{ '{' }}0{{ '}' }}|user|serviceName",
  "Email": "coalesce:field:form.Email/format:{{ '{' }}0{{ '}' }}|user|email"
{{ '}' }},
"settings": {{ '{' }}
  "redirect": false,
  "mode": "popup",
  "munchkinId": "111-111-111",
  "formId": 11111,
  "delay": 1,
  "content": {{ '{' }}
    "header": "#include:./resources/html/marketo-header.html",
    "text": "#include:./resources/html/marketo-text.html",
    "footer": "",
    "success-text": "#include:./resources/html/marketo-success.html"
    {{ '}' }},
  "no-defaults": {{ '{' }}
    "FirstName": "Awesome",
    "LastName": "Dev",
    "Company": "Awesome Org"
    {{ '}' }}
  {{ '}' }}
     </code></pre>
    </td>
    <td>
      <figure><img src="/assets/marketo-sample.png"/></figure>
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
      <code>"integration-form-submit--marketo"</code>
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
     <code>[ 10, 10, "1000px", "1000px" ]</code>
    </td>
    <td>
      Any values can be specified. <code>"position"</code> is a must unless it's a popup mode
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
  <tr>
    <td>
    <pre><code>
"binding": {{ '{' }}
  "Additional_Score_Detail__c": "format:{{ '{' }}0{{ '}' }}|__attendeePath|scenario-titles-only"
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <code>"Additional_Score_Detail__c"</code> variable keeps and aggregates the data from the last 200 pages the user visited. It can include three different parameters meaning the amount of data stored: <code>"standard"</code>, <code>"small"</code>, <code>"scenario-titles-only"</code>. If you need some definite value to be recorded, you should indicate it as <code>"dump"</code> in <code>"settings"</code>:
      <pre><code>
"settings": {{ '{' }}
  "dump": "eval:() => `\tName: ${{ '{' }}_bd.user.userName{{ '}' }}`"
  {{ '}' }}
      </code></pre>
   </td>
  </tr>
  <tr>
   <td>
    <pre><code>
"binding": {{ '{' }}
  "FirstName": "coalesce:field:form.FirstName/firstName:format:{{ '{' }}0{{ '}' }}|user|userName"
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <pre><code>binding</code></pre> binds data from models or other sources with form fields. <pre><code>coalesce</code></pre> is used to return the first value which isn't "null" either before or after the "slash".
    </td>
  </tr>  
  <tr>
   <td>
    <pre><code>
"settings": {{ '{' }}
  "redirect":
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <pre><code>redirect</code></pre> defines where the form redirects to, where <pre><code>false</code></pre> means no redirection, <pre><code>true</code></pre> means default redirection to the page defined by Marketo for this form.
    </td>
  </tr>  
  <tr>
   <td>
    <pre><code>
"settings": {{ '{' }}
  "mode": 
   {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      <pre><code>popup</code></pre> displays the form on top of the current page and the user "submits" it
      <pre><code>embedded</code></pre> displays the form in the specified "position" and the user "submits" it
      <pre><code>silent</code></pre> mode just submits the form without showing it if all the required data is available. Otherwise, it doesn't submit the form.
      <pre><code>popup-or-silent</code></pre> mode validates the data in the form, and if the data is valid, the form is submitted without showing.
    </td>
  </tr>  
  <tr>
   <td>
    <pre><code>
"settings": {{ '{' }}
  "munchkinId":
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It is a pre-defined parameter for Marketo system
    </td>
  </tr>  
  <tr>
   <td>
    <pre><code>
"settings": {{ '{' }}
  "formId":
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It is a pre-defined parameter for Marketo system
    </td>
  </tr>  
  <tr>
   <td>
    <pre><code>
"settings": {{ '{' }}
  "delay":
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Defines time after which the form appears and can be any
    </td>
  </tr>  
  <tr>
   <td>
    <pre><code>
"settings": {{ '{' }}
  "content": {{ '{' }}
    "header": "#include:./resources/html/marketo-header.html",
    "text": "#include:./resources/html/marketo-text.html",
    "footer": "",
    "success-text": "#include:./resources/html/marketo-success.html"
     {{ '}' }},
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      Content may be specified as a reference to an HTML stored in <a href="https://docs.upmix.it/scenario/resources">resources</a> . <code>"success-text"</code> may be included and will appear when Submit is hit, or it may be skipped as an option
    </td>
  </tr>  
  <tr>
   <td>
    <pre><code>
"settings": {{ '{' }}
  "no-defaults": {{ '{' }}
  "FirstName": "Awesome",
  "LastName": "Dev",
  "Company": "Awesome Org"
  {{ '}' }}
{{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It defines the default / pre-defined values which are not to be submitted with the form
    </td>
  </tr>  
  <tr>
   <td>
    <pre><code>
"settings": {{ '{' }}
  "model": "form"
  {{ '}' }}
    </code></pre>
    </td>
    <td>
      N/A
    </td>
    <td>
      It is indicated if our form belongs to the screen where other data is generated and stored in a model with another name. So, by writing this property, the user creates one more model for the data filled into the form. When added, it should be indicated in the <code>"context"</code> property of the medatada file.
    </td>
  </tr> 
</table>
