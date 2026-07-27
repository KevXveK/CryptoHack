# Level 3 — Hex → Base64

**Drill, not the official CryptoHack Base64 challenge** (this one doesn't decode into readable text — just practicing the binary → base64 conversion before level 4).

## What I did

```python
import base64

codigohex = '72bca9b68fc16ac7beeb8f849dca1d8a783e8acf9679bf9269f7bf'

def convertbase64(codigo):
    hex = bytes.fromhex(codigo)
    result = base64.b64encode(hex)
    return result, hex

imprimir, hexx = convertbase64(codigohex)
print(imprimir)
```

Output: `b'crypto/Base+64+Encoding+is+Web+Safe/'`

The raw bytes don't form text (it's genuine binary junk), but the resulting base64 happened to spell out a readable phrase — funny to see, but not a real flag, just a side effect of the base64 alphabet.

## Takeaway

`bytes.fromhex()` to get out of hex, `base64.b64encode()` to get into base64. Same logic as always: an intermediate format (bytes) bridging the two ends.
