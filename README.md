<div align="center">

# GESTALT OS
<p>
  <a href="https://docs.gestalt.ws">
    <img src="https://img.shields.io/badge/Documentation-0d5736?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Documentation" />
  </a>    
  &nbsp;
  <img alt="Build" src="https://img.shields.io/github/actions/workflow/status/OliverKeefe/open-web-drive/backend-ci.yml?branch=main&label=build&style=for-the-badge">
  &nbsp;  
  <img alt="License" src="https://img.shields.io/badge/license-GPLv2-0d5736.svg?style=for-the-badge">
</p>
</div>

## 🧭 Overview

Formerly "Little OS", Gestalt OS is a minimal, yet highly customizable operating system built on a microkernel architecture.
Currently, Gestalt OS only supports 32-bit RISC-V ("Reduced Instruction Set Computer Five") systems. In future versions, this will be expanded to 64-bit
and additional architectures, including ARM and x86.

> [!IMPORTANT]
> **🚧 Kernel Stability Status — In Development**
>
> The kernel is still heavily in-development, thus, stability and feature completeness cannot be guaranteed.

# 🛣️ Road Map

Planned features include:

- [ ] Add 64-Bit Support
- [ ] Implement `ext2` File System
- [ ] Add ARM Architecture Support
- [ ] Add x86 Architecture Support
- [ ] Add Networking (TCP/IP)
- [ ] Add Primitives For Containerization
- [ ] Add Virtualization

## ⚙️ Setting Up Dev Environment
### Install Dependencies / Tooling

> [!NOTE]
> If you're running Ubuntu 24.04+ install `qemu-system-riscv-hwe` instead of `qemu-system-riscv32`.
>

### 🐧 Linux
### RISC-V
RISC-V ("Reduced Instruction Set Computer Five")

You can read the RISC-V ISA specifications here:
[Ratified Specification](https://riscv.org/specifications/ratified/)

To setup a RISC-V virtualized testing / development environment with QEMU,
riscv32 qemu system and openSBI are required. 

#### Ubuntu / Pop_OS!
```shell
sudo apt update -y && \
sudo apt install -y clang llvm lld qemu-system-riscv-hwe curl
```

#### Debian

```shell
sudo apt update -y && \
sudo apt install -y clang llvm lld qemu-system-riscv32 curl
```

#### Install OpenSBI
```shell
curl -LO https://github.com/qemu/qemu/raw/v8.0.4/pc-bios/opensbi-riscv32-generic-fw_dynamic.bin 
```


