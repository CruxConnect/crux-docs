#### Permission Assignments Object:

permissions
: (list) Permissions are a list of available individual permissions with details as well as if the permission has been assigned to this User. {% include timp/links/available_permissions.md %}

org_user
: (object) Organization User holds the uuid for the User

status
: (string) User's account status which can be "CONFIRMATION WAITING", "ACTIVE", or "DEACTIVATED"

{% include timp/objects/permissions_list.md %}