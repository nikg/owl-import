### **style.css**

Each scenario has its own **style.css** file, which includes all styles used in the scenario. Any style can be added to your scenario through the description in the style.css file.

#### Style groups

- System styles:

    <pre><code>
    /* system styles */
    #canvas {{ '{' }}
        font-family: sans-serif;
        line-height: 1.2;
    {{ '}' }}
    #canvas .control {{ '{' }}
        padding: 0;
        margin: 0;
        font-size: 42px;
    {{ '}' }}
    </code></pre>

- Scenario custom styles:

    <pre><code>
    /* scenario custom styles */
    #canvas .start {{ '{' }}
        font-size: 30px;
        color: #000000;
    {{ '}' }}
    #canvas .start-btn {{ '{' }}
        font-size: 63px;
        color: #FFFFFF;
        font-weight: 200;
    {{ '}' }}
    </code></pre>

#### A few notes on styles

- Each style is to be specified starting with `#canvas` which means it belongs to the style of the current scenario (and not all app). As for the styles for [Marketo Form](/scenario-controls/marketo-form) control, they should always start with `#integrationFormModal`:

    <pre><code>
    #integrationFormModal {{ '{' }}
        font-family: proxima-nova;
        font-size: 14px;
    {{ '}' }}
    #integrationFormModal .modal-header {{ '{' }}
        background-image: url("tbd");
        height: 100px;
        color: white;
    {{ '}' }}
    </code></pre>

- If control style falls into "system styles" group, but you want to apply another style to it, you can indicate `!important` in its properties. See an example below:

    <pre><code>
    #canvas .fs {{ '{' }}
        font-size: 72px !important;
    {{ '}' }}
    </code></pre>

- Font sizes are to be indicated considering screen DPR, which means initial value (for DPR 1) is to be multiplied by 2 or 3 depending on DPR needed. Consider the following examples, where the first example is for DPR, and the second one is for 1:

    <pre><code>
    #canvas .fs {{ '{' }}
        font-size: 28px;
    {{ '}' }}
    </code></pre>

    <pre><code>
    #canvas .fs {{ '{' }}
        font-size: 14px;
    {{ '}' }}
    </code></pre>

- Styles are case-sensitive (e.g. H1 vs h1).
