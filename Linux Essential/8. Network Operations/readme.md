## 💻 Summary of Accomplished Tasks From Screenshots

I performed several diagnostic checks to verify the host's network configuration, name resolution, and external connectivity.

**Local Host Verification**
* **Host File Check:** I displayed the contents of `/etc/hosts` to confirm local loopback and host name mappings.
* **Local Ping Test:** I used the command `ping kali`, which successfully resolved and transmitted 10 packets with **$0\%$ packet loss**, confirming internal system functionality.

**Interface and Link Status**
* **Interface Settings:** I used `sudo ethtool eth0` to check the link status, confirming the link was detected at a **Speed of $1000\text{Mb/s}$** (Full Duplex).
* **IP Address Check:** I used `ip a brief addr show` to verify the host's assigned IP address, which was **$192.168.110.250/24$** on the `eth0` interface.

**DNS and External Connectivity**
* **Name Resolution:** I used `host`, `nslookup`, and `dig` commands to successfully resolve several external domains (`apple.com`, `daddy.com`, `amazon.com`). These lookups used the DNS server **$192.168.110.104$**.
* **Ping Test:** I attempted to reach external hosts using `ping amazon.com`. The result showed a definitive **$100\%$ packet loss** (two attempts), indicating a critical failure in external connectivity despite successful DNS resolution.

### File Creation, Manipulation, and Concatenation (From Notes)

I performed several file creation, manipulation, and concatenation tasks within the `/tmp` directory.

**File Creation and Editing (`file1.txt`)**
* **Change Directory:** I changed the current working directory to `/tmp` using the `pushd /tmp` command from the home directory (`~`).
* **Attempted Deletion:** I attempted to remove files using `rm f file*`, but the command failed because no files matching that pattern existed (the error message confirms this: `rm: cannot remove 'f file*': No such file or directory`).
* **File Creation/Editing with nano:** I opened or created a file named `file1.txt` using the `nano` text editor.
* **Content:** The content I typed was:
  > `and i will just type thngs the wau i want yeahh`
* **Verification:** I displayed the content of the newly created `file1.txt` using `cat file1.txt`.

**File Creation using Here Document (`file2.txt`)**
* **File Creation:** I created a file named `file2.txt` using a here document (`<< EOF`) piped into the `cat` command, which redirected the output (`>`) to the new file.
* **Content:** The content of `file2.txt` was:
  > `here is the annoying guy file is few and plenty bars hahahaha`
* **Verification:** I verified the content of `file2.txt` using `cat file2.txt`.

**File Concatenation and Overwriting**
* **Concatenation:** I used the `cat` command to display the content of `file2.txt` and then the content of `file1.txt`, redirecting the combined output into `file1.txt` itself: `cat file2.txt file1.txt > file1.txt`.
