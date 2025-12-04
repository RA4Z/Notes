In [[🐍Python]], multithreading creates multiple threads within a single process, sharing the same memory space.

It cannot execute bytecode in true parallelism, they run concurrently via context switching, making threading ideal for [[I & O|I/O-bound tasks]] where the CPU spends time waiting

**Multithreading = concurrency for [[I & O|I/O]]
```Python
import time
from threading import Thread
def io_bound(sec):
   print(f"Sleeping for {sec} seconds...")
   time.sleep(sec)
   print("Done sleeping.")
   
if __name__ == "__main__":
   start = time.time()
   t1 = Thread(target=io_bound, args=(3,))
   t2 = Thread(target=io_bound, args=(3,))
   t1.start(); t2.start()
   t1.join(); t2.join()
   print("Time taken:", time.time() - start)
```