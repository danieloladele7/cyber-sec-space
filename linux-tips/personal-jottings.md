To resume a **suspended process** in Ubuntu (or any Linux-based system), you can use one of the following methods depending on how the process was suspended.

---

### 🔹 1. Resume from the **Foreground**

If you suspended a process using `Ctrl + Z`, it's paused and placed in the background. You can resume it using:

```bash
fg
```

This brings the most recently suspended job back to the **foreground**.

---

### 🔹 2. Resume in the **Background**

If you want the suspended job to continue running in the background:

```bash
bg
```

This resumes the most recently suspended job in the **background**.

---

### 🔹 3. Resume a Specific Job

If you have multiple jobs, list them with:

```bash
jobs
```

Example output:

```
[1]+  Stopped                 python script.py
[2]-  Stopped                 nano
```

Then resume a specific job using its job number:

* Foreground: `fg %1`
* Background: `bg %2`

---

### 🔹 4. Resume a Process by PID (if needed)

If you know the **PID** of the suspended process (e.g., from `ps` or `top`), you can send it a `CONT` signal:

```bash
kill -CONT <pid>
```

Replace `<pid>` with the actual process ID.

---

Would you like help identifying the PID or using `jobs` to find the process?

