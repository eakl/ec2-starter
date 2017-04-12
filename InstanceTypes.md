# General Purpose

### T2
Baseline level of CPU performance with the ability to burst above the baseline. For workloads that don’t use the full CPU often or consistently, but occasionally need to burst.

| Model	     | vCPU	| CPU	Credits / hour	| Mem (GiB)	| Storage  |
|---         |---   |---                  |---        |---       |
| t2.nano	   | 1    | 3	                  | 0.5	      | EBS-Only |
| t2.micro   | 1    | 6	                  | 1	        | EBS-Only |
| t2.small   | 1    | 12	                | 2	        | EBS-Only |
| t2.medium  | 2    | 24	                | 4	        | EBS-Only |
| t2.large   | 2    | 36	                | 8	        | EBS-Only |
| t2.xlarge	 | 4    | 54	                | 16	      | EBS-Only |
| t2.2xlarge | 8    | 81	                | 32	      | EBS-Only |

### M4
Balance of compute, memory, and network resources.

| Model	      | vCPU | Mem (GiB)	| SSD Storage (GB) | Dedicated EBS Bandwidth (Mbps) |
|---          |---   |---         |---               |---                             |
| m4.large    | 2    | 8          | EBS-only         | 450                            |
| m4.xlarge   | 4    | 16         | EBS-only         | 750                            |
| m4.2xlarge  | 8    | 32         | EBS-only         | 1,000                          |
| m4.4xlarge  | 16   | 64         | EBS-only         | 2,000                          |
| m4.10xlarge | 40   | 160        | EBS-only         | 4,000                          |
| m4.16xlarge | 64   | 256        | EBS-only         | 10,000                         |


### M3
Balance of compute, memory, and network resources.

| Model      | vCPU | Mem (GiB) | SSD Storage (GB) |
|---         |---   |---        |---               |
| m3.medium  | 1    | 3.75      | 1 x 4            |
| m3.large   | 2    | 7.5       | 1 x 32           |
| m3.xlarge  | 4    | 15        | 2 x 40           |
| m3.2xlarge | 8    | 30        | 2 x 80           |

# Compute Optimized

### C4
Highest performing processors and the lowest price/compute performance in EC2.

| Model      | vCPU | Mem (GiB) | Storage  | Dedicated EBS Bandwidth (Mbps) |
|---         |---   |---        |---       |---                             |
| c4.large   | 2    | 3.75      | EBS-Only | 500                            |
| c4.xlarge  | 4    | 7.5       | EBS-Only | 750                            |
| c4.2xlarge | 8    | 15        | EBS-Only | 1,000                          |
| c4.4xlarge | 16   | 30        | EBS-Only | 2,000                          |
| c4.8xlarge | 36   | 60        | EBS-Only | 4,000                          |

### C3

| Model      | vCPU | Mem (GiB) | SSD Storage (GB) |
|---         |---   |---        |---               |
| c3.large   | 2    | 3.75      | 2 x 16           |
| c3.xlarge  | 4    | 7.5       | 2 x 40           |
| c3.2xlarge | 8    | 15        | 2 x 80           |
| c3.4xlarge | 16   | 30        | 2 x 160          |
| c3.8xlarge | 32   | 60        | 2 x 320          |

# Memory Optimized

### X1
Optimized for large-scale, enterprise-class, in-memory applications and have the lowest price per GiB of RAM among Amazon EC2 instance types.

| Model       | vCPU | Mem (GiB) | SSD Storage (GB) | Dedicated EBS Bandwidth (Mbps) |
|---          |---   |---        |---               |---                             |
| x1.32xlarge | 128  | 1,952     | 2 x 1,920        | 10,000                         |
| x1.16xlarge | 64   | 976       | 1 x 1,920        | 5,000                          |

### R4
Optimized for memory-intensive applications and offer better price per GiB of RAM than R3.

