# Level 4 — Bytes and Big Integers

**General category.** The flag comes as one giant integer — needs to become hex, then bytes.

## What I did

```python
int_value = 11515195063862318899931685488813747395775516287289682636499965282714637259206269
hex_value = hex(int_value)
hex_bytes = hex_value[2:]          # strip the "0x" prefix
bytes_value = bytes.fromhex(hex_bytes)
print(bytes_value)
```

Output: `crypto{3nc0d1n6_4ll_7h3_w4y_d0wn}`

## Understanding the process (with a "HELLO" example)

To avoid just memorizing the command without understanding it, I worked out the same path in reverse with a simple word:

```
text:         HELLO
ascii bytes:  [72, 69, 76, 76, 79]
hex bytes:    0x48, 0x45, 0x4c, 0x4c, 0x4f
base-16:      0x48454c4c4f
base-10:      310400273487
```

```python
decimal = 310400273487
hexadecimal = hex(decimal)          # 0x48454c4c4f
hex_bytes = bytes.fromhex(hexadecimal[2:])
print(hex_bytes)                    # b'HELLO'
```

## Takeaway

A giant integer is nothing more than the text's bytes read as a base-10 number. To reverse it: `hex()` turns the integer into hexadecimal, strip the `0x`, then feed it to `bytes.fromhex()`. No crypto library needed for this — it's pure base conversion. `Crypto.Util.number` only helps once the number already comes out of an RSA/etc. context.
