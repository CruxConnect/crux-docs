#### Permission Assignments Object:

permissions
: (list) Permissions are a list of available individual permissions with details as well as if the permission has been assigned to this User

org_user
: (object) Organization User holds the uuid for the User

status
: (string) Status of user account.  Possible values: 'ACTIVE' or 'INACTIVE'

#### Permission Assignments Object:

permissions
: (list) Permissions are a list of available individual permissions with details as well as if the permission has been assigned to this User

org_user
: (object) Organization User holds the uuid for the User

#### Permissions Object List:

assigned
: (boolean) Assigned indicates whether this particular Permission has been Assigned to this User

permission
: (object) Permission is an object detailing a specific Permission with a uuid, name, display name, and description

#### Permission Object:

uuid
: (string) Universal Unique Identifier for the Permission

name
: (string) Name of the Permission; written in shortened snake case

display_name
: (string) Display Name of the Permission; a more user-friendly name of the Permission

description
: (string) Description of the Permission