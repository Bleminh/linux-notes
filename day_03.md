21/07/2026

1. File Permissions:
- Permission String:
+ First character: file type. "d" = directory. "-" = regular file.
+ Next nine characters: file permission. Divided into 3 sets of 3.
+ "r" = read. "w" = write. "x" = execute. "-" = no permission granted
+ First set applies to owner (minh). Second set applies to group (staff). Third set applies to all other users on the system.
2. Modifying Permissions (chmod):
Symbolic mode:
- "u" = user/owner. "g" = group. "o" = others. "a" = all
- "+" = add a permission. "-" = remove a permission
+ Ex: chmod u+x myfile. Adds (+) execute (x) permission for user (u) on my file.
+ Ex: chmod g-w myfile.chmod ug+w myfile
Numerical mode:
- "4" = r, "2" = w, "1" = x
- ex: chmod 755 myfile. 7 (User) -> rwx. 5 (Group) = 4 + 1 -> r-x. 5 (Others) -> r-x.
- Only grant the permissions that are strictly necessary.
3. Ownership Permissions:
- Ex: sudo chown patty myfile. Change the owner to patty.
- Ex: sudo chgrp whales myfile
- Ex: sudo chown patty:whales myfile
4. Umask:
- Change default set of permissions. Instead of adding these permissions, umask takes away these permission
- Ex: umask 021. Default permissions of new files to allow users access to everything. Groups, take away write (2). Others, take away execute (1).
- Dafault: 022 -> no write access for group and others.
5. Setuid:
- "s" = SUID (Set User ID). Allows the users who launched the program to get the file owner's permission as well as execution permission.
- Modyfing SUID: sudo chmod u+s myfile.
- sudo chmod 4755 myfile. SUID = 4.
6. Setgid:
- Set group ID. Similar to setuid.
- Ex: sudo chmod g+s myfile
- sudo chmod 2555 myfile. SGID = 2
7. Process Permissions:
3 UIDs associated with every process:
- Effective user ID. When you launch a process and it runs with the same permissions as the user/group that ran it. This UID is used to grant access rights to a process.
- Real user ID.: ID of the user that launced the process. Used to track down who launched the process.
- Saved user ID. Allows switching back and forth between effective user ID and real user ID.