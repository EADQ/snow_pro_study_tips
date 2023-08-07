## ROLES IN SNOWFLAKE

### AccountAdmin
- Has full access to all features and objects in Snowflake.
- Can manage account-level resources (e.g., users, roles, integrations).
- Can view and manage billing and account settings.

### SecurityAdmin
- Can manage all security-related operations.
- Manages roles and users, but cannot grant access to database objects.
- Cannot view billing information.

### UserAdmin
- Can create, alter, and delete users.
- Cannot assign roles to users nor grant privileges to roles, except for the PUBLIC role.

### SysAdmin
- Has all privileges on all database objects, except for full control over roles and users.
- Can manage compute resources (warehouses) and storage objects (databases, schemas, tables).

### PUBLIC
- Is a predefined role that always exists and cannot be deleted.
- All users belong to the PUBLIC role by default.
- It's used to grant privileges that should be applied to all users.

