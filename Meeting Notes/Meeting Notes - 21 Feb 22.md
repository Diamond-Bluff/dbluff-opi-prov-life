# Provisioning and Platform Management Group

## Subgroup charter

### Initial discussion topics

- Boot

- Lifecycle

- Discovery

- OS environment installation to the D/IPU

- service/software installation to the D/IPU

**Organizer: Boris Glimcher, <boris.glimcher@dell.com>**

- Meeting: TBD

- How to Join: Contact Boris to receive meeting invite

- Status

- Group is starting so will be forming.

## Meeting notes from February 22, 2022

### Attendees

Boris Glimcher, Andy Butcher, Mark Sanders, Ted Streete, Kyle Mestery

- Security
    - Both in lifecycle and installations

- Discovery
    - Discovery of the DPU and optionally BMC

- Inventory
    - Vendor, SN, P/N, SW/FW versions, ...
    - Capabilities of the DPU
        - Core, memory, storage, offloads, hw vs sw capabilities

- Initial provisioning / Initial boot image...
    - PXE, local DPU storage boot, boot from the host, boot from BMC
    - Zero-trust
        - Secure boot and image signing

- Boot sequencing & crash recovery
    - Who boots first : dpu / bmc ?
    - Wait for boot ? control boot order...
    - Controlled reset -- what is the sequence?
        - Only DPU v only Host vs Both vs all DPUs (multiple DPU in the host)
        - DPU power cycle
    - Uncontrolled reset
        - When DPU SW/Kernel crashes
        - When DPU FW/NIC/powerloss crashes or reboots
        - When Host crashes soft reset
        - When Host crashes -- power cycle / reset
        - When BMC crashes?
        - PCIe uncorrectable errors
    - DPU is not booting at all
        - Corrupted flash / corrupted/missing DIMMs
        - Understand reason for not booting -- APIs...
        - Ability to debug this state

- Lifecycle & Updates
    - DPU fw
    - DPU sw
    - BMC
    - Host ? -- agent/driver on the host talking to DPU
    - Non-disruptive upgrades
        - host application is not affected if DPU is updated
        - DPU is not affected if HOST is updated

### Topics for Monday, Feb 28

- Deploy services on DPU (as oppose of OS)
    - For next week
- Monitoring & Telemetry
    - For next week
	