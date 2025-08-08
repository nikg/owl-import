### **script.js**

**script.js** file contains JavaScript functions that are run by HTML specified in [HTML](/scenario-controls/html-control) control of [meta](/scenario/screens#meta-file) file. Below is an example of how to indicate such HTML in a metadata file:

<pre><code>
"region-map": {{ '{' }}
   "type": "output-html",
   "position": [ 0, 0, 4001, 2261 ],
   "html": "#include:./resources/html/sim.html"
    {{ '}' }}
</code></pre>

Functions are run by actions indicated in the HTML. See an example of a function from a JavaScript File:

`<area shape="poly" style="outline:none; border:none; cursor: pointer;" coords="357, 2260, 883, 1623, 1134, 1452, 1362, 1344, 1625, 1528, 1915, 2260" alt="South America"  onclick="sa1()">`
