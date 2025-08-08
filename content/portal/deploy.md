### Deployment Rules

1. Only projects and modules can be deployed.

2. Empty objects cannot be deployed: only a project with a module/modules having a scenario/scenarios can be deployed. More info on modules can be found [here](/portal/modules).

3. Deployment of a parent object includes deployment of all its child objects (modules, scenarios).

4. Module can be deployed only after the project it belongs to has been deployed.

5. Project name cannot be changed after the project has been deployed. More info on projects can be found [here](/portal/projects).

6. Only library scenarios can be deployed within a project. More info on library can be found [here](/portal/library).

7. If 'Require approval for content deployment' feature is enabled for workspace, the object is to be approved by an assigned approver before being deployed. More info on approval feature can be found [here](/portal/deploy-approve).

### Deploy an Object

##### Deployment flow without [approval required](/portal/deploy-approve)

1. Push scenario to library by selecting **Push to Library** in scenario's service menu (only library scenarios can be deployed). Note that only workspace [admin](/portal/access#operational-level-roles) can execute this operation.

<figure><img src="/assets/scenario-push-to-lib.png" width="25%"/></figure>

This will change scenario status to 'library' inside its module if it has already been added.

<figure><img src="/assets/lib-icon.png" width="25%"/></figure>

2. If scenario has not been added to a module yet, proceed to your project settings, then to the module settings and click **ADD SCENARIO** which will open list of scenarios. Select the one you just pushed from the "Workspace Library" list. If you have added scenario to module earlier, you can skip this step.

<figure><img src="/assets/how-to-add-lib-scen.png"/></figure>

3. Select **Deploy** in object's context menu. This will change project status and generate deployment link.

<figure><img src="/assets/deploy_project.png" width="25%"/></figure>

##### Deployment flow with [approval required](/portal/deploy-approve)

1. Request approval. Navigate to **Settings**, then **Workspace** and enable the feature. Note that only workspace [admin](/portal/access#operational-level-roles) can execute this operation.

<figure><img src="/assets/object_publish_approve.png"/></figure>

2. Assign an approver for the workspace navigating to **Settings**, then **Users & Invites** and promoting a user to an approver role.

<figure><img src="/assets/assigning-approver.png"/></figure>

3. Go back to the object to be approved and select **Send Approval Request** in its service menu. This will open the request form.

<figure><img src="/assets/send-app-request-form.png" width="25%"/></figure>

4. Open the **User Email** drop-down menu and select an approver. If you skipped step 3 above and have not promoted any user to approver for workspace, you can type in user's email to the **User Email** field. Send the request.

<figure><img src="/assets/approve-request-form.png" width="50%"/></figure>

5. After the object has been approved by an approver, its status will change:

<figure><img src="/assets/approved-status-object.png" width="25%"/></figure>

6. After scenario has been approved, it can be pushed to library and deployed. Select **Push to Library** in scenario's service menu.

<figure><img src="/assets/push-to-lib-enabled.png" width="25%"/></figure>

7. If scenario has not been added to a module yet, proceed to your project settings, then to the module settings and click **ADD SCENARIO** which will open list of scenarios. Select the one you just pushed from the "Workspace Library" list. If you have added scenario to module earlier, you can skip this step.

<figure><img src="/assets/how-to-add-lib-scen.png"/></figure>

8. Select **Deploy** in object's context menu. This will change project status and generate deployment link.

<figure><img src="/assets/deploy-after-approval.png" width="25%"/></figure>

### Deployment Settings

After the object has been deployed, deployment settings can be viewed. Select **Deploy Settings** in project service menu. This will open a record of custom domains, deploy history and a current deployment link.

<figure><img src="/assets/deploy-settings.png" width="25%"/></figure>

### Deployment Status

Deployment lets us move an object from stage environment to production one. Object status can be seen on its card:

<figure><img src="/assets/project_stage.png" width="45%"/></figure>
