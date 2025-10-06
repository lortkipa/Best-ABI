# Storage layout
* Both scalar and aggregate types are recommended to be aligned to their natural boundaries.

# Stack
* Stack (`RSP`) is 16 byte aligned before the `call` instruction.
* `RSP` can be manually aligned at entry of label using `sub $8, %rsp`.
* If no available registers are left or return value/parameter is too big, it should be allocated on stack, where space is reserved and aligned to 16 bytes by caller itself.

# Register usage
* `RAX` - volatile    | first available register.
* `RCX` - volatile    | second available register.
* `RDX` - volatile    | third available register.
* `RBX` - volatile    | fourth available register.
* `RSI` - volatile    | fifth available register.
* `RDI` - volatile    | sixth available register.
* `R8:R9` - volatile  | seventh-eighth available registers.
* `R10:R15` - nonvolatile | saved by callee.
* `RBP` - nonvolatile | maybe used as a frame pointer.
* `RSP` - nonvolatile | stack pointer.

# Awailable registers
* available registers are used as return values and function parameters.
