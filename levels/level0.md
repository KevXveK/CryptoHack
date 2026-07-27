# Level 0 — Morse

**Not an official CryptoHack level** — I built this converter before starting the General category, just to practice the "encoding table = dictionary" idea before touching real ASCII/hex.

## What I did

```python
def morse():
    dicionario = {
        'A': '.-',    'B': '-...',  'C': '-.-.',  'D': '-..',
        'E': '.',     'F': '..-.',  'G': '--.',   'H': '....',
        'I': '..',    'J': '.---',  'K': '-.-',   'L': '.-..',
        'M': '--',    'N': '-.',    'O': '---',   'P': '.--.',
        'Q': '--.-',  'R': '.-.',   'S': '...',   'T': '-',
        'U': '..-',   'V': '...-',  'W': '.--',   'X': '-..-',
        'Y': '-.--',  'Z': '--..',
        '1': '.----', '2': '..---', '3': '...--', '4': '....-',
        '5': '.....', '6': '-....', '7': '--...', '8': '---..',
        '9': '----.', '0': '-----', ' ': '/'
    }
    traducao = []
    escolha = int(input('Type 1 to translate text to Morse or 2 for Morse to text'))
    if escolha == 1:
        texto = input('Enter the text').upper()
        for letra in texto:
            if letra in dicionario:
                traducao.append(dicionario[letra])
        return ' '.join(traducao)
    else:
        texto = input('Enter the encoded text').split()
        for caracter in texto:
            for chave, valor in dicionario.items():
                if caracter == valor:
                    traducao.append(chave)
        return ' '.join(traducao)
```

Tested with "SOS": `... --- ...`. Nothing fancy, just a letter → code dictionary and its reverse for decoding.

## Takeaway

This set the pattern I'll repeat in the next levels: any simple encoding is basically a one-way dictionary, and decoding is just reversing the lookup.
