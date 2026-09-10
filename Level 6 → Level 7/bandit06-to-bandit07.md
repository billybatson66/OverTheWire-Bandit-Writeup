# Level 6 → Level 7

### **🎯 Objective:** 
The password for the next level is stored somewhere on the server and has all of the following properties:
>
>  * owned by user bandit7
>  * owned by group bandit6
>  * 33 bytes in size

The approach is: To use the **find /** to implement on the whole root directory, with flags **-size**, **-user**, **-group** and **2>/dev/null** to filter out successful results only.

### **⌨️ Commands used:**

We'll be using **find /** to implement **find** on the whole root directory with these flags **-size 33c -user bandit7 -group bandit6** and add **2>/dev/null** at the end to get the successful attempts only (filter out "Permission denied"):

```bash
find / -size 33c -user bandit7 -group 2>/dev/null 
```

<p align ="center">
    <img src= "../assets/Level 6 -> Level 7/step1.png" />
</p>

Finally, we'll **cat** the file using specific path we learned in the last level: 

```bash
cat /var/lib/dpkg/info/bandit7.password
```

<p align ="center">
    <img src= "../assets/Level 6 -> Level 7/step2.png" />
</p>

<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3`

  </div>
</details>

---

### **💡 Key takeaways:**

Running find **/** initiates a recursive search starting from the root directory down to every accessible node on the machine.

The flags **-user** <username> and -group <groupname> allow precise filtering based on file ownership and group association.

Searching across root as an unprivileged user triggers dozens of "Permission denied" errors. Redirecting standard error (stream 2) to the null device (/dev/null) discards noise and leaves only stdout visible. 

=> Use **2>/dev/null** to filter "Permission Denied" returns.
