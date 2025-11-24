# LAB NO 7 - Cloud Computing: Environment Variables & Security

This document outlines the practical execution of essential Linux administration tasks, focusing on environment variable management, PATH configuration, firewall control using `ufw`, and secure shell (SSH) key-based authentication.

## Submission Details

| Field | Value |
| :--- | :--- |
| **Subject** | Cloud Computing |
| **Submitted By** | Rabeea Fatima |
| **Registration No** | 2023-BSE-049 |
| **Section** | B |

---

## Lab Tasks Performed

### TASK 01: Environment Variables (`printenv` and `grep`)

**Objective:** View and filter existing shell environment variables.

| Step | Command Example | Purpose |
| :--- | :--- | :--- |
| 1 | `printenv` | Display all current environment variables. |
| 2 | `printenv \| grep SHELL` | Filter output to check specific variables (`SHELL`, `HOME`, `USER`). |

### TASK 02 & 03: DB Variable Management (Ephemeral & Persistent)

**Objective:** Define temporary variables for the session, then configure them for persistence via `~/.bashrc`.

| Configuration | Variables Defined | Persistence Method |
| :--- | :--- | :--- |
| **Ephemeral** (Task 02) | `DB_URL`, `DB_USER`, `DB_PASSWORD` | `export` command in the current shell. |
| **Persistent** (Task 03) | `DB_URL`, `DB_USER`, `DB_PASSWORD` | Added `export` commands to the `~/.bashrc` file. |

### TASK 04: System-Wide Variables and PATH Configuration

**Objective:** Manage system-wide environment files and customize the execution path to run local scripts.

| Action | Commands & Files Used | Description |
| :--- | :--- | :--- |
| **System Config** | `/etc/environment` | Added system-wide variables (e.g., `CLASS`) and viewed system PATH. |
| **Script Creation** | `cat > ~/welcome` + `chmod +x` | Created an executable welcome script in the user's home directory. |
| **PATH Update** | `PATH=$PATH:~` (in `~/.bashrc`) | Added the home directory to the shell's execution path. |
| **Verification** | `source ~/.bashrc` + `welcome` | Applied changes and ran the script using only its name. |

### TASK 05: Firewall Control (`ufw`)

**Objective:** Use the Uncomplicated Firewall to block and re-allow inbound SSH access (Port 22).

| Action | Command | Result |
| :--- | :--- | :--- |
| **Initialization** | `sudo ufw enable` | Activated the firewall (Default: Deny Incoming). |
| **Block SSH** | `sudo ufw deny 22/tcp` | Remote SSH connection attempt failed ("Connection timed out"). |
| **Allow SSH** | `sudo ufw allow 22/tcp` + `sudo ufw reload` | Remote SSH connection attempt succeeded. |

### TASK 06: SSH Key-Based Authentication

**Objective:** Configure secure, password-less login using SSH key pairs.

#### Part A: Key Generation

* **Command:** `ssh-keygen -t ed25519 -f ~/.ssh/id_lab7 -c "lab_key"`
* **Result:** Generated a secure ED25519 public/private key pair.

#### Part B: Key Deployment

* **Directory Setup:** Ensured `~/.ssh` exists with `700` permissions.
* **Key Placement:** Appended the public key to `~/.ssh/authorized_keys`.
* **Permissions:** Set `~/.ssh/authorized_keys` permission to `600`.

```bash
# Deployment Commands
$mkdir -p ~/.ssh$ chmod 700 ~/.ssh
$echo "ssh-ed25519 [PUBLIC_KEY_CONTENT]..." >> ~/.ssh/authorized_keys$ chmod 600 ~/.ssh/authorized_keys
