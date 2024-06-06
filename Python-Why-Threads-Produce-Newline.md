# Why Threads produce newline.

The regular `input()` used in a thread function is producing additional newline.  
The solution is simply do not use the `input()` inside the threaded applications.  
Instead you should use `sys.stdin.readline().strip()`.

Sources:  
https://stackoverflow.com/questions/31142566/print-skipping-newline
