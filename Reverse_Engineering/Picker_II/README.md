# Picker II

## Description

Can you figure out how this program works to get the flag?

## My Solution

The previous Picker_I challenge gave flag easily, however in this challenge we cannot just provide `win` string to program. `filter` function in program checks the string whether it contain `win` string so we need an another approach using ascii codes

The code `''.join(chr(i) for i in [119,105,110])` will give the string `win` eventhough this will bypass the `filter`function it will take the result as string and will show error `TypeError: 'str' object is not callable`

To avoid this we will use `eval()` in our passing string itself `eval(''.join(chr(i) for i in [119,105,110])` thus giving the list of hexdecimal that can be converted to the flag

## Flag

`picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_b924e8e5}`
