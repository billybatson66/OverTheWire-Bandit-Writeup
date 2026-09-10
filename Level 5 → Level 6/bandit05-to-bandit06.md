# Level 5 → Level 6

### **🎯 Objective:** 
> The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
>
> * human-readable
> * 1033 bytes in size
> * not executable

The approach is: To use the command **find** with the flag **-size** and **-executable** to find file that fit these criteria first, and then we'll check which files are human-readable later.

### **⌨️ Commands used:**

We'll be using **find** with the flag **-size** and **-executable** to filter the files:

```bash
cd inhere
find . -size 1033b ! -executable
```
**1033b** means find files with the exact size of **1033 bytes** and **! -executable** means not executable.

<p align ="center">
    <img src= "../assets/Level 5 -> Level 6/step1.png" />
</p>

Finally, we only get one result, so we'll **cat** the file, if not we can check the file format and use the technique we previously used in the last level. 

```bash
cat ./maybehere07/.file2
```

<p align ="center">
    <img src= "../assets/Level 5 -> Level 6/step2.png" />
</p>

<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `pXa26xhMWaC2SvDotA4r9EgZkulOeSBW`

  </div>
</details>

---

### **💡 Key takeaways:**

The find command is ideal for pinpointing files across nested directories using filters like **-size** and permission flags.

Prepending an exclamation mark (!) negates test conditions, allowing you to easily target files that lack specific attributes (such as **! -executable** to find non-executable files).

In the find utility, appending the suffix **c** denotes exact bytes (e.g., -size 1033c), while **b** traditionally designates 512-byte blocks.
