# Level 1 — ASCII

**General category.** Given a list of ASCII codes, needed to join them into text to get the flag.

## What I did

```python
lista = [99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]

def converte_ascii(lista):
    texto = (''.join(chr(num) for num in lista))
    return texto

resultado = converte_ascii(lista)
print(resultado)
```

Output: `crypto{ASCII_pr1nt4bl3}`

## Takeaway

`chr()` on each number in the list, then join. Same reasoning as level 0's Morse, except the "table" here is just the standard ASCII table instead of one I made up.
