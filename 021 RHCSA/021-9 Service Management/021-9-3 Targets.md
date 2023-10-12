Links : [[021 RHCSA Index]]

# Targets

- In Latest Linux kernels running with system, run-levels are enhanced to targets
- Targets are known by names
- The targets available in Linux are :
	- **halt.target** is equivalent to [[021-9-2 Run Levels#^27b2cc|Run-level 0]] 
	- **rescue.target** is equivalent to [[021-9-2 Run Levels#^af6df5|Run-level 1]] (recovery console with read/write access)
	- **emergency.target** is equivalent to [[021-9-2 Run Levels#^af6df5|Run-level 1]] (recovery console with read only access). It is basically given to freshers so that they can't modify anything they can only report the error.
	- **multi-user.target** is equivalent to [[021-9-2 Run Levels#^0ae377|Run-level 3]] 
	- **graphical.target** is equivalent to [[021-9-2 Run Levels#^1f4167|Run-level 5]]
	- **reboot.target** is equivalent to [[021-9-2 Run Levels#^c1c2ef|Run-level 6]]

---

- Out of all the target, any 1 target will be **default target**
- The default target is the target in which the system boots
- The default target should be either multi-user.target or graphical.target

---

>[!Note]
>- **rescue.target** & **emergency.target** both are equivalent to [[021-9-2 Run Levels#^af6df5|Run-level 1]] so it is not a typo
>- [[021-9-2 Run Levels#^bd8387|Run-level 2]] and [[021-9-2 Run Levels#^0ae377|Run-level 4]] are not there in targets. I mean there is no concept of run-level after 3.x Linux version

---

## Commands

- To know current target
`runlevel` &rarr; it may work or maynot because it is outdated

- To switch to a target
`systemctl isolate multi-user.target`

- To know the default target
`systemctl get-default`

- To change default target
`systemctl set-default <target name>`
