# 🚀 Task 2: Compile "Hello, RISC-V"
## ✅ Step 1: Write the Minimal C Program
I created a file named hai.c with the following content:

### code in c

```bash
#include <stdio.h>
int main() {
    printf("Hello, RISC-V!\n");
    return 0;
}
```
## ✅ Step 2: Compile the C Program for RISC-V

I used the RISC-V cross-compiler to compile the program for the RV32IMC architecture:

### 🔧 Terminal Command

```bash
riscv-none-elf-gcc hai.c -march=rv32imc -mabi=ilp32 -mcmodel=medany -static -o hai.elf
```

## ✅ Step 3: Verify the Output ELF File

I checked the type of the output file to confirm it’s a 32-bit RISC-V ELF executable:

### 🔧 Terminal Command

```bash
file hai.elf
```
output
```bash
hai.elf: ELF 32-bit LSB executable, UCB RISC-V, version 1 (SYSV), statically linked, not stripped
```
![o/p of the code](https://github.com/rakeshkumar1806/vsdRiscvSoc/blob/main/week%201/compliing_in_c.png)