| Model       | vCPU | Mem (GiB) | Networking Performance | SSD Storage (GB) |
|---          |---   |---        |---                     |---               |
| r4.large    | 2    | 15.25     | Up to 10 Gigabit       | EBS-Only         |
| r4.xlarge   | 4    | 30.5      | Up to 10 Gigabit       | EBS-Only         |
| r4.2xlarge  | 8    | 61        | Up to 10 Gigabit       | EBS-Only         |
| r4.4xlarge  | 16   | 122       | Up to 10 Gigabit       | EBS-Only         |
| r4.8xlarge  | 32   | 244       | 10 Gigabit             | EBS-Only         |
| r4.16xlarge | 64   | 488       | 20 Gigabit             | EBS-Only         |

### R3
Optimized for memory-intensive applications and offer lower price per GiB of RAM.

| Model      | vCPU | Mem (GiB) | SSD Storage (GB) |
|---         |---   |---        |---               |
| r3.large   | 2    | 15.25     | 1 x 32           |
| r3.xlarge  | 4    | 30.5      | 1 x 80           |
| r3.2xlarge | 8    | 61        | 1 x 160          |
| r3.4xlarge | 16   | 122       | 1 x 320          |
| r3.8xlarge | 32   | 244       | 2 x 320          |

# Accelerated Computing Instances

### P2
For general-purpose GPU compute applications.

| Model       | GPUs | vCPU | Mem (GiB) | GPU Memory (GiB) |
|---          |---   |---   |---        |---               |
| p2.xlarge   | 1    | 4    | 61        | 12               |
| p2.8xlarge  | 8    | 32   | 488       | 96               |
| p2.16xlarge | 16   | 64   | 732       | 192              |


### G2
Optimized for graphics-intensive applications.

| Model      | GPUs | vCPU | Mem (GiB) | SSD Storage (GB) |
|---         |---   |---   |---        |---               |
| g2.2xlarge | 1    | 8    | 15        | 1 x 60           |
| g2.8xlarge | 4    | 32   | 60        | 2 x 120          |

### F1
Customizable hardware acceleration with field programmable gate arrays (FPGAs).

| Model       | FPGAs | vCPU | Mem (GiB) | SSD Storage (GB) |
|---          |---    |---   |---        |---               |
| f1.2xlarge  | 1     | 8    | 122       | 480              |
| f1.16xlarge | 8     | 64   | 976       | 4 x 960          |

# Storage Optimized

### I3
Optimized for low latency, very high random I/O performance, high sequential read throughput and provide high IOPS at a low cost.

| Model       | vCPU | Mem (GiB) | Networking Performance | Storage (TB)       |
|---          |---   |---        |---                     |---                 |
| i3.large    | 2    | 15.25     | Up to 10 Gigabit       | 1 x 0.475 NVMe SSD |
| i3.xlarge   | 4    | 30.5      | Up to 10 Gigabit       | 1 x 0.95 NVMe SSD  |
| i3.2xlarge  | 8    | 61        | Up to 10 Gigabit       | 1 x 1.9 NVMe SSD   |
| i3.4xlarge  | 16   | 122       | Up to 10 Gigabit       | 2 x 1.9 NVMe SSD   |
| i3.8xlarge  | 32   | 244       | 10 Gigabit             | 4 x 1.9 NVMe SSD   |
| i3.16xlarge | 64   | 488       | 20 Gigabit             | 8 x 1.9 NVMe SSD   |

### D2
High disk throughput, and offer the lowest price per disk throughput performance on Amazon EC2.

| Model      | vCPU | Mem (GiB) | Storage (GB)  |
|---         |---   |---        |---            |
| d2.xlarge  | 4    | 30.5      | 3 x 2000 HDD  |
| d2.2xlarge | 8    | 61        | 6 x 2000 HDD  |
| d2.4xlarge | 16   | 122       | 12 x 2000 HDD |
| d2.8xlarge | 36   | 244       | 24 x 2000 HDD |
