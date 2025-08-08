### Control: FIELD

- Field control is used as an input field to let users enter data in a single line.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

- Field can have a `Placeholder`.

<figure><img src="/assets/field-placeholder.png" width="30%"/></figure>

- Field can have `Autofill Value`.

<figure><img src="/assets/field-autofill.png" width="30%"/></figure>

### Control: HOTSPOT

- Hotspot control is used for a button.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

- Hotspot has customizable cursor.

<figure><img src="/assets/hotspot-cursor.png" width="30%"/></figure>

- Hotspot has customizable on-click actions: `Next Screen`, `Previous Screen`, `Skip to Screen` (that skips the flow till the specified step) and `restructure` action (reorders the flow according to the [short names](/scenario-edit/screen-settings#title-text-notes--short-name) of steps defined in `Advanced` step settings). Note that for the `restructure` action **ALL** scenario steps are be to included in the array:

    <pre><code>
    "action": [
      "restructure: [step2, step1, step3]"
    ]
    </code></pre>

<figure><img src="/assets/hotspot-action.png" width="30%"/></figure>

- Hotspot has customizable mouse enters & leaves actions.

<figure><img src="/assets/mouse_leave_action.png" width="30%"/></figure>

### Control: LABEL

- Label control displays text over pre-defined area that cannot be edited by the user. It can be used to display, say, a name user typed in [field](/scenario-edit/controls#control-field) control earlier.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

- If you need label to display value from a [field](/scenario-edit/controls#control-field) control, select this control as `Reference`.

<figure><img src="/assets/label-ref.png" width="30%"/></figure>

- If you need label to display default pre-defined value, specify this value as `Label Default Value`.

<figure><img src="/assets/label.png" width="30%"/></figure>

### Control: MULTIMEDIA

- Multimedia control can display an image, lottie, video or audio file.

<figure><img src="/assets/asset-types.png" width="30%"/></figure>

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

- Attach [asset](/scenario-edit/assets) file.

<figure><img src="/assets/media-asset-attach.png" width="30%"/></figure>

- If you chose `image` asset type, specify its size where
  - **Auto** is automatically defined size
  - **Fixed** is the actual size
  - **Fixed Scrollable** is the actual size that can be scrolled. It makes this control a scrollable [container](/scenario-edit/controls#common-control-properties) for others
  - **Fit Width** is the size that is shown based on the actual width
  - **Fit Height** is the size that is shown based on the actual height

<figure><img src="/assets/image-type.png" width="30%"/></figure>

### Control: SLIDER

- Slider control allows you to pick a value by dragging a pin along its bar.

<figure><img src="/assets/slider-1.png" width="30%"/></figure>

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

- Enable showing ticks if needed.

<table>
  <tr>
    <td><strong>Configuration</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td><figure><img src="/assets/slider-4.png" width="65%"/></figure></td>
    <td><figure><img src="/assets/slider-5.png" width="65%"/></figure></td>
  </tr>
</table>

- Enable discrete motion of the pin if needed.

<figure><img src="/assets/slider-6.png" width="30%"/></figure>

- Set up range for the bar.

<figure><img src="/assets/slider-7.png" width="30%"/></figure>

- Configure pin and bar colors.

<figure><img src="/assets/slider-8.png" width="30%"/></figure>

### Control: TERMINAL

<table>
  <tr>
    <td><strong>Configuration</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td><figure><img src="/assets/terminal-config-sample.png" width="65%"/></figure></td>
    <td><figure><img src="/assets/terminal-img-sample.png" width="65%"/></figure></td>
  </tr>
</table>

- Terminal control is used to simulate command-line interface.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

- Specify terminal basic properties in `Command Line` section that includes:
  - user
  - host
  - connector
  - prompt
  - font size

<figure><img src="/assets/command_line.png" width="30%"/></figure>

- Copy output data from one terminal to another using the `Copy Output from Terminal` feature.

<figure><img src="/assets/copy_output_from_terminal.png" width="30%"/></figure>

- `Auto Focus` feature allows to focus directly on the command line in the Scenario preview mode, no matter where it is on the screen.

<figure><img src="/assets/auto_focus.png" width="30%"/></figure>

- Add/edit commands, specify default ones and add their outputs by clicking the `EDIT COMMANDS` button and opening the command configuration form.

<figure><img src="/assets/edit_command_button.png" width="30%"/></figure>

- In the opened configuration form click the **Add new command** button and fill in the command and its output. Add actions if needed.

<figure><img src="/assets/add-command-output.png" width="40%"/></figure>

- Output can be chosen in the drop-down menu as a text file which was uploaded to [Assets](/scenario-edit/assets) or typed in the command editor.

<figure><img src="/assets/text_output.png" width="40%"/></figure>

Command editor:

<figure><img src="/assets/terminal_command.png" width="90%"/></figure>

- Select default command if needed.

<figure><img src="/assets/terminal_action.png" width="40%"/></figure>

### Control: TIMELINE

- Timeline control enables actions at specified timing.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

- Click the `Add Timestamp` button, add the timing in msec, select action and then its controls if needed.

<figure><img src="/assets/timeline-1.png" width="30%"/></figure>

- Timeline can be looped.

<figure><img src="/assets/timeline-6.png" width="30%"/></figure>

- A few actions can be added to one timestamp.

- A few timestamps can be added to timeline.

- Make sure the controls to be shown using timeline are not [visible](/scenario-edit/controls#common-control-properties) by default.

### Control: TYPEWRITER

- Typewriter control simulates typing in a field.

- It can type in value referenced from a [field](/scenario-edit/controls#control-field) control.

<figure><img src="/assets/typewriter-ref.png" width="30%"/></figure>

- It can type in value specified in its default value.

<figure><img src="/assets/typewriter-def.png" width="30%"/></figure>

- Specify typing interval in seconds.

<figure><img src="/assets/typewriter-interval.png" width="30%"/></figure>

### Shape: ARROW

<table>
  <tr>
    <td><strong>Configuration</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td><figure><img src="/assets/shape_arrow_setting.png" width="100%"/></figure></td>
    <td><figure><img src="/assets/shape_arrow_preview.png" width="50%"/></figure></td>
  </tr>
</table>

- This control is used to display a shape in the form of an arrow.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

The arrow can be customized according to the following **options**:

- `Line` consists of `Start point`, `End point`, `Line style`, `Line width` (in pixels), and `Color`.

<figure><img src="/assets/shape_arrow_line.png" width="30%"/></figure>

`Start point` and `End point` are represented in three forms: `None`, `Circle`, and `Arrow`.

<figure><img src="/assets/shape_start_end_arrow.png" width="30%"/></figure>

- Arrow direction is customizable using the `Rotation` slider

<figure><img src="/assets/shape_arrow_rotation.png" width="30%"/></figure>

or `Default direction`, which is represented in the following forms: `Right`, `Bottom Right`, `Bottom`, `Bottom Left`, `Left`, `Top Left`, `Top`, `Top Right`.

<figure><img src="/assets/shape_arrow_default_direction.png" width="30%"/></figure>

### Shape: CIRCLE

<table>
  <tr>
    <td><strong>Configuration</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td><figure><img src="/assets/shape_circle_setting.png" width="65%"/></figure></td>
    <td><figure><img src="/assets/shape_circle_preview.png" width="75%"/></figure></td>
  </tr>
</table>

- This control is used to display a shape in the form of a circle.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

The circle can be customized according to the following **options**:

- `Cursor` inside the circle which is represented in following forms: `default`, `alias`, `cell`, `copy`, `col-resize`, `crosshair`, `grab`, `grabbing`, `help`, `move`, `pointer`, `progress`, `row-resize`, `text`, `zoom-in`, `zoom-out` or cursor display can be disabled as `none`.

<figure><img src="/assets/shape_circle_cursor.png" width="30%"/></figure>

- `Border` of the circle can be customized with the `Width` in pixels and `Color`.

<figure><img src="/assets/shape_circle_border.png" width="30%"/></figure>

- Inside the circle `Text` can be displayed.

<figure><img src="/assets/shape_circel_text.png" width="30%"/></figure>

- `Fill Color` and `Opacity`.

<figure><img src="/assets/shape_circle_color_opacity.png" width="30%"/></figure>

- Circle shape has customizable on `Click Action`, `Mouse Enters Action` and `Mouse Leaves Action`.

`Next Screen`, `Previous Screen`, `Skip to Screen` and `Custom action` actions are available for `Click Action`.

<figure><img src="/assets/shape_circle_click_action.png" width="30%"/></figure>

`Show & Hide Controls`, `Next Screen`, and `Previous Screen` actions are presented for `Mouse Enters Action` and `Mouse Leaves Action`.

<figure><img src="/assets/shape_circle_mouse_action.png" width="30%"/></figure>

`Custom` action is available from the JSON editor only. Detailed info on actions can be found [here](/scenario-controls/controls-meta#action).

When the `Show & Hide Controls` action is chosen, then options `Show Control` and `Hide Control` are available. Any control on the current screen can be selected. For the `Show Control` option the control should have `visible=false` parameter, for `Hide Control` - `visible=true`.

<figure><img src="/assets/shape_circle_show_hide_controls.png" width="30%"/></figure>

### Shape: CURVED ARROW

<table>
  <tr>
    <td><strong>Configuration</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td><figure><img src="/assets/shape_curved_arrow_setting.png" width="65%"/></figure></td>
    <td><figure><img src="/assets/shape_curved_arrow_preview.png" width="60%"/></figure></td>
  </tr>
</table>

- This control is used to display a shape in the form of a curved arrow.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

The curved arrow can be customized according to the following **options**:

- `Line` has `Start point`, `End point`, `Line style`, `Line width` (in pixels), and `Color`.

<figure><img src="/assets/shape_curved_arrow_line.png" width="30%"/></figure>

- `Direction` is presented with the next options: `Top Right`, `Right Top`, `Right Bottom`, `Bottom Left`, `Bottom Right`, `Left Top`, `Left Bottom` and `Top Left`.

<figure><img src="/assets/shape_curved_arrow_direction.png" width="30%"/></figure>

- `Curve` is customizable by `Curve shift`, `Elbow` and `Corner radius`.

<figure><img src="/assets/shape_curved_arrow_curve.png" width="30%"/></figure>

### Shape: RECTANGLE

<table>
  <tr>
    <td><strong>Configuration</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td><figure><img src="/assets/shape_rectangle_setting.png" width="65%"/></figure></td>
    <td><figure><img src="/assets/shape_rectangle_preview.png" width="70%"/></figure></td>
  </tr>
</table>

- This control is used to display a shape in the form of a rectangle.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

The rectangle can be customized according to the following **options**:

- `Cursor` inside the rectangle is represented in following forms: `default`, `alias`, `cell`, `copy`, `col-resize`, `crosshair`, `grab`, `grabbing`, `help`, `move`, `pointer`, `progress`, `row-resize`, `text`, `zoom-in`, `zoom-out` or cursor display can be disabled by setting it to `none`.

<figure><img src="/assets/shape_rectangle_cursor.png" width="30%"/></figure>

`Border` of the rectangle can be customized with the visibility of its sides, `Width` and `Color`.

<figure><img src="/assets/shape_rectangle_border.png" width="30%"/></figure>

Rectangle's sides can be displayed in the following ways: `All`, `None`, `Left`, `Right`, `Top`, `Bottom`, `Left Right`, `Left Top`, `Left Bottom`, `Right Top`, `Right Bottom`, `Top Bottom`, `Left Right Top`, `Left Right Bottom`, `Left Top Bottom` and `Right Top Bottom`.

<figure><img src="/assets/shape_rectangle_border_sides.png" width="30%"/></figure>

Inside the rectangle `Text` can be displayed.

<figure><img src="/assets/shape_rectangle_text.png" width="30%"/></figure>

- `Fill Color` and `Opacity`.

<figure><img src="/assets/shape_rectangle_color_opacity.png" width="30%"/></figure>

- Rectangle shape is customizable on `Click Action`, `Mouse Enters Action` and `Mouse Leaves Action`.

`Next Screen`, `Previous Screen`, `Skip to Screen`, and `Custom Action` actions are available for `Click Action`.

<figure><img src="/assets/shape_rectangle_click_action.png" width="30%"/></figure>

`Show & Hide Controls`, `Next Screen`, `Previous Screen`, and `Custom action` actions are presented for `Mouse Enters Action` and `Mouse Leaves Action`.

<figure><img src="/assets/rectangle_mouse_action.png" width="30%"/></figure>

`Custom action` is available only from the JSON editor. Detailed info on actions can be found [here](/scenario-controls/controls-meta#action).

When the `Show & Hide Controls` action is chosen, then options `Show Control` and `Hide Control` are available. Any control on the current screen can be selected with these options. For the `Show Control` option the control should have `visible=false` parameter, for `Hide Control` - `visible=true`.

<figure><img src="/assets/rectangle_shpae_show_control.png" width="30%"/></figure>

### Shape: ROUNDED RECTANGLE

<table>
  <tr>
    <td><strong>Configuration</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td><figure><img src="/assets/shape_rounded_rectangle_setting.png" width="65%"/></figure></td>
    <td><figure><img src="/assets/shape_rounded_rectangle_preview.png" width="75%"/></figure></td>
  </tr>
</table>

- This control is used to display a shape in the form of a rectangle with rounded corners.

- Detailed info on common control properties can be found [here](/scenario-edit/controls#common-control-properties).

The rounded rectangle can be customized according to the following **options**:

- `Cursor` inside the rounded rectangle is represented in following forms: `default`, `alias`, `cell`, `copy`, `col-resize`, `crosshair`, `grab`, `grabbing`, `help`, `move`, `pointer`, `progress`, `row-resize`, `text`, `zoom-in`, `zoom-out` or the cursor display can be disabled by setting it to `none`.

 <figure><img src="/assets/shape_rounded_rectangle_cursor.png" width="30%"/></figure>

- `Corner` smoothness of the rounded rectangle can be adjusted either for all four corners at once or individually for each corner.

 <figure><img src="/assets/shape_rounded_rectangle_corner.png" width="30%"/></figure>

- Inside the rounded rectangle `Text` can be displayed.

<figure><img src="/assets/shape_rounded_rectangle_text.png" width="30%"/></figure>

- `Fill Color` and `Opacity`.

<figure><img src="/assets/shape_rounded_rectangle_fill_opacity.png" width="30%"/></figure>

- Rounded rectangle shape has customizable on `Click Action`, `Mouse Enters Action` and `Mouse Leaves Action`.

`Next Screen`, `Previous Screen`, `Skip to Screen`, and `Custom Action` actions are available for `Click Action`.

<figure><img src="/assets/shape_rounded_rectangle_click_action.png" width="30%"/></figure>

`Show & Hide Controls`, `Next Screen`, `Previous Screen`, and `Custom action` actions are presented for `Mouse Enters Action` and `Mouse Leaves Action`.

<figure><img src="/assets/shape_rounded_rectangle_mouse_action.png" width="30%"/></figure>

`Custom action` is available only from the JSON editor. Detailed info on actions can be found [here](/scenario-controls/controls-meta#action).

When the `Show & Hide Controls` action is chosen, then options `Show Control` and `Hide Control` are available. Any control on the current screen can be selected with these options. For the `Show Control` option the control should have `visible=false` parameter, for `Hide Control` - `visible=true`.

<figure><img src="/assets/shape_rounded_rectangle_show_controls.png" width="30%"/></figure>

### Snippet: ARROW

Arrow can be used to display a dynamic arrow on the screen.

<figure><img src="/assets/arrow_gif.gif"/></figure>

- Navigate to the screen you want to add the snippet to and select **Arrow** in the **Snippets Library**.

<figure><img src="/assets/add-arrow-snippet.png"/></figure>

- Move the snippet as needed and modify its dimensions.

<figure><img src="/assets/snippet_arrow.png"/></figure>

- Configure [common control properties](/scenario-edit/controls#common-control-properties) as needed: key, container, visibility, comment, background mask and color.

<figure><img src="/assets/arrow-config.png" width="25%"/></figure>

- Select orientation of the arrow.

<figure><img src="/assets/arrow_orientation.png" width="25%"/></figure>

### Snippet: HIGHLIGHT BOX

Highlight Box can be used to create pulse effect when we want to highlight something on the screen.

- Navigate to the screen you want to add the snippet to and select **Highlight Box** in the **Snippets Library**.

<figure><img src="/assets/add-snippets.png"/></figure>

- Move the snippet as needed and modify its dimensions.

<figure><img src="/assets/move-highlight.png"/></figure>

- Configure [common control properties](/scenario-edit/controls#common-control-properties) as needed: key, container, visibility, comment, background mask and color.

<figure><img src="/assets/common-control-prop.png" width="25%" /></figure>

- Select cursor type.

<figure><img src="/assets/highlight-cursor.png" width="25%"/></figure>

- Configure highlight duration and time of one pulse.

<figure><img src="/assets/snippet_highlight.png" width="25%"/></figure>

### Snippet: NOTIFICATION BOX

Notification Box can be used to show various types of notifications: warnings, errors and successful completions of an action.

- Navigate to the screen you want to add the snippet to and select **Notification Box** in the **Snippets Library**.

<figure><img src="/assets/add-not-box.png"/></figure>

- Move the snippet as needed and modify its dimensions.

<figure><img src="/assets/move-not-box.png"/></figure>

- Configure [common control properties](/scenario-edit/controls#common-control-properties) as needed: key, container, visibility, comment, background mask and color.

<figure><img src="/assets/not-box-common.png" width="25%" /></figure>

- Select cursor.

<figure><img src="/assets/not-box-cursor.png" width="25%" /></figure>

- Select notification type which will change box appearance correspondingly.

<figure><img src="/assets/not-types.png" width="25%" /></figure>

- Type in header and notification text.

<figure><img src="/assets/not-texts.png" width="25%" /></figure>

- Specify font size.

<figure><img src="/assets/not-font.png" width="25%" /></figure>

- Select on-click action.

<figure><img src="/assets/not-action.png" width="25%"/></figure>

### Snippet: POINTER

Pointer displays a dynamic pointer on the screen.

<figure><img src="/assets/pointer_gif.gif"/></figure>

- Navigate to the screen you want to add the snippet to and select **Pointer** in the **Snippets Library**.

<figure><img src="/assets/pointer_properties.png"/></figure>

- Move the snippet as needed and modify its dimensions.

<figure><img src="/assets/move-pointer.png"/></figure>

- Configure [common control properties](/scenario-edit/controls#common-control-properties) as needed: key, container, visibility, comment, background mask and color.

<figure><img src="/assets/common-prop-pointer.png" width="25%" /></figure>

- Select orientation of the arrow.

<figure><img src="/assets/pointer-orient.png" width="25%" /></figure>

### Align Controls

Controls can be aligned and distributed as needed. To do that:

- Select the controls by either holding down the `Shift` key on the keyboard and clicking on controls you want to select, or clicking the left mouse button and selecting the controls you want.

- Select the required alignment / distribution in the opened panel:

<figure><img src="/assets/alignment_dist.png" /></figure>

### Apply Styles

Detailed information on how to add and configure styles across the whole scenario can be found [here](/scenario-edit/scenario-settings#typography-styles).

In order to apply a style to a control:

- Open the screen and click on the control to apply style to. This will open right-hand panel.

<figure><img src="/assets/apply-style-controles.png"/></figure>

- If the styles are already configured [here](/scenario-edit/scenario-settings#typography-styles), enable or edit the necessary style.

<figure><img src="/assets/enable-configured-style.png" style="35%" /></figure>

- If a required style hasn't been added yet, [add or import](/scenario-edit/scenario-settings#typography-styles) one.

<figure><img src="/assets/add-style-control.png" style="35%" /></figure>

### Duplicate Controls

Controls can be duplicated by selecting the control and clicking the `Duplicate control` icon:

<figure><img src="/assets/duplicate_control.png" style="35%" /></figure>

Next, select number of duplicates and horizontal & vertical shifts:

<figure><img src="/assets/duplicate_config.png" style="35%" /></figure>

Note that control key will be modified automatically.

### Remove Controls

To remove a control click on it and then the **Remove control** button.

<figure><img src="/assets/control_remove.png"/></figure>

### Navigate around Controls

To switch among controls, open control menu and select the one you need.

<figure><img src="/assets/menu-of-controls.png"/></figure>

### Reorder Controls

Controls appear in the order they were added. To change the order:

- Click the `Reorder controls` button.

<figure><img src="/assets/control_order.png"/></figure>

- Change the order of controls and save the changes.

<figure><img src="/assets/order_change.png"/></figure>

### Common Control Properties

<table>
  <tr>
    <td><strong>Property</strong></td>
    <td><strong>Description</strong></td>
    <td><strong>Sample</strong></td>
  </tr>
  <tr>
    <td>Styles</td>
    <td>It defines control style. 
    <p>Info on creating styles can be found <a href="https://docs.upmix.it/scenario-edit/scenario-settings#typography-styles">here</a>.</p> <p>Info on applying styles to controls can be found <a href="https://docs.upmix.it/scenario-edit/controls#apply-styles">here</a>.</p>
    </td> 
    <td rowspan="10" style="vertical-align: middle "><figure><img src="/assets/common-contr-prop-sample.png"  /></figure></td>
  </tr>
  <tr>
    <td>Key</td>
    <td>It is a unique automatically generated identifier. It is recommended to modify it to a specific unique key.</td>
  </tr>
  <tr>
    <td>Container</td>
    <td>- It сreates scrollable parts inside screens and scrolls controls accordingly. 
    <p>- Only <code>MULTIMEDIA</code> control of <code>Image</code> <code>Fixed Scrollable</code> type can be a container.
    </p>
    <p>- <code>MULTIMEDIA Fixed Scrollable Image</code> control is automatically assigned the status of a container.
    </p>
    <p>- Controls to be scrollable within the container are to be located within the image area.
    </p>
    <p>- Container ID is the key of the scrollable <code>MULTIMEDIA Fixed Scrollable Image</code> control.
    </p>
    </td>
  </tr>
  <tr>
    <td>Visibility</td>
    <td>It defines if a control is visible/invisible in <a href="https://docs.upmix.it/portal/preview#scenario-preview">Preview</a>.</td>
  </tr>
  <tr>
    <td>Comment</td>
    <td>It is an optional field for comments visible only in screen <a href="https://docs.upmix.it/scenario-edit/screen-settings#edit-screen-json">json</a> and not in <a href="https://docs.upmix.it/portal/preview#scenario-preview">Preview</a>.</td>
  </tr>
  <tr>
    <td>Background mask</td>
    <td>It modifies control background by using a pickup tool or color palette.
    <p>
    <code>APPLY MASKS</code> is to apply the configuration;
    </p>
    <p>
    <code>PREVIEW</code> is to see the result;
    </p>
    <p>
    <code>RESTORE ORIGINAL</code> is to remove the applied mask.
    </p>
    </td>
  </tr>
  <tr>
    <td>Hint box</td>
    <td>It defines if a hint has a box around it.</td>
  </tr>
  <tr>
    <td>Hint text</td>
    <td>It defines if a hint has text or only box around it.</td>
  </tr>
  <tr>
    <td>Hint</td>
    <td>It is a field for hint text.</td>
  </tr>
  <tr>
    <td>Hint position</td>
    <td>It defines the location of hint relative to the element it highlights.</td>
  </tr>
</table>

### Advanced Control Properties

All controls can have their advanced properties enabled. Advanced properties let us configure the control manually using its json code.

<figure><img src="/assets/control-adv-prop.png"/></figure>
