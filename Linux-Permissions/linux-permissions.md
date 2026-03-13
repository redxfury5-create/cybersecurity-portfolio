# Linux File Permissions

## Objective

The objective of this exercise is to understand how Linux file permissions work and how they help protect files from unauthorized access.

---

## Understanding Linux File Permissions

Linux uses three types of users to control access to files:

* **Owner** – the user who created the file
* **Group** – users that belong to the same group
* **Others** – all other users on the system

Each of these can have three types of permissions:

* **Read (r)** – allows viewing the contents of a file
* **Write (w)** – allows modifying the file
* **Execute (x)** – allows running the file as a program

Example permission structure:

```
-rwxr-xr--
```

This means:

Owner → Read, Write, Execute
Group → Read, Execute
Others → Read only

---

## Viewing File Permissions

To view file permissions in Linux, the following command is used:

```
ls -l
```

This command lists files and displays detailed information including:

* File owner
* File group
* File permissions
* File size
* Last modification date

---

## Changing File Permissions

The **chmod** command is used to modify file permissions.

Example:

```
chmod 700 file.txt
```

Meaning:

Owner → full access (read, write, execute)
Group → no access
Others → no access

This improves security by restricting who can access sensitive files.

---

## Changing File Ownership

The **chown** command changes the ownership of a file.

Example:

```
chown user file.txt
```

This command assigns the file to a different user.

---

## Security Importance

Correct file permissions are important for system security because they help:

* Prevent unauthorized users from accessing sensitive files
* Protect system configuration files
* Maintain data integrity
* Reduce the risk of malicious modifications

Improper permissions can allow attackers to read or modify important system files.

---

## Conclusion

Linux file permissions are a fundamental part of system security. Properly configuring permissions ensures that only authorized users can access or modify files, helping maintain the security and stability of a system.
