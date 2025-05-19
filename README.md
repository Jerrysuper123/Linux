# Linux

"POSIX" and "Perl" refer to very different things in computing:

---

### 1. **POSIX (Portable Operating System Interface)**

* **What it is**: A **standard**, not a language.
* **Purpose**: Defines a set of **APIs, command-line utilities, and shell scripting standards** for maintaining compatibility between Unix-like operating systems.
* **Scope**:

  * System calls (e.g., `fork()`, `exec()`)
  * Shell scripting standards (e.g., `sh`, `grep`, `awk`)
  * File and process management
* **Used in**: Shell scripting (e.g., Bash, Dash), C programming, and OS development.

---

### 2. **Perl (Practical Extraction and Report Language)**

* **What it is**: A **programming language**.
* **Purpose**: Originally developed for text processing, but has evolved into a general-purpose language.
* **Features**:

  * Rich regular expressions
  * Text and file manipulation
  * Dynamic typing
  * Strong CPAN ecosystem (modules)
* **Used in**: Web development, system administration, bioinformatics, automation scripts.

---

### Summary of Differences

| Feature         | POSIX                             | Perl                        |
| --------------- | --------------------------------- | --------------------------- |
| **Type**        | Standard/API                      | Programming language        |
| **Scope**       | OS interface, shell scripting     | General-purpose programming |
| **Focus**       | Compatibility & portability       | Text processing & scripting |
| **Language?**   | No (but governs shells like `sh`) | Yes                         |
| **Typical Use** | Writing portable shell scripts    | Writing programs/scripts    |

---

If you're comparing in the context of **regular expressions**, then:

* **POSIX regex** is a **standard** with basic features.
* **Perl regex** is much **more powerful and expressive**, and many modern tools (like `grep -P`) borrow Perl's style.



`/usr/local/bin` is a directory on Unix-like operating systems (like Linux and macOS) that holds **executable programs** (binaries) installed **locally by the system administrator or user**, rather than by the operating system's package manager.

### Breakdown:

* `/usr` → contains user-related programs and data.
* `/usr/local` → meant for software installed **locally**, not managed by the system’s package manager (like `apt`, `yum`, or `brew`).
* `/usr/local/bin` → holds **executable files** (like scripts or binary programs) that are installed manually or by custom installers.

### Why it matters:

* It's typically included in your `$PATH`, so executables placed there can be run from anywhere in the terminal without needing to specify the full path.
* It's a safe place to put your own scripts or tools so they don’t get overwritten by system updates.

### Example use case:

If you write a script `myscript.sh`, you might do:

```bash
chmod +x myscript.sh
sudo mv myscript.sh /usr/local/bin/myscript
```

Now you can run `myscript` from any terminal session, just like any regular command.



## boot volume
usually contain the os and necessary file systems to boot the instance.
often persistent and a type of block storage.

## block storage
general purpose storage for data, application and databases, just like ssd.

block storage also can be used as boot volume.

## in /etc/ contains the system-wide configuration file
for example in /etc/environment is the global proxy setting
```
http_proxy="http://proxy.example.com:8080"
https_proxy="http://proxy.example.com:8080"
ftp_proxy="http://proxy.example.com:8080"
//define address that should by pass the proxy, meaning if going to localhost, example.com, do not go thru proxy
no_proxy="localhost,127.0.0.1,.example.com"

```

## proxy also can be set in shell startup scrpts like /etc/profile (for logins shells) or /etc/bash.bashrc (for interactive shell)
```
export http_proxy="http://proxy.example.com:8080"
export https_proxy="http://proxy.example.com:8080"

```

## in /etc/hosts, host setting, map ip addresses to hostnames manually, overriding DNS
```
127.0.0.1   localhost
192.168.1.10   myserver.local

```

## /etc/hostname (System Hostname) Contains the system’s hostname (just the name, no domain).
```
my-computer
```

## /etc/resolv.conf (DNS Configuration) Defines DNS servers used for name resolution.
```
nameserver 8.8.8.8
nameserver 8.8.4.4
```
