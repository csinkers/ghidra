# Decompiler

```
set SLEIGHHOME=path/to/ghidra
build\os\win_x86_64\decomp_dbg.exe
```

Then:
```
restore /path/to/your/exported_function.xml
load function <function_name>
```

load file /some/path - Load in raw binary
adjust vma 0x10000
load addr 0x12341234 - Load func by address
load function foo    - Load func by name

decompile:    Run the full decompilation process on the loaded function.
print raw:    Print the raw, unoptimized P-code initially generated from the assembly.
print C:      Display the finalized, structured pseudo-C code output.
print C flat: Display a flattened version of the pseudo-C representation.
step:         Advance through individual optimization rules to watch how the P-code shifts 
              structure phase by phase.

(see ifacedecomp.cc for others)

Raw Bytes --- SLEIGH ---> Pcode
Pcode ---lifted----> higher Pcode
High level constructs recovered
Generate tokens

