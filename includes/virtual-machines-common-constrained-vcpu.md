

Some database workloads like SQL Server or Oracle require high memory, storage, and I/O bandwidth, but not a high core count. Many database workloads are not CPU-intensive. Azure offers certain VM sizes where you can constrain the VM vCPU count to reduce the cost of software licensing, while maintaining the same memory, storage, and I/O bandwidth.

The vCPU count can be  constrained to one half or one quarter of the original VM size. These new VM sizes have a suffix that specifies the number of active vCPUs to make them easier for you to identify.

For example, the current VM size Standard_GS5 comes with 32 vCPUs, 448 GB RAM, 64 disks (up to 256 TB), and 80,000 IOPs or 2 GB/s of I/O bandwidth. The new VM sizes Standard_GS5-16 and Standard_GS5-8 comes with 16 and 8 active vCPUs respectively, while maintaining the rest of the specs of the Standard_GS5 for memory, storage, and I/O bandwidth.

The licensing fees charged for SQL Server or Oracle are constrained to the new vCPU count, and other products should be charged based on the new vCPU count. This results in a 50% to 75% increase in the ratio of the VM specs to active (billable) vCPUs. These new VM sizes that are only available in Azure, allowing workloads to push higher CPU utilization at a fraction of the (per-core) licensing cost. At this time, the compute cost, which includes OS licensing, remains the same one as the original size. For more information, see [Azure VM sizes for more cost-effective database workloads](https://azure.microsoft.com/blog/announcing-new-azure-vm-sizes-for-more-cost-effective-database-workloads/).


| Name                | vCPU | Specs           |
|---------------------|------|-----------------|
| Standard_M64-32ms   | 32   | Same as M64ms   |
| Standard_M64-16ms   | 16   | Same as M64ms   |
| Standard_M128-64ms  | 64   | Same as M128ms  |
| Standard_M128-32ms  | 32   | Same as M128ms  |
| Standard_E32-16_v3  | 16   | Same as E32s_v3 |
| Standard_E32-8s_v3  | 8    | Same as E32s_v3 |
| Standard_E64-32s_v3 | 32   | Same as E64s_v3 |
| Standard_E64-16s_v3 | 16   | Same as E64s_v3 |
| Standard_GS4-8      | 8    | Same as GS4     |
| Standard_GS4-4      | 4    | Same as GS4     |
| Standard_GS5-16     | 16   | Same as GS5     |
| Standard_GS5-8      | 8    | Same as GS5     |
| Standard_DS13-4_v2  | 4    | Same as DS13_v2 |
| Standard_DS13-2_v2  | 2    | Same as DS13_v2 |
| Standard_DS14-8_v2  | 8    | Same as DS14_v2 |
| Standard_DS14-4_v2  | 4    | Same as DS14_v2 |