### Steps & Screens

A scenario consists of steps which, in turn, consist of [screens](/scenario-edit/screen-settings). Each screen needs to have a [screenshot](/scenario-edit/screenshots) uploaded. We recommend adding 3 to 5 steps with 2 to 4 screens in each on average not to make the flow overloaded.

- Steps and screens are **added** in the upper right corner:

<figure><img src="/assets/add_steps.png"/></figure>

- Steps and screens have **titles and descriptions**. Titles can only contain alphanumeric characters, `()`, spaces, `-` or `_` and have maximum 100 characters.

<figure><img src="/assets/step_title.png" width="60%"/></figure>

- **Navigate** around steps & screens using the left-hand panel:

<figure><img src="/assets/scenario-navigate.png" width="25%"/></figure>

- Screens can have **Screen Notes** for adding any additional info. It will not be displayed in [Preview](/portal/preview#scenario-preview) mode and can come in handy as notes or voiceover script.

<figure><img src="/assets/screen-notes.png" /></figure>

- Steps have automatically defined **short names** used for references. You can change them if needed using only alphanumeric symbols and `_`. Note that short name must not start with a number. If you [import steps from another scenario](/scenario-edit/structure#import-step), you need to modify their short names.

<figure><img src="/assets/step_short_name.png" /></figure>

### Structure Overview

You can see scenario structure overview by navigating to the **Scenario** tab. From here, it is possible to organize steps and screens by drag and drop, and [merge](/scenario-edit/structure#merged-screens) them.

<figure><img src="/assets/navigate-structure.png" /></figure>

### Change Structure

Scenario structure can be changed by moving screens around steps as well as within a step. Click the `scenario structure` icon and rearrange the screens as needed.

<figure><img src="/assets/change_structure.png" width="90%"/></figure>

### Import Step

You can import a step from any other scenario within the same [workspace](/portal/workspace) by pressing the button:

<figure><img src="/assets/import-step.png" /></figure>

### Merged Screens

- If a few screens describe steps of one process, you can merge them. This lets all screens in the merged group share the same title and description specified for the main (first) one.

- To merge screens, navigate to the **Scenario** section, and click the `+` icon next to the screen you want to be the main. Indicate number of screens.

<figure><img src="/assets/merge_screens.png" /></figure>

- Color highlight:
  1 is for the currently open screen,
  2 is for the main within merged group,
  3 is for the merged screens.

<figure><img src="/assets/merge-colours.png" width="20%"/></figure>

- If you want one of the merged screens to have its own description, navigate to **Advanced** settings and check off **Force Description**.

<figure><img src="/assets/forced_description.png" width="60%"/></figure>

### Referenced Screens

To use the same screen more than once, you can set reference to it rather than upload it several times. Click the reference icon and select the screen you want to set reference to:

<figure><img src="/assets/referenced_screen.png" width="80%"/></figure>

### Clone Screen

- In order to clone a screen with all its [controls](/scenario-edit/controls) click the `clone current screen` icon and select the step to clone to.

<figure><img src="/assets/clone-screen.png" width="90%"/></figure>

- Make sure to modify short name of cloned screen in order to use it in screen references.

<figure><img src="/assets/cloned_modified.png" width="35%"/></figure>

- Make sure to modify keys of cloned controls, since controls shall have unique keys.

<figure><img src="/assets/change-key.png" width="30%"/></figure>

- If you are cloning a [merged screen](/scenario-edit/structure#merged-screens), make sure to reset its merge properties. Navigate to the **Scenario** tab and open the step you cloned the screen to. Click the **Sequence** button.

<figure><img src="/assets/cloned-remove-merge.png" width="60%"/></figure>

Set the number to `0`.

<figure><img src="/assets/merge-to-zero.png" width="60%"/></figure>
