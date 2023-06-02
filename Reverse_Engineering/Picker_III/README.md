# Picker I

## Description

Can you figure out how this program works to get the flag?

## Solution

This challenge is very different from picker-I and picker-II. To access the function inside the program we now have `func_table` variable and other functions which can be used for read and write variable to the program. Since we know we can write and read variable at first I tried to give statement with eval but both read and write function guard the programs with the `filter_value` and `filter_var_name` never allowed to enter those eval statements. While going through the source code we can find the `func_table` variable which contains string having all the functions. I tried to manipulate that in using `write_variable` function but issue came in when the length of the variable is checked so I crafted a string with `32 * 4 = 128` length

string: `"win ____________________________________________________________________________________________________________________________"`

After successfully changing the `func_table` variable we can enter `1` then it will take `win` function name from `func_table` and prints the hexadecimals of the flag

Output:

```
Please enter new value of variable: "win ____________________________________________________________________________________________________________________________"
==> 2
Please enter variable name to read: func_table
win ____________________________________________________________________________________________________________________________
==> 1
0x70 0x69 0x63 0x6f 0x43 0x54 0x46 0x7b 0x37 0x68 0x31 0x35 0x5f 0x31 0x35 0x5f 0x77 0x68 0x34 0x37 0x5f 0x77 0x33 0x5f 0x67 0x33 0x37 0x5f 0x77 0x31 0x37 0x68 0x5f 0x75 0x35 0x33 0x72 0x35 0x5f 0x31 0x6e 0x5f 0x63 0x68 0x34 0x72 0x67 0x33 0x5f 0x63 0x32 0x30 0x66 0x35 0x32 0x32 0x32 0x7d
```

## Flag

`picoCTF{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_c20f5222}`
