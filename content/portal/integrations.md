### Add Integration

Scenario integrations: [Password Wall](/portal/integrations#password-wall).

Project integrations: [Action Link](/portal/integrations#action-link), [Contact Form](/portal/engagement), [GTM](/portal/integrations#gtm), [Marketo Form](/portal/integrations#marketo-form), [Password Wall](/portal/integrations#password-wall), [Salesforce](/portal/integrations#salesforce), [Script](/portal/integrations#script), [Tealium](/portal/integrations#tealium).

1. Open service menu of an object and select **Integrations**.

<figure><img src="/assets/integrations.png" width="30%"/></figure>

2. Then click the **Add Integration** button.

<figure><img src="/assets/add_integration.png" width="50%"/></figure>

3. Select the service you want to integrate and click **ADD**.

<figure><img src="/assets/integration_types.png" width="75%"/></figure>

### Action Link

This is a CTA link that is applicable to [deployed](/portal/deploy) projects only.

1. Select Action Link integration and click **ADD**.

<figure><img src="/assets/cta-link-add.png" width="75%"/></figure>

2. Type in text for the link, paste URL and, if needed, enable adding scenario, module and/or project to the link. You can also type in some custom parameters.

<figure><img src="/assets/ctalink-config.png" width="50%"/></figure>

3. The configured action link will be available after deploying the project.

<figure><img src="/assets/ctalink-preview.png"/></figure>

### Contact Form

This is a call to action form. Info on creating & integrating the form can be found [here](/portal/engagement).

### GTM

Google Tag Manager (GTM) is a tag management system that allows you to update measurement codes and related code fragments collectively known as tags on your website or mobile app. The following parameter is to be specified:

<figure><img src="/assets/gtm_id.png" width="50%"/></figure>

Note that only one GTM can be integrated into a scenario.

### Marketo Form

Marketo forms are a great way to capture data from marketing campaigns.

1. Select Marketo integration and click **ADD**.

<figure><img src="/assets/marketo-integr.png" width="75%"/></figure>

2. Fill in form fields.

<figure><img src="/assets/marketo-config.png" width="50%"/></figure>

### Password Wall

This feature provides password access to **scenarios** and **projects** in [Preview](/portal/preview) as well as [Deployed](/portal/deploy#deploy-an-object) modes.

##### Password Wall (PW) Rules

1. Scenario PW is valid only for its Preview mode and becomes invalid after project deployment.

2. In deployed status ONLY project has password (NOT scenario).

3. In Preview mode both scenario and project can have individual PW.

4. The same PW is used for project preview and deployment modes.

5. Password is kept in cookies for one session only.

6. Password of deployed project can't be changed. In order to change it, the project should be re-deployed after PW update.

##### Add PW

1. Select **Integrations** in object's service menu.

<figure><img src="/assets/pw-1.png" width="20%"/></figure>

2. Click **ADD INTEGRATION** button.

<figure><img src="/assets/pw-2.png" width="70%"/></figure>

3. Select the **Password Wall** integration and click **Add**.

<figure><img src="/assets/pw-3.png" width="70%"/></figure>

4. Fill in the fields.

<figure><img src="/assets/pw-4.png" width="50%" /></figure>

##### Edit PW

In order to change password of deployed project, it is to be re-deployed.

1. Go to the **Integrations** in object's service menu and select the PW you want to edit.

<figure><img src="/assets/pw-1.png" width="20%" /></figure>

2. Open its service menu and select **Edit**.

<figure><img src="/assets/pw-5.png" width="20%"/></figure>

3. Edit the fields you want to change.

##### Configure Project PW Theme

Project PW has its own theme configuration. In order to configure PW theme for the project:

1. Navigate to project **Settings** and select **Theme Settings**.

<figure><img src="/assets/pw-theme-config.png" width="20%" /></figure>

2. Scroll down to the **PASSWORD WALL** section. The theme is configured by default depending on the selected landing page theme. You can configure the theme as needed.

<figure><img src="/assets/pw-theme-default-config.png" width="80%"/></figure>

### Salesforce

This service integration is coming soon.

### Script

This feature lets us add additional third-party scripts to landing page or simulator. Several scripts can be integrated into an object. Scripts have the following properties:

<figure><img src="/assets/script_features.png" width="50%"/></figure>

### Tealium

Tealium helps manage tags without the need to edit page code. **utag link** is to be indicated to integrate the service. Only one Tealium service can be integrated into a scenario.

<figure><img src="/assets/utag.png" width="50%"/></figure>
