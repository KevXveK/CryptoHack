# Level 2 — Hex

**Categoria General.** String em hexadecimal pra converter direto pra texto.

## O que fiz

```python
codigo = '63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d'

def converte_hex(codigo):
    resultado = bytes.fromhex(codigo)
    return resultado

resultadoo = converte_hex(codigo)
print(resultadoo)
```

Saída: `crypto{You_will_be_working_with_hex_strings_a_lot}`

## Conclusão

`bytes.fromhex()` faz o trabalho todo — cada par de dígitos hex vira um byte, e como o texto original é ASCII o resultado já sai legível. Bem mais direto que montar um dicionário na mão como nos níveis anteriores.
