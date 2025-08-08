### Scenario Key Points

Scenario is a simplified and fascinating way to navigate user through some experience. Scenario tells a story actively involving users and inviting to interact. A scenario has a pre-defined structure consisting of [steps and screens](/scenario-edit/structure) to follow.

**Some key points about scenarios**

- Scenarios are stored in the **Scenarios** section that has two types of scenarios: **MY SCENARIOS** (added by the current user) and **COLLABORATION AREA** ([shared](/portal/access#assign-access-level-role) with the current user).

<figure><img src="/assets/collab-area-scenarios.png" width="80%"/></figure>

- There is [SCENARIO LIBRARY](/portal/library) where ready for deployment scenarios are stored since only Library scenarios can be deployed. Only workspace [admin](/portal/access#operational-level-roles) has access to it.

<figure><img src="/assets/scenario-lib-directory.png" /></figure>

- Scenarios can be pushed to [Library](/portal/library) for further [deployment](/portal/deploy) within a project by workspace [admin](/portal/access#operational-level-roles).

<figure><img src="/assets/push-to-lib-scenario.png "  width="20%" /></figure>

- Inside [projects](/portal/projects), scenarios are stored in [modules](/portal/modules#4-add-scenario).

- Scenario changes its status to **library** within a module after being pushed to [Library](/portal/library).

<figure><img src="/assets/status-change-to-lib.png "  width="40%" /></figure>

- When a new version of scenario is pushed to library, library icon of scenario inside module changes its color to red and offers to pull the latest updates.

<figure><img src="/assets/pull-updates.png "  width="20%" height="80%"/></figure>

- For simultaneous work on one scenario by a few people, scenarios can be cloned, renamed to have the name of the original scenario and pushed to the library when ready.

<figure><img src="/assets/clone-rename-push.png "  width="20%" /></figure>

- Library keeps track of scenario [versions](/portal/library#version-history): author and time.

<figure><img src="/assets/version-track.png "  width="90%"/></figure>

### Create New Scenario

This option lets us create a new scenario from scratch.

1. Click the **CREATE NEW SCENARIO** button.

<figure><img src="/assets/create_button.png" width="80%" height="30%"/></figure>

2. Give it a name for internal use, title and add a short description, then click **OK**. Note that scenario name can only contain lowercase alphanumeric characters and `-`.

<figure><img src="/assets/from_scratch.png" width="40%" /></figure>

3. System will create a new scenario. Open its service menu and select **Edit**. This will open another browser tab with [Scenario Editor](/scenario-edit/structure) tool.

<figure><img src="/assets/scenario_edit.png" width="20%" /></figure>

4. Create scenario structure, add steps and screens, controls and descriptions as needed. Go to [Scenario Editor](/scenario-edit/structure) section for more detailed info.

### Import Scenario

This option lets us create a scenario by importing an existing archive from local storage.

1. Click the **IMPORT SCENARIO** button.

<figure><img src="/assets/import-option.png" width="70%"/></figure>

2. Give it a name and click **SELECT SCENARIO FILE** to start uploading scenario archive. Note that scenario name can only contain lowercase alphanumeric characters and `-`. The process can take some time to be completed. The scenario will appear in the **My Scenarios** section.

<figure><img src="/assets/upload_archive.png" width="40%" /></figure>

### Create From Library

This options lets us create a scenario from a scenario in [Library](/portal/library).

1. Click the **CREATE NEW SCENARIO** button and select **Create From Library**.

<figure><img src="/assets/create-from-lib.png" width="70%"/></figure>

2. In the opened side panel select the scenario and then give it a name. Click **OK** to proceed. The scenario will appear in the **My Scenarios** section.

<figure><img src="/assets/created-from-lib.png" width="40%" /></figure>

### Customize Scenario

In order to customize scenario within a project navigate to project module scenario is in, and select **Customize**.

<figure><img src="/assets/customize_theme.png"/></figure>

The following scenario settings can be customized within a project: title, description, icon and [theme](/portal/projects#theme-for-scenario-custom).

<figure><img src="/assets/scenario_customization.png"/></figure>

### Embed Scenario

A scenario [deployed](/portal/deploy) within a project can be embedded. If there are any changes applied, you need to redeploy project/module. In order to get a link or code to embed a scenario navigate to the **Projects** => **Settings**.

<figure><img src="/assets/embed-navigate.png" width="50%" /></figure>

Enter **Settings** of the module your scenario is in.

<figure><img src="/assets/module_embed.png" width="25%" /></figure>

In scenario service menu select the **Embed Scenario** option.

<figure><img src="/assets/embed_scenario.png" width="25%" /></figure>

You can embed a scenario deployed within a project in two ways:

**a. Embed Via Link**

Embed via link for platforms, like Wix, that support showing site in a site.

<figure><img src="/assets/embed_via_link.png" width="40%" /></figure>

**b. Embed Via Code**

Embed via code for your own sites or platforms that allow code insertion. The player will be inserted into iframe and the iframe will fill the container fully. Scrollbars will be hidden by default.

<figure><img src="/assets/embed_bia_code.png" width="40%" /></figure>

### Download Standalone Scenario

A scenario [added to a project](/portal/projects#project-settings) can be downloaded as a standalone one. In order to download a standalone scenario navigate to the **Projects** => **Settings**.

<figure><img src="/assets/embed-navigate.png" width="50%" /></figure>

Enter **Settings** of the module your scenario is in.

<figure><img src="/assets/module_embed.png" width="25%" /></figure>

In scenario service menu select the **Download Standalone Scenario** option. This will start preparation and then download.

<figure><img src="/assets/download_standalone_scenario.png" width="25%" /></figure>

Run the scenario using the `index.html` file in the downloaded folder.
