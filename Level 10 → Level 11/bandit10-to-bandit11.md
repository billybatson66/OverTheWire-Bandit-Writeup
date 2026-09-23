# Level 10 → Level 11

### **🎯 Objective:** 
> The password for the next level is stored in the file data.txt, which contains base64 encoded data

The approach is: Use command **base64** to decode base64 encoded data.

### **⌨️ Commands used:**

We'll use **base64** and the flag **-d** which means decode:

```bash
base64 -d data.txt
```

<p align ="center">
    <img src= "../assets/Level 10 -> Level 11/step1.png" />
</p>

Finally we get the password for user `bandit11` which is 


<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro`

  </div>
</details>

---

### **💡 Key takeaways:**

**base64** helps us decode and encode base64 data.
