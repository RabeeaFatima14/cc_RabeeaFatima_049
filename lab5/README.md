# Cloud Computing - Lab No. 5

**Submitted By:** Rabeea Fatima
**Registration No:** 2023-BSE-049
**Section:** B
**Subject:** CLOUD COMPUTING

---

## TASK 01: Discover Missing Commands & Install/Remove Java

This task demonstrates identifying a missing command (`java`) and then installing and removing the default Java Runtime Environment (JRE).

### Installation using `default-jre`
1.  **Run Java command to check status:**
    ```bash
    rabeeafatima@rabeea049:~$ java
    ```
    *(Output indicates 'Command 'java' not found' and suggests installation options like `openjdk-17-jre-headless` or `default-jre`)*

2.  **Install the default JRE package:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt install default-jre -y
    ```
3.  **Check for Java version installed:**
    ```bash
    rabeeafatima@rabeea049:~$ java --version
    # Example Output: openjdk 21.0.8 2025-07-15
    ```

### Removal and Verification
4.  **Remove the Java package:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt remove default-jre -y
    ```
5.  **Clear shell's cache and confirm Java is no longer available:**
    ```bash
    rabeeafatima@rabeea049:~$ hash -r
    rabeeafatima@rabeea049:~$ java
    # Output now shows the command is not found or displays the help message, confirming removal.
    ```

---

## TASK 02: Install & Remove Java Explicitly

This task re-installs and removes Java using the `apt-get` command for practice.

1.  **Update package index and install Java:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt-get update
    rabeeafatima@rabeea049:~$ sudo apt-get install default-jre -y
    ```
2.  **Verify Java version:**
    ```bash
    rabeeafatima@rabeea049:~$ java --version
    ```
3.  **Remove Java:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt-get remove default-jre -y
    ```
4.  **Clear cache and confirm removal:**
    ```bash
    rabeeafatima@rabeea049:~$ hash -r
    rabeeafatima@rabeea049:~$ java
    ```

---

## TASK 03: `apt upgrade` vs. `apt update`

This task illustrates the difference between the two primary `apt` commands.

1.  **Update the package index:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt update
    ```
2.  **Upgrade installed packages:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt upgrade -y
    ```
3.  **Difference between `update` and `upgrade`:**
    * **`apt update`** refreshes the local package index from online repositories. It does not install or upgrade any software - it only updates metadata.
    * **`apt upgrade`** installs the latest version of all currently installed packages.
    * You must always run `apt update` before `apt upgrade` to ensure you're getting the newest updates. Without `apt update`, `apt upgrade` might use old information and skip new versions.

---

## TASK 04: Install VS Code via `snap` on CLI

This task details the installation of Visual Studio Code using the Snap package manager.

1.  **Install VS Code using Snap in classic mode:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo snap install --classic code
    ```
2.  **Verify snap showing package is installed:**
    ```bash
    rabeeafatima@rabeea049:~$ snap list code
    ```
3.  **Check the installed application’s version:**
    ```bash
    rabeeafatima@rabeea049:~$ code --version
    ```
4.  **Show path of the executable:**
    ```bash
    rabeeafatima@rabeea049:~$ ls -l /snap/bin | grep code
    ```

---

## TASK 05: Install XFCE GUI + XRDP

This task covers setting up a remote desktop environment using the lightweight XFCE desktop environment and the XRDP server.

1.  **Connect in Command Prompt (SSH):**
    ```bash
    C:\Users\SST COMPUTER>ssh rabeeafatima@192.168.204.130
    ```
2.  **Update and upgrade the server packages:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt update && sudo apt upgrade -y
    ```
3.  **Install XFCE and its goodies:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt install xfce4 xfce4-goodies -y
    ```
4.  **Install and enable XRDP:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt install xrdp -y
    rabeeafatima@rabeea049:~$ sudo systemctl enable xrdp
    ```
5.  **Verify XRDP status:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo systemctl status xrdp
    ```
6.  **Configure XRDP to use the XFCE session:**
    ```bash
    rabeeafatima@rabeea049:~$ echo xfce4-session > ~/.xsession
    ```
7.  **Connect via Remote Desktop Connection** (To verify installation and configuration).

---

## TASK 06: Install `lightdm-gtk-greeter`

This task involves installing and configuring the LightDM display manager and the `lightdm-gtk-greeter` to manage the graphical login, and demonstrating how to control the GUI boot target.

1.  **Install `lightdm-gtk-greeter` and configure session:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt install lightdm-gtk-greeter -y
    # Other commands were run to fix login issue and restart lightdm
    ```
