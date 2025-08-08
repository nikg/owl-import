### Create New Screen

- Navigate to the **Scenario** tab and click the **Create new step** button. This will create a step to locate screens in.

<figure><img src="/assets/create-step1.png"/></figure>

- Give step a name, add description if needed, and modify its name in the **Advanced** section if needed. Title field can only contain alphanumeric characters, `()`, spaces, `-` or `_` and have maximum 100 characters.

<figure><img src="/assets/step-config.png"/></figure>

- Enter the created step and click the **Create new screen** button.

<figure><img src="/assets/create-screen-1.png"/></figure>

- Fill out the opened form.

### Title, Text, Notes & Short Name

- **Title, Text, Notes**:
  Fill in screen title. Screen title field can only contain alphanumeric characters, `()`, spaces, `-` or `_` and have maximum 100 characters. Then, fill in text and notes if needed. These fields are optional. Screen text will be displayed in the left-hand panel of [Default Preview Theme](/portal/preview#scenario-preview-details), whereas Screen Notes are used for any additional info and are not displayed in [Preview](/portal/preview#scenario-preview) mode.

<figure><img src="/assets/screen-settings1.png"/></figure>

- **Short name**:
  Screens have automatically defined short names used for references. You can change them if needed using only alphanumeric symbols and `_`. Note that short name must not start with a number. If you [clone](/scenario-edit/screen-settings#clone-screen) a screen, you need to modify its short name.

<figure><img src="/assets/screen_short_name.png" width="35%"/></figure>

- **Merged screens**:
  [Merged screens](/scenario-edit/structure#merged-screens) can have no title and/or text.

- **Navigating**:
  Navigate around steps & screens using the left-hand panel:

<figure><img src="/assets/structure-navigate.png" /></figure>

### Screen Media

- Screen Media lets us display a media file in the left-hand panel of a screen:

<figure><img src="/assets/screen-sample-media.png"/></figure>

- Open the screen, proceed to the **Assign Screen Media** section and click the button. Select the file to attach from Assets list. Information on how to add a file to assets can be found [here](/scenario-edit/assets). One media file can be assigned to several screens each having its own timing and actions via [Screen Media Editor](/scenario-edit/screen-settings#screen-media-editor).

<figure><img src="/assets/screen_media.png"/></figure>

### Screen Media Editor

- Click the **edit** button next to the media you want to edit. This will open media editor studio.

<figure><img src="/assets/media_edit.png"/></figure>

- If needed, add this media to another screen by hitting the **Assign** button.

<figure><img src="/assets/remove_media.png"/></figure>

- Remove the media from screen by hitting the **Remove** button.

<figure><img src="/assets/assign_media.png"/></figure>

- Edit media default dimensions.

<figure><img src="/assets/media_dim.png"/></figure>

- Specify media timing for the current screen.

<figure><img src="/assets/media_timing.png"/></figure>

- Add bookmarks to configure timestamps and actions in them.

<figure><img src="/assets/add-bookmark.png"/></figure>

- Configure bookmarks by adding timestamps. Actions should not start/end at the same time. Make sure to specify at least 0.1 s difference.

<figure><img src="/assets/adding-time-action.png"/></figure>

- Add actions to the specified timestamps. For any action to take place, you need to add at least one [control](/scenario-edit/controls) to the screen.

<figure><img src="/assets/add-actions.png"/></figure>

- If scenario [autoplay](/scenario-edit/screen-settings#autoplay-mode) mode is off but you need to enable the specified actions, check the **Forced** box off to enable the actions specified for this timestamp.

<figure><img src="/assets/forced-actions.png"/></figure>

- If you choose `hide` or `show` action, you need to specify the key of the [control](/scenario-edit/controls) to be shown/hidden. If you chose the `show` action, make sure to specify `not visible` for the control.

### Autoplay Mode

- This feature enables screen autoplay mode and executes a specified action at specified timing. Autoplay mode can be enabled for the whole scenario. Click [here](/scenario-edit/scenario-settings#autoplay-mode) for detailed info on scenario autoplay mode.

- Navigate to the required screen and proceed to the **Automode** section to enable it.

<figure><img src="/assets/screen-autoplay-enable.png"/></figure>

- Configure:
  - `Idle time` - idle time after which autoplay mode is enabled
  - `Action time` - time after which specified actions are executed
  - `Actions` - actions to be executed at specified timing. Make sure to specify control keys if you choose `show` or `hide` actions.

<figure><img src="/assets/atoplay-config-screen.png"/></figure>

### Force Description

If a screen is [merged](/scenario-edit/structure#merged-screens) and is not the main in that group, its description will not be displayed by default. In order to display it forcefully, go to screen **Advanced** settings and enable **Force Description**.

<figure><img src="/assets/force-descr.png"/></figure>

### Edit Screen JSON

For more advanced cases there is an opportunity to edit screen properties and settings via its JSON. Click the `JSON editor` button to open the editor. Make sure to save the changes once they are ready.

<figure><img src="/assets/json_edit.png"/></figure>

### Clone Screen

Information on screen cloning can be found [here](/scenario-edit/structure#clone-screen).

### Delete Screen

Open the screen to be deleted and click the **Delete** button in the upper right corner.

<figure><img src="/assets/delete-screen.png"/></figure>

### Add Screenshot

Each screen shall have a screenshot. Detailed information on taking and adding screenshots can be found [here](/scenario-edit/screenshots#screenshots).
