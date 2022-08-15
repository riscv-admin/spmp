# S-Mode Physical Memory Protection (SPMP) Task Group Charter

RISC-V based processors stimulate great interest in the emerging low-end systems like internet of things (IoT). However, as the paged virtual memory system is usually not available on low-end devices, it is hard to isolate the S-mode OSes (e.g., RTOS) and user-mode applications. To support secure processing and isolate faults of U-mode software, it is desirable to enable S-mode OS to limit the physical addresses accessible by U-mode software on a hart.

The SPMP Task Group develops the SPMP (S-mode Physical Memory Protection) extension for memory isolation on the low-end systems as an alternative to the paged virtual memory system.

The SPMP Task Group will deliver an SPMP architectural specification, which includes the following capabilities:

* Access control of read/write/execute requests by an hart, including address matching, encoding of permissions, etc.
* Exceptions for access violation
* Fast switching between different sets of SPMP entries
* Virtualization support:
  * Supports for VS/VU modes so a guest VM can use SPMP for memory protection
  * Supports for hypervisor guest memory protection (as an alternative to hgatp)

Besides the specification (which is in the Stable state now) and completing all DoD requirements, the SPMP Task Group will work with the Security HC, TEE TG, other committees/SIGs/TGs, and development partners to provide simulators (Spike and Qemu), Sail formal model, test cases, and reference code for commercial OSes (e.g., Linux and RTOS) and open-sourced hypervisors (e.g., KVM and Xvisor) for SPMP.
