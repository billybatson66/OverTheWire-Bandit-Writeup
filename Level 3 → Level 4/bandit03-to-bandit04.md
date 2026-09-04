# Level 3 → Level 4

### **🎯 Objective:** 
> The password for the next level is stored in a hidden file in the inhere directory.

The approach is: **cat** the hidden file in the hidden directory **inhere**

### **⌨️ Commands used:**

We'll be using **ls** with the flag **-a** to show all of the hidden files and directories:

```bash
ls -a
```

<p align ="center">
    <img src= "../assets/Level 3 -> Level 4/step1.png" />
</p>

Then we'll **cd** into the hidden directory **inhere** and **ls -a** its contents:

```bash
cd ./inhere
ls -a
```

<p align ="center">
    <img src= "../assets/Level 3 -> Level 4/step2.png" />
</p>

Finally, we'll **cat** the file using specific path we learned in the last level: 

```bash
cat ./...Hiding-From-You
```

<p align ="center">
    <img src= "../assets/Level 3 -> Level 4/step3.png" />
</p>

<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq`

  </div>
</details>

---

### **💡 Key takeaways:**

In Linux, any file or directory name starting with a dot (.) is hidden by default and requires the -a flag with ls to view.

Using relative paths starting with **./** tells the shell to look in the current working directory. This prevents Linux from mistaking dot-heavy filenames (like ...Hiding-From-You) or filenames starting with dashes (-) for command options or special directory references (like . or ..).
