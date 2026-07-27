# Level 1 — ASCII

**Categoria General.** Recebi uma lista de códigos ASCII e precisava juntar em texto pra achar a flag.

## O que fiz

```python
lista = [99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]

def converte_ascii(lista):
    texto = (''.join(chr(num) for num in lista))
    return texto

resultado = converte_ascii(lista)
print(resultado)
```

Saída: `crypto{ASCII_pr1nt4bl3}`

## Conclusão

`chr()` em cada número da lista e junta tudo. É o mesmo raciocínio do morse do nível 0, só que a "tabela" já é a tabela ASCII padrão em vez de uma que eu inventei.
