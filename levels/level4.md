# Level 4 — Bytes and Big Integers

**Categoria General.** A flag vem como um número inteiro gigante — precisa virar hex e depois bytes.

## O que fiz

```python
int_value = 11515195063862318899931685488813747395775516287289682636499965282714637259206269
hex_value = hex(int_value)
hex_bytes = hex_value[2:]          # remove o prefixo "0x"
bytes_value = bytes.fromhex(hex_bytes)
print(bytes_value)
```

Saída: `crypto{3nc0d1n6_4ll_7h3_w4y_d0wn}`

## Entendendo o processo (exemplo com "HELLO")

Pra não decorar o comando sem entender, montei o caminho inverso com uma palavra simples:

```
texto:        HELLO
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

## Conclusão

Um inteiro gigante nada mais é que os bytes do texto lidos como um número em base 10. Pra voltar: `hex()` transforma o inteiro em hexadecimal, corta o `0x` e joga em `bytes.fromhex()`. Não precisa de nenhuma lib de cripto pra isso, é conversão de base pura — o `Crypto.Util.number` só ajuda quando o número já vem separado de um contexto RSA/etc.
