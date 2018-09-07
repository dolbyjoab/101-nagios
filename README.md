<p align="center">
    <img src="docs/img/NagiosLogo.png"
        alt="Master">
</p>

<p align="center">
  <a href="https://github.com/dolbyjoab/101-nagios/tree/master">
    <img src="https://img.shields.io/badge/Branch-master-green.svg?longCache=true"
        alt="Branch">
  </a>
  <a href="http://www.gnu.org/licenses/">
    <img src="https://img.shields.io/badge/License-GNU-blue.svg?longCache=true"
        alt="License">
  </a>
</p>

***
<p align="center">
  <sub>Created by
  <a href="dolbyjoab.github.io">Dolbyjoab</a> and
  <a href="https://github.com/dolbyjoab/101-nagios/graphs/contributors">
    contributors
  </a>
    </sub>
</p>
  
***

## Table of Contents

- <b>[Introduction](#introduction)</b>
  * [Simple Questions](#simple-questions) - 11 questions.
- <b>[General Knowledge](#general-knowledge)</b>
  * [Junior Sysadmin](#junior-sysadmin) - 51 questions.
  * [Regular Sysadmin](#regular-sysadmin) - 73 questions.
  * [Senior Sysadmin](#senior-sysadmin) - 78 questions.
- <b>[Secret Knowledge](#secret-knowledge)</b>
  * [Guru Sysadmin](#guru-sysadmin) - 12 questions.

## <a name="general-knowledge">Introduction</a>

### :diamond_shape_with_a_dot_inside: <a name="simple-questions">Simple Questions</a>

- <b>What did you learn this week?</b>
- <b>What excites or interests you about the Sysadmin world?</b>
- <b>What is a recent technical challenge you experienced and how did you solve it?</b>
- <b>Tell me about the last major project you finished.</b>
- <b>Do you contribute to any open source projects?</b>
- <b>Describe the setup of your homelab.</b>
- <b>What personal achievement are you most proud of?</b>
- <b>Tell me about the biggest mistake you've made.</b>
- <b>Tell me about your favorite UNIX-like system.</b>
- <b>Tell me about how you manage your knowledge database (e.g. wikis).</b>
- <b>What news sources do you check daily? (Sysadmin or security-related)</b>

## <a name="general-knowledge">General Knowledge</a>

### :diamond_shape_with_a_dot_inside: <a name="junior-sysadmin">Junior Sysadmin</a>

###### System Questions

<details>
<summary><b>Give some examples of Linux distribution names.</b></summary><br>

- Red Hat Enterprise Linux
- Fedora
- CentOS
- Debian
- Ubuntu
- SUSE Linux Enterprise Server (SLES)
- SUSE Linux Enterprise Desktop (SLED)
- Slackware

Useful resources:

- [List of Linux distributions](https://en.wikipedia.org/wiki/List_of_Linux_distributions)

</details>

<details>
<summary><b>What are the differences between Unix, Linux, BSD and GNU?</b></summary><br>

GNU isn't really an OS. It's more of a set of rules or philosophies that govern free software, that at the same time gave birth to a bunch of tools while trying to create an OS. So GNU tools are basically open versions of tools that already existed, but were reimplemented to conform to principals of open software. GNU/Linux is a mesh of those tools and the Linux kernel to form a complete OS, but there are other "GNU"s, e.g. GNU/Hurd.

Unix and BSD are "older" implementations of POSIX that are various levels of "closed source". Unix is usually totally closed source, but there are as many flavors of Unix as there are Linux (if not more). BSD is not usually considered "open", but it was considered to be very open when it was released. Its licensing also allowed for commercial use with far fewer restrictions than the more "open" licenses of the time allowed.

Linux is the newest of the four. Strictly speaking, it's "just a kernel"; however, in general, it's thought of as a full OS when combined with GNU Tools and several other core components.

The main governing differences between these are their ideals. Unix, Linux, and BSD have different ideals that they implement. They are all POSIX, and are all basically interchangeable. They do solve some of the same problems in different ways. So other then ideals and how they choose to implement POSIX standards, there is little difference.

For more info I suggest your read a brief article on the creation of GNU, OSS, Linux, BSD, and UNIX. They will be slanted towards their individual ideas, but those articles should give you a better idea of the differences.

Useful resources:

- [What is the difference between Unix, Linux, BSD and GNU? (original)](https://unix.stackexchange.com/questions/104714/what-is-the-difference-between-unix-linux-bsd-and-gnu)
- [The Great Debate: Is it Linux or GNU/Linux?](https://www.howtogeek.com/139287/the-great-debate-is-it-linux-or-gnulinux/)

</details>

<details>
<summary><b>What is a CLI?</b></summary><br>

<b>CLI</b> is an acronym for Command Line Interface or Command Language Interpreter. The command line is one of the most powerful ways to control your system/computer.

In Linux, CLI is the interface by which a user can type commands for the system to execute. The CLI is very powerful, but is not very error-tolerant.

Useful resources:

- [Command Line Interface Definition](http://www.linfo.org/command_line_interface.html)

</details>

<details>
<summary><b>What is your favourite shell and why?</b></summary><br>

BASH is my favorite. It’s really a preferential kind of thing, where I love the syntax and it just "clicks" for me. The input/output redirection syntax (<code>>></code>, <code><< 2>&1</code>, <code>2></code>, <code>1></code>, etc) is similar to C++ which makes it easier for me to recognize.

I also like the ZSH shell, because is much more customizable than BASH. It has the Oh-My-Zsh framework, powerful context based tab completion, pattern matching/globbing on steroids, loadable modules and more.

Useful resources:

- [Comparison of command shells](https://en.wikipedia.org/wiki/Comparison_of_command_shells)

</details>

<details>
<summary><b>How do you get a list of logged-in users?</b></summary><br>

For a summary of logged-in users, including each login of a username, the terminal users are attached to, the date/time they logged in, and possibly the computer from which they are making the connection, enter:

```bash
who
```

For extensive information, including username, terminal, IP number of the source computer, the time the login began, any idle time, process CPU cycles, job CPU cycles, and the currently running command, enter:

```bash
w
```

<details>
<summary><b>How do you run commands in the background? *</b></summary><br>

To be completed.

</details>

</details>

<details>
<summary><b>What does it mean when the effective user is "root", but the real user ID is still your name?</b></summary><br>

The real user ID is who you really are (the user who owns the process), and the effective user ID is what the operating system looks at to make a decision whether or not you are allowed to do something (most of the time, there are some exceptions).

When you log in, the login shell sets both the real and effective user ID to the same value (your real user id) as supplied by the password file.

If, for instance, you execute setuid, and besides running as another user (e.g. root) the setuid program is also supposed to do something on your behalf:

After executing setuid, it will have your real id (since you're the process owner) and the effective user id of the file owner (for example root) since it is setuid.

Let's use the case of passwd:

```bash
-rwsr-xr-x 1 root root 45396 may 25  2012 /usr/bin/passwd
```

When user2 wants to change their password, they execute `/usr/bin/passwd`.

The **RUID** will be user2 but the **EUID** of that process will be root.

user2 can use only passwd to change their own password, because internally passwd checks the **RUID** and, if it is not root, its actions will be limited to real user's password.

It's neccesary that the **EUID** becomes root in the case of passwd because the process needs to write to `/etc/passwd` and/or `/etc/shadow`.

Useful resources:

- [Difference between Real User ID, Effective User ID and Saved User ID? (original)](https://stackoverflow.com/questions/30493424/what-is-the-difference-between-a-process-pid-ppid-uid-euid-gid-and-egid)
- [What is the difference between a pid, ppid, uid, euid, gid and egid?](https://stackoverflow.com/questions/30493424/what-is-the-difference-between-a-process-pid-ppid-uid-euid-gid-and-egid)

</details>

<details>
<summary><b>Another admin is running all commands as root. Why is this a bad idea?</b></summary><br>

Running everything as root is bad because:

- **Stupidity**: nothing prevents you from making a careless mistake. If you try to change the system in any potentially harmful way, you need to use sudo, which ensures a pause (while you're entering the password) to ensure that you aren't about to make a mistake.

- **Security**: harder to hack if you dont know the admin user's login account. root means you already have one half of the working set of admin credentials.

- **You don't really need it**: if you need to run several commands as root, and you're annoyed by having to enter your password several times when `sudo` has expired, all you need to do is `sudo -i` and you are now root. Want to run some commands using pipes? Then use `sudo sh -c "command1 | command2"`.

- **You can always use it in the recovery console**: the recovery console allows you to recover from a major mistake, or fix a problem caused by an app (which you still had to run as `sudo`). Ubuntu doesn't have a password for the root account in this case, but you can search online for changing that - this will make it harder for anyone that has physical access to your box to be able to do harm.

Useful resources:

- [Why is it bad to log in as root? (original)](https://askubuntu.com/questions/16178/why-is-it-bad-to-log-in-as-root)

</details>

<details>
<summary><b>Which command is used to review boot messages?</b></summary><br>

<code>dmesg</code> is used to review boot messages. This command will display system messages contained in the kernel ring buffer. We can use this command immediately after booting to see boot messages. A ring buffer is a buffer of fixed size for which any new data added to it overwrites the oldest data in it.

</details>

<details>
<summary><b>What is the swap space?</b></summary><br>

Swap space is used when the amount of physical memory (RAM) is full. If the system needs more memory resources and the RAM is full, inactive pages in memory are moved to the swap space. While swap space can help machines with a small amount of RAM, it should not be considered a replacement for more RAM. Swap space is located on hard drives, which have a slower access time than physical memory.

</details>

<details>
<summary><b>How to check memory stats and CPU stats?</b></summary><br>

You'd use `top/htop` for both. Using <code>free</code> and <code>vmstat</code> command we can display the physical and virtual memory statistics respectively. With the help of <code>sar</code> command we see the CPU utilization & other stats (but `sar` isn't even installed in most systems).

</details>

<details>
<summary><b>What is load average?</b></summary><br>

Linux load averages are "system load averages" that show the running thread (task) demand on the system as an average number of running plus waiting threads. This measures demand, which can be greater than what the system is currently processing. Most tools show three averages, for 1, 5, and 15 minutes.

Some interpretations:

- If the averages are 0.0, then your system is idle.
- If the 1 minute average is higher than the 5 or 15 minute averages, then load is increasing.
- If the 1 minute average is lower than the 5 or 15 minute averages, then load is decreasing.
- If they are higher than your CPU count, then you might have a performance problem (it depends).

</details>

<details>
<summary><b>How to create partition and filesystem?</b></summary><br>

1) <code>fdisk</code> or <code>gparted</code> - create a new partition<br>
2) <code>mkfs</code> - create a new filesystem

</details>

<details>
<summary><b>Where journaling is dedicated?</b></summary><br>

Journaling has a dedicated area in the file system, where all the changes are tracked. When the system crashes, the possibility of file  system corruption is less because of journaling.

</details>

<details>
<summary><b>What are the kinds of permissions under Unix-like?</b></summary><br>

- <b>Read</b>: users can read the files or list the directory<br>
- <b>Write</b>: users may write to the file or add new files to the directory<br>
- <b>Execute</b>: users may run the file or lookup a specific file within a directory

</details>

<details>
<summary><b>Where is password file located in Linux?</b></summary><br>

Linux passwords are stored in the <b>/etc/shadow</b> file. They are salted and the algorithm being used depends on the particular distribution and is configurable.

</details>

<details>
<summary><b>How do you change directory and subdirectory with file permissions in Linux/UNIX?</b></summary><br>

To change all the directories e.g. to 755 (drwxr-xr-x):<br>

<code>
find /opt/data -type d -exec chmod 755 {} \;
</code><br><br>

To change all the files e.g. to 644 (-rw-r--r--):<br>

<code>
find /opt/data -type f -exec chmod 644 {} \;
</code><br><br>

</details>

<details>
<summary><b>What is redirection?</b></summary><br>

It’s a fairly simple process, allowing you to direct data from one output to another. You can also use it to direct an output as an input to another process.

</details>

<details>
<summary><b>What is grep command?</b></summary><br>

<code>grep</code> searches file patterns. If you are looking for a specific pattern in the output of another command, grep highlights the relevant lines. Use this grep command for searching log files, specific processes, and more.<br>

</details>

<details>
<summary><b>Explain file content commands along with the description.</b></summary><br>

- <b>head</b>: to check the starting of a file.<br>
- <b>tail</b>: to check the ending of the file. It is the reverse of head command.<br>
- <b>cat</b>: used to view, create, concatenate the files.<br>
- <b>more</b>: used to display the text in the terminal window in pager form.<br>
- <b>less</b>: used to view the text in the backward direction and also provides single line movement.

</details>

<details>
<summary><b>Explain SIGHUP, SIGINT, SIGKILL and SIGTERM Posix signals.</b></summary><br>

- <b>SIGHUP</b> - the SIGHUP signal is sent to a process when its controlling terminal is closed. It was originally designed to notify the process of a serial line drop (a hangup). Many daemons will reload their configuration files and reopen their logfiles instead of exiting when receiving this signal.<br>
- <b>SIGINT</b> - the SIGINT signal is sent to a process by its controlling terminal when a user wishes to interrupt the process. This is typically initiated by pressing Ctrl+C, but on some systems, the "delete" character or "break" key can be used.<br>
- <b>SIGKILL</b> - the SIGKILL signal is sent to a process to cause it to terminate immediately (kill). In contrast to SIGTERM and SIGINT, this signal cannot be caught or ignored, and the receiving process cannot perform any clean-up upon receiving this signal.<br>
- <b>SIGTERM</b> - the SIGTERM signal is sent to a process to request its termination. Unlike the SIGKILL signal, it can be caught and interpreted or ignored by the process. This allows the process to perform nice termination releasing resources and saving state if appropriate. SIGINT is nearly identical to SIGTERM.

</details>

<details>
<summary><b>What is the difference between <code>rm</code> and <code>rm -rf</code>?</b></summary><br>

<code>rm</code> removes files and <code>-rf</code> are two options:<br>

- <code>-r</code> remove directories and their contents recursively<br>
- <code>-f</code> ignore nonexistent files, never prompt

</details>

<details>
<summary><b>How do you list contents of archive.tgz and extract only one file?</b></summary><br>

```bash
tar tf archive.tgz
tar xf archive.tgz filename
```

</details>

<details>
<summary><b>How to sync two local directories?</b></summary><br>

To sync the contents of dir1 to dir2 on the same system, type:

```bash
rsync -av --progress --delete dir1/ dir2
```

- <code>-a, --archive</code> - archive mode
- <code>--delete</code> - delete extraneous files from dest dirs
- <code>-v, --verbose</code> - verbose mode (increase verbosity)
- <code>--progress</code> - show progress during transfer

</details>

<details>
<summary><b>How to quickly backup a file?</b></summary><br>

```bash
cp filename{,.orig}
```

</details>

<details>
<summary><b>How to find all files larger than 20M?</b></summary><br>

```bash
find / -type f -size +20M
```

</details>

<details>
<summary><b>Why do we use <code>sudo su -</code> and not just <code>sudo su</code>?</b></summary><br>

<code>su -</code> invokes a login shell after switching the user. A login shell resets most environment variables, providing a clean base.

<code>su</code> just switches the user, providing a normal shell with an environment nearly the same as with the old user.

</details>

<details>
<summary><b>How to find files that have been modified on your system in the past 60 minutes?</b></summary><br>

```bash
find / -mmin 60 -type f
```

</details>
