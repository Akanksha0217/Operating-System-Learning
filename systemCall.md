# 📘 OS System Calls – Notes

## 1. fork()
- Creates a new process.
- Parent → original process, Child → new process.
- Return values:
  - 0 → child process
  - >0 → PID of child to parent
  - -1 → error
- Both processes run independently.

---

## 2. pipe()
- Used for **Inter-Process Communication (IPC)**.
- One end → write (`fd[1]`), other end → read (`fd[0]`).
- Unidirectional (one-way communication).
- For two-way → need two pipes.

---

## 3. getpid()
- Returns the **Process ID (PID)** of the calling process.
- Useful for debugging and distinguishing parent/child processes.

---

## 4. open()
- Opens/creates a file → returns file descriptor (fd).
- Syntax: `int open(const char *pathname, int flags, mode_t mode);`
- Common flags:
  - `O_RDONLY` → read only
  - `O_WRONLY` → write only
  - `O_RDWR` → read + write
  - `O_CREAT` → create if not exist

---

## 5. close()
- Closes an opened file descriptor.
- Frees system resources.
- Must be used after every `open()`.

---

# ✅ Quick Summary
- **fork()** → create new process  
- **pipe()** → communication between processes  
- **getpid()** → get current process ID  
- **open()** → open/create file  
- **close()** → close file  
