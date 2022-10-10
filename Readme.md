# An internal error in Verilator

## Debug output

```
%Error: Internal Error: ../src/internalerror_0.1/src/pickled.sv:69815:24: ../V3Dfg.h:381: non-packed has no 'width()'
69815 |    logic [width_p-1:0] mem [els_p-1:0];
      |                        ^~~
%Error: Internal Error: Aborting since under --debug
Aborted
```

## How to reproduce

1. Clone this repo

```
git clone https://github.com/flaviens/verilator_internal_err_undriven.git
cd verilator_internal_err_undriven
```

2. Make sure you have FuseSoC installed

```
pip install fusesoc
```

3. Add the library and launch the compilation

```
fusesoc library add internalerror .
fusesoc run internalerror
```