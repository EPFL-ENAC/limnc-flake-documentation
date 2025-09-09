# Managing roles in GitLab

To manage roles in the instrument repository in GitLab, follow these steps:

1. Navigate to the instrument repository on GitLab.
2. Click on "Manage" in the left sidebar.
3. Select "Members" from the dropdown menu.
4. Then,
    1. If the user is not yet a member of the repository:
        1. In the "Invite member" section, enter the GitLab username or email address of the user you want to assign a role to.
        2. Choose the appropriate role from the "Select a role" dropdown menu. The available roles are:
            - Guest: Can view issues and merge requests.
            - Reporter: Can view and create issues, and view merge requests.
            - Developer: Can create and manage branches, issues, and merge requests.
            - Maintainer: Can manage the repository, including settings and members.
            - Owner: Has full control over the repository (only available for group owners).
        3. Click the "Invite" button to assign the role to the user.
    2. If the user is already a member of the repository:
        1. Find the user in the list of members.
        2. Click on the dropdown menu next to their current role.
        3. Select the new role you want to assign to the user.
