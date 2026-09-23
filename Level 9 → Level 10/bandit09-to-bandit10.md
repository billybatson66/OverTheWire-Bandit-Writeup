# Level 9 → Level 10

### **🎯 Objective:** 
> The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters.

The approach is: Use the command **strings** to help locate the human-readable strings and then **grep** all the lines that has the "=" character.

### **⌨️ Commands used:**

We'll use **strings** followed by a line separator and **grep**:

```bash
strings data.txt | grep "="
```

<p align ="center">
    <img src= "../assets/Level 9 -> Level 10/step1.png" />
</p>

Finally we get the password for user `bandit10` which is 


<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `B0s2khmbT9u0geKuOoVGW3JZKhndE3BG`

  </div>
</details>

---

### **💡 Key takeaways:**

**strings** helps us prints out human-readable strings.
