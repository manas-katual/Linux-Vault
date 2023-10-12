Links : [[021 RHCSA Index]]

# Advance User Management 2

- By default, useradd command refers default values for creating a user from /etc/login.defs and /etc/default/useradd file
- Admin can create a customized user by mentioning the values in the command
- Such command is called an extended useradd command

---

## Commands :-

Create a user 'harry' with UID as 6003
`# useradd -u 6003 harry`

Create a user 'susan' with home directory in /usr/local
`# useradd -b /usr/local susan`

Create a user 'Donald' with a no login shell
`# useradd -s /sbin/nologin donald`

Let's understand this command
`# useradd -u 9993 -b /usr/local/bin -G hr natasha`

---

### Command Lifeline :-

To see short description of command
`# useradd --help`
`ls --help`

To see full detail of a command
`# man useradd`
`# man tar`
