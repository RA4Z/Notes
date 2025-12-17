Cache memory is a type of high-speed memory located on the CPU that stores frequently accessed data to improve processing efficiency.

#### L1 Cache
Also known as primary cache, is the smallest and fastest type of cache memory. It is typically around 64KB per core and is divided into two parts: L1-I (instruction) and L1-D (data).
The L1-I cache stores instructions for the CPU, while the L1-D cache stores data. L1 cache operates at the same speed as the CPU, making it extremely efficient for quick data access.

#### L2 Cache
L2 cache is larger but slower than L1 cache. It is usually around 256KB to 1MB per core and is also embedded within each CPU core. L2 cache server as a secondary storage for data that is not found in the L1 cache. It is still much faster than the main system memory (RAM) but slower than L1 cache.

#### L3 Cache
L3 cache is the largest and slowest among the three levels of cache. It is typically shared among all the cores in a CPU and can range from a few megabytes to several tens of megabytes. L3 cache acts as a shared storage pool that reduces the chances of a cache miss, thereby improving overall performance. Unlike L1 and L2 caches, L3 cache is not embedded within each core but is located on the CPU chip.
