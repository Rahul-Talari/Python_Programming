# Programming Languages Overview

## Language Comparison
- **C++**
- **Java**
- **Python**

## How Programming Languages Execute

### Key Execution Models

**Compiler:** Source Code → Compiler → [Compilation Errors? Stop : No Errors? Continue] → Native Machine Code (Executable File) → OS Loads → CPU Executes

**Interpreter:** Source Code → Interpreter → Translate & Execute Step by Step → [Error Encountered? Stop & Report Error]



## Language Details

### C++
- **Execution:** Source Code → Compiler → [Compilation Errors? Stop : No Errors? Continue] → Native Machine Code (Executable) → OS Loads → CPU Executes
- **Advantages:** Fully compiled language; produces fast native binaries that run directly on OS & CPU
- **Applications:** Gaming, System Programming, Embedded Systems

### Java
- **Execution:** Source Code → Compiler → [Compilation Errors? Stop : No Errors? Continue] → Bytecode → JVM (Interpreter + JIT Compiler) → Machine Code
- **Advantages:** Compiled + interpreted (JIT-based), Platform Independent, Portable, Secure, "Write Once Run Anywhere"
- **Applications:** Enterprise Applications, Web Applications, Distributed Systems

### Python
- **Execution:** Source Code → CPython Compiler → [Syntax Errors? Stop : No Errors? Continue] → Python Bytecode (.pyc) → Python VM → Execution
- **Threading Note:** Uses the GIL in CPython: only 1 thread executes Python bytecode at a time within a process
- **Advantages:** Interpreted language with internal bytecode compilation, Simple syntax, Huge library ecosystem, Rapid development
- **Applications:** AI/ML, Data Science, Web Development, Automation

