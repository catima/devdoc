# User management


## User roles

CATIMA has the following user roles:

- **Guest**: a guest is a non-authenticated user. Visibility is limited to public catalogs.
- **User**: needs to sign on. Visibility is limited to public catalogs like a guest. But a user can create favourites for any publicly visible item.
- **Member**: can view restricted catalogs and fields if the right is given by the catalog admin. Member is a catalog-specific role (a user can be member for a given catalog but not another one).
- **Editor**: can add and edit items in a catalog. Editing is limited to the items created by the editor. This is also a catalog-specific role.
- **Super Editor**: like an editor, but can edit and delete all items of the catalog.
- **Reviewer**: like a super editor, but has additionnally the possibility to validate items.
- **Catalog admin** (or simply **Admin**) can completely manage a catalog, and give access rights to other users for the catalog. A catalog admin cannot create another catalog.
- **System admin** (or simply **Sys Admin**) is the super user of CATIMA and has all rights. A system admin can notably create catalogs and define catalog admins for any catalog.


## User groups

<p style="color: #f00;"><b>Notice:</b> User groups are currently in development.</p>

Access rights can be given to a specific user or a group of users. As only catalog and sys admins can give access rights to users, they are also the only ones to be able to give access rights to groups.

A user group can be created by any user. A group has at least one **group admin** (by default the creator of the group, but this can be changed later). It is possible to have several admins for a group.

A **group admin** can add existing CATIMA users to a group, or invite users not yet existing by providing an email address. A group admin can also give the group admin rights to another member of the group.

A group can have two **visibility statuses**: **public** or **restricted**. A restricted group is only visible to the group members. A public group is visible to any CATIMA user. For public groups, a CATIMA user can request to become a member. The group admin validates the request.

