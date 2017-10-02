# docker-R-benchmarking
Using virtualized environments can somtimes abstract away performace issues. For
instance, how many virtualized cores are mapped to bare metal cores? Does this effect
performance?  

The goal of this repo is to provide two docker contianers that allow benchmarking
of compute heavy workloads, so that benchmarking on different environments allows for 
more transparency into slow running processes.

We will use Microsoft R Open to examine multi-threaded performance.


## How to use?
First grab a local copy:
```
git clone https://github.com/Duke-Translational-Bioinformatics/docker-R-benchmarking.git
```
### Base R
Build a Base R image:
```
cd ./baser-docker
docker build -t baser-benchmark .
```
Run the container, output is directed to stdout:
```
docker run baser-benchmark
```

### Microsoft R Open
Build a Microsoft R Open Image (see README for attributing credit).
```
cd ./mro-docker
docker build -t mro-benchmark .
```
Run the container, output is directed to stdout:
```
docker run mro-benchmark
```

## Performance Metrics
| Environment   | Container     | Results  |
| ------------- |:-------------:| -----:|
| Laptop<sup>*</sup>        | Base R        | [results](results/laptop_baser.txt) |
| Laptop<sup>*</sup>        | Microsoft R Open<sup>**</sup>      |   [results](results/laptop_mro.txt) |

<sup>*</sup> - cpu: 4 / ram: 16GB  
<sup>**</sup> - *defaults to using 2 cores*

