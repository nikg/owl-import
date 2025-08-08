### **Resources**

All scenario resources can be stored in **resources** folder that can include:

- images

- [HTML](/scenario/resources#html-file) files

- icons

- [JS](/scenario/resources#js-file) files with functions

- other required resources.

The directory is indicated as follows: `"icon": "./resources/main-icon.png"`.

Note that if a file name starts with a capital letter, it should be specified exactly in the same way (capital letter) in a meta file.

#### **.html** file

**.html** file is used for the [html](/scenario-controls/html-control) control and can include:

1. Text to be shown

2. Control style

3. Reference (which includes the global object (`"cside."`) and a function)

#### **.js** file

If **.js** code is to be included into the scenario, save it in a file in the **resources** folder and include a reference to it as:

`#include:./resources/js/name.js`

Here's an example of js function:

<pre><code>
eval:(bm) => 
{{ '{' }}
  var str = bm.user.userName + '@' + bm.user.company + '.com';
  return lc.replace(/ /g,'.');
{{ '}' }}
</code></pre>
