# Picker I

## Description

Can you figure out how this program works to get the flag?

## My Solution

Source code have a funciton called eval. This eval function will evaluatea passed string parameter

For example `eval('print("Hello")')` will give output as `Hello`
That means whatever the string we give inside `eval` function it will parse and execute in as python code
`getRandomNumber` is a function in the source code which can be easily called through eval and given as example for us.

Passing `win` string will call the function and will give hexdecimals characters which can be converted to ascii using the below snippet

```
for i in hexstr.split()
    print(chr(int(i,16)), end='')
```

## Flag

`picoCTF{7h15_15_wh47_w3_g37_w17h_u53r5_1n_ch4rg3_c20f5222}`
