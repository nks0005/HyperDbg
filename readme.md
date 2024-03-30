# HyperDBG
![hyper dbg system](https://raw.githubusercontent.com/HyperDbg/graphics/master/Diagrams/source-tree/source-tree.png)



# 빌드
1. https://docs.hyperdbg.org/getting-started/build-and-install 
순서대로 visual studio > windows sdk > wdk 설치 

build 폴더에서 MAKE 실행



2. 원격 연결 ( 시리얼 포트 설정 : \\.\pipe\HyperDbgPipe)
VM 내부 > .debug prepare serial 115200 com1 
호스트 > .debug remote namedpipe \\.\pipe\HyperDbgPipe


















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

..



# Code Analyze

## VM EXIT - EPT_VIOLATION
[<a href="https://github1s.com/nks0005/HyperDbg/blob/master/hyperdbg_/hyperdbg/hprdbghv/code/vmm/vmx/Vmexit.c#L85" target="_blank">vm exit</a>]
1. VM EXIT > EPT_VIOLATION 흐름

EPT Violation 발생
VM EXIT > VM EXIT Handler 호출
이때 인자로 guest의 레지스터 정보들이 인자로 들어옴

guest로 넘어올때 기본적으로 cpu의 레지스트리에 저장됨 > 이를 함수로 호출하기 위해 스택에 넣는 asm 코드 작업이 필요함
[<a href="https://github1s.com/nks0005/HyperDbg/blob/master/_hyperdbg/hyperdbg/hprdbghv/code/assembly/AsmVmexitHandler.asm">asm 코드</>]


** VM EXIT가 발생하면 VMM은 guest의 eip를 조정해줘야함 > 안그럼 무한 루프에 빠짐 **

```c
typedef struct GUEST_REGS
{
    //
    // DO NOT FUCKING TOUCH THIS STRUCTURE WITHOUT COORDINATION WITH SINA
    //

    UINT64 rax; // 0x00
    UINT64 rcx; // 0x08
    UINT64 rdx; // 0x10
    UINT64 rbx; // 0x18
    UINT64 rsp; // 0x20
    UINT64 rbp; // 0x28
    UINT64 rsi; // 0x30
    UINT64 rdi; // 0x38
    UINT64 r8;  // 0x40
    UINT64 r9;  // 0x48
    UINT64 r10; // 0x50
    UINT64 r11; // 0x58
    UINT64 r12; // 0x60
    UINT64 r13; // 0x68
    UINT64 r14; // 0x70
    UINT64 r15; // 0x78

    //
    // DO NOT FUCKING TOUCH THIS STRUCTURE WITHOUT COORDINATION WITH SINA
    //

} GUEST_REGS, *PGUEST_REGS;
```

switch 문을 통해 EPT_VIOLATION 인지 확인함

VCpu = Virtual Machine State 구조체 (==? VMCS)
https://github1s.com/nks0005/HyperDbg/blob/master/_hyperdbg/hyperdbg/hprdbghv/header/common/State.h#L285-L339


```c
VmxVmexitHandler(_Inout_ PGUEST_REGS GuestRegs)
    ...

    case VMX_EXIT_REASON_EPT_VIOLATION:
    {
        if (EptHandleEptViolation(VCpu) == FALSE)
        {
            LogError("Err, there were errors in handling EPT violation");
        }

        break;
    }
```

EptHandleEptViolation > TRUE의 경우 의도한 EPT Violation ( ept 훅 등... )



VCpu의 ExitQualification 값을 이용하여 무슨 violation 종류인지 값을 담음]
VMX_EXIT_QUALIFICATION_EPT_VIOLATION 구조체
https://github1s.com/nks0005/HyperDbg/blob/master/_hyperdbg/hyperdbg/dependencies/ia32-doc/out/ia32.h#L18596-L18790

