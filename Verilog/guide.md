# Verilog Style Guide

The point of this document is not to join the holy war of coding styles, but simply to provide one of the many possibilities, so that if you have the same taste, you may simply follow this guide instead of writing one.

## General Rules

When coding, always keep in mind that simplicity and clarity are important, because about 80% of the time are actually spent on maintaining. If there is a conflict between simplicity and clarity, choose clarity. This document may never be complete as Verilog is a so complex language, so whenever you meet something not mentioned in this guide, just remember to keep everything clean and simple.

## Naming

### File, Class, and Module Names

File, class, and module names should be all lower-case with underscore '_'. If there's just one class or module in the file then its name should be the same as the filename.

```Verilog
// lowercase_with_underscore.sv
class lowercase_with_underscore;
endclass: lowercase_with_underscore

module lowercase_with_underscore;
endmodule: lowercase_with_underscore
```

### Interface Names

Interface definitions should be all lower-case with underscore '_', ending in "_io", and interface instances end in "_if".

```Verilog
interface bus_io(input bit clk);
    // ...
endinterface: bus_io

module tb_top;
    bus_io bus_if(clk);
endmodule: tb_top
```

### Variable Names

Variable names should be all lower-case with underscore '_'.

```Verilog
logic [31:0] lwu;
```

### Struct, Union, and Enum Names

Do not typedef struct, union, or enum if unnecessary, and use lower-case with underscore '_'.

```Verilog
struct {
    // ...
} any_struct;
```

### Macro Names

Macro names should be all uppercase with underscores '_'.

```Verilog
`define PRINT_BYTES(arr, startbyte, numbytes) // ...
```

## Formatting

### Line Length

Each line of code should be at most 100 characters long.

### Spaces vs. Tabs

Use only spaces, and indent 4 spaces for each level.

### Layout

For now, please refer to [Style Guide for SystemVerilog Code](https://www.systemverilog.io/styleguide) for code layout, such as "begin & end", "if & else", and so on.

## References

* [Style Guide for SystemVerilog Code](https://www.systemverilog.io/styleguide)