2.  **Control GUI at boot (Enable/Disable graphical target):**
    ```bash
    # Set default target to graphical (enables GUI on boot)
    rabeeafatima@rabeea049:~$ sudo systemctl set-default graphical.target
    # Set default target to multi-user (disables GUI on boot, boots to CLI)
    rabeeafatima@rabeea049:~$ sudo systemctl set-default multi-user.target
    ```
    *Commands to start/stop the GUI manually:*
    ```bash
    rabeeafatima@rabeea049:~$ sudo systemctl start lightdm
    rabeeafatima@rabeea049:~$ sudo systemctl stop lightdm # stop GUI now
    ```

---

## TASK 07: Install Google Chrome by its APT Code & Key

This task demonstrates adding a third-party APT repository by manually adding the source list and signing key.

1.  **Attempt to install directly (shows package is not found):**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt install google-chrome-stable -y
    # Output: E: Unable to locate package google-chrome-stable
    ```
2.  **Add Chrome repository metadata to a source file:**
    The following lines were added to the APT source configuration (e.g., using `nano`):
    ```
    Types: deb
    URIs: [http://dl.google.com/linux/chrome/deb/](http://dl.google.com/linux/chrome/deb/)
    Suites: stable
    Components: main
    Architectures: amd64
    Signed-By: /etc/apt/keyrings/google.gpg
    ```
3.  **Download and add the Google signing key:**
    ```bash
    rabeeafatima@rabeea049:~$ curl -fSSL [https://dl.google.com/linux/linux_signing_key.pub](https://dl.google.com/linux/linux_signing_key.pub) | sudo gpg --dearmor -o /etc/apt/keyrings/google.gpg
    ```
4.  **Update APT index and install Google Chrome:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt update
    rabeeafatima@rabeea049:~$ sudo apt install google-chrome-stable -y
    ```
5.  **Creating a dedicated one-line source list file:**
    This command can create the source list in one step:
    ```bash
    rabeeafatima@rabeea049:~$ echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/google.gpg] [http://dl.google.com/linux/chrome/deb/](http://dl.google.com/linux/chrome/deb/) stable main" | sudo tee /etc/apt/sources.list.d/google-chrome.list
    ```
    *(Steps 12 & 13 repeat the key re-addition, update, and install with the new dedicated list file)*

---

## TASK 08: Install Applications via PPA

This task demonstrates using Personal Package Archives (PPA) to install applications not found in the standard Ubuntu repositories.

### Audacity Installation
1.  **Add Audacity PPA:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo add-apt-repository ppa:ubuntuhandbook1/audacity -y
    ```
2.  **Update and install Audacity:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt update
    rabeeafatima@rabeea049:~$ sudo apt install audacity -y
    ```
3.  **Launch Audacity to verify:**
    ```bash
    rabeeafatima@rabeea049:~$ audacity --version
    rabeeafatima@rabeea049:~$ audacity
    ```

### OBS Studio Installation
4.  **Add OBS Studio PPA:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo add-apt-repository ppa:obsproject/obs-studio -y
    ```
5.  **Update package index:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt update
    ```
6.  **Install and Launch OBS Studio:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt install obs-studio -y
    rabeeafatima@rabeea049:~$ obs --version
    rabeeafatima@rabeea049:~$ obs
    # Note: Launching OBS failed in the lab, likely due to a missing display server dependency when run over an SSH/remote session.
    ```

---

## TASK 09 & 10: Create and Edit a Kubernetes Sample YAML using VIM

This task covers using the `vim` text editor to create and modify a Kubernetes Pod manifest file.

1.  **Install VIM (if not present) and check version:**
    ```bash
    rabeeafatima@rabeea049:~$ sudo apt install vim -y
    ```
2.  **Create and navigate to the working directory:**
    ```bash
    rabeeafatima@rabeea049:~$ mkdir -p ~/Lab5
    rabeeafatima@rabeea049:~$ cd ~/Lab5
    ```
3.  **Create Kubernetes YAML file using `vim`:**
    ```bash
    rabeeafatima@rabeea049:~/Lab5$ vim k8s-sample.yaml
    ```
    The initial content of the file (`k8s-sample.yaml`) was:
    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: nginx-pod
    spec:
      containers:
        - name: nginx
          image: nginx:1.19
          ports:
            - containerPort: 80
      restartPolicy: Always
    ```
4.  **Edit the Kubernetes YAML (Task 10):**
    The file was modified to add an `annotations` field under `metadata`.
    ```bash
    rabeeafatima@rabeea049:~/Lab5$ cat k8s-sample.yaml
    ```
    The content after editing:
    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: nginx-pod
      annotations:
        lab: lesson11
    spec:
      containers:
        - name: nginx
          image: nginx:1.19
          ports:
            - containerPort: 80
      restartPolicy: Always
    ```
    An additional comment `#temp: donot keep_` was also shown in the `vim` editor during a subsequent step.
