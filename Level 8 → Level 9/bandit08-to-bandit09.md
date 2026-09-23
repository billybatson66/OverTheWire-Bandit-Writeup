# Level 8 → Level 9

### **🎯 Objective:** 
> The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

The approach is: To **sort** the files so that duplicate strings will be adjacent to each other, which is essential so that we can use **uniq** to compare adjacent lines and remove the duplicate ones, returning only the **-u (unique)**.

### **⌨️ Commands used:**

We'll be using **sort** and then **uniq** the output with line separator.

```bash
sort data.txt | uniq -u 
```

<p align ="center">
    <img src= "../assets/Level 8 -> Level 9/step1.png" />
</p>

Finally we get the password for user `bandit9` which is 


<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl`

  </div>
</details>

---

### **💡 Key takeaways:**

**Uniq** compares adjacent (neighboring lines) and prints the output, with the flag **-u**, it returns only unique lines.

**Sort** sorts the content of the files alphabetically.
