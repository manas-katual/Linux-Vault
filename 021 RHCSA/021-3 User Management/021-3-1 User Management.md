Links : [[021 RHCSA Index]]

### Server access types :-

  **OS access -** performed by admins and developers for administration and development
  **Application access -** performed by end users for accessing application

### AAA process :- (This Process is required to access any application or OS)

  **A &rarr; Authentication  (aap kaun hai)**
  **A &rarr; Authorization (aap kya yeh kar sakte hai)**
  **A &rarr; Accounting (aapne kya kya kiya)**


- Credential or token used for AAA is called a user
- To secure the access of a user, we must define a password
- When we create a user in Linux, it gets created in locked state
- To unlock a user, it is mandatory to either set a password or disable password


### User types :- (I have to put it in a box)

- **local user** :- end user with limited privileges
- **Super user** :- admin user with full privileges (root). ==In android we root our devices to get root access==
- **System user** :- inbuilt user used by the *OS* and application internally (we cannot login with this user)