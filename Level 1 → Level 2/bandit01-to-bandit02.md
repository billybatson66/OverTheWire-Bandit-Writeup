# Level 1 → Level 2

### **🎯 Objective:** 
> The password for the next level is stored in a file called - located in the home directory

The approach is: To **cat** the file without the syntax reading it as a prefix **-** to a flag.

### **⌨️ Commands used:**

We will be stating the specific path which is **cat ./-** (**.** stands for the current working directory) or  **/home/bandit1/-** to solve this issue

```bash
cat ./-
```

or

```bash
cat /home/bandit1/-
```

<p align ="center">
    <img src= "../assets/Level 1 -> Level 2/step1.png" />
</p>

Finally we get the password for user `bandit2` which is 


<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `PK8fYLZg2hnHSz83plBL1iEPKdD3QToB`

  </div>
</details>

---

### **💡 Key takeaways:**

**🚩 Flag & Syntax Behaviors:**
* Commands expect options to start with a dash (-): Whenever **cat** sees a **-**, it immediately assumes you are trying to give it a setting, option, or flag.
=> We can solve this issue by stating the explicit path.