### Roles

There are two types of user roles in Portal:

1. [Access-level roles](/portal/access#access-level-roles): reader, contributor, editor, owner. They are assigned for an object only (scenario, module, project) and define types of rights for this object.

2. [Operational-level roles](/portal/access#operational-level-roles): admin, approver. They are assigned across the whole workspace and define rights to perform various operations.

### Access-level roles

**Reader** role lets only preview and clone a shared object without making any changes to it.

**Contributor** role lets modify the shared object without changing its structure: preview, clone, rename, edit content (not structure).

**Editor** role lets modify the shared object's both structure and content. Editor can perform all actions with the shared object.

**Owner** role is assigned when creating an object. Owner has full rights for the object.

<table>
  <tr>
    <td><strong>Action</strong></td>
    <td><strong>Reader</strong></td>
    <td><strong>Contributor</strong></td>
    <td><strong>Editor</strong></td>
    <td><strong>Owner</strong></td>
  </tr>
  <tr>
    <td colspan="5" style="text-align:center;"><strong>SCENARIO</strong></td>
  </tr>
  <tr>
    <td>clone</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>delete</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>edit content</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>edit structure</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>integrate</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>preview</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>rename</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>see analytics</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>share</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td colspan="5" style="text-align:center;"><strong>MODULE/PROJECT</strong></td>
  </tr>
  <tr>
    <td>clone</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>delete</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>deploy</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>edit content</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>edit structure</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>integrate</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>preview</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>see analytics</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>share</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>theme settings</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#29AB87">yes</td>
  </tr>
</table>

**Key points on access-level roles**

- There are four access-level roles: owner, editor, contributor, reader.
- Access level roles are based on access rights to objects (scenarios, modules, projects). They are valid across an object assigned.
- Access level roles allow users only get access to [Library](/portal/library) scenarios and not modify or perform other operations.
- Editor, contributor, reader roles are assigned by inviting to an object.
- Owner role is assigned when creating an object.
- The same user can be re-invited to the same object with a new role. The new role will override the previous one.
- Role assigned to parent element is applied to its child elements.
- In order to invite to child element, user needs to share access to its parent element.
- Project and its modules can be shared with different roles.

#### Assign access-level role

1. In order to invite a user to an object, click the **invite** icon on object card. This will open the **Collaborators** window.

<figure><img src="/assets/invite-icon.png" width="20%" /></figure>

2. Type in email, select a role in the drop-down menu and click **SEND AN INVITE**.

<figure><img src="/assets/send-an-invite.png" width="60%" height="20%"/></figure>

3. The invited user will see a notification of the invite in the upper right corner with the **ACCEPT** and **DECLINE** options.

<figure><img src="/assets/accept-decline.png" /></figure>

4. Аfter the invitation has been accepted, user name will appear in the **Collaborators** list with their role.

### Operational-level roles

**Admin** role lets perform various operations across the whole workspace, such as workspace settings, assigning operational-level roles, updating library, etc.

**Approver** role lets approve the requests for objects if requested.

<table>
  <tr>
    <td><strong>Action</strong></td>
    <td><strong>Admin</strong></td>
    <td><strong>Approver</strong></td>
  </tr>
  <tr>
    <td>approve requested objects</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#29AB87">yes</td>
  </tr>
  <tr>
    <td>create contact form</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#FF0000">no</td>
  </tr>
  <tr>
    <td>enable approval request</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#FF0000">no</td>
  </tr>
  <tr>
    <td>library: push/import/update/see versions/remove scenario</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#FF0000">no</td>
  </tr>
  <tr>
    <td>promote to admin, approver</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#FF0000">no</td>
  </tr>
  <tr>
    <td>see resource library</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#FF0000">no</td>
  </tr>
  <tr>
    <td>see subscription</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#FF0000">no</td>
  </tr>
  <tr>
    <td>see users & invites</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#FF0000">no</td>
  </tr>
  <tr>
    <td>see workspace objects without invite</td>
    <td style="color:#FF0000">no</td>
    <td style="color:#FF0000">no</td>
  </tr>
  <tr>
    <td>select theme for preview</td>
    <td style="color:#29AB87">yes</td>
    <td style="color:#FF0000">no</td>
  </tr>
</table>

**Key points on operational-level roles**

- There are two operational level roles: admin and approver.
- Operational level roles are based on rights to perform various operations in workspace. They are valid across a workspace.
- Only admin role grants operational access to workspace [Settings](/portal/workspace#workspace-settings), [Engagement](/portal/engagement) and Scenario [Library](/portal/library). Admin cannot modify objects within workspace without assigned access-level rights, but can perform such operations, as workspace settings, updating library and assigning other operational-level roles.

#### Assign operational-level role

**Admin**

In order to be an admin, a user needs either to

1. Create their own workspace or

<figure><img src="/assets/create-workspace-admin.png" width="75%" /></figure>

2. To be promoted to admin by workspace admin.

<figure><img src="/assets/promote-to-admin.png" /></figure>

**Approver**

In order to promote to approver either:

1. Admin needs to **PROMOTE TO APPROVER** in the workspace settings or

<figure><img src="/assets/assigning-approver.png" /></figure>

2. If there is no approver assigned in workspace settings, select **Send Approval request** in object's service menu and type in email in approve request form and click **SEND REQUEST**.

<figure><img src="/assets/approve-request-form.png" width="50%"/></figure>

More info on the approval request can be found [here](/portal/deploy-approve#enable-deployment-approval).
