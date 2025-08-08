### Enable Deployment Approval

This feature makes it necessary for objects (project, module, scenario) to get approval before content [deployment](/portal/deploy). This feature is optional and can be enabled or disabled as needed by workspace [admin](/portal/access#operational-level-roles).

Navigate to **Settings**, then **Workspace** and enable the feature:

<figure><img src="/assets/object_publish_approve.png"/></figure>

### Assign Approver

1. Assign an approver for the workspace navigating to **Settings** and then **Users & Invites**. Promote a user to an approver role (more info on roles and how to invite users can be found [here](/portal/access)). This will open a form.

<figure><img src="/assets/assigning-approver.png"/></figure>

2. Check the required boxes and click **OK**.

<figure><img src="/assets/approver-rights.png" width="40%"/></figure>

3. Navigate to the **Approvers** section to see the assigned approvers for the workspace.

<figure><img src="/assets/approver-list.png"/></figure>

### Request Approval

1. Go to the object to be approved and select **Send Approval Request** in its service menu. This will open the request form.

<figure><img src="/assets/send-app-request-form.png" width="25%"/></figure>

2. Open the **User Email** drop-down menu and select an approver. If you have not promoted any users to approver for workspace, you can type in user's email to the **User Email** field. Send the request.

<figure><img src="/assets/approve-request-form.png" width="50%"/></figure>

3. Approver will see a notification in the upper right corner. After the object has been approved, its status will update in the workspace.

<figure><img src="/assets/approval-popup.png" width="50%"/></figure>

4. As soon as the object gets approval, publish to library and deploy options are enabled. Note that pushing approved scenario to library for further deployment removes approval status from the original scenario.
