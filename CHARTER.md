# S-Mode Memory Protection Unit (SMPU) Task Group Charter

RISC-V based processors stimulate great interest in the emerging low-end systems like internet of things (IoT). However, as the paged virtual memory system is usually not available on low-end devices, it is hard to isolate the S-mode OSes (e.g., RTOS) and user-mode applications. To support secure processing and isolate faults of U-mode software, it is desirable to enable S-mode OS to limit the physical addresses accessible by U-mode software on a hart.

The SMPU Task Group develops the SMPU (S-mode Memory Protection Unit) extension for memory isolation on the low-end systems as an alternative to the paged virtual memory system.

The SMPU Task Group will deliver an SMPU architectural specification, which includes the following capabilities:

* Access control of read/write/execute requests by an hart, including address matching, encoding of permissions, etc.
* Exceptions for access violation
* Fast switching between different sets of SMPU entries
* Virtualization support:
  * Supports for VS/VU modes so a guest VM can use SMPU for memory protection
  * Supports for hypervisor guest memory protection (as an alternative to hgatp)

Besides the specification (which is in the Stable state now), the SMPU Task Group will work with the Security HC, TEE TG, other committees/SIGs/TGs, and development partners to provide simulators (Spike and Qemu), Sail formal model, test cases, and reference code for commercial OSes (e.g., Linux and RTOS) for SMPU.
