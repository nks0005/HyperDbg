# HyperDBG
![hyper dbg system](https://raw.githubusercontent.com/HyperDbg/graphics/master/Diagrams/source-tree/source-tree.png)



## Unique Features
### First Release (v0.1.0.0)
* Advanced Hypervisor-based Kernel Mode Debugger [<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/getting-started/attach-to-hyperdbg/debug" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/getting-started/attach-to-hyperdbg/local-debugging" target="_blank">link</a>]
* Classic EPT Hook (Hidden Breakpoint) [<a href="https://docs.hyperdbg.org/commands/extension-commands/epthook" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/features/vmm-module/design-of-epthook" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/hooking-any-function" target="_blank">link</a>]
* Inline EPT Hook (Inline Hook) [<a href="https://docs.hyperdbg.org/commands/extension-commands/epthook2" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/features/vmm-module/design-of-epthook2" target="_blank">link</a>]
* Monitor Memory For R/W (Emulating Hardware Debug Registers Without Limitation) [<a href="https://docs.hyperdbg.org/commands/extension-commands/monitor" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/features/vmm-module/design-of-monitor" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/monitoring-accesses-to-structures" target="_blank">link</a>]
* SYSCALL Hook (Disable EFER & Handle #UD) [<a href="https://docs.hyperdbg.org/commands/extension-commands/syscall" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/features/vmm-module/design-of-syscall-and-sysret" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/intercepting-all-syscalls" target="_blank">link</a>]
* SYSRET Hook (Disable EFER & Handle #UD) [<a href="https://docs.hyperdbg.org/commands/extension-commands/sysret" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/features/vmm-module/design-of-syscall-and-sysret" target="_blank">link</a>]
* CPUID Hook & Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/cpuid" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/triggering-special-instructions" target="_blank">link</a>]
* RDMSR Hook & Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/msrread" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/identifying-system-behavior" target="_blank">link</a>]
* WRMSR Hook & Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/msrwrite" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/identifying-system-behavior" target="_blank">link</a>]
* RDTSC/RDTSCP Hook & Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/tsc" target="_blank">link</a>]
* RDPMC Hook & Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/pmc" target="_blank">link</a>]
* VMCALL Hook & Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/vmcall" target="_blank">link</a>]
* Debug Registers Hook & Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/dr" target="_blank">link</a>]
* I/O Port (In Instruction) Hook & Monitor  [<a href="https://docs.hyperdbg.org/commands/extension-commands/ioin" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/triggering-special-instructions" target="_blank">link</a>]
* I/O Port (Out Instruction) Hook & Monitor  [<a href="https://docs.hyperdbg.org/commands/extension-commands/ioout" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/triggering-special-instructions" target="_blank">link</a>]
* MMIO Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/monitor" target="_blank">link</a>]
* Exception (IDT < 32) Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/exception" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/features/vmm-module/design-of-exception-and-interrupt" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/identifying-system-behavior" target="_blank">link</a>]
* External-Interrupt (IDT > 32) Monitor [<a href="https://docs.hyperdbg.org/commands/extension-commands/interrupt" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/features/vmm-module/design-of-exception-and-interrupt" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/events/identifying-system-behavior" target="_blank">link</a>]
* Running Automated Scripts [<a href="https://docs.hyperdbg.org/commands/scripting-language/debugger-script" target="_blank">link</a>]
* Transparent-mode (Anti-debugging and Anti-hypervisor Resistance) [<a href="https://docs.hyperdbg.org/tips-and-tricks/considerations/transparent-mode" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/misc/defeating-anti-debug-and-anti-hypervisor-methods" target="_blank">link</a>]
* Running Custom Assembly In Both VMX-root, VMX non-root (Kernel & User) [<a href="https://docs.hyperdbg.org/using-hyperdbg/prerequisites/how-to-create-an-action" target="_blank">link</a>]
* Checking For Custom Conditions [<a href="https://docs.hyperdbg.org/using-hyperdbg/prerequisites/how-to-create-a-condition" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/debugger-internals/conditions" target="_blank">link</a>]
* Process-specific & Thread-specific Debugging [<a href="https://docs.hyperdbg.org/commands/meta-commands/.process" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/commands/meta-commands/.thread" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/user-mode-debugging/examples/basics/switching-to-a-specific-process-or-thread" target="_blank">link</a>]
* VMX-root Compatible Message Tracing [<a href="https://docs.hyperdbg.org/design/features/vmm-module/vmx-root-mode-compatible-message-tracing" target="_blank">link</a>]
* Powerful Kernel Side Scripting Engine [<a href="https://docs.hyperdbg.org/commands/scripting-language" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/design/script-engine" target="_blank">link</a>]
* Support To Symbols (Parsing PDB Files) [<a href="https://docs.hyperdbg.org/commands/meta-commands/.sympath" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/commands/meta-commands/.sym" target="_blank">link</a>]
* Mapping Data To Symbols & Create Structures, Enums From PDB Files [<a href="https://docs.hyperdbg.org/commands/debugging-commands/dt" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/commands/debugging-commands/struct" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/basics/mapping-data-and-create-structures-and-enums-from-symbols" target="_blank">link</a>]
* Event Forwarding (#DFIR) [<a href="https://docs.hyperdbg.org/tips-and-tricks/misc/event-forwarding" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/commands/debugging-commands/output" target="_blank">link</a>]
* Transparent Breakpoint Handler [<a href="https://docs.hyperdbg.org/commands/debugging-commands/bp" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/using-hyperdbg/kernel-mode-debugging/examples/basics/setting-breakpoints-and-stepping-instructions" target="_blank">link</a>]
* Various Custom Scripts [<a href="https://github.com/HyperDbg/scripts" target="_blank">link</a>]

### Second Release (v0.2.0.0)
* HyperDbg Software Development Kit (SDK) [<a href="https://docs.hyperdbg.org/using-hyperdbg/sdk" target="_blank">link</a>]

### Third Release (v0.3.0.0)
* Event Short-circuiting [<a href="https://docs.hyperdbg.org/tips-and-tricks/misc/event-short-circuiting" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/commands/scripting-language/functions/events/event_sc" target="_blank">link</a>]
* Tracking records of function calls and return addresses [<a href="https://docs.hyperdbg.org/commands/extension-commands/track" target="_blank">link</a>]
* Kernel-level Length Disassembler Engine (LDE) [<a href="https://docs.hyperdbg.org/commands/scripting-language/functions/diassembler/disassemble_len" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/commands/scripting-language/functions/diassembler/disassemble_len32" target="_blank">link</a>]

### Fourth Release (v0.4.0.0)
* Memory Execution Monitor & Execution Blocking [<a href="https://docs.hyperdbg.org/commands/extension-commands/monitor" target="_blank">link</a>]
* Custom Page-fault Injection [<a href="https://docs.hyperdbg.org/commands/meta-commands/.pagein" target="_blank">link</a>]

### Fifth Release (v0.5.0.0)
* Different Event Calling Stages [<a href="https://docs.hyperdbg.org/tips-and-tricks/misc/event-calling-stage" target="_blank">link</a>]

### Sixth Release (v0.6.0.0)
* Injecting Custom Interrupts/Exceptions/Faults [<a href="https://docs.hyperdbg.org/commands/scripting-language/functions/events/event_inject" target="_blank">link</a>][<a href="https://docs.hyperdbg.org/commands/scripting-language/functions/events/event_inject_error_code" target="_blank">link</a>]

### Seventh Release (v0.7.0.0)
* Instant events in the Debugger Mode [<a href="https://docs.hyperdbg.org/tips-and-tricks/misc/instant-events" target="_blank">link</a>]

### Eighth Release (v0.8.0.0)
* Detect kernel-to-user and user-to-kernel transitions [<a href="https://docs.hyperdbg.org/commands/extension-commands/mode" target="_blank">link</a>]


# Analyze Features
## Advanced Hypervisor-based Kernel Mode Debugger
 
windbg, gdb 같은 커널 디버거는 크게 바뀌지 않음 -> 커널 모드를 디버깅하려는 디버거는 하드웨어 계층(링) 측면에 더 많은 권한을 가져야 함 
-> 운영 체제를 방해하지 않고 별도의 레이어 -> hypervisor

hyperDbg는 하이퍼바이저 기술을 이용하여 디버깅 기술을 구현 + Anti-디버깅 & Anti-하이퍼바이저 우회

VMI - Virtual Machine Interface 모드 -> 가상 머신의 메모리 덤프를 생성 & 프로세스 상태 등을 실시간으로 분석하고 모니터링 하기 위 해사용
[<a href="https://github.com/Wenzel/r2vmi?tab=readme-ov-file" target="_blank">r2vmi github</a>]

## Classic EPT Hook [ Hidden Breakpoint ] 
EPT 