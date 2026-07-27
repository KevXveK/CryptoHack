# Level 2 — Hex

**General category.** A hex string to convert straight into text.

## What I did

```python
codigo = '63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d'

def converte_hex(codigo):
    resultado = bytes.fromhex(codigo)
    return resultado

resultadoo = converte_hex(codigo)
print(resultadoo)
```

Output: `crypto{You_will_be_working_with_hex_strings_a_lot}`

## Takeaway

`bytes.fromhex()` does all the work — each pair of hex digits becomes a byte, and since the original text is ASCII the result comes out readable. Much more direct than building a dictionary by hand like the earlier levels.
