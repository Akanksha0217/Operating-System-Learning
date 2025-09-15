# 📘 OS Process Commands – Notes  

## 1. top  
- Displays **real-time information** about running processes.  
- Shows CPU usage, memory usage, process ID, etc.  
- Useful for monitoring system performance.  
- Press `q` to quit.  

---

## 2. kill  
- Sends a **signal** to a process (commonly used to stop/terminate).  
- Syntax:  
  - `kill PID` → sends `SIGTERM` (terminate)  
  - `kill -9 PID` → sends `SIGKILL` (force kill)  
- PID can be found using `ps` or `top`.  

---

## 3. wait (system call)  
- Makes a parent process **wait** until its child process finishes execution.  
- Used with `fork()` to synchronize parent and child.  
- Syntax:  
  ```c
  pid_t wait(int *status);
  ```
## 4. sleep
- Suspends execution of a process for a given time (in seconds).

## ✅ Quick Summary
- top → Monitor running processes.
- kill → Terminate processes using PID.
- wait → Parent waits for child process to finish.
- sleep → Pause process for some time
