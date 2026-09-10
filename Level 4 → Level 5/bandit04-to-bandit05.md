# Level 4 → Level 5

### **🎯 Objective:** 
> The password for the next level is stored in the only human-readable file in the inhere directory. Tip: if your terminal is messed up, try the “reset” command.

The approach is: To use the command **file** to check for file types, if it's in the ASCII text format then it is human-readable. We can also take the longer route of **cat** every single file to see which one is human-readable.

### **⌨️ Commands used:**

We'll be using **cd** to change into the "inhere" directory and **file /.*** to show all of the human-readable files:

```bash
cd inhere
file ./*
```
  
<p align ="center">
    <img src= "../assets/Level 4 -> Level 5/step1.png" />
</p>

Then we'll check which file is in the format of ASCII Text (which in this case is the **-file07** file, and then we'll **cat** that file:

```bash
cat ./-file07
```

<p align ="center">
    <img src= "../assets/Level 4 -> Level 5/step2.png" />
</p>


<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG`

  </div>
</details>

---

### **💡 Key takeaways:**

Instead of inspecting every file manually with cat (which can break your terminal when printing binary data), use file ./* to inspect magic bytes and identify ASCII text or human-readable formats instantly.
