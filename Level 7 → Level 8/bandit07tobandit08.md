# Level 7 → Level 8

### **🎯 Objective:** 
> The password for the next level is stored in the file data.txt next to the word millionth.

The approach is: To **cat** the file called "data.txt", but the problem is this file contains too much content for us to actually locate the flag which is next to the word "millionth", we'll use **grep** to help us locate the flag.

### **⌨️ Commands used:**

We'll be using **cat** in combination with **grep** to find the flag:

```bash
cat data.txt | grep "millionth"
```

<p align ="center">
    <img src= "../assets/Level 7 -> Level 8/step1.png" />
</p>

Finally we get the password for user `bandit8` which is 


<details>
  <summary>Click to reveal spoiler</summary>
  <br>
  <div align="center">

  ### `VR1ljMayciFxbnUokuQmJFw6QC9VKtub`

  </div>
</details>

---

### **💡 Key takeaways:**

**grep** helps us locate certain phrases, keyword and text patterns inside of a file. The separator **|** means taking the output of **Cat data.txt** and running the content through **grep**.
