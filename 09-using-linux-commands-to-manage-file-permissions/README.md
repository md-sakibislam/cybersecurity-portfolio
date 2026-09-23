\# Using Linux Commands to Manage File Permissions



\## Project Description

Auditing and correcting file/directory permissions in a `/home/researcher2/projects`

directory using `ls -la` and `chmod`, to bring access controls in line with an

organization's security requirements.



\## Initial State

$ ls -la

drwxr-xr-x 3 researcher2 research\_team 4096 .

drwxr-xr-x 3 researcher2 research\_team 4096 ..

-rw--w---- 1 researcher2 research\_team 46 .project\_x.txt

drwx--x--- 2 researcher2 research\_team 4096 drafts

-rw-rw-rw- 1 researcher2 research\_team 46 project\_k.txt

-rw-r----- 1 researcher2 research\_team 46 project\_m.txt

-rw-rw-r-- 1 researcher2 research\_team 46 project\_r.txt

-rw-rw-r-- 1 researcher2 research\_team 46 project\_t.txt



Used `ls -la` (`-l` for detailed permissions, `-a` to include hidden files) to inventory

existing access. A 10-character permission string breaks down as: file type, then

three groups of three (user/group/other), each showing `r`/`w`/`x` or `-`.



\## Task 1: Remove world-write access from project files

\*\*Requirement:\*\* other users should not have write access to any project file.



Identified `project\_k.txt` as `-rw-rw-rw-` (world-writable) and corrected it:



chmod o-w project\_k.txt



Result: `-rw-rw-r--` — write access removed from "other," read access retained.



\## Task 2: Fix permissions on a hidden file

\*\*Requirement:\*\* nobody should have write access to `.project\_x.txt`, but user and

group should both have read access.





chmod u-w,g-w,g+r .project\_x.txt



\- `u-w` — removed write from the user

\- `g-w` — removed write from the group

\- `g+r` — added read for the group



Result: `-r--r-----` — read-only for user and group, no access for others.



\## Task 3: Restrict directory execute access

\*\*Requirement:\*\* only `researcher2` should have execute access to the `drafts`

directory.



chmod g-x drafts



Result: `drwx------` — group execute access removed; `researcher2` retained

execute access as the owner.



\## What This Demonstrates

Reading and interpreting Linux permission strings, auditing a directory for

overly permissive access (including hidden files), and using `chmod`'s symbolic

mode (`u`/`g`/`o` with `+`/`-`) to apply the principle of least privilege at the

filesystem level.



\## Files

\- `docs/File\_permissions\_in\_Linux.pdf` — full walkthrough with commands and terminal output

\- `docs/Current\_file\_permissions.pdf` — reference listing of the directory's starting permissions

