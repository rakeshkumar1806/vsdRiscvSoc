# vsdRiscvSoc
## week 1

### Task 1

I have downloaded riscv-toolchain-rv32imac-x86_64-ubuntu.tar.gz. How exactly do I 
unpack it, add it to PATH, and confirm the gcc, objdump, and gdb binaries work? 

1)AI Response: 
Here's a clear, step-by-step guide on how to unpack the xPack RISC-V toolchain, add it to 
your PATH, and verify that gcc, objdump, and gdb work properly:
1. Download the Toolchain 
(Use the latest version; for example:) 
```bash
wget https://github.com/xpack-dev-tools/riscv-none-elf-gcc
xpack/releases/download/v14.2.0-3/xpack-riscv-none-elf-gcc-14.2.0-3-linux-x64.tar.gz 
```
This is the output of the installation


![GCC Version](https://github.com/rakeshkumar1806/vsdRiscvSoc/blob/main/installation.png)
2. Unpack the Archive 
```bash
tar -xvzf xpack-riscv-none-elf-gcc-14.2.0-3-linux-x64.tar.gz 
```
This creates a folder named something like xpack-riscv-none-elf-gcc-14.2.0-3. 
![GCC Version](https://github.com/rakeshkumar1806/vsdRiscvSoc/blob/main/extracting.png)
3. Add the Toolchain to Your PATH (Temporarily) 
Run this command in your terminal to add the toolchain binaries to your current session’s 
PATH:
```bash
export PATH=$PWD/xpack-riscv-none-elf-gcc-14.2.0-3/bin:$PATH 
```
![GCC Version](https://github.com/rakeshkumar1806/vsdRiscvSoc/blob/main/exporting_temporary.png)
• Here, $PWD is your current directory where the extracted folder is located. 
• This makes commands like riscv-none-elf-gcc accessible right away. 
4. Check if Binaries Work 
```bash
riscv-none-elf-gcc --version 
riscv-none-elf-objdump --version 
riscv-none-elf-gdb --version
```
Output of the verifications

![GCC Version](https://github.com/rakeshkumar1806/vsdRiscvSoc/blob/main/exporting_permently_and_verification_of_binary_works.png)
