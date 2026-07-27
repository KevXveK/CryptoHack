# Level 3 — Hex → Base64

**Treino, não é o hex oficial do CryptoHack** (esse aqui não decodifica pra um texto legível — é só pra praticar a conversão binário → base64 antes do nível 4).

## O que fiz

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

Saída: `b'crypto/Base+64+Encoding+is+Web+Safe/'`

Os bytes crus não formam texto (é lixo binário mesmo), mas por coincidência o base64 resultante caiu formando uma frase legível — engraçado de ver, mas não é uma flag de verdade, só o efeito colateral do alfabeto do base64.

## Conclusão

`bytes.fromhex()` pra sair do hex, `base64.b64encode()` pra entrar no base64. Mesma lógica de sempre: um formato intermediário (bytes) conectando as duas pontas.
