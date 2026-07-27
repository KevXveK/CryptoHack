# Level 0 — Morse

**Não é um nível oficial do CryptoHack** — fiz esse conversor antes de começar a categoria General, só pra treinar a ideia de "tabela de codificação = dicionário" antes de mexer com ASCII/hex de verdade.

## O que fiz

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
    escolha = int(input('Digite 1 para traduzir texto para morse ou 2 para morse para texto'))
    if escolha == 1:
        texto = input('Digite o texto').upper()
        for letra in texto:
            if letra in dicionario:
                traducao.append(dicionario[letra])
        return ' '.join(traducao)
    else:
        texto = input('Digite o codigo cifrado').split()
        for caracter in texto:
            for chave, valor in dicionario.items():
                if caracter == valor:
                    traducao.append(chave)
        return ' '.join(traducao)
```

Testando com "SOS": `... --- ...`. Nada sofisticado, só um dicionário letra → código e o inverso pra decodificar.

## Conclusão

Serviu pra fixar o padrão que vou repetir nos próximos níveis: toda codificação simples é basicamente um dicionário de mão única, e decodificar é só inverter a busca.
