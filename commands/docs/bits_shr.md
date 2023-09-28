---
title: bits shr
categories: |
  bits
version: 0.85.0
bits: |
  Bitwise shift right for integers.
usage: |
  Bitwise shift right for integers.
---
<!-- This file is automatically generated. Please edit the command in https://github.com/nushell/nushell instead. -->

# <code>{{ $frontmatter.title }}</code> for bits

<div class='command-title'>{{ $frontmatter.bits }}</div>

## Signature

```> bits shr (bits) --signed --number-bytes```

## Parameters

 -  `bits`: number of bits to shift right
 -  `--signed` `(-s)`: always treat input number as a signed number
 -  `--number-bytes {string}`: the word size in number of bytes, it can be 1, 2, 4, 8, auto, default value `8`


## Input/output types:

| input     | output    |
| --------- | --------- |
| int       | int       |
| list\<int\> | list\<int\> |
## Examples

Shift right a number with 2 bits
```shell
> 8 | bits shr 2
2
```

Shift right a list of numbers
```shell
> [15 35 2] | bits shr 2
╭───┬───╮
│ 0 │ 3 │
│ 1 │ 8 │
│ 2 │ 0 │
╰───┴───╯

```


**Tips:** Command `bits shr` was not included in the official binaries by default, you have to build it with `--features=extra` flag