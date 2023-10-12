Links : [[021 RHCSA Index]]

# Group Management

- A Group is a set of multiple users
- With every user, a default group is created.
- The name of default group is same as the name of user
- By default, every user is associated with its own group
- root can create additional groups
- Just creating group is not enough, group and user must be associated
- A user can associate with multiple groups
- A user is a user, A group is a group
- Their association is either primary or supplementary. **A group or user is not primary or supplementary**
- A user can have multiple groups associated as supplementary, but their can be only 1 primary group for a user

---

**To create a group**
`# groupadd sales`

To delete a group
`# groupdel sales`

To create primary association
`# usermod -g sales ganesh`

To create supplementary association
`# usermod -aG sales ganesh`

To check group association of a group
`# id ganesh`

To check existence of group
`# getent group sales`
`# getent group`
