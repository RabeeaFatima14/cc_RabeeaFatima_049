# LAB NO 6 - Cloud Computing

This document outlines the steps performed for Lab No. 6, covering fundamental Linux commands related to user/group management, file permissions, shell scripting, and basic command-line utilities.

## Submission Details

* [cite_start]**Subject:** Cloud Computing [cite: 187]
* [cite_start]**Submitted By:** Rabeea Fatima [cite: 186]
* [cite_start]**Registration No:** 2023-BSE-049 [cite: 186]
* [cite_start]**Section:** B [cite: 187]

## Lab Tasks

### [cite_start]TASK 01: Switch to root with `su` [cite: 188, 189]

1.  [cite_start]Set a root password[cite: 190].
2.  [cite_start]Switch and verify[cite: 191].
3.  [cite_start]Switch back to normal[cite: 192].

### [cite_start]TASK 02: Create user `tom` [cite: 193]

1.  [cite_start]Create user `tom`[cite: 195].
2.  [cite_start]Verify `tom` in system files[cite: 196].

### [cite_start]TASK 03: Create groups [cite: 197, 198]

1.  [cite_start]Create groups and verify[cite: 199].
2.  [cite_start]Change `tom`'s primary group and verify[cite: 200].
3.  [cite_start]Add secondary group to `tom` and verify[cite: 201].
4.  [cite_start]Replace all secondary groups[cite: 202].

### [cite_start]TASK 04: Create/delete users and groups [cite: 203, 204]

1.  [cite_start]Create users[cite: 205].
2.  [cite_start]Try to login to `Scooby` immediately[cite: 206].
3.  [cite_start]Set a password[cite: 207].
4.  [cite_start]Logging in again[cite: 208].
5.  [cite_start]Logging in again (another attempt)[cite: 209].
6.  [cite_start]Manually creating home directory[cite: 210].
7.  [cite_start]Login on `Scooby` again[cite: 211].
8.  [cite_start]Verify users in system files[cite: 212].
9.  [cite_start]Change the shell[cite: 213].
10. [cite_start]Create groups[cite: 214].
11. [cite_start]Delete groups and users[cite: 215].

### [cite_start]TASK 05: Create user `Student` [cite: 216, 217]

1.  [cite_start]Create user[cite: 218].
2.  [cite_start]Switch and create files[cite: 219].
3.  [cite_start]Change owner and then group[cite: 220].
4.  [cite_start]Identify file/directories[cite: 221].
5.  [cite_start]Exit[cite: 222].

### [cite_start]TASK 06: Change permission using symbolic mode [cite: 223, 224]

1.  [cite_start]Ensure `Student` and file present[cite: 225].
2.  [cite_start]Remove all permissions[cite: 226].
3.  [cite_start]Add read to all[cite: 227].
4.  [cite_start]Add execute to user[cite: 228].
5.  [cite_start]Add write to user and group[cite: 229].
6.  [cite_start]Remove all permissions[cite: 230].

### [cite_start]TASK 07: Change permission using symbolic mode with `set` [cite: 231, 232]

1.  [cite_start]Set all to `rwx`[cite: 233].
2.  [cite_start]Remove execute[cite: 234].
3.  [cite_start]Remove all permissions[cite: 235].

### [cite_start]TASK 08: Change permission using numeric mode [cite: 236, 237]

1.  [cite_start]Step 1 (Instruction not fully detailed in text content)[cite: 238].
2.  [cite_start]Step 2 (Instruction not fully detailed in text content)[cite: 239].
3.  [cite_start]Step 3 (Instruction not fully detailed in text content)[cite: 240].
4.  [cite_start]Step 4 (Instruction not fully detailed in text content)[cite: 241].
5.  [cite_start]Step 5 (Instruction not fully detailed in text content)[cite: 242].
6.  [cite_start]Step 6 (Instruction not fully detailed in text content)[cite: 243].
7.  [cite_start]Step 7 (Instruction not fully detailed in text content)[cite: 244].

### [cite_start]TASK 09: Practice pipes, pagers, grep etc [cite: 245, 246]

1.  [cite_start]`less`[cite: 247].
2.  [cite_start]`more`[cite: 248].
3.  [cite_start]`grep` failure/error[cite: 249].
4.  [cite_start]Redirect[cite: 250].

### [cite_start]TASK 10: Script `setup.sh` (File Operations) [cite: 251, 252]

1.  [cite_start]Include bash shebang[cite: 253].
2.  [cite_start]Define `var1` and echo it[cite: 254].
3.  [cite_start]Save output[cite: 255].
4.  [cite_start]Create directory and show an output[cite: 256].
5.  [cite_start]Create if `dir1/file2` exists (check/create logic)[cite: 257].
6.  [cite_start]Check permissions and grant them[cite: 258].

### [cite_start]TASK 11: Script `setup.sh` arguments comparison [cite: 259, 260]

1.  [cite_start]Create file with shebang[cite: 261].
2.  [cite_start]Add the `-eq` test[cite: 262].

### [cite_start]TASK 12: Script `setup.sh` print all arguments for loop [cite: 172]

### [cite_start]TASK 13: Script `setup.sh` while loop summation and function [cite: 172]

### [cite_start]TASK 14: Running the GUI setup in codespace [cite: 179]

1.  [cite_start]Fork the repository to the GitHub account[cite: 179].
2.  [cite_start]Open in GitHub Codespace[cite: 179].
3.  [cite_start]Verify the start script[cite: 179].
4.  [cite_start]Run the start script[cite: 179].
5.  [cite_start]Verify the ports[cite: 179].
6.  [cite_start]Open forward port 6080[cite: 179].
7.  [cite_start]Stop the GUI in codespace[cite: 179].

## Exam Evaluation Questions

1.  **Group Management:**
    * [cite_start]Create groups `g1`, `g2`, and `g3`[cite: 179].
    * [cite_start]Change `examuser`’s primary group to `g3` and add `g1` and `g2` as supplementary groups[cite: 180].
    * [cite_start]Show the final `id` and `/etc/group` lines that prove the changes[cite: 180].
2.  [cite_start]**Ownership and Permission Tasks** [cite: 180]
3.  [cite_start]**Pipes, Grep, and Redirection Practice** [cite: 180]
4.  [cite_start]**Script: Variables, Command Substitution, File & Dir Checks** [cite: 180, 181]
    * [cite_start]Define variable `var1` and echo it[cite: 180].
    * [cite_start]If directory `dir1` exists echo a message; else create it[cite: 181].
    * [cite_start]If file `dir1/file2` does not exist, create it[cite: 181].
5.  [cite_start]**Script: Comparisons and String Tests** [cite: 181, 182]
    * [cite_start]Incrementally add numeric and string comparison tests to a script and show both true/false cases[cite: 181].
    * [cite_start]`-eq` test (equal)[cite: 182].
    * [cite_start]`-ne` test (not equal)[cite: 182].
    * [cite_start]`-le` test (less than or equal)[cite: 182].
6.  [cite_start]**Script: For Loop and Argument Handling** [cite: 182]
    * [cite_start]Scenario: Write a script that prints all provided arguments and demonstrate correct handling of quoted multi-word arguments[cite: 182].
7.  [cite_start]**Script: While Loop Summation and Functions** [cite: 183]
    * [cite_start]Write an interactive while-loop that accumulates numbers until `q` is entered and shows running totals[cite: 183].
