# Level 2 → Level 3

### **🎯 Objective:** 
> The password for the next level is stored in a file called --spaces in this filename-- located in the home directory.

The approach is: To **cat** the file called "--spaces in this filename--", but the problem is this file has both the **-** preceding it and spaces in the name. To solve this issue, we'll be using quotations in combination with stating the explicit path we did last level.

### **⌨️ Commands used:**

We'll be using both quotations and explicit path:

```bash
cat ./"--spaces in this filename--"
```

<p align ="center">
    <img src= "../assets/Level 2 -> Level 3/step1.png" />
</p>

Finally we get the password for user `bandit1` which is 


<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME`

  </div>
</details>

---

### **💡 Key takeaways:**

Enclosing a filename in quotes forces the shell to treat spaces as literal characters within a single file name rather than as separators.
