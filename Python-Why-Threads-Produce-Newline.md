# Why Threads produce newline.

The regular `input()` used in a thread function is producing additional newline.  
The solution is simply do not use the `input()` inside the threaded applications.  
Instead you should use `sys.stdin.readline().strip()`.

The `input()` produces additional line because it thinks that it needs to produce it.  
And also the `stdin` stream automatically attaches a newline,  
therefore using `.strip()` makes sure it won't happen.

Sources:  
https://stackoverflow.com/questions/31142566/print-skipping-newline
