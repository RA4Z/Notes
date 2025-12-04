In [[🐍Python]], multiprocessing spawns separate processes, each with its own [[🐍Python]] interpreter and memory space. 

It allows **true parallelism** across multiple CPU cores, making it suitable for **CPU-bound tasks**

**Multiprocessing = parallelism for CPU**
```Python
from multiprocessing import Process
import math, time
def cpu_bound(n):
   print(f"Calculating sum of squares up to {n}...")
   total = sum(i * i for i in range(n))
   print("Done.")
   
if __name__ == "__main__":
   start = time.time()
   p1 = Process(target=cpu_bound, args=(10_000_000,))
   p2 = Process(target=cpu_bound, args=(10_000_000,))
   p1.start(); p2.start()
   p1.join(); p2.join()
   print("Time taken:", time.time() - start)
```