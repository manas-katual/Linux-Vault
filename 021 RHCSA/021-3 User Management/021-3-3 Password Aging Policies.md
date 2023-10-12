Links : [[021 RHCSA Index]]

# Password Aging Policies

## Password aging policies are critical for user security

**There are 4 main password aging policy**
- **minimum age "0"** : days gap between two password change
- **maximum age "99999"** : days after which password is expired
- **warning age "7"** : days before password expiry, that user is warned
- **password inactive "-1"** days after password expiry that account is disabled

To change aging policy of a user :
`# chage jane`
To check aging policy of a user :
`# chage -l jane`

There are also password complexity policies like inclusion of upper-case/lower-case character, digit, special characters, minimum passwd length 

<u>**Command to set complexity parameters**</u> :
```bash
authconfig --enablerequpper --enablereqlower --enablereqdigit --enablereqother --passminlen=8 --update
```
---
**Dictionary check** &rarr; It means we cannot use any dictionary words for our password