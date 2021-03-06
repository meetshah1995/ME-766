# Matrix Multiplication using MPI and OpenMP

#### Meet Pragnesh Shah | 13D070003  

### Experiments and Conclusion

I ran the experiments for square matrices of size N = [ 100, 1000 , 2000 ]. The time taken by matrices larger than N = 2000 was larger than a couple minutes and the trends in the graphs were similar and hence I have skipped them. The plots of the time taken for computing A*B for the given sizes are plotted against the number of threads varying from 1 to 8.

As we can see from the plots the reduction in time is significant when going from `n_threads` going from 1 to 2/3, but later this reduction dies out. This can be reasoned due to the fact that the latency of the message transmissions becomes comparable to the individual parallel computations and hence there is no significant reduction in the total time taken,

NOTE : This trends are a bit random. I observed a ~5% change in times when computed in the same environment under similar conditions. 
 
#### N = 100

Time Taken vs n_threads 

![N = 100](n100.png)


#### N = 1000

Time Taken vs n_threads

![N = 1000](n1000.png)

#### N = 2000

Time Taken vs n_threads 

![N = 2000](n2000.png)


### Desktop Configuration

* Architecture:          x86_64
* CPU op-mode(s):        32-bit, 64-bit
* Byte Order:            Little Endian
* CPU(s):                4
* On-line CPU(s) list:   0-3
* Thread(s) per core:    2
* Core(s) per socket:    2
* Socket(s):             1
* NUMA node(s):          1
* Vendor ID:             GenuineIntel
* CPU family:            6
* Model:                 61
* Stepping:              4
* CPU MHz:               804.750
* BogoMIPS:              4788.76
* Virtualization:        VT-x
* L1d cache:             32K
* L1i cache:             32K
* L2 cache:              256K
* L3 cache:              4096K
* NUMA node0 CPU(s):     0-3

### Memory Configuration

* Total RAM = 2x4096 MB

* Handle 0x0055, DMI type 17, 34 bytes
* Memory Device
	* Array Handle: 0x0050
	* Error Information Handle: Not Provided
	* Total Width: 64 bits
	* Data Width: 64 bits
	* Size: 4096 MB
	* Form Factor: SODIMM
	* Set: None
	* Locator: DIMM A
	* Bank Locator: Not Specified
	* Type: DDR3
	* Type Detail: Synchronous
	* Speed: 1600 MHz
	* Manufacturer: Kingston
	* Serial Number: 9F8887E6
	* Asset Tag: 9876543210
	* Part Number: KNWMX1-ETB
	* Rank: 1
	* Configured Clock Speed: 1600 MHz