총 17개 종류가 있음 - 각 1비트로 계산됨
    ReadAccess: 데이터 읽기 액세스가 EPT 위반의 원인인 경우 설정됩니다.
    WriteAccess: 데이터 쓰기 액세스가 EPT 위반의 원인인 경우 설정됩니다.
    ExecuteAccess: 명령어 실행이 EPT 위반의 원인인 경우 설정됩니다.
    EptReadable: EPT 위반의 원인이 된 가상 주소가 읽기 가능한지 여부를 나타냅니다.
    EptWriteable: EPT 위반의 원인이 된 가상 주소가 쓰기 가능한지 여부를 나타냅니다.
    EptExecutable: EPT 위반의 원인이 된 가상 주소가 실행 가능한지 여부를 나타냅니다.
    EptExecutableForUserMode: 사용자 모드 선형 주소에서 실행 가능한지 여부를 나타냅니다.
    ValidGuestLinearAddress: 게스트 선형 주소 필드가 유효한지 여부를 나타냅니다.
    CausedByTranslation: 주소 변환에 의해 EPT 위반이 발생한 경우 설정됩니다.
    UserModeLinearAddress: 사용자 모드 선형 주소 여부를 나타냅니다.
    ReadableWritablePage: 읽기/쓰기 가능한 페이지인지 여부를 나타냅니다.
    ExecuteDisablePage: 실행 비활성 페이지 여부를 나타냅니다.
    NmiUnblocking: IRET으로 인한 NMI 언블로킹 여부를 나타냅니다.
    ShadowStackAccess: 쉐도우 스택 액세스 여부를 나타냅니다.
    SupervisorShadowStack: 슈퍼바이저 쉐도우 스택 여부를 나타냅니다.
    GuestPagingVerification: 게스트 페이징 확인 여부를 나타냅니다.
    AsynchronousToInstruction: 명령어 실행과 비동기적으로 관련된 액세스 여부를 나타냅니다.

```c
BOOLEAN
EptHandleEptViolation(VIRTUAL_MACHINE_STATE * VCpu)
{
    UINT64                               GuestPhysicalAddr;
    VMX_EXIT_QUALIFICATION_EPT_VIOLATION ViolationQualification = {.AsUInt = VCpu->ExitQualification};

    //
    // Reading guest physical address
    //
    __vmx_vmread(VMCS_GUEST_PHYSICAL_ADDRESS, &GuestPhysicalAddr);
   
```

https://ocw.snu.ac.kr/sites/default/files/NOTE/2566.pdf


ExecTrapHandleEptViolationVmexit > MBEC (Monitor Mode Execution Control) 후킹과 관련된 EPT (Extended Page Tables) 위반을 처리하는 데 사용

MBEC -> 실제 물리 메모리를 등록해서 해당 물리 메모리를 모니터링 -> 트랩 발생 ( EPT VIOLATION ? ) 
    epthook2 기능이 아닐지?


    
```c
    if (ExecTrapHandleEptViolationVmexit(VCpu, &ViolationQualification))
    {
        return TRUE;
    }
    else if (EptHandlePageHookExit(VCpu, ViolationQualification, GuestPhysicalAddr))
    {
        //
        // Handled by page hook code
        //
        return TRUE;
    }
    else if (VmmCallbackUnhandledEptViolation(VCpu->CoreId, (UINT64)ViolationQualification.AsUInt, GuestPhysicalAddr))
    {
        //
        // Check whether this violation is meaningful for the application or not
        //
        return TRUE;
    }

    LogError("Err, unexpected EPT violation at RIP: %llx", VCpu->LastVmexitRip);
    DbgBreakPoint();
    //
    // Redo the instruction that caused the exception
    //
    return FALSE;
}
```

## VM EXIT - VM CALL? 

hyperdbg
```c
    case VMX_EXIT_REASON_EXECUTE_VMCALL:
    {
        //
        // Handle vm-exits of VMCALLs
        //
        DispatchEventVmcall(VCpu);

        break;
    }
```

cheat_engine
```c

```